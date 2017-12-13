jacquie: x:1004:1004: jacquie, 1,,:/home/jacquie :/bme the user signs into the system, he/she is taken to their Home directory, where 
all their personal files reside. This field provides the absolute path to the user's home directory (/home/jamal in this case). 7. 
Shell: This field show, the user has access to the shell mentioned in this field (user 'jamal' has been given access to /bin/bash or 
simply bash shell).

Adding new user accounts to Linux system 

There are tow option to add a user to the system eithet by using the desktop tools or by using command line. We can use the command 
line by using a simple command adduser with the new user name it will created account for the new user with some files that will help 
to configure his account. When running command adduser the system will ask additional information for the new user. 

I will explain this information step by step.

We will take an exampile to add new user jamal to the system.

$ sudo adduser jamal

Adding user 'jamal' ...

Adding new group 'jamal'(100) ...

Adding new user 'jamal'(100)with group 'jamal' ...

Creating home directory '/home/jamal' ...

Copying files from '/etc/skel; ...

Enter new UNIX password:

Retype new UNIX password:

Passwd:password updated successfully

Changing the user information for jamal

Enter the new value, or press ENTER for the defualt

Full name []: jamal ibrahim

Room Number []:

Work Phone []:

Other []:

Is the information correct?[Y/n] Y

As we see in the above example, how the adduser command add the new user information to the file (/etc/passwd) and create the new home 
directory and establish with some files from the /etc/skel then ask for new password and identify the information.

**Deleting user account from Linux system.

After we learning how to add a new user to the system, also we will learn how to delete the user account from the linux system. 

To remove user's name or account from the local system/server/workstation we should use the command userdel.

root/h/elivuser>>> sudo userdel jamal

To remove all file along with the home directory and mail spool we add -r to userdel

root/h/eliveuser>>> sudo userdel-r jamal

userdel:jamal mail spool(/var/mail/jamal)not found

This is all about the adding AND DELETING THE NEW USER ACCOUNT TO THE lINUX SYSTEM.

Package Managementin/bash

jacquiematthew: x:10041005:10041005: jacquiematthew, 1,,:/home/jacquiematthew :/bin/bash

matthew: x:1005:1005: matthew, 1,,:/home/matthew :/bin/bash 

to get depth in the file I will take the entry of my username jamal.


/etc/passwd fields

1. **Username field**: This field show the user account name; this user name must be used every time when we log in to the system.

2. **Password field**: Second field is the Password field, not showing the actual password though. The 'x' in this field show the password is encrypted and saved in the /etc/shadow file.
3. **UID field**: Every time when a user account is created, it is assigned with a user id or UID (UID for the user 'jamal' is 1001, in this case) and this field specifies the same.
4. **GID field**: Similar to the UID field, this field specifies which group the user belongs to, the group details being present in /etc/group file.
5. **Comment/Description/User Info field**: This field is the short comment/description/information of the user account.

6. **User Home Directory**: Every ti6. **User Home Directory**: Every time the user signs into the system, he/she is taken to their Home directory, where all their personal files reside. This field provides the absolute path to the user's home directory (/home/jamal in this case).
7. **Shell**: This field show, the user has access to the shell mentioned in this field (user 'jamal' has been given access to /bin/bash or simply bash shell).
