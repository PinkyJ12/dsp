# Learn command line

Please follow and complete the free online [Bash Scripting Tutorial](https://ryanstutorials.net/bash-scripting-tutorial/) or [Codecademy's Learn the Command Line](https://www.codecademy.com/learn/learn-the-command-line). These are helpful tutorials. You should be able to go through these in a couple of hours.

**Note:** Bash is not installed on a PC. Rather, PC users must install Cygwin. Once Cygwin has been installed, the command line interface witll _emulate_ bash. You can find all information regarding Cygwin [here](https://www.cygwin.com/).

---

### Q1.  Cheat Sheet of Commands  

Here's a list of items with which you should be familiar:  
* show current working directory path
* creating a directory
* deleting a directory
* creating a file using `touch` command
* deleting a file
* renaming a file
* listing hidden files
* copying a file from one directory to another

Make a cheat sheet for yourself: a list of at least **ten** commands and what they do.  (Use the 8 items above and add a couple of your own.)  

> > 
| Action | Command |
| --- | ---- |
| show current working directory path |	pwd |
| creating a directory	| mkdir |
| deleting a directory |	rmdir -d/-r # remove empty directories / remove directory with its subdirectories |
| creating a file using touch command	| touch somfile.txt|
| deleting a file	| rm (filename)|
| renaming a file	| mv original.txt new.txt|
| listing hidden files |	ls -a|
| copying a file from one directory to another	| cp (copied_file) (desired_directory_path)|
| searches a plain text file for a line matching a regex | grep (stands for 'global regular expression print').|
| makes command case insensitive | grep -i|
| searches all files in a directory and oputs filenames and lines containing matched results | grep -R(-R stands for recursive)|
|returns names of files containing a match | grep -Rl |


---

### Q2.  List Files in Unix   

What do the following commands do:  
`ls`  
`ls -a`  
`ls -l`  
`ls -lh`  
`ls -lah`  
`ls -t`  
`ls -Glp`  

> > 
* ls:	Short listing
* ls -l:	Long listing
* ls -a:	Listing including hidden files
* ls -lh	:Long listing with Human readable file sizes
* ls -lah: Displays long list, including hidden files with a human readable file size
* ls -t	Displays files forder by latest date and time
* ls -Glp: list all contents in directory in long format, excluding display group and directories with a '/'

---

### Q3.  More List Files in Unix  

Explore these other [ls options](http://www.techonthenet.com/unix/basic/ls.php) and pick 5 of your favorites:

> > 
| Command | What it does |
| ---- | ---- |
| -q	| Displays all nonprinting characters as ? |
| -r	| Displays files in reverse order.|
| -R	| Displays subdirectories as well.|
| -t	| Displays newest files first. (based on timestamp)|
| -1	| Displays each entry on a line.|
| -p	| Displays directories with / |

---

### Q4.  Xargs   

What does `xargs` do? Give an example of how to use it.

> > The most important usage of xargs command is to combine Xargs with Find Command. When you need to find certain type of files and perform certain actions on them (most popular being the delete action). https://www.thegeekstuff.com/2013/12/xargs-examples/ **
So, in this example, the output of the find command is all the files with *.c extension, which is given as input to the xargs command, which in-turn execute “rm -rf” command on all the *.c files.**
$ ls **
one.c  one.h  two.c  two.h **

$ find . -name "*.c" | xargs rm -rf **

$ ls **
one.h  two.h


 

