# Linux Commands

## Informational Commands

* `whoami` to return your username
* `uname` to print the kernel name
* `uname -a` to print all kernel information
*  `cat /etc/os-release` OS imformation
* `id` to display the user and group id
* `df` to print available disk space
* `df -h` to print available disk space in human readable format
* `ps` to list running processes and their process id
* `ps -e` to list all processes
* `ps -eaf` to list all processes with full information
* `top` to view a real-time table of processes
* `top -n 10` to view a real-time table of the top 10 processes. Shift + M to order in terms of memory usage. Shift + P to order in terms of CPU usage. Shift + Q to quit
* `echo` to print given text
* `date to display the current time and date
* `date +%T` to display the current time
* `man` to get the user manual for a command
  
## File wrangling commands

* `sort abc.txt` to sort a file in alpha-numeric order
* `sort -r abc.txt` to sort a file in reverse alpha-numeric order
* `uniq` to remove duplicate lines from a file
* `cat` to print the contents of a file
* `head -n 5` to print the first 5 lines of a file
* `tail -n 5` to print the last 5 lines of a file
* `more` to display the contents of a file one page at a time, use `space` to go to next page and `q` to quit
* `less` to display the contents of a file one page at a time, you can go back to the previous page by pressing `b`.
* `grep abc abc.txt` to search for a string in a file
* `grep -i abc abc.txt` to search for a string in a file, ignoring case
* `cut -c 2-9 abc.txt` to print the second to ninth character of each line in a file
* `cut -d ',' -f1 abc.csv` to print the first column of a csv file
* `paste -d ',' abc.txt def.txt` to paste two files together using comma as delimiter
* `wc abc.txt` to count the number of lines, words and characters in a file

## File permissions in Linux

In Linux, file permissions determine the actions that can be performed on a file or directory. There are three types of permissions:

* **Read (r)**: User can read the contents of the file.
* **Write (w)**: User can modify the contents of the file.
* **Execute (x)**: User can run the file as a program.
* **directory (d)**: User can list the contents of the directory.

These permissions can be set for three types of users:

* **User (u)**: The owner of the file.
* **Group (g)**: The users who are members of the file's group.
* **Others (o)**: All other users.

You can use the `chmod` command to change the permissions of a file or directory. For example, `chmod u+x filename` will give the user (u) execute (x) permission on the file.

## Achieve and  compress files

### Compressing and Archiving

Tar (tape archive) is a command line utility that allows you to create and extract tar archives.

|Option|Description          |
|------|---------------------|
|-c|Create new archive file|
|-v|Verbosely list files processed|
|-f|Archive file name|
|-x|Extract archive|

* `tar -cf notes.tar notes` to create a tar archive of the notes directory
* `tar -czf notes.tar notes` `z` will compress the tar archive using gzip
* `tar -tf archive.tar` will list the contents of a tar archive
* `zip -r notes.zip notes` to create a zip archive

### Extracting and Un-compressing

* `tar -xf archive.tar my_folder` to extract a tar archive
* `tar -xzf notes.tar.gz` to extract a tar archive that has been compressed with gzip
* `unzip notes.zip`

## Networking commands

* `hostname -I` to display the IP address of the machine
* `ping` to ping a server
* `ifconfig` to display network information.
* `curl -O` to download a file from a server and save it with the same name
* `curl -O -L -u username:password` to download a file from a server and save it with the same name, following redirects, authenticating with username and password
* `curl -L -u username:password -o newname` to download a file from a server and save it with a new name, following redirects, authenticating with username and password
* `wget -O newname` to download a file from a server and save it with a new name
* `wget -O newname -u username:password` to download a file from a server and save it with a new name, authenticating with username and password
* `wget -O newname -u username:password --no-check-certificate` to download a file from a server and save it with a new name, authenticating with username and password, ignoring certificate errors
