## KEY TAKEAWAYS FROM THIS MODULE:
- man is the manual
- apropos to search through man pages, use mandb to intialize the database for this command
- -r for recursive calls
- ln to create a hard link, ln -s for a soft link
- Use stat on a file to view detailed logs about that file vs. ls -l which shows a decent amount of details for the whole pwd

## DOCUMENTATION

-   "**man**" command shows a written manual for a given command
-   "--**help**" shows a really brief desc about a command, man is more detailed
-   "**apropos**" allows us to search through man pages to look for a command
    -   "**apropos director**" searches through man pages that contain director
    -   **apropos**  NEEDS a db to function, run sudo mandb to initiate the db
    -   "**-s**" lets us define a range of what we want to be returned

## DIRECTORIES

-   "**ls**" command shows files in current dir
    -   -l is for long list format
    -   -a shows hidden files
        -   you can combine flags like this -a -l => -al
-   Filesystem Tree
    -   Absolute Path always starts at the root and then goes to the target file
    -   Relative Path is a file location based on your pwd
-   pwd to see the current dir
-   cd
    -   / takes you to root dir: cd /
    -   -   takes you to previous dir
    -   cd by itself takes you to home dir
-   cp to copy files
    -   cp [source_file] [dest]
    -   Good practice to end dirs in a /
    -   -r is for recursive, you can use this to copy dirs
        -   Goes down the tree until there is no other files and works its way up
-   mv is similar to copy but you will not have two copies of the file
    -   cp [source_file] [dest]
-   rm to delete files
    -   -r option should be used to del dirs to recursively delete all files present in that dir

## HARD AND SOFT LINKS
- stat allows us to view certain things about a file
	- file points to inode which points to th blocks of data that make up this file
		- this is known as a hard link
- Hard Links are basically labels or an alias for a file, you cannot hl to dirs or external file systems
	- We can have multiple hard links point ot the same file to save space for example
	- use ln to create a hard link
- An Inode stores metadata about a file and points to all the data that make up the file
- When an inode has zero links, it deletes the data and itself
- While Hard Links points to Inodes, Soft Links point to a file itself. 
	- Soft Links are basically text files that have a directory to a file 
	- Soft Links are called symbolic links
	- ln -s targetfile pathtolink
- Use readlink to see where a symbolic links points to
- If you something in the path of the link, the link will break
- You can soft link to dirs and file in external file systems

## FILE PERMISSIONS
- Every file and dir is owned by a user and group, use ls -l 
- chgrp to change the assigned group of a file or dir
- groups allows us to view all groups on this machine
- chown to change the owner of a group, usually sudo
- 