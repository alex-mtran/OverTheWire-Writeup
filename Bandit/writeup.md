# Table of Contents
| Level             | Skills / Techniques Learned |
|------------------|-----------------------------|
| [Level 0](#bandit-level-0)             | SSH |
| [Level 0 → 1](#bandit-level-0-to-1)     | File permissions |
| [Level 1 → 2](#bandit-level-1-to-2)     | File reading |
| [Level 2 → 3](#bandit-level-2-to-3)     | Strings from binaries |
| [Level 3 → 4](#bandit-level-3-to-4)     | Hidden files / dirs |
| [Level 4 → 5](#bandit-level-4-to-5)     | Directory permissions |
| [Level 5 → 6](#bandit-level-5-to-6)     | Symlinks |
| [Level 6 → 7](#bandit-level-6-to-7)     | File ownership & permissions |
| [Level 7 → 8](#bandit-level-7-to-8)     | `find` command |
| [Level 8 → 9](#bandit-level-8-to-9)     | `grep` / text search |
| [Level 9 → 10](#bandit-level-9-to-10)   | Base64 decoding |
| [Level 10 → 11](#bandit-level-10-to-11) | ROT13 / simple ciphers |
| [Level 11 → 12](#bandit-level-11-to-12) | `.gz` compression |
| [Level 12 → 13](#bandit-level-12-to-13) | `.bz2` compression |
| [Level 13 → 14](#bandit-level-13-to-14) | Executable / permission bits |
| [Level 14 → 15](#bandit-level-14-to-15) | Hex / binary inspection |
| [Level 15 → 16](#bandit-level-15-to-16) | Password-protected archives |
| [Level 16 → 17](#bandit-level-16-to-17) | SSH private key usage |
| [Level 17 → 18](#bandit-level-17-to-18) | SSH key permissions |
| [Level 18 → 19](#bandit-level-18-to-19) | Local file access |
| [Level 19 → 20](#bandit-level-19-to-20) | Netcat / networking |
| [Level 20 → 21](#bandit-level-20-to-21) | Cron jobs / background tasks |
| [Level 21 → 22](#bandit-level-21-to-22) | Script analysis / setuid binaries |
| [Level 22 → 23](#bandit-level-22-to-23) | Env vars / command injection |
| [Level 23 → 24](#bandit-level-23-to-24) | Bash scripting | Cron jobs | Chmod |


<br><br><br><br><br><br><br><br><br>

## Bandit Level 0

### Login

[OverTheWire Bandit Level 0](https://overthewire.org/wargames/bandit/bandit0.html)

#

### Description

The goal of this level is for you to log into the game using **ssh**. The host to which you need to connect is **bandit.labs.overthewire.org**, on **port 2220**. The **username is bandit0** and the **password is bandit0**. Once logged in, go to the Level 1 page to find out how to beat Level 1.

#

### Theory

Use `man command` to look up the manual on command. In this case use `man ssh`.

#

### Steps

```bash
ssh -p 2220 bandit0@bandit.labs.overthewire.org
```
Input `bandit0` for password prompt.

#
[OverTheWire Bandit Level 0](https://overthewire.org/wargames/bandit/bandit0.html)
<br><br><br><br><br><br><br><br><br>










## Bandit Level 0 to 1

### Login

```bash
ssh -p 2220 bandit1@bandit.labs.overthewire.org
```
Password: [bandit01]
#

### Description

The password for the next level is stored in a file called `readme` located in the **home** directory. Use this password to log into bandit1 using SSH. Whenever you find a password for a level, use SSH (on port 2220) to log into that level and continue the game.

#

### Theory


#

### Steps


#
[OverTheWire Bandit Level 0 → 1](https://overthewire.org/wargames/bandit/bandit1.html)
<br><br><br><br><br><br><br><br><br>









## Bandit Level 1 to 2

### Login

```bash
ssh -p 2220 bandit2@bandit.labs.overthewire.org
```
Password: [bandit12]
#

### Description

The password for the next level is stored in a file called `-` located in the **home** directory.

#

### Theory


#

### Steps


#
[OverTheWire Bandit Level 1 → 2](https://overthewire.org/wargames/bandit/bandit2.html)
<br><br><br><br><br><br><br><br><br>









## Bandit Level 2 to 3

### Login

```bash
ssh -p 2220 bandit3@bandit.labs.overthewire.org
```
Password: [bandit23]
#

### Description

The password for the next level is stored in a file called `--spaces in this filename--` located in the **home** directory.

#

### Theory


#

### Steps


#
[OverTheWire Bandit Level 2 → 3](https://overthewire.org/wargames/bandit/bandit3.html)
<br><br><br><br><br><br><br><br><br>









## Bandit Level 3 to 4

### Login

```bash
ssh -p 2220 bandit4@bandit.labs.overthewire.org
```
Password: [bandit34]
#

### Description

The password for the next level is stored in a hidden file in the **inhere** directory.

#

### Theory


#

### Steps


#
[OverTheWire Bandit Level 3 → 4](https://overthewire.org/wargames/bandit/bandit4.html)
<br><br><br><br><br><br><br><br><br>








## Bandit Level 4 to 5

### Login

```bash
ssh -p 2220 bandit5@bandit.labs.overthewire.org
```
Password: [bandit45]
#

### Description

The password for the next level is stored in the only human-readable file in the **inhere** directory. Tip: if your terminal is messed up, try the “reset” command.

#

### Theory


#

### Steps


#
[OverTheWire Bandit Level 4 → 5](https://overthewire.org/wargames/bandit/bandit5.html)
<br><br><br><br><br><br><br><br><br>








## Bandit Level 5 to 6

### Login

```bash
ssh -p 2220 bandit6@bandit.labs.overthewire.org
```
Password: [bandit56]
#

### Description

The password for the next level is stored in a file somewhere under the **inhere** directory and has all of the following properties:

* human-readable
* 1033 bytes in size
* not executable

#

### Theory


#

### Steps


#
[OverTheWire Bandit Level 5 → 6](https://overthewire.org/wargames/bandit/bandit6.html)
<br><br><br><br><br><br><br><br><br>









## Bandit Level 6 to 7

### Login

```bash
ssh -p 2220 bandit7@bandit.labs.overthewire.org
```
Password: [bandit67]
#

### Description

The password for the next level is stored **somewhere on the server** and has all of the following properties:

* owned by user bandit7
* owned by group bandit6
* 33 bytes in size

#

### Theory


#

### Steps


#
[OverTheWire Bandit Level 6 → 7](https://overthewire.org/wargames/bandit/bandit7.html)
<br><br><br><br><br><br><br><br><br>










## Bandit Level 7 to 8

### Login

```bash
ssh -p 2220 bandit8@bandit.labs.overthewire.org
```
Password: [bandit78]
#

### Description

The password for the next level is stored in the file `data.txt` next to the word **millionth**.

#

### Theory


#

### Steps


#
[OverTheWire Bandit Level 7 → 8](https://overthewire.org/wargames/bandit/bandit8.html)
<br><br><br><br><br><br><br><br><br>









## Bandit Level 8 to 9

### Login

```bash
ssh -p 2220 bandit9@bandit.labs.overthewire.org
```
Password: [bandit89]
#

### Description

The password for the next level is stored in the file `data.txt` and is the only line of text that occurs only once.

#

### Theory


#

### Steps


#
[OverTheWire Bandit Level 8 → 9](https://overthewire.org/wargames/bandit/bandit9.html)
<br><br><br><br><br><br><br><br><br>








## Bandit Level 9 to 10

### Login

```bash
ssh -p 2220 bandit10@bandit.labs.overthewire.org
```
Password: [bandit910]
#

### Description

The password for the next level is stored in the file `data.txt` in one of the few human-readable strings, preceded by several ‘=’ characters.

#

### Theory


#

### Steps


#
[OverTheWire Bandit Level 9 → 10](https://overthewire.org/wargames/bandit/bandit10.html)
<br><br><br><br><br><br><br><br><br>









## Bandit Level 10 to 11

### Login

```bash
ssh -p 2220 bandit11@bandit.labs.overthewire.org
```
Password: [bandit1011]
#

### Description

The password for the next level is stored in the file `data.txt`, which contains base64 encoded data.

#

### Theory


#

### Steps


#
[OverTheWire Bandit Level 10 → 11](https://overthewire.org/wargames/bandit/bandit11.html)
<br><br><br><br><br><br><br><br><br>









## Bandit Level 11 to 12

### Login

```bash
ssh -p 2220 bandit12@bandit.labs.overthewire.org
```
Password: [bandit1112]
#

### Description

The password for the next level is stored in the file `data.txt`, where all lowercase (a-z) and uppercase (A-Z) letters have been rotated by 13 positions.

#

### Theory


#

### Steps


#
[OverTheWire Bandit Level 11 → 12](https://overthewire.org/wargames/bandit/bandit12.html)
<br><br><br><br><br><br><br><br><br>









## Bandit Level 12 to 13

### Login

```bash
ssh -p 2220 bandit13@bandit.labs.overthewire.org
```
Password: [bandit1213]
#

### Description

The password for the next level is stored in the file `data.txt`, which is a hexdump of a file that has been repeatedly compressed. For this level it may be useful to create a directory under `/tmp` in which you can work. Use `mkdir` with a hard to guess directory name. Or better, use the command `mktemp -d`. Then copy the datafile using `cp`, and rename it using `mv` (read the manpages!).

#

### Theory


#

### Steps


#
[OverTheWire Bandit Level 12 → 13](https://overthewire.org/wargames/bandit/bandit13.html)
<br><br><br><br><br><br><br><br><br>









## Bandit Level 13 to 14

### Login

```bash
ssh -p 2220 -i sshkey14.private bandit7@bandit.labs.overthewire.org
```
#

### Description

The password for the next level is stored in `/etc/bandit_pass/bandit14` and can only be read by user **bandit14**. For this level, you don’t get the next password, but you get a private SSH key that can be used to log into the next level. Look at the commands that logged you into previous bandit levels, and find out how to use the key for this level.

#

### Theory


#

### Steps


#
[OverTheWire Bandit Level 13 → 14](https://overthewire.org/wargames/bandit/bandit14.html)
<br><br><br><br><br><br><br><br><br>









## Bandit Level 14 to 15

### Login

```bash
ssh -p 2220 bandit15@bandit.labs.overthewire.org
```
Password: [bandit1415]
#

### Description

The password for the next level can be retrieved by submitting the password of the current level to **port 30000 on localhost**.

#

### Theory


#

### Steps


#
[OverTheWire Bandit Level 14 → 15](https://overthewire.org/wargames/bandit/bandit15.html)
<br><br><br><br><br><br><br><br><br>









## Bandit Level 15 to 16

### Login

```bash
ssh -p 2220 bandit16@bandit.labs.overthewire.org
```
Password: [bandit1516]
#

### Description

The password for the next level can be retrieved by submitting the password of the current level to **port 30001 on localhost using SSL/TLS encryption**.

Helpful note: Getting “DONE”, “RENEGOTIATING” or “KEYUPDATE”? Read the “CONNECTED COMMANDS” section in the manpage.

#

### Theory


#

### Steps


#
[OverTheWire Bandit Level 15 → 16](https://overthewire.org/wargames/bandit/bandit16.html)
<br><br><br><br><br><br><br><br><br>









## Bandit Level 16 to 17

### Login

```bash
ssh -p 2220 -i sshkey16.private bandit7@bandit.labs.overthewire.org
```
#

### Description

The credentials for the next level can be retrieved by submitting the password of the current level to a **port on localhost in the range 31000 to 32000**. First find out which of these ports have a server listening on them. Then find out which of those speak **SSL/TLS** and which don’t. There is only 1 server that will give the next credentials, the others will simply send back to you whatever you send to it.

Helpful note: Getting “DONE”, “RENEGOTIATING” or “KEYUPDATE”? Read the “CONNECTED COMMANDS” section in the manpage.

#

### Theory


#

### Steps


#
[OverTheWire Bandit Level 16 → 17](https://overthewire.org/wargames/bandit/bandit17.html)
<br><br><br><br><br><br><br><br><br>









## Bandit Level 17 to 18

### Login

```bash
ssh -p 2220 bandit18@bandit.labs.overthewire.org
```
Password: [bandit1718]
#

### Description

There are 2 files in the homedirectory: `passwords.old` and `passwords.new`. The password for the next level is in `passwords.new` and is the only line that has been changed between `passwords.old` and `passwords.new`.

NOTE: if you have solved this level and see ‘Byebye!’ when trying to log into bandit18, this is related to the next level, bandit19

#

### Theory


#

### Steps


#
[OverTheWire Bandit Level 17 → 18](https://overthewire.org/wargames/bandit/bandit18.html)
<br><br><br><br><br><br><br><br><br>









## Bandit Level 18 to 19

### Login

```bash
ssh -p 2220 bandit19@bandit.labs.overthewire.org
```
Password: [bandit1819]
#

### Description

The password for the next level is stored in a file `readme` in the **homedirectory**. Unfortunately, someone has modified `.bashrc` to log you out when you log in with SSH.

#

### Theory


#

### Steps


#
[OverTheWire Bandit Level 18 → 19](https://overthewire.org/wargames/bandit/bandit19.html)
<br><br><br><br><br><br><br><br><br>









## Bandit Level 19 to 20

### Login

```bash
ssh -p 2220 bandit20@bandit.labs.overthewire.org
```
Password: [bandit1920]
#

### Description

To gain access to the next level, you should use the setuid binary in the homedirectory. Execute it without arguments to find out how to use it. The password for this level can be found in the usual place (`/etc/bandit_pass`), after you have used the setuid binary.

#

### Theory


#

### Steps


#
[OverTheWire Bandit Level 19 → 20](https://overthewire.org/wargames/bandit/bandit20.html)
<br><br><br><br><br><br><br><br><br>









## Bandit Level 20 to 21

### Login

```bash
ssh -p 2220 bandit21@bandit.labs.overthewire.org
```
Password: [bandit2021]
#

### Description

There is a setuid binary in the homedirectory that does the following: it makes a connection to localhost on the port you specify as a commandline argument. It then reads a line of text from the connection and compares it to the password in the previous level (bandit20). If the password is correct, it will transmit the password for the next level (bandit21).

NOTE: Try connecting to your own network daemon to see if it works as you think.

#

### Theory


#

### Steps


#
[OverTheWire Bandit Level 20 → 21](https://overthewire.org/wargames/bandit/bandit21.html)
<br><br><br><br><br><br><br><br><br>









## Bandit Level 21 to 22

### Login

```bash
ssh -p 2220 bandit22@bandit.labs.overthewire.org
```
Password: [bandit2122]
#

### Description

A program is running automatically at regular intervals from **cron**, the time-based job scheduler. Look in `/etc/cron.d/` for the configuration and see what command is being executed.

#

### Theory


#

### Steps


#
[OverTheWire Bandit Level 21 → 22](https://overthewire.org/wargames/bandit/bandit22.html)
<br><br><br><br><br><br><br><br><br>









## Bandit Level 22 to 23

### Login

```bash
ssh -p 2220 bandit23@bandit.labs.overthewire.org
```
Password: [bandit2223]
#

### Description

A program is running automatically at regular intervals from **cron**, the time-based job scheduler. Look in `/etc/cron.d/` for the configuration and see what command is being executed.

NOTE: Looking at shell scripts written by other people is a very useful skill. The script for this level is intentionally made easy to read. If you are having problems understanding what it does, try executing it to see the debug information it prints.

#

### Theory


#

### Steps


#
[OverTheWire Bandit Level 22 → 23](https://overthewire.org/wargames/bandit/bandit23.html)
<br><br><br><br><br><br><br><br><br>









## Bandit Level 23 to 24

### Login

```bash
ssh -p 2220 bandit0@bandit.labs.overthewire.org
```
Password: [password2223]

#

### Description

A program is running automatically at regular intervals from **cron**, the time-based job scheduler. Look in `/etc/cron.d/` for the configuration and see what command is being executed.

#

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

* The script runs as **bandit24**, so `myname` = `bandit24` → changes directory to `/var/spool/bandit24`.
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
[OverTheWire Bandit Level 23 → 24](https://overthewire.org/wargames/bandit/bandit24.html)
