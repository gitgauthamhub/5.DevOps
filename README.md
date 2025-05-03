# 5.DevOps
==============

Permissions
Permissions define who can access a file or directory and what actions they can perform (read, write, or execute). 
Permissions are a core part of Linux’s security model, controlling access for users, groups, and others.

======================
R -> 4,    W -> 2,   X -> 1

-			rw-		r--		r--

file/		user/   group	others

owner

directory     u       g       o

ec2-user   ec2-user

user		   group
======================

$ touch devops.txt
>> ls -l

$ chmod ugo+w devops.txt
$ chmod 700 devops.txt

>> Only Owner/Root user can change the permissions

Ownership
===========
>> Ownership refers to the user and group associated with a file or directory, Note : Now change User/Group ownership 

chown <user>:<group> devops.txt

Change the path
$ cd /tmp/
>> ls -l

$ touch aws.txt
>> ls -l            

Sudo access to user
===================
>> sudo access to a user in Linux allows them to execute commands with superuser (root) privileges,  You must be logged in as the root user or a user with sudo privileges to make these changes.

$ sudo useradd gautham
>> ls -l
$ chown  // it will not work bcz file ownership can only be modified by root user

$ sudo chown gautham aws.txt
>> ls -l

$ sudo chown gautham:gautham aws.txt  
>> ls -l

Key based authentication
========================
>> Secure method for authenticating users to a remote server (e.g., via SSH) using a pair of cryptographic keys instead of passwords.
>> How can you give key based access to linux user?


1. create user
2. sivakumar can send his public key to admin user
3. /home/gautham admin creates .ssh in /home/gautham folder
4. gautham is the only owner to this folder... 700
5. create a file called authorized_keys with max access 600
6. admin keeps gautham public key here.
7. now gautham should be able to login

>> $ pwd  >> $ cd  >> $ ls -la  >> $ cd .ssh  >> $ ls -l  >> cat filename

$ systemctl status sshd
>> Note here u can see the content

>> Note : 65,536 ports 0-65,535  || Ports enable a single device (with one IP address) to run multiple services (e.g., web server, SSH, database) by directing traffic to the correct application.
Think of an IP address as a building’s address and a port as an apartment number.

























