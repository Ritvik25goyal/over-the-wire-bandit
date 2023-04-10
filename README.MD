From level0 to level1
$ ssh -p 2220 bandit0@bandit.labs.overthewire.org
pass- bandit0
bandit0@bandit:~$ ls
readme
bandit0@bandit:~$ cat readme
NH2SXQwcBdpmTEzi3bvBHMM9H66vVXjL

----------------------------------------------------------------

From level1 to level2
$ ssh -p 2220 bandit1@bandit.labs.overthewire.org
pass- NH2SXQwcBdpmTEzi3bvBHMM9H66vVXjL
bandit1@bandit:~$ ls
-
bandit1@bandit:~$ cat ./-
rRGizSaX8Mk1RTb1CNQoXTcYZWU6lgzi

----------------------------------------------------------------

From level2 to level3
$ ssh -p 2220 bandit2@bandit.labs.overthewire.org
pass- rRGizSaX8Mk1RTb1CNQoXTcYZWU6lgzi
bandit2@bandit:~$ ls
spaces in this filename
bandit2@bandit:~$ cat "spaces in this filename"
aBZ0W5EmUfAf7kHTQeOwd8bauFJ2lAiG

----------------------------------------------------------------

From level3 to level4
$ ssh -p 2220 bandit3@bandit.labs.overthewire.org
pass- aBZ0W5EmUfAf7kHTQeOwd8bauFJ2lAiG
bandit3@bandit:~$ ls
inhere
bandit3@bandit:~$ cd inhere
bandit3@bandit:~/inhere$ ls
bandit3@bandit:~/inhere$ ls -la
total 12
drwxr-xr-x 2 root    root    4096 Feb 21 22:03 .
drwxr-xr-x 3 root    root    4096 Feb 21 22:03 ..
-rw-r----- 1 bandit4 bandit3   33 Feb 21 22:03 .hidden
bandit3@bandit:~/inhere$ cat .hidden
2EW7BBsr6aMMoJ2HjW067dm8EgX26xNe

----------------------------------------------------------------

