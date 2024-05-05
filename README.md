# Complete Linux Course
How to install Zsh and configure its themes
--> https://phoenixnap.com/kb/install-zsh-ubuntu

My Theme: Steeef
```bash
echo $PATH //This command is used to check which directory is used for executables files (Env variables)
```
*****************Linux Commands
> ls (for list of directories)
> "ll" or "ls -l" (for detailed list of directories)
> sudo apt install package_name (use to install latest packages here apt means "Advance package tool manager" and sudo means "superuser do")

********Working with directories
> Man name_of_any_command (this command is used to see the manual of any thing that you will provide. e.g, "man cd" this command will give you the manual of cd command.
In linux a folder name start with "." will be considered as hidden file. It will be disappeared in GUI. If you want to see all you files whether they are hidden or not then you can use the following comman:
> ls -a (here -a flag is for all)
> ls -la (here -la is a combination of two flag that is length for l and all for a)
> ls -lah (here you will get all you files with long details and h for unit of their size like KB etc.)
> pwd (this command is used for checking the location where we are as it stands for print working directory)
> mkdir (this command is used for making directories)
> cd (This command is used to change the directory. This command requires an argument as name or path of directory where you want to go. If only cd alone is executed then it will bring you     to the home directory by default)
> mkdir -p folder1/folder2/folder3 (this command "mkdir -p" is used to create a tree nested folders in one line)
> rmdir (this command is used to remove the directory of which name the user have provided)
NOTE: we cannot delete a folder which is not empty
> rmdir -p folder1/folder2/folder3 (this command "rmdir -p" is used to delete nested folders in one line)

**********Working with files
// In linux files and folder names are case sensitive.
// In linux even a directory is considered as file. It is considered as special type of file. But yes, it is considered as a file.
> file (this command is used to check the type of the file which you have provided in the argument.
> touch file_name (this command is used to create empty files of which name is provided as an argument. NOTE: you can create more than one file by providing more than one names at once like >touch file1 file2 file3 (this will create 3 files))
> rm file_name (this command is used to delete the files. You can delete more than one file at a time)
> rm -i file_names (this commadn is to interact with the command while deleting. Like this will ask before deleting the file. For responsd "yes" for delete and "no" for ingore
> rm -rf (here -rf means recursive force. This command can be used to delete file or folder forcefully)
> cp file_name path newFileName (this command is used to copy files e.g > cp file1 /home/docs/ file1copied)
NOTE: If you want to copy the file within the same directory then you do not have to provide a path you simply have to provide a new name as you cannot copy or create files with the same name within the same directory but you can do it in other directory.
> cp -r folder_name path newFolderName (this command is used to copy directories. This will also copy the content which is in the directory)
> mv (this command is used to move and rename a file or folder. Syntax: >mv fileName path newFilename (this will move your file to the given path and will rename it at the same time.)
> mv fileName NewFileName (this command will only rename your file)

********************Working with file Content
> head file_name (this command is used to get the first 10 lines of the file)
> head -5 file_name (this command will onlly bring the first 5 lines. You add any number you want from 1 to 10)
> tail file_name (this command is used to get the last 10 lines of the files)
> tail -5 file_name (this command will onlly bring the last 5 lines. You add any number you want from 1 to 10)
> cat file_name (this command is used to print the full file. Here cat means concatenate. Here if you would print more than 1 file by giving each name in one line separated by spaces then it will print the contant of all files)
> echo your_content > fileName (this command is used to create files with the provided content. Here ">" this symbol is a part of the syntax)
> cat > fileName.extension (here cat command can also be used to create files and write content in it. After typing this command you will be get entered into writing mode. Write your content whatever you want and then to get exit of the writing mode press Ctrl + D )
> cat filename > newFileName (cat command can also be used to rename the file)
> more file_name (this command is also used to read the document. But this will print the file per page at a time. Like it will print let say 30% of the content then on pressing space button it will print the next 30% and so on)
> less file_name (this command is opposite of more.)

***********************System information commands
NOTE: Why use these commands? The answer is that when you will be working with the servers then there will not be any GUI then you have to do all things with commands.
> uptime (this command is used to check how long has been your system is running)
> free (this command is used to check how much your memory is free and how much your memory is in use)
> ps -A (tihs command is used to get the snapshot of current running processes)
> df (this command give you all info about your hard disk)
> sudo fdisk -l (this command is used to get the information about your disk partitions. Here sudo is used for administrative right. As this fdisk command cannot run without sudo)
> lsblk (this command is used to check the list of block devices)
> top (this command is used to display the linux processes in GUI format within the terminal)
> htop (this command is the upgraded version of top command and it will give you a better representation of linux processes. if this command is not installed by default then you can download it by using: > sudo apt install htop)
***************************Networking
> ifconfig (this command is used to get the network information of your system)
> ip or ip a (this command is used to show/manipulate routing, network devices.)

***************************Linux Package Manager
NOTE: There are some operations that linux restrict to their user to perform. In order to perform such actions sudo command is used which is used to execute the command as another user or super user
> sudo apt update (this command will tell you about the packages which are supposed to update. This command will only tell you. This will not update your packages)
> sudo apt upgrade (this command will upgrade your packages)
> sudo apt search package_name (this command is used to search the packages)
> sudo apt install package_name (this command is used to install the packages)
> sudo apt remove package_name (this command is used to uninstall the packages)

*********Text editors
There are several text editors in linux. While working with server there may be a need to edit files. There you will have to open then in any text editor of your choice with in the terminal and then use it.
we will learn 2 of them:
1. Nano
2. Vim

1) Nano:
> Nano file_name (this will simply open up the file in the terminal in insert mode. You simple have to write whatever you want and then press Ctrl+X. This will ask you to save or not. Y for yes and N for No.)
Now you can verify your changes by using >cat file_name

2)vim
>sudo apt install vim
>vim file_name (this will just open your file in vim editor in terminal in read mode. You wont be able to write anything as it is in read mode. To start writing you have to click "i" to enable --insert mode and then to save the changes you have to press escape first to get out of insert mode and then press 	colon ":" and write w so in short write :w and press enter.
to get exit from vim editor write :q
To get exit and save file in one command write :wq

************Some other commands
There three roles of a file
User, group and other (u, g, o)

And there are three position or conditions
Read, write and execute (r, w, x)

---     ---     ---
 u       g       o
rwx     rwx     rwx

We can make combinations and peform our desired action such as

>chmod r+w, r+x, x note
Means
User can read and write
Group can read and execute
Other can execute only

In terms of octal notation
r=6
w= 4
x=1

>chmod 555 note write and execute as w+x=4+1=5

Means ugo all 3 can


**NOTE**: Any file that start with . is a hidden file. To see hidden files we can do
```bash
ls -a
```
```bash
vi path_to_file // this command is used to edit the file
```
**TIP**: 
press esc and :q to get exit without saving tha file 
press esc and :wq to get exit and saving tha file

```bash
nano path_to_file // this command is used to edit the file, they are also text editor
```
```bash
chsh -s $(which zsh) // chsh - change login shell, here the command changes the default shell to Zsh for the current user. To start using the Z Shell, log out of the terminal and log back in.
```

```bash
ls -R //here -R flag means recursive (shows folder inside folders inside folders and so on)
```
```bash
cat > hello.txt (this command will create hello.txt file and you will enter into the editing mode, now write what you want to write in this file)
```
```bash
cat hello.txt (this command will be used to read all the content of hello.txt)
```
```bash
echo "hello world" // echo command is used as print command
```
```bash
echo "hello world" > file.txt // now using > this symbol, the echo command will write the given text in file.txt
```
## if you want to make your file content in upper case

```bash
cat newFile.txt | tr a-z A-Z > Upper.txt //here "tr" command is used to translate the content. I am translating all characters from a-z to A-Z and saving it into a new file called upper.txt
```

## how to create a directory between two existing directories?

```bash
mkdir -p hello/middleFolder/cool
```
here middleFolder will be created inside hello folder...now hello folder will have two directories middleFolder and cool Folder

**NOTE**:
For ppl who are confused,
mkdir -p
It will create parent directory first, if it doesn't exist. But if it already exists, then it will not print an error message and will move further to create sub-directories. This command is most helpful in the case when you don't know whether a directory already exists or not.

## how to delete a directory that is not empty

```bash
rm -r path_to_folder
```
```bash
rm -r !(path_to_folder) //means remove all files except in the round bracket
```

here - r is for recursive
```bash
touch fileName //this command will be used to create a filef
```

```bash
## merging the content of two files in a new single file
```bash
cat hello.txt hello2.txt > myNewFile.txt (this command will be used to read all the content of hello.txt)
```
## copying the files
```bash
cp textfile.txt newTextFile.txt //this will make copy of the file with newName
```
```bash
cp -R folder1 folder2 //this will copy all the content even folder inside folders from folder 1 and folder 2
```


**TIP**: Ctrl + X for exiting the file and Ctrl + S for saving the file

## How to move files and Rename it

```bash
mv file.txt path-to_the_folder //this will move your file 
```
```bash
mv file.txt newFile.txt //this will rename your file name
```

## moving and renaming at the same time:
```bash
mv file.txt ../newFile.txt //this will move your file to the previous directory and will rename it at the same time.
```
# new commands
```bash
df //this command is used to check disk space and all other stuff related to disk
```
```bash
du //this command is used to check disk usage
```
```bash
head file.txt //will show 1st 10 lines only
```
```bash
head -n 4 file.txt //will show 1st 4 lines only
```
```bash
tail file.txt //will show last ten lines only
```
```bash
tail -n 4 file.txt //will show last 4 lines only
```
## installing locate command
```bash
sudo apt install plocate // find files by name, quickly
```
```bash
locate "*.txt" //will locate all files ending with .txt 
```

# find files
```bash
find file // find - search for files in a directory hierarchy. This command is used to find files only
```
```bash
find file1 -type f //here f flag reprsents file
```
```bash
find . -type f -name "two*" //here f flag reprsents file
```
This command means that find in the current directory type should be file and name should be start with two

**NOTE** All names we are providing is case sensitive. If you want that it should search without any case sensitive then it should you can do -iname flag instead of -name flag
```bash
find . -type f -iname "two*" //here f flag reprsents file
```

# finding files on the basis of time

```bash
find . -type f -mmin -20 //all files in the current direcotry modified less than 20 mins
```
```bash
find . -type f -mmin +15 //all files in the current direcotry modified more than 15 mins
```
# finding files on the basis of days

```bash
find . -type f -mtime -10 //all files in the current direcotry modified less than 10 days
```
```bash
find . -type f -mtime +15 //all files in the current direcotry modified more than 15 days
```



```bash
find . -type f -empty //all files in the current direcotry that are empty
```
```bash
find . -type f -size +1k //all files in the current direcotry that are more than 1 KB
```

# finding folders
```bash
find testing -type d //here d flag reprsents directory
```

# Permissions

```bash
ls -l fileName.txt //This command will give you info about the permisions of the file
```

There are three types of users:
1) User u
2) Group g
3) Other o
3) root sudo


# Changing the permissions
Method 1
```bash
chmod u=rwx,g=rx,o=r myFile.txt
```

ugo <-- user , group, other

read r = 4
write w = 2
execute x = 1

so rwx = 7
rx = 5
rw = 6
wx = 3
rx = 4
and so on.

Method 2
```bash
chmod 754 myFile.txt 
```
754 means
u=rwx,g=rx,o=r

# how to change the user/owner 
```bash
whoami // this command is used to check who is the user
```
```bash
sudo chown root myFile.txt //now this will change access to this file to only root user. Means to do operations on myFile.txt you have to use sudo
```
```bash
cat myFile.txt // You will get error cuz you are trying to access this file as a current user where the access is only allowed to the root user
```
```bash
sudo cat myFile.txt // now you will have access as now you are trying to get access as a root user
```

# how to delete multple files or folders:

```bash
find . -type f -name "*.txt" -exec rm -rf {} +
```

//here {} is the place holder and all the result of find command will go inside the place holder {} and exec will help us to execute the rm command.
In the same way you can rename multiple files are the same time.

# how to search for the content inside a file

```bash
grep "Hello world" myFile.txt // this is case sensistive
```

```bash
grep -p "\your_regex_will_go_here\" myFile.txt //this is case sensistive
```
# Checking the History
```bash
history //this command will show you the history of commands
```

```bash
history | grep "ls" //this command will search the history of ls commands
```

here | symbol means piping

# sort command
```bash
sort myFile.txt //this command will sort the content inside it
```
# System info commands
```bash
you can check IP address of your ISp (Internet service provider) by this command
> curl ifconfig.me -s
```

```bash
ping google.com //cconnects to the server extract info and check ping
```

```bash
wget url //this command is used to download content from the url
```
```bash
wget -o newName url //this command is used to download content from the url
```

```bash
uname //this command will tell you about your system info
```
```bash
uname -o //this command will tell you about your system info type
```
```bash
uname -m //this command will tell you about your os architecture
```
```bash
cat /etc/os-release //this command will tell you about release information
```
```bash
lscpu //command for cpu details
```
```bash
free //command for checking free memory
```
```bash
vmstate //command for virtual memory stat
```
```bash
lsof //command for any file that is currently open by the system
```
```bash
nslookup googl.com //tells you about the server ids
```

```bash
hostname //this command is used to get the host name
```
```bash
hostname -i //this command is used to get ip address of your host
```
```bash
netstate //to get all the ports that are currently opened
```

# how to add user
```bash
sudo useradd newuser //add user
```
```bash
sudo passwd newuser //set password for new user
```
```bash
sudo userdel newuser //delete user
```
```bash
ps aux //to see processes
```
# how many processes are running
```bash
top
```

# zipping and unzipping files
```bash
zip myZippedFile.zip content.txt content2.txt //this will zip content and content2 into myZippedFile
```
```bash
unzip myZippedFile.zip //this will unzip myZippedFile
```
# Alias

# Keyboard shortcuts

```bash
ctrl + a //to get the cursor at the beginning of the line
```
```bash
ctrl + e //to get the cursor at the end of the line
```
```bash
ctrl + k //to remove text after the cursor
```
```bash
ctrl + u //to remove all the text from the line
```
```bash
!serialNumberFromHistoryOfCommands //can be used to execute previous commands
```
```bash
Ctrl + r //this command is used to search pervious commands
```
```bash
git add . ;git commit -m "initial commit"; git push origin main //using ; you can execute multiple commands in a single line
```

## how to group two commands?
```bash
echo "hey" && {echo "hi; echo "I am good"}
```
## How to append text in a file
```bash
echo "heeyyy" >> myFile.txt //this command will append heeyyy in myFile.txt
```
