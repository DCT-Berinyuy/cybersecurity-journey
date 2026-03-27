## Linux Fundamentals Part 2

## Filesystem Interactions

More specifically, the following commands:

Command	Full Name	Purpose
touch	touch	Create file
mkdir	make directory	Create a folder
cp	copy	Copy a file or folder
mv	move	Move a file or folder
rm	remove	Remove a file or folder
file	file	Determine the type of a file

## Permissions

Understanding File Permissions in Numeric Format
In Linux, every file and directory has a set of permissions that control who can read, write, or execute it. These permissions are often displayed in symbolic format, such as:

rwxrwxrwx
This format is split into three groups:

Section	Applies To	Example
First 3	Owner	rwx
Next 3	Group	rwx
Last 3	Others	rwx


Converting Symbolic Permissions to Numbers
Each permission has a numeric value:

Permission	Value
Read (r)	4
Write (w)	2
Execute (x)	1
To calculate the numeric value, we add the values together for each group.

Example: rwxrwxrwx
Break it down:

Group	Permissions	Calculation	Value
Owner	rwx	4 + 2 + 1	7
Group	rwx	4 + 2 + 1	7
Others	rwx	4 + 2 + 1	7
So:

rwxrwxrwx = 777
More Common Examples
Symbolic	Numeric	Meaning
rwxr-xr-x	755	Owner can do everything, others can read and execute
rw-r--r--	644	Owner can read/write, others can only read
rwx------	700	Only the owner has access

Why This Matters
Understanding numeric permissions is important because:

Many Linux commands use numeric values (e.g. chmod 755 file)
You can quickly identify security risks
You can control who can access sensitive files
For example:

chmod 750 system_overview.txt
This means:

Owner: full access
Group: read + execute
Others: no access

## Common Directories

### /etc

This root directory is one of the most important root directories on your system. The etc folder (short for etcetera) is a commonplace location to store system files that are used by your operating system. 

### /var

The "/var" directory, with "var" being short for variable data,  is one of the main root folders found on a Linux install. This folder stores data that is frequently accessed or written by services or applications running on the system. For example, log files from running services and applications are written here (/var/log), or other data that is not necessarily associated with a specific user (i.e., databases and the like).

Nice work! This room was quite theory-heavy and covered quite a range of the fundamentals in getting you familiar with Linux. To quickly recap, this room taught you:

How to connect to a Linux machine remotely using SSH
Advancing your use of commands by providing flags, switches and where you can go to learn about these for each command (man pages)
Some more commands that you'll frequently be using to interact with the filesystem and its contents
A brief introduction to file permissions & switching users
A summary paragraph of the important root directories on a Ubuntu Linux install and how we may be able to use the data stored within these.
I encourage you to go through this room again once or twice to gain some familiarity with the concepts. After all, practice makes perfect! 