From level4 to level5
$ ssh -p 2220 bandit4@bandit.labs.overthewire.org
pass- 2EW7BBsr6aMMoJ2HjW067dm8EgX26xNe
bandit4@bandit:~$ ls
inhere
bandit4@bandit:~$ cd inhere
bandit4@bandit:~/inhere$ ls
-file00  -file01  -file02  -file03  -file04  -file05  -file06  -file07  -file08  -file09
bandit4@bandit:~/inhere$ file ./*
./-file00: data
./-file01: data
./-file02: data
./-file03: data
./-file04: data
./-file05: Non-ISO extended-ASCII text, with NEL line terminators
./-file06: Non-ISO extended-ASCII text, with no line terminators, with escape sequences
./-file07: ASCII text
./-file08: data
./-file09: data
bandit4@bandit:~/inhere$ cat ./-file07
lrIWWI6bB37kxfiCQZqUdOIYfr6eEeqR

----------------------------------------------------------------

From level5 to level6
$ ssh -p 2220 bandit5@bandit.labs.overthewire.org
pass- lrIWWI6bB37kxfiCQZqUdOIYfr6eEeqR
bandit5@bandit:~/inhere$ cd ..
bandit5@bandit:~$ ls
inhere
bandit5@bandit:~$ cd inhere
bandit5@bandit:~/inhere$ ls
maybehere00  maybehere03  maybehere06  maybehere09  maybehere12  maybehere15  maybehere18
maybehere01  maybehere04  maybehere07  maybehere10  maybehere13  maybehere16  maybehere19
maybehere02  maybehere05  maybehere08  maybehere11  maybehere14  maybehere17
bandit5@bandit:~/inhere$ find -size 1033c
./maybehere07/.file2
bandit5@bandit:~/inhere$ cat ./maybehere07/.file2
P4L4vucdmLnm8I7Vl7jG1ApGSfjYKqJU

----------------------------------------------------------------

From level6 to level7
$ ssh -p 2220 bandit6@bandit.labs.overthewire.org
pass- P4L4vucdmLnm8I7Vl7jG1ApGSfjYKqJU
bandit6@bandit:~$ ls
bandit6@bandit:~$ find / -user bandit7 -group bandit6 -size 33c
find: ‘/sys/kernel/tracing’: Permission denied
find: ‘/sys/kernel/debug’: Permission denied
find: ‘/sys/fs/pstore’: Permission denied
find: ‘/sys/fs/bpf’: Permission denied
find: ‘/lost+found’: Permission denied
find: ‘/boot/efi’: Permission denied
find: ‘/drifter/drifter14_src/axTLS’: Permission denied
find: ‘/proc/tty/driver’: Permission denied
find: ‘/proc/3257814/task/3257814/fd/6’: No such file or directory
find: ‘/proc/3257814/task/3257814/fdinfo/6’: No such file or directory
find: ‘/proc/3257814/fd/5’: No such file or directory
find: ‘/proc/3257814/fdinfo/5’: No such file or directory
find: ‘/run/chrony’: Permission denied
find: ‘/run/user/11026’: Permission denied
find: ‘/run/user/11017’: Permission denied
find: ‘/run/user/11032’: Permission denied
find: ‘/run/user/11010’: Permission denied
find: ‘/run/user/11021’: Permission denied
find: ‘/run/user/11011’: Permission denied
find: ‘/run/user/11003’: Permission denied
find: ‘/run/user/11019’: Permission denied
find: ‘/run/user/11022’: Permission denied
find: ‘/run/user/11025’: Permission denied
find: ‘/run/user/11002’: Permission denied
find: ‘/run/user/11016’: Permission denied
find: ‘/run/user/11024’: Permission denied
find: ‘/run/user/11009’: Permission denied
find: ‘/run/user/11015’: Permission denied
find: ‘/run/user/11007’: Permission denied
find: ‘/run/user/11014’: Permission denied
find: ‘/run/user/11023’: Permission denied
find: ‘/run/user/11008’: Permission denied
find: ‘/run/user/11005’: Permission denied
find: ‘/run/user/11004’: Permission denied
find: ‘/run/user/11013’: Permission denied
find: ‘/run/user/11001’: Permission denied
find: ‘/run/user/11020’: Permission denied
find: ‘/run/user/11012’: Permission denied
find: ‘/run/user/11000’: Permission denied
find: ‘/run/user/11006/systemd/inaccessible/dir’: Permission denied
find: ‘/run/sudo’: Permission denied
find: ‘/run/screen/S-bandit25’: Permission denied
find: ‘/run/screen/S-bandit9’: Permission denied
find: ‘/run/screen/S-bandit21’: Permission denied
find: ‘/run/screen/S-bandit20’: Permission denied
find: ‘/run/multipath’: Permission denied
find: ‘/run/cryptsetup’: Permission denied
find: ‘/run/lvm’: Permission denied
find: ‘/run/credentials/systemd-sysusers.service’: Permission denied
find: ‘/run/systemd/propagate’: Permission denied
find: ‘/run/systemd/unit-root’: Permission denied
find: ‘/run/systemd/inaccessible/dir’: Permission denied
find: ‘/run/lock/lvm’: Permission denied
find: ‘/snap/core18/2679/etc/ssl/private’: Permission denied
find: ‘/snap/core18/2679/root’: Permission denied
find: ‘/snap/core18/2679/var/cache/ldconfig’: Permission denied
find: ‘/snap/core18/2679/var/lib/private’: Permission denied
find: ‘/snap/core20/1822/etc/ssl/private’: Permission denied
find: ‘/snap/core20/1822/root’: Permission denied
find: ‘/snap/core20/1822/var/cache/ldconfig’: Permission denied
find: ‘/snap/core20/1822/var/cache/private’: Permission denied
find: ‘/snap/core20/1822/var/lib/private’: Permission denied
find: ‘/snap/core20/1822/var/lib/snapd/void’: Permission denied
find: ‘/tmp’: Permission denied
find: ‘/dev/mqueue’: Permission denied
find: ‘/dev/shm’: Permission denied
find: ‘/etc/polkit-1/localauthority’: Permission denied
find: ‘/etc/multipath’: Permission denied
find: ‘/etc/sudoers.d’: Permission denied
find: ‘/etc/ssl/private’: Permission denied
find: ‘/root’: Permission denied
find: ‘/home/drifter6/data’: Permission denied
find: ‘/home/drifter8/chroot’: Permission denied
find: ‘/home/bandit27-git’: Permission denied
find: ‘/home/bandit31-git’: Permission denied
find: ‘/home/ubuntu’: Permission denied
find: ‘/home/bandit29-git’: Permission denied
find: ‘/home/bandit28-git’: Permission denied
find: ‘/home/bandit5/inhere’: Permission denied
find: ‘/home/bandit30-git’: Permission denied
find: ‘/var/cache/apt/archives/partial’: Permission denied
find: ‘/var/cache/private’: Permission denied
find: ‘/var/cache/pollinate’: Permission denied
find: ‘/var/cache/apparmor/e10c1cf9.0’: Permission denied
find: ‘/var/cache/apparmor/c47eabf7.0’: Permission denied
find: ‘/var/cache/ldconfig’: Permission denied
find: ‘/var/crash’: Permission denied
find: ‘/var/log’: Permission denied
find: ‘/var/snap/lxd/common/lxd’: Permission denied
find: ‘/var/tmp’: Permission denied
find: ‘/var/spool/cron/crontabs’: Permission denied
find: ‘/var/spool/rsyslog’: Permission denied
find: ‘/var/spool/bandit24’: Permission denied
find: ‘/var/lib/apt/lists/partial’: Permission denied
find: ‘/var/lib/polkit-1’: Permission denied
find: ‘/var/lib/ubuntu-advantage/apt-esm/var/lib/apt/lists/partial’: Permission denied
find: ‘/var/lib/private’: Permission denied
find: ‘/var/lib/chrony’: Permission denied
find: ‘/var/lib/amazon’: Permission denied
/var/lib/dpkg/info/bandit7.password
find: ‘/var/lib/snapd/void’: Permission denied
find: ‘/var/lib/snapd/cookie’: Permission denied
find: ‘/var/lib/update-notifier/package-data-downloads/partial’: Permission denied
bandit6@bandit:~$cat /var/lib/dpkg/info/bandit7.password
z7WtoNQU2XfjmMtWA8u5rN4vzqu4v99S

----------------------------------------------------------------

From level7 to level8
$ ssh -p 2220 bandit7@bandit.labs.overthewire.org
pass- z7WtoNQU2XfjmMtWA8u5rN4vzqu4v99S
bandit7@bandit:~$ ls
data.txt
bandit7@bandit:~$ grep "millionth" data.txt
millionth       TESKZC0XvTetK0S9xNwm25STk5iWrBvP

----------------------------------------------------------------

From level8 to level9 
$ ssh -p 2220 bandit8@bandit.labs.overthewire.org
pass- TESKZC0XvTetK0S9xNwm25STk5iWrBvP
bandit8@bandit:~$ ls
data.txt
bandit8@bandit:~$ cat data.txt| sort| uniq -u
EN632PlfYiZbn3PhVK3XOGSlNInNE00t

----------------------------------------------------------------

From level9 to level10
$ ssh -p 2220 bandit9@bandit.labs.overthewire.org
pass- EN632PlfYiZbn3PhVK3XOGSlNInNE00t
bandit9@bandit:~$ ls
data.txt
bandit9@bandit:~$ strings data.txt |grep "="
dS=5
f========== theM
=XeOh
=vb`
O=Nq
=I6aT
========== password
========== is
2\:=7
u=]ThS>
%AM_9=
1~=y
Q=9(
j=GD
b=fFD
0?F=(
.DX_/=
========== G7w8LIi6J3kTb8A7j9LgrywtEUlyyp6s

----------------------------------------------------------------

From level10 to level11
$ ssh -p 2220 bandit10@bandit.labs.overthewire.org
pass- G7w8LIi6J3kTb8A7j9LgrywtEUlyyp6s
bandit10@bandit:~$ ls
data.txt
bandit10@bandit:~$ cat data.txt
VGhlIHBhc3N3b3JkIGlzIDZ6UGV6aUxkUjJSS05kTllGTmI2blZDS3pwaGxYSEJNCg==
bandit10@bandit:~$ echo "VGhlIHBhc3N3b3JkIGlzIDZ6UGV6aUxkUjJSS05kTllGTmI2blZDS3pwaGxYSEJNCg==" | base64 -d
The password is 6zPeziLdR2RKNdNYFNb6nVCKzphlXHBM

----------------------------------------------------------------

From level11 to level12
$ ssh -p 2220 bandit11@bandit.labs.overthewire.org
pass- 6zPeziLdR2RKNdNYFNb6nVCKzphlXHBM
bandit11@bandit:~$ ls
data.txt
bandit11@bandit:~$ cat data.txt
Gur cnffjbeq vf WIAOOSFzMjXXBC0KoSKBbJ8puQm5lIEi
by ROT13 decryptor :-
The password is JVNBBFSmZwKKOP0XbFXOoW8chDz5yVRv

----------------------------------------------------------------

From level12 to level13
$ ssh -p 2220 bandit12@bandit.labs.overthewire.org
pass- JVNBBFSmZwKKOP0XbFXOoW8chDz5yVRv
bandit12@bandit:~$ ls
data.txt
bandit12@bandit:~$ cd /tmp
bandit12@bandit:/tmp$ mkdir why
bandit12@bandit:/tmp$ cd
bandit12@bandit:~$ cp data.txt /tmp/why
bandit12@bandit:~$ cd /tmp/why
bandit12@bandit:/tmp/why$ ls
data.txt
bandit12@bandit:/tmp/why$ xxd -r data.txt > data.gz
bandit12@bandit:/tmp/why$ ls
data.gz  data.txt
bandit12@bandit:/tmp/why$ gzip -d data.gz
bandit12@bandit:/tmp/why$ ls
data  data.txt
bandit12@bandit:/tmp/why$ mv data data.bz2
bandit12@bandit:/tmp/why$ ls
data.bz2  data.txt
bandit12@bandit:/tmp/why$ bzip2 -d data.bz2
bandit12@bandit:/tmp/why$ ls
data  data.txt
bandit12@bandit:/tmp/why$ file data
data: gzip compressed data, was "data4.bin", last modified: Tue Feb 21 22:02:52 2023, max compression, from Unix, original size modulo 2^32 20480
bandit12@bandit:/tmp/why$ mv data data.gz
bandit12@bandit:/tmp/why$ gzip -d data.gz
bandit12@bandit:/tmp/why$ ls
data  data.txt
bandit12@bandit:/tmp/why$ file data
data: POSIX tar archive (GNU)
bandit12@bandit:/tmp/why$ mv data data.tar
bandit12@bandit:/tmp/why$ tar xf data.tar
data5.bin
bandit12@bandit:/tmp/why$ ls
data5.bin  data.tar  data.txt
bandit12@bandit:/tmp/why$ file data5.bin
data5.bin: POSIX tar archive (GNU)
bandit12@bandit:/tmp/why$ rm data.tar
bandit12@bandit:/tmp/why$ mv data5.bin data.tar
bandit12@bandit:/tmp/why$ ls
data.tar  data.txt
bandit12@bandit:/tmp/why$ tar xf data.tar
bandit12@bandit:/tmp/why$ ls
data6.bin  data.tar  data.txt
bandit12@bandit:/tmp/why$ file data6.bin
data6.bin: bzip2 compressed data, block size = 900k
bandit12@bandit:/tmp/why$ mv data6.bin data.bz2
bandit12@bandit:/tmp/why$ ls
data.bz2  data.tar  data.txt
bandit12@bandit:/tmp/why$ bzip2 -d data.bz2
bandit12@bandit:/tmp/why$ ls
data  data.tar  data.txt
bandit12@bandit:/tmp/why$ file data
data: POSIX tar archive (GNU)
bandit12@bandit:/tmp/why$ mv data data.tar
bandit12@bandit:/tmp/why$ ls
data.tar  data.txt
bandit12@bandit:/tmp/why$ tar xf data.tar
bandit12@bandit:/tmp/why$ ls
data8.bin  data.tar  data.txt
bandit12@bandit:/tmp/why$ file data8.bin
data8.bin: gzip compressed data, was "data9.bin", last modified: Tue Feb 21 22:02:52 2023, max compression, from Unix, original size modulo 2^32 49
bandit12@bandit:/tmp/why$ mv data8.bin
mv: missing destination file operand after 'data8.bin'
Try 'mv --help' for more information.
bandit12@bandit:/tmp/why$ mv data8.bin data.gz
bandit12@bandit:/tmp/why$ gzip -d data.gz
bandit12@bandit:/tmp/why$ ls
data  data.tar  data.txt
bandit12@bandit:/tmp/why$ file data
data: ASCII text
bandit12@bandit:/tmp/why$ cat data
The password is wbWdlBxEir4CaE8LaPhauuOo6pwRmrDw

----------------------------------------------------------------

From level13 to level14
$ ssh -p 2220 bandit13@bandit.labs.overthewire.org
pass- wbWdlBxEir4CaE8LaPhauuOo6pwRmrDw
bandit13@bandit:~$ ls
sshkey.private
bandit13@bandit:~$ cat sshkey.private
-----BEGIN RSA PRIVATE KEY-----
MIIEpAIBAAKCAQEAxkkOE83W2cOT7IWhFc9aPaaQmQDdgzuXCv+ppZHa++buSkN+
gg0tcr7Fw8NLGa5+Uzec2rEg0WmeevB13AIoYp0MZyETq46t+jk9puNwZwIt9XgB
ZufGtZEwWbFWw/vVLNwOXBe4UWStGRWzgPpEeSv5Tb1VjLZIBdGphTIK22Amz6Zb
ThMsiMnyJafEwJ/T8PQO3myS91vUHEuoOMAzoUID4kN0MEZ3+XahyK0HJVq68KsV
ObefXG1vvA3GAJ29kxJaqvRfgYnqZryWN7w3CHjNU4c/2Jkp+n8L0SnxaNA+WYA7
jiPyTF0is8uzMlYQ4l1Lzh/8/MpvhCQF8r22dwIDAQABAoIBAQC6dWBjhyEOzjeA
J3j/RWmap9M5zfJ/wb2bfidNpwbB8rsJ4sZIDZQ7XuIh4LfygoAQSS+bBw3RXvzE
pvJt3SmU8hIDuLsCjL1VnBY5pY7Bju8g8aR/3FyjyNAqx/TLfzlLYfOu7i9Jet67
xAh0tONG/u8FB5I3LAI2Vp6OviwvdWeC4nOxCthldpuPKNLA8rmMMVRTKQ+7T2VS
nXmwYckKUcUgzoVSpiNZaS0zUDypdpy2+tRH3MQa5kqN1YKjvF8RC47woOYCktsD
o3FFpGNFec9Taa3Msy+DfQQhHKZFKIL3bJDONtmrVvtYK40/yeU4aZ/HA2DQzwhe
ol1AfiEhAoGBAOnVjosBkm7sblK+n4IEwPxs8sOmhPnTDUy5WGrpSCrXOmsVIBUf
laL3ZGLx3xCIwtCnEucB9DvN2HZkupc/h6hTKUYLqXuyLD8njTrbRhLgbC9QrKrS
M1F2fSTxVqPtZDlDMwjNR04xHA/fKh8bXXyTMqOHNJTHHNhbh3McdURjAoGBANkU
1hqfnw7+aXncJ9bjysr1ZWbqOE5Nd8AFgfwaKuGTTVX2NsUQnCMWdOp+wFak40JH
PKWkJNdBG+ex0H9JNQsTK3X5PBMAS8AfX0GrKeuwKWA6erytVTqjOfLYcdp5+z9s
8DtVCxDuVsM+i4X8UqIGOlvGbtKEVokHPFXP1q/dAoGAcHg5YX7WEehCgCYTzpO+
xysX8ScM2qS6xuZ3MqUWAxUWkh7NGZvhe0sGy9iOdANzwKw7mUUFViaCMR/t54W1
GC83sOs3D7n5Mj8x3NdO8xFit7dT9a245TvaoYQ7KgmqpSg/ScKCw4c3eiLava+J
3btnJeSIU+8ZXq9XjPRpKwUCgYA7z6LiOQKxNeXH3qHXcnHok855maUj5fJNpPbY
iDkyZ8ySF8GlcFsky8Yw6fWCqfG3zDrohJ5l9JmEsBh7SadkwsZhvecQcS9t4vby
9/8X4jS0P8ibfcKS4nBP+dT81kkkg5Z5MohXBORA7VWx+ACohcDEkprsQ+w32xeD
qT1EvQKBgQDKm8ws2ByvSUVs9GjTilCajFqLJ0eVYzRPaY6f++Gv/UVfAPV4c+S0
kAWpXbv5tbkkzbS0eaLPTKgLzavXtQoTtKwrjpolHKIHUz6Wu+n4abfAIRFubOdN
/+aLoRQ0yBDRbdXMsZN/jvY44eM+xRLdRVyMmdPtP8belRi2E2aEzA==
-----END RSA PRIVATE KEY-----
bandit13@bandit:~$ exit
exit: command not found
bandit13@bandit:~$
logout
Connection to bandit.labs.overthewire.org closed.
Ritvik@DESKTOP-4RHVIFV MINGW64 ~
$ echo "-----BEGIN RSA PRIVATE KEY-----
MIIEpAIBAAKCAQEAxkkOE83W2cOT7IWhFc9aPaaQmQDdgzuXCv+ppZHa++buSkN+
gg0tcr7Fw8NLGa5+Uzec2rEg0WmeevB13AIoYp0MZyETq46t+jk9puNwZwIt9XgB
ZufGtZEwWbFWw/vVLNwOXBe4UWStGRWzgPpEeSv5Tb1VjLZIBdGphTIK22Amz6Zb
ThMsiMnyJafEwJ/T8PQO3myS91vUHEuoOMAzoUID4kN0MEZ3+XahyK0HJVq68KsV
ObefXG1vvA3GAJ29kxJaqvRfgYnqZryWN7w3CHjNU4c/2Jkp+n8L0SnxaNA+WYA7
jiPyTF0is8uzMlYQ4l1Lzh/8/MpvhCQF8r22dwIDAQABAoIBAQC6dWBjhyEOzjeA
J3j/RWmap9M5zfJ/wb2bfidNpwbB8rsJ4sZIDZQ7XuIh4LfygoAQSS+bBw3RXvzE
pvJt3SmU8hIDuLsCjL1VnBY5pY7Bju8g8aR/3FyjyNAqx/TLfzlLYfOu7i9Jet67
xAh0tONG/u8FB5I3LAI2Vp6OviwvdWeC4nOxCthldpuPKNLA8rmMMVRTKQ+7T2VS
nXmwYckKUcUgzoVSpiNZaS0zUDypdpy2+tRH3MQa5kqN1YKjvF8RC47woOYCktsD
o3FFpGNFec9Taa3Msy+DfQQhHKZFKIL3bJDONtmrVvtYK40/yeU4aZ/HA2DQzwhe
ol1AfiEhAoGBAOnVjosBkm7sblK+n4IEwPxs8sOmhPnTDUy5WGrpSCrXOmsVIBUf
laL3ZGLx3xCIwtCnEucB9DvN2HZkupc/h6hTKUYLqXuyLD8njTrbRhLgbC9QrKrS
M1F2fSTxVqPtZDlDMwjNR04xHA/fKh8bXXyTMqOHNJTHHNhbh3McdURjAoGBANkU
1hqfnw7+aXncJ9bjysr1ZWbqOE5Nd8AFgfwaKuGTTVX2NsUQnCMWdOp+wFak40JH
PKWkJNdBG+ex0H9JNQsTK3X5PBMAS8AfX0GrKeuwKWA6erytVTqjOfLYcdp5+z9s
8DtVCxDuVsM+i4X8UqIGOlvGbtKEVokHPFXP1q/dAoGAcHg5YX7WEehCgCYTzpO+
xysX8ScM2qS6xuZ3MqUWAxUWkh7NGZvhe0sGy9iOdANzwKw7mUUFViaCMR/t54W1
GC83sOs3D7n5Mj8x3NdO8xFit7dT9a245TvaoYQ7KgmqpSg/ScKCw4c3eiLava+J
3btnJeSIU+8ZXq9XjPRpKwUCgYA7z6LiOQKxNeXH3qHXcnHok855maUj5fJNpPbY
iDkyZ8ySF8GlcFsky8Yw6fWCqfG3zDrohJ5l9JmEsBh7SadkwsZhvecQcS9t4vby
9/8X4jS0P8ibfcKS4nBP+dT81kkkg5Z5MohXBORA7VWx+ACohcDEkprsQ+w32xeD
qT1EvQKBgQDKm8ws2ByvSUVs9GjTilCajFqLJ0eVYzRPaY6f++Gv/UVfAPV4c+S0
kAWpXbv5tbkkzbS0eaLPTKgLzavXtQoTtKwrjpolHKIHUz6Wu+n4abfAIRFubOdN
/+aLoRQ0yBDRbdXMsZN/jvY44eM+xRLdRVyMmdPtP8belRi2E2aEzA==
-----END RSA PRIVATE KEY-----" > private.key
Ritvik@DESKTOP-4RHVIFV MINGW64 ~
$ ssh -p 2220 bandit14@bandit.labs.overthewire.org -i private.key
bandit14@bandit:~$ cd /etc/bandit_pass/bandit14
-bash: cd: /etc/bandit_pass/bandit14: Not a directory
bandit14@bandit:~$ cd /etc/bandit_ass
-bash: cd: /etc/bandit_ass: No such file or directory
bandit14@bandit:~$ cd /etc/bandit_pass
bandit14@bandit:/etc/bandit_pass$ cat bandit14
fGrHPx402xGC7U7rXKDaxiWFTOiF0ENq

----------------------------------------------------------------

From level14 to level15
$ ssh -p 2220 bandit14@bandit.labs.overthewire.org
pass- fGrHPx402xGC7U7rXKDaxiWFTOiF0ENq
bandit14@bandit:~$ nc localhost 30000
fGrHPx402xGC7U7rXKDaxiWFTOiF0ENq
Correct!
jN2kgmIXJ6fShzhT2avhotn4Zcka6tnt

----------------------------------------------------------------

finally reached level 15



























