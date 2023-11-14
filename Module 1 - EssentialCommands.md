## DOCUMENTATION
- "**man**" command shows a written manual for a given command
- "--**help**" shows a really brief desc about a command, man is more detailed
- "**apropos**" allows us to search through man pages to look for a command
	- "**apropos director**" searches through man pages that contain director
	- **apropos** NEEDS a db to function, run sudo mandb to initiate the db
	- "**-s**" lets us define a range of what we want to be returned

## DIRECTORIES
- "**ls**" command shows files in current dir
	- -l is for long list format
	- -a shows hidden files
		- you can combine flags like this -a -l => -al
- Filesystem Tree
	- Absolute Path always starts at the root and then goes to the target file
	- Relative Path is a file location based on your pwd
- pwd to see the current dir
- cd 
	- / takes you to root dir: cd /
	- - takes you to previous dir
	- cd by itself takes you to home dir
- cp to copy files
	- cp [source_file] [dest]
	- Good practice to end dirs in a /
	- -r is for recursive, you can use this to copy dirs
		- Goes down the tree until there is no other files and works its way up
- mv is similar to copy but you will not have two copies of the file
	- cp [source_file] [dest]
- rm to delete files
	- -r option should be used to del dirs to recursively delete all files present in that dir
