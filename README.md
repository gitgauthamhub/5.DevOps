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
ls -l

$ chmod ugo+w devops.txt
$ chmod 700 devops.txt

>> Only Owner/Root user can change the permissions

Ownership
Ownership refers to the user and group associated with a file or directory,

chown <user>:<group> devops.txt

 


















