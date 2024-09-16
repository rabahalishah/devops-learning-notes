# Introduction to DevOps
# What is devops?
DevOps is a culture. A devOps engineer job is to improve the delivery time of an application by implementing the automation, making sure the quality, implementing the monitoring and testing the application.

# Why DevOps Engineer?
Ten year back there were roles like, System Administrator, Build and Release Engineer, Sever Admin. System admin used to create a server, Server engineer creates the application server and do all the testing on Server, Build and release engineer deploy the application to the server.
This whole process from development to production/delivery requires are manual process that was time taken as the work was divided on different roles. Then DevOps comes into play whose job is to improve the delivery time of an application by implementing the automation, making sure the quality, implementing the monitoring and testing the application.

## SLDC (Software Development Life Cycle)
When you are developing a product you have to follow some standards. SLDC is a standard that every team has to follow to build a high quality product.
SLDC contains the following steps:

1) Planning and Requirements: In this phase you do research and find the requirement of the customer. let say you are adding a feature for kids in an e-commerce store. Then you will do all 				your research that for which range of age of kids are high in demand. Then after all you research you create a document called "Software requirement 					specification document"
2) Defining: In this stage, you define that what you are going to achieve on the basis of the Software requirement specification document". Let say you define that in summers your kids 		section should be highly available and scalable.
3) Designing: This phase has 2 stages. High Level Design and Low Level Design. HLD: Here you design the architect of your product in a higher level view. LLD: Here you define that which tech 		stack that you are going to use. How your DB will look like etc.
4) Building/Developing: After desiging, Developers start developing the product, store in local repository and then finally push to git centralised repository.
5) Testing: QA engineers test the code. 
6) Deployment: And then the product is finally deployed.

DevOps role comes into picture for Building, Testing and Deployment. DevOps engineer role is to increase the efficiency of these three phases. Efficiency can be increase by automating these processes. Making the development, testing and deployment part smooth.

**NOTE:** In most of the companies Agile methodology is followed. In which we work in sprints, We dont wait for one phase to complete. Once the part of a phase has completed, we start working on other phase. All phases are running in parallel. 

**What are Virtual machines?**
Lets understand them with an example. let say you have a land of 1 acre and you live a very luxurious life there. After some time you realised that you are only using 1/2 acre and the other 1/2 acre is spare. So you thought to give that other 1/2 acre on rent. Now without disturbing your luxurious life you have gave 1/2 of it on the rent. Now you are using your land efficiently. As we know DevOPs is all about efficiency. Here, In case of servers, Let say AWS setup their Data center in Pakistan. Their server is of let say 100GB and have 100 cores. They installed a hypervisor (Hypervisor is a software that we used to logically divide the system into our desired chunks). Here with the help of Supervisors such and VMware or Xen. We have logically divided our 100GB server into 10GB 10Cores 10 mini servers. Now these servers will be used by millions of users. 
Now let say someone from US request for a virtual machine of the requirement having 5GB and 2 cores to AWS. The AWS will ask the hypervisor and will look for which partition is idle. Then it will give access to the user to that idle server. This will act as a virtual machine as Physically I dont own any physical server. I am just using it virtually and paying for it.

Same way in your PC you can use virtual box of oracle. And you can give remote access to that virtual box to any member of your family. Here 2 members are using the same laptop. One is physically using and one is remotely accessing some of its part via virtual box.

**NOTE:** Remember that, every logical partitiion is complete system in its own way. It has its own memory, storage, processor etc.

## Difference between physical server and Virtual server/machine:

**Physical Server:** A physical server is a tangible piece of hardware, typically a computer or server machine, that houses the CPU, memory, storage drives, and other components needed to run an operating system and applications.
**Virtual Server:** A virtual server, also known as a virtual machine (VM), is an emulated computer system created by software (hypervisor) that partitions physical hardware resources of a single physical server into multiple virtual environments. Each virtual server runs its own operating system and applications, sharing the underlying physical resources with other virtual servers.

**Resource Allocation:**
Physical Server: Resources such as CPU, memory, storage, and network bandwidth are dedicated solely to the physical server and are not shared with other servers.
Virtual Server: Resources are dynamically allocated and can be shared among multiple virtual servers running on the same physical hardware. Resource allocation can be adjusted as needed to meet the demands of each virtual server.

**Flexibility and Scalability:**
Physical Server: Scaling a physical server typically involves adding more hardware components, such as CPU, memory, or storage, which can be a time-consuming and costly process.
Virtual Server: Virtual servers offer greater flexibility and scalability. Additional virtual servers can be created or existing ones can be resized (allocated more or fewer resources) with relative ease, without requiring additional physical hardware.

**Isolation and Security:**
Physical Server: Each physical server operates independently, providing strong isolation between applications and potentially higher levels of security.
Virtual Server: Virtual servers share physical hardware resources, which introduces a degree of resource contention and potential security risks if not properly configured. However, modern virtualization technologies offer robust isolation mechanisms to mitigate these risks.

**Management and Maintenance:**
Physical Server: Managing and maintaining physical servers involve tasks such as hardware installation, firmware updates, and troubleshooting hardware failures.
Virtual Server: Virtual servers can be managed and provisioned using software tools, allowing for centralized management, automated deployment, and easier backup and recovery processes.

## How to create and automate VM
As we have discussed above that we make request (which should be valid, authenticated and authorized) to the cloud providers such as AWS, Azure or Google plateform to create VM. In terms of AWS it is called EC2 instance. This is also called code infrastructure. We simply make request to these cloud service providers and they create the instances using hypervisor and then generate IP address and all the information to get access to this EC2 instance. The procedure and concept is same for all service providers.

Let say someone ask you how can you automate the cloud infrastructure?
you have to write an automation script You can do that in the following ways:
For AWS there are 4 ways:
AWS CLI: Here you can automate the process using CLI
AWS API: AWS also generate the API so that you can interact with it. e.g in python you can use BOTO3 to use AWS API
AWS CFT: Cloud Formation template. AWS CloudFormation simplifies provisioning and management on AWS. You can create templates for the service or application architectures you want and have 	AWS CloudFormation use those templates for quick and reliable provisioning of the services or applications (called “stacks”).
AWS CDK: AWS Cloud development Kit.

There is another option that you can use is "Terraform"
Terraform can be used to automate and manage any cloud infrastructure of any cloud service provider. But if your use case is only AWS then AWS CDK is better than Terraform.


## Hybrid cloud model
There is another cloud model called Hybrid. In this cloud code infrasturture we have used more than one cloud service. For example: google cloud platform is very famous for AI/ML so we can deploy that part on GCP and other on AWS or Azure etc. 


# Complete Linux Course
How to install Zsh and configure its themes
--> https://phoenixnap.com/kb/install-zsh-ubuntu

My Theme: Steeef
```bash
echo $PATH //This command is used to check which directory is used for executables files (Env variables)
```
# Linux Commands
```
> ls (for list of directories)
> "ll" or "ls -l" (for detailed list of directories)
> sudo apt install package_name (use to install latest packages here apt means "Advance package tool manager" and sudo means "superuser do")
```
# Working with directories
```
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
```
# Working with files
In linux files and folder names are case sensitive.
In linux even a directory is considered as file. It is considered as special type of file. But yes, it is considered as a file.
```
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
```
# Working with file Content
```
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
```
# System information commands
NOTE: Why use these commands? The answer is that when you will be working with the servers then there will not be any GUI then you have to do all things with commands.
```
> uptime (this command is used to check how long has been your system is running)
> free (this command is used to check how much your memory is free and how much your memory is in use)
> ps -A (tihs command is used to get the snapshot of current running processes)
> df (this command give you all info about your hard disk)
> sudo fdisk -l (this command is used to get the information about your disk partitions. Here sudo is used for administrative right. As this fdisk command cannot run without sudo)
> lsblk (this command is used to check the list of block devices)
> top (this command is used to display the linux processes in GUI format within the terminal)
> htop (this command is the upgraded version of top command and it will give you a better representation of linux processes. if this command is not installed by default then you can download it by using: > sudo apt install htop)
```
# Networking
```
> ifconfig (this command is used to get the network information of your system)
> ip or ip a (this command is used to show/manipulate routing, network devices.)
```
# Linux Package Manager
**NOTE:** There are some operations that linux restrict to their user to perform. In order to perform such actions sudo command is used which is used to execute the command as another user or super user
```
> sudo apt update (this command will tell you about the packages which are supposed to update. This command will only tell you. This will not update your packages)
> sudo apt upgrade (this command will upgrade your packages)
> sudo apt search package_name (this command is used to search the packages)
> sudo apt install package_name (this command is used to install the packages)
> sudo apt remove package_name (this command is used to uninstall the packages)
```
# Text editors
There are several text editors in linux. While working with server there may be a need to edit files. There you will have to open then in any text editor of your choice with in the terminal and then use it.
we will learn 2 of them:
1. Nano
2. Vim

1) Nano:
> Nano file_name (this will simply open up the file in the terminal in insert mode. You simple have to write whatever you want and then press Ctrl+X. This will ask you to save or not. Y for yes and N for No.)
Now you can verify your changes by using >cat file_name

2) vim
>sudo apt install vim
>vim file_name (this will just open your file in vim editor in terminal in read mode. You wont be able to write anything as it is in read mode. To start writing you have to click "i" to enable --insert mode and then to save the changes you have to press escape first to get out of insert mode and then press 	colon ":" and write w so in short write :w and press enter.
to get exit from vim editor write :q
To get exit and save file in one command write :wq

# Some other commands
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

# Introduction to Bash Scripting
Bash scripting is very similar to a programming language. All we have to follow some standards and then simply run the script. 

## Command to know which shell you are using
```bash
echo $SHELL
```

## Creating first bash script

```bash
nano myfirstbashscript.sh

// inside myfirstbashscript.sh
echo "hello world"
```

## changing the file to executable
```bash
sudo chmod +x myfirstbashscript.sh
```

## executing script
```bash
./myfirstbashscript/sh
```

**NOTE:** The problem here is that if you would run more than one command then command will execute line by line which we do not want. We want to execute the file as a whole. And if we do not specify .sh extension then how would the bash know that it is a bash script?
To answer both of the valid question we have to create a bash file in a right way.

# Creating a bash file using best practices:
```bash
nano myfirstbashscript.sh

// inside myfirstbashscript.sh
#!/bin/bash   <---this line will turn this file into a true bash script
echo "hello world"
```

# Using Variables in Linux:
```
// inside mybashscript.sh
#!/bin/bash

myname = "Rabah Ali Shah"
now=$(date)  //there should be space between them

echo "my name is $myname"
echo "Today data is $now"
echo "my username is $USER"

```

**Output**
```bash

my name is Rabah Ali Shah
Today data is Wed Aug 21 08:32:28 PM PKT 2024
my username is rabahalishah

```

- Here you can see myname is simply a variable
- here now = $(date), now is storing an output of a command. Here $() is a subshell. Means shell inside a shell where you can run commands and can store their information.
- here $USER is a built in environment variable. Therefore, its in Capital letter distinguishing it self from other. Therefore, it is recommended not to define user defined variables in captial letter.

## Checking the list of environmental variables:
simply run:

```bash
env
```

# Evaluating mathematical Expressions in bash:

```
expr 40 + 40
// output 80

expr 18 \* 2
// output 36
```

# If statement in Bash:
```
#!/bin/bash
num=200

if [ $num -eq 200 ]
then
 echo "yes equal"
else
  echo "No"
```
```
#!/bin/bash
package=/usr/bin/htop

if [ -f $package ]
then
 echo "Yes, package exists, lets run it"
else
  echo "No, package does not exist. Lets install it"
   sudo apt update && sudo apt install htop -y
fi #<-- closing if condition
$package
```
**NOTE:** Here -f is used for checking whether a file exists or not. It is same as using -d for checking whether a directory exists or not. And spaces are compulsory between []

# Exit Code in bash:
Exit codes are used to check whether a command has been successfully ran or not. If atus is 0 then it is success else fail or something went wrong. Below commands can be used to check the status code of most recent command executed. The location of $? command is extremely important in the code. It must be run right after the command of which exit code  you want to get.
```
echo $?
```


```
#!/bin/bash
package=akdsnsfd

sudo apt update && sudo apt install $package >> installation_success.log

if [ $? -eq 0 ]
then
 echo "$package has been installed successfully!"
else
 echo "$package cannot found package" >> failure.log
fi
```

# While loop in Bash:

## Real-time monitoring whether a file exists or not
```bash
#!/bin/bash
file=~/abc

while [ -f $file ]
do
  echo "file exists by $(date)"
  sleep 0.5
done

```

# universal OS update script:
```
#!/bin/bash
release_file=/etc/os-release

if grep -q "Arch" $release_file
then
   sudo pacman syu #<-- used to update packages in Arch Linux
fi
if grep -q "Debian" $release_file || grep -q "Ubuntu" $release_file
then
   sudo apt updateas
fi


```

# for loop in bash
The below script will convert all files ended with .log in logfiles directory into zip file.

```
#!/bin/bash

for file in logfiles/*.log
do
   tar -czvf $file.tar.gz $file  #<-- tar command is used to make archive/zip file
done


```

# Where to store you bash script?
According to Linux FHS File hierarchy system you must store your bash files in /usr/local/bin

lets move our universal update script from our home to usr/local/bin

```
sudo mv ./update /usr/local/bin

#changing its permissions
sudo chown root:root /usr/local/bin/update

```
since we have moved it to usr/local/bin now we can run update script simply by typing 'update'. Linux will automatically look in the PATH and we all know usr/bin/local is already in PATH variable

**HOW TO UPDATE YOUR PATH VARIABLE**
```
export PATH=/your_custom_path:$PATH
```

# Dealing with Data Streams and Error Streams 

In linux when a command got successful we get an exit code of 0 otherwise any non-zero value.
Error streams are nothing but the errors that we see when we run a command such as permission-denied errors etc.
We can simply check it by the following command:

```bash
echo $?
```

But in case we ran a command let say find command:
```bash
find /etc -type f
```
this find command is simply gonna find all the files present inside /etc folder. You would see some error streams such as permission denied etc. While writing scripts we have to make sure that we do not get any kind of interaction all process should be automated so these error streams should not be shown. So we can redirect them as well. 

We can do it by using **2>** symbol, but if we want to redirect our data streams we can use it like either this **>** or **1>**
we can also redirect both data streams and error streams as well using **&>**.

```bash
find /etc -type f 2> ./errorstream.txt
```
```bash
find /etc -type f 1> ./datastream.txt
# this will redirect datastream to datastream.txt

or

find /etc -type f > ./datastream.txt
#both are same.
```
```bash
find /etc -type f &> ./errorAndDataStream.txt

#This will redirect both data and error stream inside errorAndDataStream.txt
```
-----------------------------------------------
# YAML File:
YAML means "Yet another markup language"
YAML "YAML ain't markup language"

There are also other Markup languages such as mark down languages such HTML. Mark up langugaes provide you a child parent relationship.

YAML is simply a data transfer format which can be easily transferable. 

## Serialization & De-serialization:
Converting the data objects into the series of chunks using the serializer to send it to the YAML fail, database etc.
And converting back file into data object code is called de-serialization

## working with YAML files
YAML is case sensitive.
```
# Key Data Type
"apple": "I am a red fruit"
1: "This is rabah's roll number"

# lists
--- 
- apple
- mango 
- Banana
- Apple 

# block data type:
---
cities:
 - Lahore
 - Rawalpindi
 - Peshawar
 - D.I Khan
 - Faisalabad

---
// Method 2: Flow data type Same as above:
cities:[Lahore, Rawalpindi, Peshawar, D.I khan, Faisalabad]


---

# string variables:

fruit: "apple"
---

bio: |
 hey may name is Rabah

---
# writing a single lines in multiple lines
message: >
 this will
 all be 
 in a single line

---
message: this will all be in a single line
---
# writing a single lines in multiple lines
  message: >
    this will
    all be 
    in a single line

  ---
  message: this will all be in a single line
  ---
  number: 123456
  marks: 25.7
  booleanValueInYAML: No
  # Boolean Datatypes in YAML for false: n, N, No, no,  False, FALSE, flase
  # Boolean Datatypes in YAML for true: y, Y, Yes, yes, True, TRUE, true

  ---
  # Specifying the type
  zero: !!int 0
  positiveNum: !!int 547
  negativeNum: !!int -67
  binaryNum: !!binary 0b110011
  OctalNum: !!int 0675
  hexaNum: !!int 0x45
  marks: !!float 56.85
  commanvalue: !!int +540_000
  ---
  # floating point number

  marks: !!float 58.4
  infinite: !!float .inf
  booleanValue: !!bool Yes
  message: !!str This is a string bro

  # Null datatypes:
  surname: !!null Null #or null, NULL, ~
  ~: This is a null key

  # dates and time:
  date: !!timestamp 2003-08-30
  ...
...
```
**NOTE**: Here we have 3 different documents in a single YAML file. Each document is separated by --- and it can be end with using ...

### YAML to JSON:
**YAML Format:**
```
cities:
 - Lahore
 - Rawalpindi
 - Peshawar
 - D.I Khan
 - Faisalabad
```

**JSON:**
```
{
  "cities": [
    "Lahore",
    "Rawalpindi",
    "Peshawar",
    "D.I Khan",
    "Faisalabad"
  ]
}
```


``` bash
---
# Advance Data Types:
# Nested list
-
 - apple
 - mango
-
 - grapes
 - banana
-

---
# In JSON:
[
  [
    "apple",
    "mango"
  ],
  [
    "grapes",
    "banana"
  ],
  null
]
...
```

```bash
---
# nested mapping: map inside a map
# Key value pairs are called maps

name: Kunal Khushwana
role:
  age: 78
  job: student

---
#method 2 same as:
name: Kunal Khushwana
role: { age: 78, job: student }

---
#list of arrays inside hashtables:

pairs example: !!pairs
 - job: student
 - job: teacher

# In JSON:
# {
#   "pairs example": [
#     [
#       "job",
#       "student"
#     ],
#     [
#       "job",
#       "teacher"
#     ]
#   ]
# }
---
# set will allow you to have unique values
names: !!set
 ? Hadi
 ? Rabah
 ? Wahaj
 ? Musa

---
#dictionary:
# when you want a whole list as a single value
People: !!omap
 - Kunal:
    name: Kunal Khushwaha
    age: 78
    position: ase
 - Rahul:
    name: Rahul Kawaria
    age: 65
    position: devOPs engr

---
# resuing some properties using anchors here we will not repeat our code
likings: &likes
  fav fruit: mango
  dislikes: grapes


person1:
  name: Rabah Ali Shah
  <<: *likes
person2:
  name: wahaj Ali Shah
  <<: *likes
  dislikes: apple
  # here dislikes will be overriden from grapes to apple for person 2
person3:
  name: musa Ali Shah
  <<: *likes
```


# XML vs JSON vs YAML
```
# XML:

<?xml version="1.8" encoding="UTF-8"?>
<school name="DPS" principal:"someone">
     <Students>
         <Student>
             <name>"Rabah"</name>
             <rollno>344806</rollno>
             <marks>85</marks>
         </Student>
     </Students>
 </school>

# JSON

 {
   "school": [
     {
       "name": "DPS",
       "principal": "someone",
       "students": [{ "name": "Rabah", "rollno": 344806, "marks": 85 }]
     }
   ]
 }


# YAML
---
school:
- name: DPS
  principal: someone
  students:
  - name: Rabah
    rollno: 344806
    marks: 85

```

# Tools for working with YAML:
- **Datree:** Used for validate your YAML
- **Monokle:** Used for validate kubernetes templates
- **Lens:** Used to write YAML file for kubernetes using GUI

# Docker
## Why Docker?
What was the problem that docker came into existance?
In early stages, only one application can be run on a server. If you have multiple applications then you would have multiple servers to run those applications. VMware was the company that solved this problem by creating virtual machines. But there was also a problem with virtual machines. Virtual machines also requires their own OS and we know that OS requires its own dedicated hardware and other resources. This was the problem.
### Architecture of Virtual machines

App 1      |   App 2    |   App 3    |
bin/lib    |  bin/lib   |  bin/lib   |
Guest OS 1 | Guest OS 2 | Guest OS 3 |
              Hypervisor
Your Local Host Machine / Database Server / Cloud


**HYPERVISOR**: Hypervisor is program that creates virtual machines on your local host and manage the resource and hardware.
Now here as you can see in case of virtual machines we have 3 VMs and 3 separated OS.

Moreover, Let say you have built an application and you want to send it to your friend. Your friend says that this application is not running on my PC as it is requiring x version and blah blah. To solve such problem we have "**containers**"

## Architecture of Containers

App 1      |   App 2    |   App 3    |
bin/lib    |  bin/lib   |  bin/lib   |
           Container Engine
              Single OS
Your Local Host Machine / Database Server / Cloud

Here you can see we have single OS and a container engine that is managing all different applications on a single machine.

Containers are isolated environments that runs application in isolated environment.
Its same as shipping the application to the friend in a conatiner that will contain all the resources that will be required to run that application. This container will make sure that the application run correctly in the friends machine.

Now Docker is a tool/Container Platform that helps us creating, managing and scaling containers.

# Docker Architecture

3. Orchestration
2. Engine
1. Runtime

**Runtime:** Containes runc, and Containerd. Runc is responsible for turning ON and OFF the container. Containerd is responsible for managing container
**Engine:** Here we communication with the server using Docker CLI using APIs
**Orchestration:** In orchestration, in simple we manage containers. We can scale our application to more containers let say it is currently running in 10k containers we want to scale it into 20k. Moreover, Let say our application wants to update to v2 then instead of stopping the application and then updating it we can smoothly do it in less time using orchestration engine. Which is also provided by Kubernetes.

# Docker File and Docker Image
Let say you are eat noodles and your friend who is in another city wants to taste them. So what would you do is that you will send him the recipe to make that dish. Here the recipe is like set of instructions to create that dish. Now Imagine that dish as an application and recipe as the set of instruction to create the application in a container.
Here the file that contains the set of instruction is called docker file. And the application that will be created by following those instruction will be called as Docker Images. Which will run on containers. 
Containers are the instance of running images of the application. 

If you have an application that you want to containerize then you have to write a docker file that will create docker images that will run on container.
- Assume Docker files are the set of instructions to create that file
- Assume Docker images as Template/Class
- Assume Docker Containers as Instance of the class/Objects

Docker Files --> Docker Images --> Container

# OCI (Open Container Initiative
We have various runtime to run container, Which one we should use to run images. To answer that we have OCI which have defined some standards on the bases of Docker file specifications and docker image specifications which we have to follow. On top of that we can do what we want.

# Docker Commands
First download and install docker from their official website 

```bash
docker run hello-word //this command can be used to check whether you docker has correctly installed or not.
```
This command means that "run that image to create the container" Here hello-word is an image name. Here this above command went to the docker hub and dowloaded that image "hello-world" from docker hub and ran it into my PC.

```bash
docker images // this command is used to check all downloaded images in your local machine
```
```bash
docker container ls // this command is used to check all downloaded containers in your local machine
```
```bash
docker pull mysql // this command is used to download images without running them in a container
```
```bash
docker pull ubuntu:16.04 // this command is used to download specifc version of the image
```
```bash
docker run -it ubuntu:16.04 // here -it flag means interactive environment. This will keep the image running in the background. You have to manaully get exit from the image.
```
```bash
docker ps // this command is used to check which docker containers are currently running
```
```bash
docker ps -a // this command will also tell you about the process that has been stopped
```
```bash
docker rm container_Id // this command will remove the history of that container from the log
```
```bash
docker rmi image_Id or image_name // this command will remove image
```
```bash
docker stop container_Id // this command is used to stop the running container
```
```bash
docker inspect image_name / image_id // this command is used get all the details about image
```
```bash
docker stop  container_id // this command is used get all the logs of your container
```
```bash
docker container prune -f // this command is used to delete all the containers that are stopped. Here -f means force. Dont ask again. Just do it
```
```bash
docker run alpine ping www.google.com // this command is using alpine OS and then running ping command to check the ping of google.com
```
```bash
docker run -d alpine ping www.google.com // this will exactly as above but it will do in the background 
```
```bash
docker logs container_id // this will show all the logs of the container
```
```bash
docker images -q // to get all the ids of images
```
```bash
docker images -q --no-trunc // to get all the SHA256 ids of images
```
```bash
docker rmi -f $(docker images -q) // this will delete all your images
```
```bash
docker run -p host_port:container_port image_name
 or
docker run -p 8080:80 my_docker_image //8080:80 specifies that port 8080 on the host machine should be mapped to port 80 on the container

```

# Connecting two containers
```bash
docker exec -it container_Id bash // here you have to provide the container Id of the container that is currently running and you want to attached the bash with it. Means that two bash will be run in the same container so that the container could interact with each other.
```

# Docker Commits: How to create a new image out of an image
Let say you have ran your container. Let say you ran ubuntu OS and created a file in that OS in a container. But if you create another container then that file wont be available there. So make it accessible for anybody you can create its new image using commit messages.

```bash
> docker start container_id / here start your container on which you had created name.txt file. Provide its containder_id
> docker commit -m "Added names.txt file" container_id my_firts_image:1.01  // now here provide the id of the container of which new Image you wanna create.
```
here :0.01 is the version of the image that I have created

## HOW Docker RUN works:
When we run > docker run image_name . Then Docker ask the docker daemon that is this image is locally installed in my PC? If yes, then run it. If NO, then download it from online registry (docker hub). This will download that image and will create a container and will run that image. 

Docker is very helpful and time saving hackathons. Where if you dont want to download any tool or software then you can use its intance using the images of docker availble on Docker hub. For example: docker run mysql etc.

## HOW Docker is running the images in a container?

As we have discussed above that Images are basically instances/templates that runs in a container. Images also contains OS files. Even the dependencies of the software which are required to run that software. Docker uses the Docker engine to communicate with our local hardware. This is how Docker container runs an image.


## How to access containers locally on your machine
```bash
docker -d -p port 8080:80 nginx
```
here -d is for detach..means run in background. -p means foward port. 8080 is the Port that I am providing. 80 is the defualt port of nginx. You can git default ports by googling it.
Here, after runnin this command if you would go to your browser and will search localhost:8080 then you have running nginx on your local host from the port you had provided.

# Layers
All images are basically built in layers. Docker is smart enough that it downloads the images in the form of layers and each layer contains its own unique id. What is the reason of doing this all? The reason is that if let say there are two images show use same files/layers. Then does it make sense to download those files again and again when downloading the new image? The answer is NO. So Docker so the same. Therefore, it downloads each image in the form of layer so that in case of any layer that is used by the other image it do not download it. This is what that makes docker fast.
You can check how many layers an image is containing by using the following command:
```
docker inspect image_id / image_name
```

# How to create your own Dockerfiles and images and upload it on registry?
Go to your CMD
```bash
docker login //then provide credentials
```
```bash
vim Dockerfile //creating docker file
```
**NOTE:** Its a convention to use Dockerfile name with no extension

```bash
//inside Dockerfile

FROM alpine
RUM sudo apt-get update
CMD ["echo","My name is Rabah Ali Shah"]
```

```bash
docker build -t myfirstimage
```

Congrats! you have made it

# More on Dockers Engine Architecture
        Docker Client
            Daemon 
            Conainterd
/             |          \
shim         shim      shim
runc         runc      runc
container container container


when you write commands from docker command CLI its ask Daemon which calls containerd which is a high level runtime it manages the runc and runc manages the container. Here Shim allows us to run the containers even the daemons are down. This is called daemonless containers.

# Writing Docker File

**Name Convention:** Dokerfile

**NOTE:** Imagine while writing Dockerfile is that you are writing steps to install the application on any machine. Always refer dockers official documentation for help

Below are some sample Docker files:

**Syntax:** INSTRUCTION arguments

```bash
# using alpine as base image
FROM alpine:3.18

# installing curl
RUN apk add curl

# setting word directory as downloads
WORKDIR /downloads

# adding user as rabahalishah
RUN adduser -D rabahalishah

# setting the current user as rabahalishah
USER rabahalishah
```
Building the docker File: docker build -t myimage
Verifying the dockerfile: docker run myimage whoami


```bash
# using alpine as base image
FROM mcr.microsoft.com/powershell

# creating directory namely demo
RUN mkdir -p /demo

# setting shell to the powershell as our base image is windows and in windows we use either cmr or powershell
SHELL ["pwsh", "-command"]

# adding user as rabahalishah
RUN "hello world!" | Out-File -Path /demo/message.txt
```
Building the docker File: docker build -t myimage
Verifying the dockerfile: docker run myimage

```bash
# using python as base image
FROM python

# setting the working directory as code
WORKDIR /code

# defining anv variable
ENV app_host = 0.0.0.0

# defining another environment variable
ENV app_port = 5000 
```

Building the docker File: docker build -t myimage
Verifying the dockerfile: docker run myimage env

localhost:8080

```bash
# using python as base image
FROM python

# setting the working directory as code
WORKDIR /code

# copying app.py to code folder
COPY app.py /code/

# copying the myfile.txt from the link
ADD https://www.abc.com/myfile.txt .

# Exposing this container to run at 5000 port
EXPOSE 5000
```
Building the docker File: docker build -t myimage
Verifying the dockerfile: docker run myimage ls /code

Verifying the dockerfile: docker run -it -d -p 8080:5000 myimage ls /code

## commands like npm run dev
CMD ["executable", "parameter 1", "parameter 2"
CMD ["npm", "run", "dev"]


# ByteWise Fellowship DevOps Track:
# Chapter 01
# Linux Concepts and Keywords for DevOps

## General Concepts

 1 `Kernel`: The core part of Linux, responsible for managing the system’s resources and hardware.

 2 `Shell`: A command-line interpreter that allows users to interact with the operating system.

 3 `User Space`: Memory areas where all user mode applications run.

 4 `Filesystem Hierarchy`: The layout of directories and files on a Linux system, structured hierarchically.

 5 `Processes`: Instances of executing programs managed by the Linux kernel.

 6 `Daemons`: Background services that start up during the boot process or after logging into the desktop.

 7 `Package Manager`: Tools that automate the process of installing, upgrading, configuring, and removing software.

 8 `System Calls`: Interfaces that provide services of the kernel to the user applications.

 9 `Virtualization`: The creation of a virtual (rather than actual) version of something, such as an OS, a server, or network resources.

 10 `Containers`: Lightweight, executable software packages that include everything needed to run an application: code, runtime, libraries, and settings.

## Architecture Components

 11 `Bootloader`: Software that manages the boot process of a computer, such as GRUB.

 12 `Init System`: The first process started by the Linux kernel, responsible for controlling system startup and services (e.g., systemd, SysVinit).

 13 `System Libraries`: Code libraries used by the kernel to perform different operations.

 14 `GUI (Graphical User Interface)`: Graphical interfaces like GNOME or KDE that make interaction user-friendly.

 15 `CLI (Command Line Interface)`: Interface for typing commands on a terminal to interact with the system.

 16 `POSIX (Portable Operating System Interface)`: A family of standards specified by the IEEE for maintaining compatibility between operating systems.

 17 `IPC (Inter-Process Communication)`:A mechanism that allows processes to communicate and synchronize their actions.

 18 `Sysfs (Filesystem for Sysfs)`: A virtual filesystem used by Linux that provides a tree of system devices.

 19 `Procfs (Filesystem for Procfs)`: A virtual filesystem that provides detailed information about Linux processes.

 20 `Sockets`: Endpoints for sending and receiving data between processes over a network or within the same system.

## Components

 21 `BASH (Bourne Again SHell)`: A widely used default command shell in Linux.

 22 `Apache`: A popular web server software for Linux.

 23 `Nginx`: High-performance HTTP and reverse proxy server.

 24 `Systemd`: A system and service manager for Linux, providing parallelization capabilities.

 25 `LVM (Logical Volume Manager)`: A device mapper that provides logical volume management for the Linux kernel.

 26 `KVM (Kernel-based Virtual Machine)`: A virtualization module in the Linux kernel that allows the kernel to function as a hypervisor.

 27 `X Window System`: A windowing system for bitmap displays.

 28 `SELinux (Security Enhanced Linux)`: A security architecture integrated into the kernel that supports access control security policies.

 29 `iptables`: A user-space utility program that allows a system administrator to configure the IP packet filter rules of the Linux kernel firewall.

 30 `Cron`: A time-based job scheduler in Unix-like operating systems.

## Network Components

 31 `TCP/IP`: A set of networking protocols that allow communication over interconnected networks.

 32 `DHCP (Dynamic Host Configuration Protocol)`: A network management protocol used to dynamically assign IP addresses to devices on a network.

 33 `DNS (Domain Name System)`: A hierarchical decentralized naming system for computers, services, or other resources connected to the Internet or a private network.

 34 `SSH (Secure Shell)`: A cryptographic network protocol for operating network services securely over an unsecured network.

 35 `FTP (File Transfer Protocol)`: A standard network protocol used for the transfer of computer files between a client and server on a computer network.

 36 `HTTP/HTTPS`: Protocols used for transmitting web pages over the Internet.

 37 `Samba`: A free software re-implementation of the SMB networking protocol, which allows end users to access and use files, printers, and other commonly shared resources.

 38 `NFS (Network File System)`: A distributed file system protocol allowing a user on a client computer to access files over a network similar to how local storage is accessed.

 39 `VLAN (Virtual Local Area Network)`: A network protocol to create multiple distinct broadcast domains, which are mutually isolated.

 40 `SNMP (Simple Network Management Protocol)`: An Internet Standard protocol for collecting and organizing information about managed devices on IP networks.

 41 `IPsec (Internet Protocol Security)`: A protocol suite for securing Internet Protocol (IP) communications by authenticating and encrypting each IP packet of a communication session.

 42 `Firewall`: A network security system that monitors and controls incoming and outgoing network traffic based on predetermined security rules.

 43 `Load Balancer`: A device that acts as a reverse proxy and distributes network or application traffic across a number of servers.

 44 `VPN (Virtual Private Network)`: Extends a private network across a public network, enabling users to send and receive data across shared or public networks as if their computing devices were directly connected to the private network.

## System Administration

 45 `RAID (Redundant Array of Independent Disks)`: A data storage virtualization technology that combines multiple physical disk drive components into one or more logical units.

 46 `Monitoring Tools`: Tools that check the health and status of systems and networks (e.g., Nagios, Zabbix, Prometheus).

 47 `Backup and Recovery`: Strategies and solutions for data protection in case of data loss or system failure.

 48 `Log Management`: Processes and solutions for systematic collection, storage, analysis, and disposal of system logs.

 49 `Job Scheduling`: Use of cron or other tools to schedule scripts or commands to run at specific times.

 50 `User Management`: Handling user accounts including creating, modifying, and granting permissions.

 51 `Disk Management`: Managing disk space usage on systems through tools like `fdisk`, `parted`, and filesystem-specific commands.

 52 `Patch Management`: The process of updating security patches for software applications and technologies.

 53 `Automation Tools`: Tools designed to minimize manual interventions (e.g., Ansible, Puppet, Chef).

 54 `Security Auditing`: Checking system security settings and policies to ensure they meet the required security guidelines.

## Advanced Concepts

 55 `Cgroups (Control Groups)`: A Linux kernel feature to limit, account for, and isolate the resource usage (CPU, memory, disk I/O, etc.) of process groups.

 56 `Containerization`: Isolating applications within separate environments to enhance security and operational efficiency.

 57 `SELinux Contexts`: Security settings that define the permissions processes and files have within a system running Security-Enhanced Linux.

 58 `Inodes`: Data structures on a filesystem that store information about files and directories, except their names.

 59 `Soft and Hard Links`: Soft links (or symbolic links) refer to a symbolic path indicating the abstract location of another file, while hard links are direct references to the content of the files.

 60 `D-Bus`: A message bus system that provides a simple way for inter-process communication and allows multiple programs to interact.

 61 `Swap Space`: A form of virtual memory that a computer can use to support physical memory (RAM) on the system.

 62 `File Permissions`: Settings that control who can read, write, or execute files or directories.

 63 `Access Control Lists (ACLs)`: A more flexible permission mechanism for file systems that allows you to specify detailed user permissions for a file or directory.

 64 `Ext2/Ext3/Ext4`: Filesystems commonly used in Linux, where Ext4 is the most recent evolution providing various improvements over its predecessors.

 65 `XFS`: A high-performance 64-bit journaling file system created by Silicon Graphics, Inc.

 66 `Btrfs`: A modern file system developed to address the expanding scalability and reliability requirements of contemporary operating environments.

 67 `Journalling`: A process that helps protect the integrity of the filesystem by keeping a log of ongoing changes.

 68 `LUKS (Linux Unified Key Setup)`: A specification for disk encryption to secure data on devices using cryptographic techniques.

 69 `Logical Volume Manager (LVM)`: A device mapper framework that provides logical volume management for the Linux kernel.

 70 `RAID (Redundant Array of Independent Disks)`: A data storage virtualization technology that combines multiple physical disk drive components into one or more logical units for redundancy or performance improvement.

 71 `Root Account`: The default superuser account in Linux systems that has access to all commands and files.

 72 `Umask`: A command that determines the default file permission sets for newly created files and directories.

 73 `SSH Keys`: Cryptographic keys used for secure remote login using the SSH protocol.

 74 `TCP Wrappers`: Host-based Networking ACL system, used to filter network access to Internet protocol servers on (Unix-like) operating systems.

 75 `Environment Variables`: Variables that are defined in the shell and are available system-wide to influence the behavior of processes.

 76 `Cron Jobs`: Scheduled commands that use the cron daemon to execute scripts at specified times and intervals.

 77 `Syslog`: A standard for message logging, where messages are stored for dealing with system management and security auditing.

 78 `Network Interfaces`: Components that facilitate the connection between a computer and a network.

 79 `Kernel Modules`: Pieces of code that can be loaded and unloaded into the kernel upon demand, extending the functionality of the core system without rebooting.

 80 `Proc File System (/proc)`: A virtual filesystem in Linux that provides a mechanism for kernel-space to send information to user-space.

 81 `Uptime`: Command to find out how long the system has been running.

 82 `/etc/fstab`: A configuration file that contains information about the various partitions and storage devices in use.

 83 `Systemd Units`: Configuration files for systemd that manage the behavior of services, mount points, and other system components.

 84 `Grub Bootloader`: A program that loads the Linux kernel into the computer's main memory to begin its operations.

 85 `Kernelspace vs Userspace`: Distinct areas where the core system (kernel) and the user applications run, ensuring security and stability.

 86 `iptables/netfilter`: Tools that define rules for packet filtering and NAT to secure networks on Linux systems.

 87 `uname Command`: Command used to print system information including the Linux kernel version and hardware platform.

 88 `Shared Libraries`: Libraries that can be simultaneously used by multiple programs in Linux to save memory and enhance functionality.

 89 `Runlevels`: Predefined modes of operation in Unix-like systems that determine which programs can execute at startup.

 90 `Shell Scripting`: Writing scripts using shell commands to automate tasks.

 91 `GNU Tools`: Collection of tools developed by the GNU project including compilers, editors, and various utilities.

 92 `Namespaces`: Features of the Linux kernel that partition kernel resources such that one set of processes sees one set of resources while another set of processes sees a different set of resources.

# Chapter 02: Computer Networking
# Advance Computer Networking
## Network Devices 1:
### Layer 1 Devies:
**Analog Modem:** Modem word came from modulating and demodulating. It is take digital signal  coming from digital node and then modulates it into analogue signal and in return it receives anlogue signal and its de-modulates it into digital signal. Modems were used for creating connections between network segments via public network switches

**Hub:** Hub are the devices that repeat the signals. They dont have brain like they do no care that from where the signal is coming and where its going it will simply replicates the signal out of the ports. You can assume hubs as the enhancers to make the signals travel long distances.

### Layer 2 Devices:
**Switch:** Its kind of a hub with brain. It uses ASIC chips that have specific programming. It helps the Switch to understand when a device on a network will be connected and which port of its to connect.  A switch only communicates with Local network devices. They can be very simple and complex.

**WAP:** Its a bridge that connects wireless network segment with a wired network segment. It also only communicate with local network devices.


### Layer 3 Devices:
**MUltlayer switch:** A multilayer switch (also known as a layer 3 switch) is a networking device that combines the functions of a traditional layer 2 switch with those of a Layer 3 router.
**Router:** Its a device that connect various devices using OSI model. It uses software programming for decision making as compared to switches which uses ASIC chips. Router keeps tracking different network and finds the best possible route to reach those networks. It can communicate with both Local and non-local network devices.


# Network Devices 2:
### Secturity Devices:
**1) Firewall:** It is police of network traffic. It can be software or devcied based. Firewall monitors the data coming and leaving the network and will either allow or deny the internet traffic according to the set of pre-defined rules. In case of stateless inspection: Firewalls will monitor singal data packet coming or leaving the network against the set of rules. whereas in case of stateful inspection: It do not inspect the data packets. It only examine the state of the network connection between internal and external network. Its job is to protec the internal network from the external network according to the set of predefined rules.

**2) IDS:** Intrusion detection system, Its a passive system designed, Identify network breaches and attackes. It will inform the network administrator about the data breaches threats attackes but it wont take any action. Threat detection can be signatured based (evaluates network traffic for known malware), Anomaly based (evaluates on suspecious network changes) and policy based.

**3) IPS:** Intrusion protection system, Its an active system designed to stop or prevent the data breaches attacks. It is placed between the router and the desitnation network segment. All the data flows through it. It can also terminate the network sessions, redirect the attacks and block the offensive IP addresses.


**VPN Concentrator:** VPN Concentrator provides proper tunneling and encryption between the various allowed VPN connections. Many VPN concentrators work on multiple OSI layers. specially 2 3 and 7


### Optimization Devies:
**Load balancer:** These are the devices/softwares that are used to manage the network traffic between different hosts/servers containing the same data. Load Balancer makes sure that none of the server become overloaded. It distributed the request between diff servers containing the same data.

**Proxy servers:** These are the servers that acts on the behalf of their clients. They make requests on the behalf of their client to retreive data from outside untrusted network. It hides and protect the requesting client. It also caches the most visited webpages for network performance optimization.

## Network services and Applications 1
## Basics of VPN:
VPN is a virtual private network that is used by remote hosts to access a private network through an encrypted tunnel through a public network.
(Here when we acces the blocked sites those sites are the private network and we are remote hosts and the internet coming to our home via whcih we are connected is a public network.)

When a VPN connction has been established we are no longer seen as remote host we will be seen as the local host. It established the direct connection between the remote host and a private network.

### VPN Types:
**Site-to-site:** Connects remote sites to the main sites and can be seen as a local network. VPN concentrator on both ends will manage the VPN
**host-to-site:** Connections between remote users and local networks. Here VPN connection will be managed by VPN concentrator on the local network.
**host-to-host (SSL):** Allows connection between two systems without VPN client software. It is the most secure encrypted connection.

### Protocols used by VPN:
## IPsec (Internet protocol security):
This protocol is a set of several protocols such as: 
**AHP** (Authentication Header protocol) This only offers authentication but no encryption. 

**ESP (Encapsulating security protocol):** Both authencication and encryption.

Both AHP and ESP and operate on both modes (transport (host-to-host), tunnel (site-to-site))
IPsec implements ISAKMP (Internet security association and key management protocol). This provides the method to for transferring security key and authentication data between systems.

### GRE (Generic Routing Encapsulation protocol):
Its a tunnel protocol. It is used as to create sub-tunnel with IPsec protocol as IPsec only transmits unicast packets (one to one communication) but in many cases tehre is a need to transmit multicast (one to some) or broadcast (one to many) Thats why GRE protocol is implemented.

### PPTP (point to point tunneling protocol):
Its an older VPN technology it lacked security features.

**Transport Security Layer (TSL):**
TSL is cryptographic protocol to create secure encrypted connection between two devices. It uses asymmetrical cryptographic authentication and a security key which is used to encrypt the session. It has largely replaces SSL (Secure Socket Layer).


**SSL (Secure Socket Layer):**
SSL is an older cryptographic protocol that is very similar to TSL. 

SSL is an older technology that contains some security flaws. Transport Layer Security (TLS) is the upgraded version of SSL that fixes existing SSL vulnerabilities.


## Network services and applications 2:
### Network access services:
**NIC (Network interface controller):**
Its a hardware device. Most of the PCs come with at least one NIC port. It works with the 2 layers of OSI. Data link layer where it defines which protocol is gonna be used and it also provides the local network node address through its burned in physical MAC address. 
And at physical layer it determines how the network traffic will be converted a bit at a time into an electrical signal.

**RADIUS (Remote authentication dial in user service):**
It uses **AAA (Authentication, authorization and accounting)** protocol to grant access to the authorized network resources.

**TACACS+ (Terminal access control access control system plus):** A remote access service that is used to authenticate remote devices and grant them access to authorized network resources. All transmission between the devices are encrypted.


**Services:**
### RAS (Remote access services):
its not a protocol. Its a combination of software and hardware used for remote access connections. User requests acess from the RAS server which either reject or grant the access.


### Web services:
Used for communicaion between different packages by converting it into XML.

**DHCP (Dynamic Host control protocol):**
IP address are assigned to the devices that are connected to a network using DHCP protocol. 

### How a PC came to know about its IP configuration and DNS address?
**Static IP vs Dynamic IP:**
To have two devices to communicate via a network a set of information such as IP address, gateways, subnet mask address, DNS address and other configuration informations are required. If these informations are provided manually then these would be called as static IP and that won't be change. In case of any changes, configurations are need to be change accordingly.

Whereas in DHCP server an administrator configure a DHCP server which dynamically assignes the IP address and all other configuration informations that are required to communicate with the other devices. In case of any change DHCP will handle it dynamically.



**HOW DHCP works?**
When a DHCP server has configured by an administrator. And on boot up then a system makes request on(255.255.255.255:67  67 is UDP port) by sending a "Discovery packet" (Which means is there any DHCP server who can help me?) Then if DHCP server is available then it will receive that discovery packet and will send back "Offer packet" on (port 68) (which means Yes, I am a DHCP server I am available to help you)" Then on receiving the offer packet from the DHCP server the system sends Request packet. And then DHCP returns all configuration information required to connect to the network.


**Components of DHCP server:**
**port used:** listen to port 67 for discovery packet and uses port 68 for sending offer packet to PCs MAC address.

**Address scope:** There is range of IP address till which DHCP can work with.

**Address reservations:** Admin can reserve specific IP addresses for specific MAC address. This is helpful for the devices that should have same IP address.

**leases:** Configuration information are good only for short period of time. After that system can make request as well.

**NOTE:** PCs can also have some preffered IP addresses.


### What if DHCP server is not residing on a local network segment?

Broadcast transmissions cannot pass throught routers. If there is no DHCP server at the local network segment then router can be configured to a DHCP relay. In such case the PC will request to DHCP relay which will further make request to DHCP server and then DHCP server will send back information to DHCP Relay and then back to the PC in the same way as DHCP server works.


### DNS Servers
DNS is process of mapping human friendly names of domains to the actual ip address to reach the desired server to get the response. DNS servers are the are servers that contains all the DNS record. DNS servers do not require FQDN (fully qualified domain names like www.google.com only searching "google" can lead to the same response. Thats cool). 

If one DNS server do not contains the response it will forward the request to the other DNS server until the positive response we get.

**www. is specific servic
google is the domain name
.com is the top level domain.**


## Different levels of DNS servers. How a request is made to DNS server
There are three levels of making request to DNS server:
1) **Root level:** At first the request is sent to the root servers that contians the record of all TLD servers. For www.google.com it will forward reques to the .com TLD server.
2) **Top Level Domain (TLD servers):** The TLD server is specific for specific top level domains. This contains all the records of domains associated with it. Then it will map through it. TLD servers also forward down the request to the other TLD server to manage the load and finally connects the local ip domain with the request IP address by forwarding it to the local DNS server
3) **Local DNS:** This contains the hosts file and map through the FQDN to the ip address and returns the response.


**Authoritative DNS server:** These servers are specifically configured for the requests contains the specific information.
**Non-Authoritative DNS server:** These servers responds to the requests that are coming from another DNS server. In most cases when we make request to DNS serves those are non-Authoritative DNS server.


### DNS records:
**A records:**
Maps hostnames to their IPv4 addresses

**AAAA Records:**
Maps hostnames to their IPv6 address

**CNAME records:**
Map canonical names to hostnames (A canonical URL is the URL of the best representative page from a group of duplicate pages, according to Google. For example, if you have two URLs for the same page (such as example.com? dress=1234 and example.com/dresses/1234 ), Google chooses one as canonical.)

**PTR records:**
Pointer records that points to Canonical names.

**MX records:**
Maps to the email server for specific domains. Determines how email will travel from sender to receiver.


**Dynamic Domain name service:**
Here if the ip address of the public network get changes the user will still able to access the requested servers. As DDNS will dynamically map through the domains names and IP addresses. 
useful when FQDN remain same but IP addresses get chaneged



**DDNS Updating:**
A software is used to monitor the ip address of the system. In case of any change it will send the update to the proper DNS server without the intervention of the admin. And will update it dynamically.


### Network Access Translation:
NAT solves the problem for accessing the non-routable IP addresses.

NAT simply translate the local IP address to the routable IP address.

**For example:** 192.168.0.1 says Hey I want to google something. The router 192.168.0.2 will say you are not routable you cannot leave the local network, Let me first assigned you a routable IP address.
NOTE: Translations happens both times. Request leaving the local network and response entering back to the local network.

### How NAT works:
**SNAT:** Static Network access translation contains manually assigning of routable IP address to the local system which is very complex, expensive and creates scalable issues. 
**DNAT:** Dynamic NAT solves this problem of manually assigning routable IPs but DNAT uses a Pool of routable IP address out of which it assigns IP addresses. If all IPs from the pool has assigned no more requests can be handle. There will be a scalability issue in case of more devices.
**PAT (recommended):** Port Network access protocol solves this problem by adding port number at the end of each routable IP address. This also uses a Pool of routable IP addresses but it also use PORT numbers which makes it to handle more request by ensuring that each request is going to a specific right server.


### NAT Terminologies:

**Inside local:** IP address of the local system. (Like my PC who is making request to google.com)
**Inside global:** Routable IP address that will be assigned to the local system (which is requesting)

**Outside local:** IP address of the NAT enabled router which is forwarding my request to google.com
**Outside Globale:** IP address of google.com server


### WAN Technologies 1 (Wide area network):
If you own and can control the line which is using for data transmission then you are not using WAN. You are more likely using a LAN connection. One of the most important and commonly used network infrastructures used in WAN technology is PSTN (Public switched telephone network) due to it swide spread availability.

### Technologies using PSTN
**Dial-up:** Uses PSTN for transmitting data traffic in analogue signals. This requires an analogue modem to format the network traffic.
**ISDN (Integrated services digital network):** Digital Point to point WAN technology.
**xDSL (Digital Subscriber line):** Requires digital modem to operate
**SDSL (synchornous):** Uploading and downloading speed are same. Do not carry voice communcation.
**ADSL (Asynchornous):** Uploading and downloading speed are NOT same.

** Broadband cables:**
cable companies can provide broadband cable connection to their customers. These are capable of carrying data, voice and television all through the same cable. The signal is formatted at the headend and deliver to the distribution network.

**Coaxial cable network:**
Can transmit data, voice and television all through the same network. it has broad band width.
Unicast: one to one
Multicast: One to many or many to manay
broadcast: One to thousands

The main difference between broadcast and multicast is that during the broadcast, the packet is sent to all of the hosts that are connected to the network, but during the multicast, the packet is sent only to the hosts that are supposed to receive it as the intended receivers.


### Fiber optics network:
Use light to transmit signals and data. very fast. More bandwidth and greater distance.

US uses SONET standard (Synchronous optical networking)

**DWDM (Dense wavelength division multiplexing method)** is used to increase the bandwidth by multiplexing several OC (optical carriers) levels upto 32 channels to single optical fiber.
**CWDM (coars wavelength division mutliplexing methd):** same as DWDM but only allows 8 channels.

### WAN Technologies 2 (Wide area network):
**CDMA (code division multiple access)** use to connect devices to the network.
**GSM (Global system for mobiles)** used for connecting mobile devices (majority of the world uses this).

### Celullar networking
In celullar netwroking mobile phones are used more than just phone calls. 1G, 2G, 3G, 4G LTE
The first-generation mobile networks (1G) used analogue technologies: AMPS, NMT, TACS, J-TACS and C-Netz. The following generations were digital and used GSM, D-AMPS and IS-95 for second-generation (2G), CDMA2000 and UMTS for third (3G), LTE for fourth (4G) and NR for the fifth generation (5G).

# What do the terms 1G, 2G, 3G, 4G and 5G really mean?
The first generation of mobile networks used analogue technologies to deliver mobile communications services. Later, with technological developments and constant demand for new services, we moved into the secure world of digital communications.

Analogue mobile systems were based on FDMA technology. FDMA stands for Frequency Division Multiple Access and uses separate frequency bands to transmit and receive communication wirelessly. The frequency bands are then divided into multiple sub-frequencies, also known as channels, to enable communication between the mobile network and the mobile phone.

Analogue networks do not have encryption capabilities, making them susceptible to security issues. The continuous nature of the radio signal also makes the analogue systems more prone to noise.

The mobile networks started their digital era in the early 1990s to overcome the challenges that analogue networks could not address. This digital journey started with the second generation of mobile networks, also known as 2G. The technology standards that enabled the second generation of mobile networks (2G) followed two major tracks.

The first track used a combination of FDMA (Frequency Division Multiple Access) and TDMA (Time Division Multiple Access). The other track employed the CDMA technology (Code Division Multiple Access) for the first time in mobile communications. More about 2G and later generations can be found in the following sections, but have a look at the table below for a summary of the technologies used for various generations of mobile networks.


## 1G – First Generation
1G stands for the first generation of mobile networks that were designed to provide basic voice calling services. 1G networks started in the early 1980s and were introduced in different parts of the world through various FDMA-based analogue technologies, including AMPS, NMT, TACS, J-TACS and C-Netz.

First-generation (1G) cellular technologies included AMPS (Advanced Mobile Phone System), NMT (Nordisk MobilTelefoni or Nordic Mobile Telephone), TACS (Total Access Communications System) and C-Netz (Funktelefonnetz-C or Radio Telephone Network C). AMPS was primarily used in the US and some Asian countries, whereas NMT was deployed in the Nordic/Scandinavian region, TACS mainly in the UK, and C-Netz in Germany.

## 2G – Second Generation
2G stands for the second generation of mobile networks that initially offered voice calls, text messages and limited mobile internet. 2G networks started in the early 1990s and were introduced in different parts of the world through various digital technologies, including GSM, D-AMPS and IS-95.

The second-generation (2G) mobile networks are digital, and they replaced the first-generation (1G) networks. 2G networks enabled highly secure voice calls, text messages (SMS), and limited mobile data services. 2G networks started in the 1990s and were deployed in different parts of the world through various digital technologies.

The most widely used technology standard for the second generation of mobile networks is Global System for Mobile Communications (GSM). Digital Advanced Mobile Phone System (D-AMPS) and Interim Standard 95 (IS-95) are the other technologies that were used for launching second-generation mobile networks (2G).

## 3G – Third Generation
3G stands for the third generation of mobile networks that offer voice, text and data services. The technologies that enable 3G are UMTS and CDMA2000 which are based on the CDMA technology. UMTS is the 3G technology for GSM, and CDMA2000 is the 3G technology for IS-95.

There have been two 3G migration tracks which were both based on the CDMA technology (Code Division Multiple Access). The first track was UMTS for migrating GSM networks to 3G, and the other track was CDMA2000 for IS-95 and D-AMPS.

UMTS, which represents the first track, stands for Universal Mobile Telecommunication System. It employs Wideband Code Division Multiple Access (WCDMA) for its air interface to offer peak download data rates of up to 2 Mbps. The average data rate with UMTS is around 384 kbps.

## 4G – Fourth Generation
4G stands for the fourth generation of mobile networks that are data-only networks enabled by the LTE technology. 4G networks use packet-switching to offer IP-based voice calls and text messages in addition to high-speed mobile data. LTE is the 4G technology for both UMTS and CDMA2000.

4G is enabled by the LTE technology, which stands for Long Term Evolution (of mobile networks). LTE is the 4G migration path for key 3G technologies, including UMTS and CDMA2000. Even though another technology WiMAX (Worldwide Interoperability for Microwave Access), can also fulfil the 4G requirements, LTE has been the primary technology for worldwide 4G deployments.

LTE networks are fully packet-switched and do not have a circuit-switched part. A packet-based technology Voice over LTE (VoLTE), is responsible for enabling voice calls and text messaging in 4G LTE networks. However, LTE networks have a 2G/3G circuit-switched fallback, which allows them to facilitate voice calls and SMS over 2G or 3G networks if the VoLTE capability is not supported by the phone or your mobile operator.

## 5G – Fifth Generation
5G stands for the fifth generation of mobile networks that are data-only and offer average download speeds of around 150 to 200 Mbps. It is the latest generation of mobile networks enabled by the New Radio technology (NR). 5G networks can offer latencies as low as one millisecond.

The 5G New Radio (NR) technology is based on Orthogonal Frequency Division Multiple Access (OFDMA), just like LTE. However, it is different from the earlier generations of mobile networks as it can cater to a wide variety of use cases by leveraging its in-built flexibility. It can also operate in various frequency bands, including high and low frequencies.

The higher frequency bands for 5G have limited coverage but very low latency (less than one millisecond), suitable for real-time services. The use cases for 5G are categorised into three main classes: enhanced mobile broadband (eMBB), massive Machine Type Communication (mMTC) and ultra-reliable low latency communications (uRLLC). We have a dedicated post on eMBB, mMTC and uRLLC, which can help you understand these three critical pillars of 5G.

WiMAX (Worldiwide interoperability microwave access):
It uses microwave tramissions over the air method to transmit voice and data. WiMAX can be used for covering significant geografical longgg distances. It is count as a type of 4G technology but also LTE conpatible. They are not compatible with 3G. You have seeing a towers in your areas they might be WiMAX.


### Satellite WAN connection
uses mircro waves to transmit data and voice using over the air method. It can be used to tranmist data which places are hard to reach. There is a high chance of latency in sending and receiving signals. Low polar and polar orbits are used to boost the microwave signals before sending back signals to earth.


## WAN Technologies 3 (Wide area network):
Metro Ethernet WAN connection:
It is when the service provider connects the customer site through an RJ45 connector.


## Leased line connection:
A leased line is a dedicated circuit connection between two end points used for communication. It is usually a 	digital point to point connection. Its expensive as the circuit cannot be used by any other entity it will be solely used by the customer. Speed can be increased by using multiplexing. PPP (point to point protocol) is used by Leased line.

**Common standards:**
T lines
T1 composed of 24 DSO channles, 1.544 Mbps
T3 composed of 28 T1 lines, 44.736 Mbps

E carrier lines
E1 composed of 30 DSO channels., 2.048 Mbps
E3 composed of 16 E1 lines, 34.368 Mbps

Optical carriers lines
OC 1, 51 Mbps
OC 3, 155 Mbps
OC 12, 622 Mbps
OC 48, 2.44 Gbps
OC 192 9.95 Gbps


## WAN Technologies 4 (Wide area network):
Circuit switched networks:
They haved dedicated ciruits to communicate between devices. Phone call via landline is an example of this. 

Packet switched networks:
In this type of network the data is divided in the forms of data chunks packtes and then re-assembled on the receiving side. 

**Frame relay:**
In this network variable length of data packets are send across the network

**ATM (Asynchronousd transfer mode):**
In this network, a fixed length of data packet sends through the network.


### What is multiprotocol label switching (MPLS)?
Multiprotocol label switching (MPLS) is a technique for speeding up network connections that was first developed in the 1990s. The public Internet functions by forwarding packets from one router to the next until the packets reach their destination. MLPS, on the other hand, sends packets along predetermined network paths. Ideally, the result is that routers spend less time deciding where to forward each packet, and packets take the same path every time.

Consider the process of planning a long drive. Instead of identifying which towns and cities one must drive through in order to reach the destination, it is usually more efficient to identify the roads that go in the correct direction. Similarly, MPLS identifies paths — network "roads" — rather than a series of intermediary destinations.

### How does routing normally work?
Anything sent from one computer to another over the Internet is divided up into smaller pieces called packets, instead of getting sent all at once. For example, this webpage was sent to your computer or device in a series of packets that your device reassembled and then displayed. Each packet has an attached header that contains information about where the packet is from and where it is going, including its destination IP address (like the address on a piece of mail).

For a packet to reach its intended destination, routers have to forward it from one network to the next until it finally arrives at the network that contains its destination IP address. That network will then forward the packet to that address and the associated device.

Before routers can forward a packet to its final IP address, they must first determine where the packet needs to go. Routers do this by referencing and maintaining a routing table, which tells them how to forward each packet. Each router examines the packet's headers, consults its internal routing table, and forwards the packet to the next network. A router in the next network goes through the same process, and the process repeats until the packet arrives at its destination.

This approach to routing works well for most purposes; most of the Internet runs using IP addresses and routing tables. However, some users or organizations want their data to travel faster over paths they can directly control.

### How does routing work in MPLS?
In typical Internet routing, each individual router makes decisions independently based on its own internal routing table. Even if two packets come from the same place and are going to the same destination, they may take different network paths if a router updates its routing table after the first packet passes through. However, with MPLS, packets take the same path every time.

In a network that uses MPLS, each packet is assigned to a class called a forwarding equivalence class (FEC). The network paths that packets can take are called label-switched paths (LSP). A packet's class (FEC) determines which path (LSP) the packet will be assigned to. Packets with the same FEC follow the same LSP.

Each packet has one or more labels attached, and all labels are contained in an MPLS header, which is added on top of all the other headers attached to a packet. FECs are listed within each packet's labels. Routers do not examine the packet's other headers; they can essentially ignore the IP header. Instead, they examine the packet's label and direct the packet to the right LSP.

Because MPLS-supporting routers only need to see the MPLS labels attached to a given packet, MPLS can work with almost any protocol (hence the name "multiprotocol"). It does not matter how the rest of the packet is formatted, as long as the router can read the MPLS labels at the front of the packet.

### Is an MPLS network a 'private' network?
MPLS can be "private" in the sense that only one organization uses certain MPLS paths. However, MPLS does not encrypt traffic. If packets are intercepted along the paths, they can be read. A virtual private network (VPN) does provide encryption and is one method for keeping network connections truly private.

### What are the drawbacks of MPLS?
**Cost:** MPLS is more expensive than regular Internet service.

**Long setup time:** Setting up complicated dedicated paths across one or more large networks takes time. LSPs have to be manually configured by the MPLS vendor or by the organization using MPLS. This makes it difficult for organizations to scale up their networks quickly.

**Lack of encryption:** MPLS is not encrypted; any attacker that intercepts packets on MPLS paths can read them in plaintext. Encryption has to be set up separately.

**Cloud challenges:** Organizations that rely on cloud services may not be able to set up direct network connections to their cloud servers, as they do not have access to the specific servers where their data and applications live.


## Cables in networking
I'll only name those cables that we see in our day to day life.
**RJ-11:** This is used for transmitting voice only and it is used to connect with the telephones.
**RJ-45:** This is our ethernet wire. it has 8 positions and 8 contact (8P8C) modular connector. Can carry data or voice.


**DB-9 (RS-232):** A nine pin D-subminiature developed for async serial communication between nodes. Most commonly used between computers and external analog modem. (This is like a blue cable in computers)
**DB-25 (RS-232 serial):** A 25 bin D-subminiature. works same as DB-9


**Media converters:**
In a large network its a common problem that different kind of cables might be used for transmitting the same data. In such case we use media converter. Like joining the fiber optics cable along with a copper wire can be possible using a media converter. some famous media converters are SMF (single mode fiber) to ethernet, Fiber optics to Coaxial cables. etc.


### Topologies 
Topologies simply tells us how to connect different devices together. To connect devices we need cables and ports. There are several arrangements to connect the devices such as Mesh, Star, Bus, Ring, Hybrid. The important point to here is that if the number of device which are supposed to be connected together are known then how can we tell how many cables and ports are required to connect them.

Let say there are 4 devices connected in mesh topology: no. of cables = [n(n-1)]/2 = 6 cables would be required no. of ports of each device = (n-1) = 3 Reliability: means if any of the device get failed is there any way to send its message to other device? In case of 4 devices connected in mesh topology configuration these devices the reliability is High. Cost: Is also high Security: Is high. If one device A is contacting with device B then other devices will have no idea about their communication.

**Mesh Topology:**
Mesh topology supports point to point communication. In this combination each device is connected with every computer. It is expensive as many wires are used and when a new computer is added then it has to be connected with all other computer. It is scalability issue.

**Tree topology It is a combination of bus and star/hub topology.**

**Hub Topology**: In case of hub topology many device are connected with hub assume hub in center and other devices are connected with hub like server

Let say there are 4 devices connected in hub topology: no. of cables = [n(n-1)]/2 = 6 cables would be required no. of ports of each device = (n-1) = 3 total no. of ports = n(n-1) = 12 Reliability: means if any of the device get failed is there any way to send its message to other device? In case of 4 devices connected in huv topology configuration these devices the reliability is very low. In case of hub failure whole system will be failed no one would be able to communicate. Cost: low Security: low. As hub is to communicate in a broadcast way by default. On message sent by A device would be sent to all devices connected with the hub

**Bus Topology:** In this configuration there is a straight wire called back bone wire of large bandwidth having multiple devices connected with it. Imagine a stem having several leaves. Here stem is a back bone wire and leaves are devices.

Let say there are 4 devices connected in bus topology: no. of cables = n+1 = 5 cables would be required no. of ports of each device = n= 4 Reliability: reliability is very low. As if backbone wire fails whole system will be failed. Security: security is also low. As all messages will be send through a single wire so all can access them.

collision is problem in bus topology. As all devices at once sent a single so due to single back bone wire all signals can collide.

**Ring Topology:**
In this configuration there is a circular wire called back bone wire of large bandwidth having multiple devices connected with it. Imagine a stem in circular ring shape having several leaves. Here stem is a back bone wire and leaves are devices.

Let say there are 4 devices connected in ring topology: no. of cables = n+1 = 5 cables would be required no. of ports of each device = n= 4 Reliability: reliability is very low. As if backbone wire fails whole system will be failed. Security: security is also low. As all messages will be send through a single wire so all can access them.

collision is problem in bus topology. As all devices at once sent a single so due to single back bone wire all signals can collide.


**MPLS (Multiprotocol label switching):**
MPLS is a topology.


******************IPv4 Part-1:
If john wants to see a web page hosted on server C, how would john's computer will know where to send bob?
The answer is IP addresses

IP address provides our computer a logical addressing scheme for our computers so that our computers can communicate on networks.
Being logical IP addresses can be change any time unlike MAC address that are physically embedded into device.

IPv4 is made up of 32 bit binary number, there are 2^32 bit possible address combination. 
01010010.
01010010.
00100101.
01010010.

Divided into 4 sets of eight bits. IP address requires subnet masks to identify that which part defines the network portion and which part defines the host portion. 
Subnet mask address has the same format as IP address.

Sure! Here's a simple explanation of subnet masking in computer networking:

### What is Subnet Masking?

**Subnet masking** is a way of dividing a large network into smaller, more manageable pieces called subnets. This helps improve network performance and security.

### How it Works

1. **IP Address:** Every device on a network has a unique IP address (like a home address for your computer).

2. **Subnet Mask:** The subnet mask helps determine which part of the IP address refers to the network and which part refers to the device (host) within that network.

### Example

- **IP Address:** `192.168.1.10`
- **Subnet Mask:** `255.255.255.0`

### Breaking It Down

- **Subnet Mask `255.255.255.0`:**
  - The `255` parts indicate the network portion.
  - The `0` part indicates the host portion.

For the example above:
- **Network Part:** `192.168.1`
- **Host Part:** `.10`

### Why It's Useful

- **Improves Performance:** By dividing a large network into smaller subnets, data can travel more efficiently.
- **Enhances Security:** Subnetting can isolate different parts of a network, making it harder for unauthorized users to access all areas.

### Visual Analogy

Think of subnet masking like an address system in a city:
- **City (Network):** `192.168.1`
- **Street (Host):** `10`

The subnet mask helps you quickly identify which part of the address is the city and which part is the specific street.

### Conclusion

Subnet masking is a technique used to divide a larger network into smaller, more efficient sub-networks. It uses a subnet mask to distinguish between the network portion and the host portion of an IP address.

Sure! Let's explain subnetting IPv4 in the simplest way possible.

### What is Subnetting?

**Subnetting** is the process of dividing a larger IP network into smaller, more manageable sub-networks, or subnets. This helps in organizing the network, improving performance, and enhancing security.

### How IPv4 Subnetting Works

1. **IP Address and Subnet Mask:** An IPv4 address is a 32-bit number usually written as four decimal numbers separated by dots (e.g., `192.168.1.10`). A subnet mask is also a 32-bit number that divides the IP address into the network part and the host part.

2. **Binary Representation:** Both the IP address and the subnet mask can be represented in binary. For example:
   - IP Address: `192.168.1.10` → `11000000.10101000.00000001.00001010`
   - Subnet Mask: `255.255.255.0` → `11111111.11111111.11111111.00000000`

3. **Network and Host Parts:**
   - The subnet mask has ones (`1`) in the positions that represent the network part.
   - The subnet mask has zeros (`0`) in the positions that represent the host part.

### Simple Example

Let's take a simple example to explain subnetting:

- **IP Address:** `192.168.1.10`
- **Subnet Mask:** `255.255.255.0`

### Steps to Subnet an IP Network

1. **Determine the Network Address:**
   - Perform a bitwise AND operation between the IP address and the subnet mask.
   - For `192.168.1.10` and `255.255.255.0`:
     - IP Address: `11000000.10101000.00000001.00001010`
     - Subnet Mask: `11111111.11111111.11111111.00000000`
     - Network Address: `11000000.10101000.00000001.00000000` → `192.168.1.0`

2. **Determine the Number of Subnets:**
   - Decide how many subnets you need and adjust the subnet mask accordingly.
   - For example, if you need 4 subnets, you will borrow 2 bits from the host part (since 2^2 = 4).

3. **Calculate the New Subnet Mask:**
   - Original Subnet Mask: `255.255.255.0` → `11111111.11111111.11111111.00000000`
   - New Subnet Mask: `255.255.255.192` → `11111111.11111111.11111111.11000000` (borrowing 2 bits)

4. **Find the Subnet Addresses:**
   - The new subnet mask creates subnets by dividing the original network.
   - For example, `192.168.1.0/26`, `192.168.1.64/26`, `192.168.1.128/26`, and `192.168.1.192/26`. (These are CIDR (classless inter-domain routing) notations. Classless addressing was introduced to 		 slow down the growth of routing tables)

### Visual Analogy

Think of subnetting like dividing a big piece of land (the network) into smaller plots (subnets) where each plot can have its own houses (hosts).

### Why Subnetting is Useful

- **Improves Network Performance:** Smaller subnets reduce the size of broadcast domains.
- **Enhances Security:** Limits the spread of broadcast traffic and contains network issues within subnets.
- **Efficient IP Management:** Optimizes the use of IP addresses.

### Conclusion

Subnetting in IPv4 involves dividing a larger network into smaller subnets by modifying the subnet mask. This process helps in better managing and organizing the network, leading to improved performance and security.


# IPv4 part 2:
Certainly! Let's break down the different IP address classes and automatic private IP addressing in a simple way.

### IPv4 Address Classes

IPv4 addresses are divided into different classes, each with a specific range and purpose:

#### Class A
- **Range:** `1.0.0.0` to `126.0.0.0`
- **Default Subnet Mask:** `255.0.0.0`
- **Number of Networks:** 128 (but effectively 126, since `0.0.0.0` and `127.0.0.0` are reserved)
- **Number of Hosts per Network:** 16,777,214 (2^24 - 2)
- **Use Case:** Large organizations and networks

#### Class B
- **Range:** `128.0.0.0` to `191.255.0.0`
- **Default Subnet Mask:** `255.255.0.0`
- **Number of Networks:** 16,384
- **Number of Hosts per Network:** 65,534 (2^16 - 2)
- **Use Case:** Medium-sized organizations and networks

#### Class C
- **Range:** `192.0.0.0` to `223.255.255.0`
- **Default Subnet Mask:** `255.255.255.0`
- **Number of Networks:** 2,097,152
- **Number of Hosts per Network:** 254 (2^8 - 2)
- **Use Case:** Small organizations and networks

#### Class D
- **Range:** `224.0.0.0` to `239.255.255.255`
- **Use Case:** Multicasting (sending data to multiple destinations simultaneously)
- **Not used for:** Regular host addresses or subnetting

#### Class E
- **Range:** `240.0.0.0` to `255.255.255.255`
- **Use Case:** Reserved for experimental purposes
- **Not used for:** Regular host addresses or subnetting

### Automatic Private IP Addressing (APIPA)

When a device in a network cannot get an IP address from a DHCP (Dynamic Host Configuration Protocol) server, it can assign itself an Automatic Private IP Address (APIPA). This allows the device to communicate with other devices on the same local network.

- **Range:** `169.254.0.0` to `169.254.255.255`
- **Default Subnet Mask:** `255.255.0.0`
- **Use Case:** Allows communication within a local network when DHCP is unavailable.

## Public IP address vs Private IP address
Public IP addresses are routable. Each number must be a unique number.
Private IP addresses are not routable.


## IPv6
What do we do about running out of IPv4 addresses? The answer is IPv6

Its a 128 bit hexadecimal number separated by colon and contains 16 bits each.

It has 340x10^36

### IPv6 local address structure:
The first 64 bit represents the local network. 
The IPv6 local address structure follows the EUI-64 bit format (extended unique identifier) Which contains 48-bit MAC address, padded with 16 bits to make it 64 bits.
Local address always always starts with fe80

### IPv6 Global address structure:
The host address is always the last 64 bit address.
It is unique
Global IPv6 address always begin with in the range 2000 to 3999


### IPv6 Do not need DHCP configuration
When implemented IPv6 automatically configure both the local and global IPv6 addresses that are required to be unique in a network.  When a device first comes online it will use NDP (neighbour discovery protocol) to discover what are required network addresses. Both logical and global. This allows the device to configure its own IPv6 addresses.

### IPv6 notation:
128 bit hexadecimal number fe80:0000:13a1:8857:e388:2cc7 can also be written as fe80::13a1:8857:e388:2cc7


### IPv6 network transmission:
Unicast: one to one. A specific device sending traffic to another specific device. Unicast can occur on the local network (fe80) and global address (2000 to 3999)
Multicast: One to many or many to many. One device sending traffic to a specific group of devices that are registered. Multicast addresses always begins with ff.
broadcast: One to thousands. One devices is sending traffic to all devices connected to it.
Anycast: One to the closest. One devices is sending traffic to a specific IPv6 addresss that has been assigned to multiple devices.


### DHCPv6
IPv6 can auto configure its local and global ip addresses. In certain situations it is not always desirable. 
DHCPv6 can configured to handout the specific IPv6 addresses. Useful for load balancing a network.


### IPv6 and IPv4 
Dual stack configuration.
The network and the devices on the network can recevies both IPv4 and IPv6 configuration.


### Tunneling:
6to4 tunneling is used to travel IPv6 datapacket to travel through IPv4 Datagram. allowing IPv6 packet to travel accross all IPv4 networks.
6to4 tunneling also called Teredo tunneling.



# Special networking concepts:
**MAC (Media access control) Address:**
MAC address is also referes as the physical address or burned address that is physically embededn into the device by the manufacturer. 
**MAC address format:**
It is a combination of OUI (Orginanization Unique identifier) and EUI (EXtedned Unique identifier) Both are combined to make it a 64 bit number. The OUI is also called the serial number of the device and given by the manufacturer. Whereas EUI is padded to makee it 64 bit number.
Swticher and OSI layer 2 rely on MAC addresses.

### Collision domain vs Broadcast domain
Ethernet networks uses a technology called CSMA/CD (carrier sense multiaccess with collision detection) to detect the colission
### Collision Domain
- **What it is**: A collision domain is a network segment where data packets can collide with each other when being sent on a shared medium or through repeaters. Collisions occur when two devices send packets at the same time on the same network segment.
- **Analogy**: Imagine a group of people in a room talking at the same time. If two people talk simultaneously, their voices collide, and it’s hard to understand what either of them is saying. This room is like a collision domain.
- **Example**: In a traditional Ethernet network using a hub, all devices connected to the hub are in the same collision domain.

### Broadcast Domain
- **What it is**: A broadcast domain is a network segment in which if a device sends a broadcast frame, all devices in that segment will receive it. Broadcasts are messages sent to all devices on the network segment.
- **Analogy**: Think of a radio station broadcasting a signal. Everyone within the range of the signal can receive it. The area covered by the signal is like a broadcast domain.
- **Example**: In a typical LAN (Local Area Network) with switches, all devices connected to the switch are in the same broadcast domain unless VLANs (Virtual Local Area Networks) are used to segment the network.

### Key Differences
- **Collision Domain**: Limited by devices that share the same physical medium, like a hub. Switches and routers separate collision domains.
- **Broadcast Domain**: Limited by network boundaries defined by routers. Switches do not separate broadcast domains; only routers and VLANs do.

### Visualization
- **Collision Domain**: All devices connected to a hub.
- **Broadcast Domain**: All devices connected to a switch or multiple switches in the same network without a router in between.

In summary:
- **Collision domains** deal with data packet collisions and are managed using switches.
- **Broadcast domains** deal with broadcast traffic and are managed using routers and VLANs.

## NOTE:
IPv6 do not uses broadcast domain instead they use anycast domain.


**Routing Concept Part - 1:**
Purpose of routing: The purpose of routing is simple. routing was introduced to connect different devices so that they can communicate and pass data traffic. Routing protocols are used which tells how 	networkds determine where to send the network traffic.


# Basic Routing Concept:
## Static Routing:
In this routing the path is already configured by the admin.
The path from A to B and then from B to A must be configured to have both way communication.
Static routing is easy to setup for small networks but not easy to maintain and will only change when the admin change it.

## Dynamic Routing:
Routers uses protocols in order to determine the best possible path between two routers.

All routers must be using the same protocols. An exception is when router distribution is implemented. Routing protocols can be stacked within a router.


## Default Route:
The direction where the router will send traffic if there is no route in the routing table. It is assigned by network admin.

## Routing Table:
The list of known routes to all know routes from the routers perspective. 
it is established by admin in case of static routing.
And dynamically built in case of dynamic routing.

### Loopback Interface

**Loopback Interface:**

1. **Definition:**
   - The loopback interface is a virtual network interface in a computer or a router that is used to test and manage network software. It is primarily used for testing network applications and the stack, ensuring that they are running correctly without the need for a physical network.

2. **Characteristics:**
   - The IP address range for the loopback interface is `127.0.0.0/8`, with `127.0.0.1` being the most commonly used address, often referred to as "localhost."
   - It is always up and can never be down as long as the device is powered on.
   - It is used internally within the device and cannot be reached from any external network.

3. **Uses:**
   - **Testing and Diagnostics:** Developers use the loopback interface to test network applications locally without sending traffic over the actual network.
   - **Management:** Network administrators use it for management tasks. For example, configuring and testing routing protocols and ensuring that the network stack is functioning properly.
   - **Software Development:** It allows developers to test applications that require a network connection without needing a physical network.

### Routing Loop

**Routing Loop:**

1. **Definition:**
   - A routing loop occurs when packets are continuously transmitted within a series of routers without reaching their intended destination. This can happen due to incorrect routing table entries or misconfigurations, causing the packet to circulate indefinitely.

2. **Causes:**
   - **Incorrect Routing Information:** Errors in routing tables can cause a router to forward packets back to a router that has already processed them.
   - **Slow Convergence:** In dynamic routing protocols, a routing loop can occur during the convergence process, where routers are updating their routing tables and network topology changes are not yet fully propagated.
   - **Configuration Errors:** Misconfigurations in routing policies or protocols can lead to loops.

3. **Effects:**
   - **Network Congestion:** Packets caught in a loop consume bandwidth, leading to network congestion.
   - **Increased Latency:** Continuous looping increases the delay for packet delivery.
   - **Resource Depletion:** Routers and network devices expend additional resources processing the same packets repeatedly.

4. **Prevention and Resolution:**
   - **Time-to-Live (TTL) Field:** The TTL field in an IP packet header is decreased by one each time the packet passes through a router. When the TTL reaches zero, the packet is discarded, preventing it from looping indefinitely.
   - **Routing Protocol Features:** Many routing protocols have built-in mechanisms to prevent routing loops. For example, distance-vector protocols use techniques like split horizon, route poisoning,: and hold-down timers to prevent loops.
   - **Proper Configuration:** Ensuring that routing protocols and network devices are properly configured and regularly updated to reflect accurate network topology.

## Routing Mertics:
There may more be more than one possible route available to a remote network. Routing protocols are used to determine the best possible path to reach the destination betwene two routers.

## Hop Count:
The number of routers between two end points
Determine from the senders perspective.

## Maximum Transission Time (MTU):
Maximum allowed size of a packet. measured in bytes. The standard MTU for ethernet is 1500 bytes.
Packest exceeding the MTU must be fragmented into smaller pieces.

## Bandwidth:
A measure of speed of network. usually in Kbps, Mbps, Gbps

## latency:
A measure of time that a packet takes to traverse the Link.

## Administrative Distance:
AD helps us determining which routing protocol is to use when there is more than one routing protocol is installed on a system.
The lowest AD will determine the protocol to used.


### Common AD are as follow:
- Connected interface	0
- Static route	1
- Enhanced Interior Gateway Routing Protocol (EIGRP) summary route	5
- External Border Gateway Protocol (BGP)	20
- Internal EIGRP	90
- IGRP	100
- OSPF	110
- Intermediate System-to-Intermediate System (IS-IS)	115
- Routing Information Protocol (RIP)	120
- Exterior Gateway Protocol (EGP)	140
- On Demand Routing (ODR)	160
- External EIGRP	170
- Internal BGP	200
- Unknown*	255


### Route Aggregation

**Route Aggregation:**

1. **Definition:**
   - Route aggregation, also known as route summarization, is the process of combining multiple IP routes into a single summary route. This reduces the number of routes that need to be advertised and managed, thereby simplifying the routing table and improving the efficiency of the routing process.

2. **Purpose:**
   - **Reduce Routing Table Size:** By aggregating routes, the number of entries in the routing table is minimized, which conserves memory and processing power on routers.
   - **Improve Routing Efficiency:** Fewer routes mean quicker route lookup and faster routing decisions, improving overall network performance.
   - **Enhance Stability:** Aggregating routes can help limit the scope of route flaps (frequent changes in route status), thus enhancing the stability of the network.
   - **Optimize Network Bandwidth:** Reducing the number of route advertisements conserves bandwidth on network links used for routing updates.

3. **Example:**
   - Suppose a router has the following routes:
     - 192.168.1.0/24
     - 192.168.2.0/24
     - 192.168.3.0/24
     - 192.168.4.0/24
   - These can be aggregated into a single summary route:
     - 192.168.0.0/22
   - This summary route encompasses all four of the original routes, reducing the number of routes the router needs to advertise.

4. **Implementation:**
   - **Manual Aggregation:** Network administrators manually configure route aggregation on routers by specifying the summary routes.
   - **Automatic Aggregation:** Some routing protocols, such as OSPF and EIGRP, support automatic route summarization at network boundaries or on specific interfaces.

5. **Considerations:**
   - **Subnet Boundaries:** Effective route aggregation depends on the routes being on contiguous subnet boundaries. If the subnets are not contiguous, aggregation may not be possible.
   - **Route Specificity:** Aggregated routes are less specific than individual routes. While this simplifies routing, it can also lead to suboptimal routing paths in some scenarios.
   - **Route Flapping:** In environments with dynamic changes, route aggregation can help mitigate the impact of route flapping by containing it within a smaller area of the network.

### Example Scenario

Let's look at a more detailed example to understand route aggregation in practice:

#### Scenario:
A network administrator manages a network with multiple subnets assigned to different departments within a company. The subnets are as follows:
- Department A: 10.1.1.0/24
- Department B: 10.1.2.0/24
- Department C: 10.1.3.0/24
- Department D: 10.1.4.0/24

Instead of advertising these four individual routes, the administrator can configure route aggregation as follows:
- Aggregated Route: 10.1.0.0/22

This single summary route 10.1.0.0/22 covers all IP addresses from 10.1.0.0 to 10.1.3.255, which includes all the individual subnets of the departments.

#### Benefits:
- **Reduced Routing Table Size:** The router will now advertise one route (10.1.0.0/22) instead of four individual routes.
- **Simplified Management:** The routing table is easier to manage and maintain with fewer entries.
- **Improved Network Performance:** Routing decisions are made faster with a smaller routing table, and there is less overhead in route advertisement traffic.

### Conclusion

Route aggregation is a valuable technique in network design and management that helps to optimize the efficiency, performance, and stability of routing in IP networks. By consolidating multiple specific routes into a single, broader summary route, network administrators can achieve significant improvements in routing scalability and manageability.

## High Availablity:
Part of a network administrator's job is to ensure that networks remain up and active. 
Admin achieve this by avoiding single point failure in the network.


Hot Standby Router Protocol (HSRP) and Virtual Router Redundancy Protocol (VRRP)
Hot Standby Router Protocol (HSRP)
**HSRP Overview:**
HSRP is a Cisco proprietary redundancy protocol designed to increase the availability of the default gateway servicing hosts on a subnet.
It allows multiple routers to participate in a virtual router group, with one router acting as the active router and another as the standby router.
The active router handles all the traffic sent to the virtual IP address. If the active router fails, the standby router takes over without any disruption in service.
How HSRP Works:

**Virtual IP and MAC Address:**

HSRP routers share a virtual IP address that is used as the default gateway for the hosts.
The active router answers ARP requests for this IP address with a virtual MAC address.

**Priority and Preemption:**

Each router in the HSRP group has a priority value (default is 100). The router with the highest priority becomes the active router.
Preemption allows a router with a higher priority to take over as the active router if it becomes available again after a failure.
Hello Packets:

Routers send hello packets to each other at regular intervals to indicate that they are operational.
If the standby router stops receiving hello packets from the active router, it assumes the active router has failed and takes over.

**HSRP States:**
Initial: Starting state.
Learn: The router has not determined the virtual IP address and is waiting to hear from the active router.
Listen: The router knows the virtual IP address but is neither the active nor standby router.
Speak: The router sends periodic hello messages and participates in the election process.
Standby: The router is a candidate to become the next active router and sends hello messages.
Active: The router forwards packets that are sent to the virtual MAC address.

**HSRP Example:**
Routers R1 and R2 are configured in an HSRP group with a virtual IP address of 192.168.1.1.
R1 has a priority of 120, and R2 has a priority of 100. Therefore, R1 is the active router, and R2 is the standby router.
Hosts on the network use 192.168.1.1 as their default gateway.
If R1 fails, R2 will take over as the active router, ensuring continuous network availability.
Virtual Router Redundancy Protocol (VRRP)

**VRRP Overview:**
VRRP is an open standard protocol defined in RFC 5798, which provides redundancy for the default gateway.
It allows multiple routers to form a virtual router group with one router acting as the master and the others as backups.
Similar to HSRP, VRRP ensures high availability by allowing the backup router to take over if the master router fails.
How VRRP Works:

**Virtual IP and MAC Address:**
VRRP routers share a virtual IP address used by hosts as their default gateway.
The master router handles ARP requests for this IP address using a virtual MAC address.
Priority and Preemption:
Each router in the VRRP group has a priority value (default is 100). The router with the highest priority becomes the master router.
Preemption is enabled by default, allowing a router with a higher priority to become the master router if it becomes available after a failure.

**Advertisement Packets:**
The master router sends VRRP advertisements at regular intervals to inform other routers of its status.
If the backup router does not receive advertisements from the master, it assumes the master has failed and takes over.

**VRRP States:**
Initialize: Starting state.
Backup: The router is monitoring advertisements from the master and will take over if the master fails.
Master: The router is forwarding packets sent to the virtual MAC address and sending advertisements.
VRRP Example:

Routers R1 and R2 are configured in a VRRP group with a virtual IP address of 192.168.1.1.
R1 has a priority of 150, and R2 has a priority of 100. Therefore, R1 is the master router, and R2 is the backup router.
Hosts on the network use 192.168.1.1 as their default gateway.
If R1 fails, R2 will take over as the master router, ensuring continuous network availability.



# Unified Communication (UC)
Unified Communication (UC) is a system that integrates different communication methods into a single, cohesive experience. This makes it easier for people to communicate and collaborate, regardless of the device or platform they're using.

**Key Features of UC:**
Instant Messaging (IM): Sending text messages in real-time.
Voice Calls: Traditional phone calls or internet-based calls.
Video Conferencing: Holding face-to-face meetings over the internet.
Email: Integrating email services.
File Sharing: Sharing documents and files seamlessly.
Presence Information: Showing the availability status of team members (e.g., online, busy, away).

**Benefits of UC:**
Improved Collaboration: Teams can communicate more effectively.
Increased Productivity: Easy access to multiple communication tools in one place.
Flexibility: Communicate from anywhere using various devices (e.g., smartphones, tablets, computers).
Voice over IP (VoIP)
Voice over IP (VoIP) is a technology that allows you to make voice calls using an internet connection instead of a traditional phone line.

## How VoIP Works:
Voice Conversion: Your voice is converted into digital data.
Data Transmission: This data is sent over the internet.
Receiving End: The data is converted back into voice at the receiving end.
**Key Features of VoIP:**
Internet Calls: Make phone calls over the internet.
Lower Cost: Typically cheaper than traditional phone services, especially for long-distance calls.
Flexibility: Use various devices to make calls (e.g., computers, smartphones, VoIP phones).
Benefits of VoIP:
Cost Savings: Reduced phone bills, especially for international calls.
Scalability: Easily add or remove lines as needed.
Advanced Features: Access to features like call forwarding, voicemail to email, and video calls.
Visual Analogy:
Unified Communication: Imagine having a Swiss Army knife with all your communication tools in one place – you have a blade (instant messaging), scissors (voice calls), and a screwdriver (video conferencing) all in one tool.
VoIP: Think of VoIP as sending a letter via email instead of traditional mail. It’s faster and often cheaper because it uses the internet.

# Virtualization concept:
What is the difference between virtual machine manager and hypervisor:
Both terms are used interchangably. Both can have same meaning. But some people say VMM requires a host system to operate such as OS, Windows and linux where as Hypervisor do not need any host system to operate.

### Components of virtual machine:
## Virtual Desktop:
A virtual machine that function as a desktop. 
Any modern OS can be run on VM desktop. Multiple Virtual machines can be hosted on a single OS.

## Virtual servers:
A virtual machine that function as a server.


## Virtual switches, firewall, and routers:
A virtual machine that fulfulls the functions of switch, firewall and router.

They are effective when combined with a metwork.


### Software defined network:
Software defined network is the process of allowing the administration and configuration of a network to be done dynamically.
SND can be used as front end to make adjustments to the network configurations. SND allows network administrator to make adjustments to the network dynamically.

# Differences between SAN (Storage Area Network) and NAS (Network Attached Storage):

### SAN (Storage Area Network)
- **Purpose**: SAN is designed to provide high-performance, block-level storage access to servers.
- **Connection**: Uses a dedicated, high-speed network (often fiber optic) separate from the regular data network.
- **Usage**: Typically used in large data centers and enterprise environments where speed and performance are critical.
- **Access**: Appears to servers as if they are locally attached storage devices (block storage).
- **Complexity**: Generally more complex and expensive to set up and manage.

**Analogy**: Think of SAN like a private road network just for storage traffic, ensuring fast and exclusive access for vehicles (data).

### NAS (Network Attached Storage)
- **Purpose**: NAS provides file-level storage access over a standard network.
- **Connection**: Connects to the existing local area network (LAN) via Ethernet.
- **Usage**: Commonly used in homes, small to medium-sized businesses for file sharing, backup, and general storage.
- **Access**: Appears to users and applications as a shared network drive (file storage).
- **Simplicity**: Easier and cheaper to set up and manage compared to SAN.

**Analogy**: Think of NAS like a shared public road where many people can access and share files (data) using the existing infrastructure.

### Key Differences
- **Type of Storage**:
  - **SAN**: Block-level storage (like a hard drive).
  - **NAS**: File-level storage (like a shared folder).
  
- **Network**:
  - **SAN**: Uses a separate, high-speed network.
  - **NAS**: Uses the existing Ethernet network.
  
- **Performance**:
  - **SAN**: Higher performance, suitable for high-speed data transfer.
  - **NAS**: Adequate performance for general file sharing and backup.

- **Complexity and Cost**:
  - **SAN**: More complex and expensive.
  - **NAS**: Simpler and more affordable.

In summary:
- **SAN** is like having a dedicated, private highway for fast and efficient data transfer between storage and servers.
- **NAS** is like having a shared, public road for convenient and accessible file sharing over a regular network.

# Basics of Cloud Computing
Cloud computing is where the resources on the internet are not physically in nature but present virtually to the users and can be used accoding to their needs only. 
They are highly configurable.

### Classification of cloud computing:
**Public cloud:**
System can interact with servers and devices within the public cloud network e.g internet

**private cloud:**
only accessible for the authorized users.

**hybrid cloud:**
Combines the aspects fo both private and public

**community cloud:**
used by the community who have common interests.


## Types of cloud computing:

# Differences between SaaS (Software as a Service), PaaS (Platform as a Service), and IaaS (Infrastructure as a Service) in the simplest terms:

### SaaS (Software as a Service)
- **Purpose**: Provides ready-to-use software applications over the internet.
- **Usage**: Users can access software applications without worrying about the underlying infrastructure or platforms. Examples include email services, office tools, and customer relationship management (CRM) systems.
- **Management**: The service provider manages everything: applications, data, runtime, middleware, OS, virtualization, servers, storage, and networking.
- **Example**: Google Workspace (Gmail, Google Docs), Microsoft 365, Salesforce.

**Analogy**: Think of SaaS as renting a fully furnished apartment. You just move in and start using it without worrying about furniture or maintenance.

### PaaS (Platform as a Service)
- **Purpose**: Provides a platform allowing customers to develop, run, and manage applications without dealing with the underlying infrastructure.
- **Usage**: Developers use it to build and deploy applications. It offers tools and services to facilitate application development.
- **Management**: The service provider manages the infrastructure (servers, storage, networking) and the platform (OS, middleware, runtime), while users manage the applications and data.
- **Example**: Google App Engine, Microsoft Azure App Service, Heroku.

**Analogy**: Think of PaaS as renting a workshop with all the tools and equipment provided. You bring your materials (code and data) and create your products (applications) without worrying about the tools and workshop maintenance.

### IaaS (Infrastructure as a Service)
- **Purpose**: Provides virtualized computing resources over the internet.
- **Usage**: Users can rent virtual servers, storage, and networking, and they have control over the operating systems and applications they run.
- **Management**: The service provider manages the physical infrastructure (servers, storage, networking), while users manage the OS, middleware, runtime, applications, and data.
- **Example**: Amazon Web Services (AWS) EC2, Microsoft Azure Virtual Machines, Google Cloud Compute Engine.

**Analogy**: Think of IaaS as renting a piece of land with basic utilities provided (electricity, water). You build your own house (install your OS, applications) and manage it as you see fit.

### Key Differences
- **SaaS**: Complete software solutions delivered over the internet.
  - **Users**: End-users who need to use software applications without worrying about the infrastructure.
  
- **PaaS**: Platforms for building, testing, and deploying applications.
  - **Users**: Developers who need a platform to build and deploy applications without managing the underlying infrastructure.
  
- **IaaS**: Virtualized computing resources over the internet.
  - **Users**: IT administrators and developers who need control over the infrastructure to install and manage their own operating systems and applications.

In summary:
- **SaaS** is like renting a fully functional apartment (software).
- **PaaS** is like renting a workshop with tools (development platform).
- **IaaS** is like renting land with basic utilities (virtualized infrastructure).


# Implementing the basic network:

### Network Planning

1. **Determine Network Requirements**
   - **Identify Users and Devices**: Determine the number of users and devices that will connect to the network.
   - **Usage Requirements**: Identify the types of applications and services that will be used (e.g., email, web browsing, video conferencing, file sharing).
   - **Performance Needs**: Assess the required bandwidth, latency, and performance for each application.

2. **Design the Network Topology**
   - **Choose the Type of Network**: Decide whether to use a LAN (Local Area Network), WAN (Wide Area Network), or both.
   - **Select a Topology**: Choose a suitable topology (e.g., star, mesh, ring, bus) based on your requirements and layout.
   - **Plan for Scalability**: Design the network with future growth in mind.

3. **Select Network Hardware**
   - **Routers and Switches**: Determine the number and type of routers and switches needed.
   - **Access Points**: Decide on the number of WAPs required for wireless coverage.
   - **Cabling**: Choose the type of cabling (e.g., Cat5e, Cat6) and plan the cable runs.

4. **Plan Network Security**
   - **Firewall**: Decide on the use of firewalls to protect the network.
   - **VPN**: Consider setting up VPNs for remote access.
   - **Access Control**: Plan for user authentication, access control lists (ACLs), and other security measures.

5. **IP Addressing and Subnetting**
   - **IP Scheme**: Develop an IP addressing scheme, including the assignment of static and dynamic IP addresses.
   - **Subnetting**: Determine how to segment the network into subnets for better management and security.

### Network Configuration

1. **Setup and Configure Hardware**
   - **Install and Connect Devices**: Physically install and connect routers, switches, access points, and other network devices.
   - **Power On Devices**: Ensure all devices are powered on and functioning.

2. **Configure Routers and Switches**
   - **Router Configuration**: Set up the routers with basic configurations like hostname, passwords, and interfaces.
   - **Switch Configuration**: Configure switches with VLANs, trunking, and port settings.

3. **Implement IP Addressing**
   - **Assign IP Addresses**: Assign IP addresses to network devices and ensure all devices are reachable.
   - **Configure DHCP**: Set up a DHCP server to dynamically assign IP addresses to devices.

4. **Configure Network Services**
   - **DNS and DHCP**: Set up DNS and DHCP servers for name resolution and IP address management.
   - **File and Print Services**: Configure servers for file and print sharing as needed.

5. **Configure Wireless Network**
   - **Setup Access Points**: Configure WAPs with SSIDs, security settings, and channel settings.
   - **Test Wireless Coverage**: Ensure that wireless coverage is adequate throughout the area.

6. **Implement Security Measures**
   - **Firewall Configuration**: Set up firewalls with appropriate rules to protect the network.
   - **Access Control**: Implement ACLs, user authentication, and other security measures.
   - **Update Firmware**: Ensure all devices are running the latest firmware and software updates.

7. **Test the Network**
   - **Connectivity Testing**: Verify that all devices can communicate with each other and access the internet.
   - **Performance Testing**: Test the network performance to ensure it meets the required standards.
   - **Security Testing**: Conduct security tests to identify and fix any vulnerabilities.

8. **Document the Network**
   - **Network Diagram**: Create a detailed network diagram showing all devices and connections.
   - **Configuration Documentation**: Document all configurations and settings for future reference.

9. **Monitor and Maintain the Network**
   - **Network Monitoring**: Set up monitoring tools to keep track of network performance and health.
   - **Regular Maintenance**: Perform regular maintenance tasks like firmware updates, configuration backups, and security audits.

This procedure provides a general framework for planning and configuring a network. Depending on the specific requirements and complexity of your network, additional steps and considerations may be necessary.

# Backups

### Full Backup
- **What it is**: A complete copy of all the data you want to back up.
- **Pros**: Easy to restore because all data is in one backup set.
- **Cons**: Takes the most time and storage space.
- **Example**: If you have 100 GB of data, a full backup will copy all 100 GB every time you do a backup.

**Analogy**: Imagine making a photocopy of an entire book. Every time you make a backup, you copy the entire book, regardless of whether any pages have changed.

### Incremental Backup
- **What it is**: A backup of only the data that has changed or been added since the last backup of any type (whether full or incremental).
- **Pros**: Saves time and storage space because only changes are backed up.
- **Cons**: Slower to restore because you need the last full backup and all incremental backups since then.
- **Example**: After the initial full backup, if 5 GB of data changes the next day, only that 5 GB will be backed up.

**Analogy**: Imagine adding a note to a photocopy of the book only for the pages that have new changes. To restore, you need the original book and all the notes.

### Differential Backup
- **What it is**: A backup of all the data that has changed since the last full backup.
- **Pros**: Faster to restore than incremental because you only need the last full backup and the last differential backup.
- **Cons**: Takes more storage than incremental but less than full backups as changes accumulate.
- **Example**: After the initial full backup, if 5 GB of data changes, a differential backup will copy that 5 GB. If another 3 GB changes the next day, the next differential backup will copy a total of 8 GB (the 5 GB from before plus the new 3 GB).

**Analogy**: Imagine updating the photocopy of the book with all changes since the last full copy was made. To restore, you need the original book and the latest updated copy.

### Summary
- **Full Backup**: Copies everything every time. Easy to restore, takes the most space and time.
- **Incremental Backup**: Copies only changes since the last backup (full or incremental). Saves space and time, but slower to restore.
- **Differential Backup**: Copies all changes since the last full backup. Faster to restore than incremental, but takes more space over time.

## Segmentation:
Segmentation is basically dividing a large network into smaller manageabel segments.
Segmentation can be done at physical layer by dealing with physical resources such as cables switches etc and can be done logically at Data link layer and networking layer. Logical segmentation requires the least resources.

### Importamce of segmentation:
- To ease administrative tasks
- To achieve performance gains
- To increase security

## Compliance:
Means keeping the data separate. For example, keeping the user private information from the business information etc. This can be achieve by  network segmentation.

**Network Performance optimization:**
The network increase in size the amount of data flowing through it increases. This can slow down the perfomance of the network. Segmentation breaks the network into smaller network reducing the amount of data flowing through it hence increasing the network performance optimization.

**Creating high performance network:**
some applications require more bandwidth in order to perform at a desire high level. 

**Separate private network from public network**
## Honeynets:
Honeynets are the systems that are configured to be attractive for the other networks. These systems are configured to drawn the network attackers from the main network. The network segment of honeypots allows the main network to remain secure and give admin an opportunity to study an attack.


# VLAN (Virtual Local Area Network)

#### What is a VLAN?
A VLAN is a way to create separate, isolated networks within a single physical network. This helps in organizing and managing network traffic efficiently.

#### Key Points:
- **Segmentation**: VLANs allow you to segment a physical network into multiple logical networks. Each VLAN acts as its own separate network.
- **Security**: Devices on different VLANs cannot communicate directly with each other without a router or layer 3 switch, which enhances security.
- **Management**: Makes it easier to manage and control network traffic, as you can group devices based on function, department, or other criteria.

#### Example:
In an office, you can have one VLAN for the sales department, another for the HR department, and another for the IT department. Even though all departments are on the same physical network, the traffic is separated.

### Spanning Tree Protocol (STP)

#### What is STP?
STP is a network protocol that ensures a loop-free topology for Ethernet networks. It prevents network loops, which can cause broadcast storms and network failures.

#### Key Points:
- **Loop Prevention**: STP identifies and disables redundant paths in the network, ensuring there are no loops.
- **Tree Structure**: Creates a spanning tree by selecting a single root bridge and blocking redundant paths to prevent loops.
- **Path Selection**: Uses bridge protocol data units (BPDUs) to exchange information and determine the best path.

#### Example:
In a network with multiple switches connected in a mesh, STP will disable some connections to prevent loops, ensuring that there is only one active path between any two devices.

### Rapid Spanning Tree Protocol (RSTP)

#### What is RSTP?
RSTP is an evolution of STP that provides faster convergence. It rapidly recalculates the spanning tree topology in the event of a topology change or failure.

#### Key Points:
- **Faster Convergence**: RSTP can recover from network changes much quicker than STP, usually within a few seconds.
- **Backward Compatibility**: RSTP is backward compatible with STP, meaning it can interoperate with devices running STP.
- **Improved Port Roles**: Introduces new port roles and states to enhance the speed of the spanning tree recalculation.

#### Example:
In a network with RSTP, if a switch or link fails, the protocol quickly reconfigures the network to restore connectivity without the lengthy delays associated with STP.

### Summary
- **VLAN**: Segments a physical network into multiple logical networks to improve management and security.
- **STP**: Prevents network loops by creating a loop-free tree structure in Ethernet networks.
- **RSTP**: An improved version of STP that provides faster recovery from network changes and failures.

## Wireless LAN infrastructure
Roaming in networking refers to the ability of a device to move between different network areas or access points without losing its connection or service. 

### Key Points:
- **Seamless Connectivity**: Roaming ensures that a device maintains a continuous connection to the network even when moving from one location to another.
- **Common in Wi-Fi and Cellular Networks**: Used extensively in Wi-Fi networks (e.g., moving around a building with multiple Wi-Fi access points) and cellular networks (e.g., moving from one cell tower coverage area to another).
- **Handoff Process**: When a device moves out of the range of one access point or cell tower, it automatically connects to another, ensuring uninterrupted service.

### Example:
	Imagine you are using your smartphone to browse the internet while walking through your office. As you move from the reception area to a meeting room, your phone automatically switches from one Wi-Fi access point to another without disconnecting your internet session. This automatic switching and maintaining the connection is what roaming in networking is all about.
 
##Common Network vulnerablilities:
**Telnet:** A protocol that is used to create a virtual terminal connection that is commonly used for trouble shooting. Telnet is very unsecure because all communication happens in the form of clear text. telnet doesn't support encryption.

**FTP:** File transfer protocol is used to tranfer the files over the internet also do not support encryption thats why it is unsecure as well. But it requires credentials/authentication for use.
**SFTP:** Secure FTP. It supports encryption.

**TFTP:** Trivial FTP. Its a stripped down version of FTP that doesn't support authentication like Standard FTP. This protocol is used to download configuration files over the internet.
**HTTP:** To transfer HTML files. It is also not encrypted.
**HTTPS:** It is the encrypted version of HTTP.

**Open port:** An open port is hole in a network security. Not all ports can be or should be closed. Instead security should be placed on those ports and remain the ports open. Port scanner must  be used to verify that only absolutely required application ports are open.


# Network Threats:
**ARP cache poisoning:** In this process the attacker maps the IP address to the MAC addresses of the devices and he will get to know that which device has which IP address or you can say which MAC address is associated with which IP address.

**Protocol Abuse:** Commonly used to bypass the routers. To get  the router access list from inside a network.

**Man in the middle attack:** Here attacker is not necessary to be inside the network. Here the attacker will reside between two enp points. In most cases MIMA is used to disrupt the ARP process. This attack allows the attacker to see the network packets flowing through the connections.

**VLAN Hopping:** In VLAN Hopping the traffic from one VLAN can pass through the other VLAN using the tags. In actual, Traffic in one VLAN cannot pass through the other VLAN without the intervention of the router. In VLAN Hopping tags are attached to the network traffic which allows them to pass through the switches.

**Brute Force attack:** Using computing power to make combinations of credentials from the dictionary to crack the password.

**Spoofing:** In this attack the IP address of MAC address is modied to a friendly looking IP or MAC address to bypass network security. This shows the outside host as the trusted inside host.

Session Hijacking. This attack starts when a user has been authenticated and his session has started.

**Denial of service Attack (DoS):** Covers a very bad category of threat. Its an attempt to flood the network with enough traffic to bring it down.

**Permanent DoS:** Attempt to permanently down the network. Can be achieved using malware that corrupts or damages the underlying digital system.

**Distributed DoS:** More than one distributed attackers are trying to send traffic to the network.

**Reflecting DoS:** Ampliefied form of DoS. The source remain hidden in such type of attacks. In this attack the attacker usually spoofs (fake or pretend) the targeted IP address and sends request to the open DNS server and then DNS server reponds back with enough traffic to the actual target IP address resulting in down the network.

**Evil twin Attack:** Used to capture the sensitive information by becoming a very similar authorized version.

**Bluejacking:** Sending unsolicited messages over the bluetooth connection in an effort to keep the target from responding to valid request.

## Making network more secure:
**SSH (Secure Shell):** A protocl that is used to create an encrypted communication session between devices
**SNPM (Simple network management protocol):** Used to manage and configure devices remotely.

**TLS Transport layer security:** Used to encrypt protcols online. It uses certificates and asymmetrical cryptographic to authenticate hosts. It is better than SSL.

**Host-based anti-malware:** Protect individual nodes.
**Network-based anti-malware:** Protect local network.
**Cloud-based anti-malware:** the application resides in the cloud and is served to the clients inside the local network.

Implement switch and router security: This includes adjusting VLAN settings, MAC addressing filtering (only specific MAC addresses devices are allowed). To harden the router at least one ACL (Access control list) must be active on it. All ACLs have implicit deny at the end of the list.

## Symmetric vs Asymmetric keys:
**Symmertic** encryption key we have only one key for encrypt and decrypt the data. PSK (pre shared key) is symmetric in nature.

**Asymmetric** encryption key: We have two keys private key for encryption and public key for decryption.

On the return, This is reverse, The original receiver encrypts with the original sender's public key. which then gets decrypted with the private key.

**Sender side:**
Private key--> Encrypt
Public key --> Decrypt

**Receiver Side:**
Public key of sender --> encrypt
Private key of sender --> decrypt


# Firewall basics:
Types of firewalls:
Host based firewalls: Installed on the node usually a desktop computer that needs the protection.

Network based firewall: Installed on the perimeter of network that needs the protection. Are used to protect private network from public networks. It can either be a software installed on Routers OS or or on the server.

**SOHO small office home office:**
The network firewall is provided by a WAN connection device.


## Stateless vs stateful inspection firewall.
**Stateless inspection firewall:**
It is not concern with the state of the network. It examines each and every packet entering or leaving the network and compare it against the set of rules called an ACL Access control list. ACL rules are defined by static values by the admin.

Stateful inspection: Do not care about the packet. It cares about the state of the network. As a general rule, connections outside of the local aree network are not allowed. Only packets going from inside of the network are going to check against the set of rules.


**REMEMBER:** Firewalls not only can examine the packets but also the protocols, devices, and other services as well.	

## Firewall placements
Most firewalls are implemented on routers interface or at the host level. An exception is for virtual firewall. It is placed between the two devices. Not functioning as the router or switch it contains two interfaces as packet passes through the interface the packet is compared with ACL.

In external placements Firewall will be placed outside the local area network means at WAN.
In internal placements firewall will be placed in a logical central location.

## Demilitarized Zone (DMZ)
A specific zone created between two firewalls. Which allows the access to the outside network while the inside network is still protected from the outside network.
The external facing router will allow the specifc outside traffic into DMZ

ACL: Every fire wall compare packets against the set of rules defined by the admin and those rules are called ACL Access control list. Rules can be based on such criteria as source or destination MAC , IP addresses, protocol and time of day.


# Network Troubleshooting commands:
```bash
ping
```

To check if there is a connectivity between two nodes.

syntax example:
```bash
ping 0.0.0.0 
ping www.google.com
```

**tracert/traceroute:**

tracert for windows
traceroute for linux
used to determine the path used between two routes

syntax example:
```bash
traceroute 0.0.0.0 
traceroute www.google.com
```
 

**PathPing**
combination of ping and traceroute
**ipconfig/ifconfig:**

used to determine the ip configuration of the given node. Can also be used to change the ip configuration using this command.

**arp:**
address resolution protocol.
Used to corelate the IP address to MAc address.


**nslookup**
stands for name server lookup

Used to diagnose DNS related issues.

```bash
nslookup www.google.com
```

**dig:**
 dig  is a flexible tool for interrogating DNS name servers. It performs
       DNS lookups and displays the answers that are returned  from  the  name
       server(s)  that  were queried. Most DNS administrators use dig to trou‐
       bleshoot DNS problems because of its  flexibility,  ease  of  use,  and
       clarity  of  output. Other lookup tools tend to have less functionality
       than dig.
```bash
dig www.google.com
```

**route**
Used to view and manipulate routing tables.

**netstat**
Print network connections, routing tables, interface statis‐
       tics, masquerade connections, and multicast memberships
Netstat prints information about the Linux networking  subsystem.   The
       type  of  information  printed  is controlled by the first argument, as
       follows:

# OSI Model:

1. **Physical Layer**
   - **Description**: This is the lowest layer of the OSI model. It deals with the physical connection between devices and the transmission and reception of raw bit streams over a physical medium.
   - **Example**: Cables, switches, and other hardware that transmit and receive data.

2. **Data Link Layer**
   - **Description**: This layer is responsible for node-to-node data transfer and error detection and correction. It ensures that data transferred is free from errors.
   - **Example**: Ethernet, Wi-Fi, MAC addresses.

3. **Network Layer**
   - **Description**: This layer handles the routing and forwarding of data packets. It determines the best path for data to travel from source to destination.
   - **Example**: IP addresses, routers.

4. **Transport Layer**
   - **Description**: This layer ensures that data is transferred completely and correctly between systems. It provides error checking and data flow control.
   - **Example**: TCP (Transmission Control Protocol), UDP (User Datagram Protocol).

5. **Session Layer**
   - **Description**: This layer manages sessions between applications. It establishes, maintains, and terminates connections between applications.
   - **Example**: Remote procedure calls, session management in web applications.

6. **Presentation Layer**
   - **Description**: This layer translates data between the application layer and the network. It handles data encryption, decryption, compression, and translation.
   - **Example**: Data encryption, JPEG image format, ASCII text.

7. **Application Layer**
   - **Description**: This is the topmost layer, closest to the end-user. It provides network services directly to the user’s applications and manages communication between networked applications.
   - **Example**: Web browsers, email clients, FTP (File Transfer Protocol).

Mnemonic to remember the OSI layers from bottom to top: **Please Do Not Throw Sausage Pizza Away** (Physical, Data Link, Network, Transport, Session, Presentation, Application).


## TCP/IP and UDP protocol:

We already know that TCP/IP make sure that each and every packet has sent in a correct sequence. This is done by its three way handshake method. In which it send the request to the reciver and then receiver sends back an acknowledgment response then it sends the sequence number of the data. 

While sending each packet this 3 way handshake has to be done. If receiver do not send an acknowledgment response of receiving the packet then the sender will send the packet again.

on the otherhand UDP do not care about that it sends and receives and do not care about the packet loss.


## Data packets collision avoidance algorithms:


### CSMA/CD (Carrier Sense Multiple Access with Collision Detection)

**Used in:** Wired networks (like Ethernet)

**How it works:**
1. **Carrier Sense:** Before a device sends data, it listens to the network to check if another device is already transmitting. This is like checking if a road is clear before driving.
2. **Multiple Access:** Multiple devices can use the same network. It's like many cars using the same road.
3. **Collision Detection:** While sending data, if the device detects that another device is sending data at the same time (a collision), it stops and waits for a random time before trying again. It's like two cars bumping into each other, stopping, and then deciding to take turns.

### CSMA/CA (Carrier Sense Multiple Access with Collision Avoidance)

**Used in:** Wireless networks (like Wi-Fi)

**How it works:**
1. **Carrier Sense:** Similar to CSMA/CD, a device listens to the network before sending data.
2. **Multiple Access:** Again, multiple devices can use the same network.
3. **Collision Avoidance:** Instead of just listening, the device also waits for a specific time (random backoff time) and sends a small signal (Ready to Send - RTS) to the destination device. If the destination device is ready, it sends back a Clear to Send (CTS) signal. Only then does the device send the actual data. This extra step helps prevent collisions before they happen.

### Key Differences:
- **CSMA/CD** is for wired networks and handles collisions after they happen by detecting them.
- **CSMA/CA** is for wireless networks and tries to avoid collisions before they happen with extra signaling steps.

In essence, CSMA/CD deals with problems after they occur, while CSMA/CA tries to prevent them from happening in the first place.

## Encapsulation and Modualtion in OSI model:
### Encapsulation

**Encapsulation** in the context of the OSI (Open Systems Interconnection) model refers to the process of adding headers (and sometimes trailers) to data as it moves down the layers from the application to the physical layer. Here’s a simple way to understand it:

1. **Application Layer (Layer 7)**: This is where user applications operate (e.g., web browsers, email clients). Data is created here.
2. **Presentation Layer (Layer 6)**: Data is formatted and encrypted here.
3. **Session Layer (Layer 5)**: Manages sessions (connections) between applications.
4. **Transport Layer (Layer 4)**: Adds transport header with information like source and destination ports, and sequence numbers (e.g., TCP/UDP).
5. **Network Layer (Layer 3)**: Adds network header with logical addressing (e.g., IP addresses).
6. **Data Link Layer (Layer 2)**: Adds link layer header and trailer, including physical addressing (e.g., MAC addresses).
7. **Physical Layer (Layer 1)**: Converts data into electrical, optical, or radio signals for transmission.

**Analogy**: Think of encapsulation like mailing a letter. The message is the data. You put it in an envelope (presentation layer), then put that envelope in a larger envelope (session layer), and keep adding layers of packaging (headers) until it’s ready to be sent over the network.

### Modulation

**Modulation** occurs at the Physical Layer (Layer 1) of the OSI model and refers to the process of converting digital data into signals that can be transmitted over physical media like cables or air (for wireless communication).

1. **Modulation Types**: 
   - **Amplitude Modulation (AM)**: Varies the amplitude of the signal.
   - **Frequency Modulation (FM)**: Varies the frequency of the signal.
   - **Phase Modulation (PM)**: Varies the phase of the signal.

**Analogy**: Think of modulation like turning your voice into a radio signal. When you speak into a microphone, your voice (digital data) is converted into radio waves (signals) that can travel through the air and be received by a radio (receiver).

### How Encapsulation and Modulation Fit in the OSI Model:

- **Encapsulation**: Happens as data moves down from Layer 7 (Application) to Layer 1 (Physical). Each layer adds its own header, which contains information necessary for that layer to process the data.
- **Modulation**: Occurs at Layer 1 (Physical) when the fully encapsulated data is converted into signals for transmission over the physical medium.



## Difference between ports and protocols:
### Difference Between Ports and Protocols

**Ports** and **protocols** are both essential concepts in networking, but they serve different purposes. Here’s a simple explanation of each and how they differ:

### Ports

1. **Definition**: 
   - A port is a numerical identifier in the transport layer of the OSI model used to distinguish different services or applications running on a single device.

2. **Purpose**:
   - Ports help direct network traffic to the correct application or service on a device. They act like doors or channels through which data is sent and received.

3. **Types**:
   - **Well-Known Ports** (0-1023): Reserved for common services (e.g., HTTP uses port 80, HTTPS uses port 443, FTP uses port 21).
   - **Registered Ports** (1024-49151): Used by applications or services that are not as widely used.
   - **Dynamic or Private Ports** (49152-65535): Typically used for temporary purposes or by client-side applications.

4. **Analogy**:
   - Think of a port like an extension number in a company’s phone system. The company’s main phone number (IP address) connects you to the building, and the extension number (port) directs your call to the right person or department.

### Protocols

1. **Definition**:
   - A protocol is a set of rules and standards that define how data is transmitted and received over a network.

2. **Purpose**:
   - Protocols ensure that devices on a network can communicate effectively. They define the format, timing, sequencing, and error checking for data transmission.

3. **Examples**:
   - **HTTP (Hypertext Transfer Protocol)**: Used for transferring web pages.
   - **HTTPS (Hypertext Transfer Protocol Secure)**: Secure version of HTTP.
   - **FTP (File Transfer Protocol)**: Used for transferring files.
   - **TCP (Transmission Control Protocol)**: Ensures reliable data transmission.
   - **UDP (User Datagram Protocol)**: Allows faster, but less reliable, data transmission.

4. **Analogy**:
   - Think of a protocol like a language. Just as two people need to speak the same language to understand each other, two devices need to use the same protocol to communicate.

### Key Differences

- **Function**:
  - **Ports** are used to identify specific applications or services on a device, ensuring data reaches the correct destination within the device.
  - **Protocols** are used to define how data is transmitted and received, ensuring devices can understand each other and communicate effectively.

- **Layer in OSI Model**:
  - **Ports** operate at the Transport Layer (Layer 4) of the OSI model.
  - **Protocols** can operate at various layers of the OSI model, including the Application Layer (Layer 7), Transport Layer (Layer 4), Network Layer (Layer 3), and others.

### Summary

- **Ports** are like specific channels or doors through which data enters and exits a device, helping direct traffic to the right application or service.
- **Protocols** are sets of rules that define how data is transmitted and interpreted, ensuring successful communication between devices on a network.

## Common protocols and their assigned ports:
### 1. HTTP (Hypertext Transfer Protocol)
- **Port Number**: 80
- **Function**: Used for transferring web pages and resources on the internet. It's the foundation of data communication for the World Wide Web.

### 2. HTTPS (Hypertext Transfer Protocol Secure)
- **Port Number**: 443
- **Function**: Secure version of HTTP that uses SSL/TLS to encrypt data, providing secure communication over the internet.

### 3. NetBIOS (Network Basic Input/Output System)
- **Port Numbers**: 137 (NetBIOS Name Service), 138 (NetBIOS Datagram Service), 139 (NetBIOS Session Service)
- **Function**: Provides services related to the session layer of the OSI model allowing applications on different computers to communicate within a local network.

### 4. SMTP (Simple Mail Transfer Protocol)
- **Port Number**: 25
- **Function**: Used for sending emails between servers.

### 5. POP3 (Post Office Protocol 3)
- **Port Number**: 110
- **Function**: Used by email clients to retrieve emails from a server. Downloads emails to the client device and usually deletes them from the server.

### 6. IMAP (Internet Message Access Protocol)
- **Port Number**: 143
- **Function**: Used by email clients to retrieve emails from a server. Unlike POP3, it allows multiple devices to access the same mailbox and keeps emails on the server.

### 7. SIP (Session Initiation Protocol)
- **Port Number**: 5060 (unencrypted), 5061 (encrypted)
- **Function**: Used to initiate, maintain, and terminate real-time sessions that include voice, video, and messaging applications.

### 8. RTP (Real-time Transport Protocol)
- **Port Numbers**: Dynamic (commonly 5004 and 5005)
- **Function**: Provides end-to-end network transport functions suitable for applications transmitting real-time data, such as audio, video, or simulation data.

### 9. MGCP (Media Gateway Control Protocol)
- **Port Number**: 2427 (Gateway), 2727 (Call Agent)
- **Function**: Used for controlling media gateways on Internet Protocol (IP) networks and the public switched telephone network (PSTN).

### 10. H.323
- **Port Number**: Dynamic (commonly 1720 for call signaling)
- **Function**: Used for audio, video, and data communication across IP networks such as the Internet.

### 11. FTP (File Transfer Protocol)
- **Port Numbers**: 20 (data transfer), 21 (command/control)
- **Function**: Used for transferring files between a client and a server on a network.

### 12. TFTP (Trivial File Transfer Protocol)
- **Port Number**: 69
- **Function**: Simplified version of FTP that uses UDP and provides basic file transfer functionality without authentication.

### 13. SNMP (Simple Network Management Protocol)
- **Port Numbers**: 161 (agent), 162 (manager)
- **Function**: Used for collecting and organizing information about managed devices on IP networks and for modifying that information to change device behavior.

### 14. Telnet
- **Port Number**: 23
- **Function**: Provides a command-line interface for communication with a remote device or server over a network.

### 15. SSH (Secure Shell)
- **Port Number**: 22
- **Function**: Provides a secure way to access a remote device or server over a network, encrypting the communication.

### 16. DNS (Domain Name System)
- **Port Numbers**: 53
- **Function**: Translates domain names into IP addresses, allowing users to access websites using human-readable addresses.

These protocols and their associated port numbers are fundamental to the functioning of networks and the internet, facilitating various types of communication and data transfer.


# Chapter 03: Virtualization:

# What is Virtualization?

Virtualization is technology that you can use to create virtual representations of servers, storage, networks, and other physical machines. Virtual software mimics the functions of physical hardware to run multiple virtual machines simultaneously on a single physical machine. Businesses use virtualization to use their hardware resources efficiently and get greater returns from their investment. It also powers cloud computing services that help organizations manage infrastructure more efficiently.

# Why is virtualization important?

By using virtualization, you can interact with any hardware resource with greater flexibility. Physical servers consume electricity, take up storage space, and need maintenance. You are often limited by physical proximity and network design if you want to access them. Virtualization removes all these limitations by abstracting physical hardware functionality into software. You can manage, maintain, and use your hardware infrastructure like an application on the web.

# Virtualization example

Consider a company that needs servers for three functions:

1. Store business email securely
2. Run a customer-facing application
3. Run internal business applications

Each of these functions has different configuration requirements:

- The email application requires more storage capacity and a Windows operating system.
- The customer-facing application requires a Linux operating system and high processing power to handle large volumes of website traffic.
- The internal business application requires iOS and more internal memory (RAM).

To meet these requirements, the company sets up three different dedicated physical servers for each application. The company must make a high initial investment and perform ongoing maintenance and upgrades for one machine at a time. The company also cannot optimize its computing capacity. It pays 100% of the servers’ maintenance costs but uses only a fraction of their storage and processing capacities.

### Efficient hardware use

With virtualization, the company creates three digital servers, or virtual machines, on a single physical server. It specifies the operating system requirements for the virtual machines and can use them like the physical servers. However, the company now has less hardware and fewer related expenses.

### Infrastructure as a service

The company can go one step further and use a cloud instance or virtual machine from a cloud computing provider such as AWS. AWS manages all the underlying hardware, and the company can request server resources with varying configurations. All the applications run on these virtual servers without the users noticing any difference. Server management also becomes easier for the company’s IT team.

# What is virtualization?

To properly understand Kernel-based Virtual Machine (KVM), you first need to understand some basic concepts in virtualization. Virtualization is a process that allows a computer to share its hardware resources with multiple digitally separated environments. Each virtualized environment runs within its allocated resources, such as memory, processing power, and storage. With virtualization, organizations can switch between different operating systems on the same server without rebooting.

Virtual machines and hypervisors are two important concepts in virtualization.

### Virtual machine

A virtual machine is a software-defined computer that runs on a physical computer with a separate operating system and computing resources. The physical computer is called the host machine and virtual machines are guest machines. Multiple virtual machines can run on a single physical machine. Virtual machines are abstracted from the computer hardware by a hypervisor.

### Hypervisor

The hypervisor is a software component that manages multiple virtual machines in a computer. It ensures that each virtual machine gets the allocated resources and does not interfere with the operation of other virtual machines. There are two types of hypervisors.

#### Type 1 hypervisor

A type 1 hypervisor, or bare-metal hypervisor, is a hypervisor program installed directly on the computer’s hardware instead of the operating system. Therefore, type 1 hypervisors have better performance and are commonly used by enterprise applications. KVM uses the type 1 hypervisor to host multiple virtual machines on the Linux operating system.

#### Type 2 hypervisor

Also known as a hosted hypervisor, the type 2 hypervisor is installed on an operating system. Type 2 hypervisors are suitable for end-user computing.

# What are the benefits of virtualization?

Virtualization provides several benefits to any organization:

### Efficient resource use

Virtualization improves hardware resources used in your data center. For example, instead of running one server on one computer system, you can create a virtual server pool on the same computer system by using and returning servers to the pool as required. Having fewer underlying physical servers frees up space in your data center and saves money on electricity, generators, and cooling appliances.

### Automated IT management

Now that physical computers are virtual, you can manage them by using software tools. Administrators create deployment and configuration programs to define virtual machine templates. You can duplicate your infrastructure repeatedly and consistently and avoid error-prone manual configurations.

### Faster disaster recovery

When events such as natural disasters or cyberattacks negatively affect business operations, regaining access to IT infrastructure and replacing or fixing a physical server can take hours or even days. By contrast, the process takes minutes with virtualized environments. This prompt response significantly improves resiliency and facilitates business continuity so that operations can continue as scheduled.

# How does virtualization work?

Virtualization uses specialized software, called a hypervisor, to create several cloud instances or virtual machines on one physical computer.

### Cloud instances or virtual machines

After you install virtualization software on your computer, you can create one or more virtual machines. You can access the virtual machines in the same way that you access other applications on your computer. Your computer is called the host, and the virtual machine is called the guest. Several guests can run on the host. Each guest has its own operating system, which can be the same or different from the host operating system.

From the user’s perspective, the virtual machine operates like a typical server. It has settings, configurations, and installed applications. Computing resources, such as central processing units (CPUs), Random Access Memory (RAM), and storage appear the same as on a physical server. You can also configure and update the guest operating systems and their applications as necessary without affecting the host operating system.

### Hypervisors

The hypervisor is the virtualization software that you install on your physical machine. It is a software layer that acts as an intermediary between the virtual machines and the underlying hardware or host operating system. The hypervisor coordinates access to the physical environment so that several virtual machines have access to their own share of physical resources.

For example, if the virtual machine requires computing resources, such as computer processing power, the request first goes to the hypervisor. The hypervisor then passes the request to the underlying hardware, which performs the task.

The following are the two main types of hypervisors.

#### Type 1 hypervisors

A type 1 hypervisor—also called a bare-metal hypervisor—runs directly on the computer hardware. It has some operating system capabilities and is highly efficient because it interacts directly with the physical resources.

#### Type 2 hypervisors

A type 2 hypervisor runs as an application on computer hardware with an existing operating system. Use this type of hypervisor when running multiple operating systems on a single machine.

# What are the different types of virtualization?

You can use virtualization technology to get the functions of many different types of physical infrastructure and all the benefits of a virtualized environment. You can go beyond virtual machines to create a collection of virtual resources in your virtual environment.

### Server virtualization

Server virtualization is a process that partitions a physical server into multiple virtual servers. It is an efficient and cost-effective way to use server resources and deploy IT services in an organization. Without server virtualization, physical servers use only a small amount of their processing capacities, which leave devices idle.

### Storage virtualization

Storage virtualization combines the functions of physical storage devices such as network attached storage (NAS) and storage area network (SAN). You can pool the storage hardware in your data center, even if it is from different vendors or of different types. Storage virtualization uses all your physical data storage and creates a large unit of virtual storage that you can assign and control by using management software. IT administrators can streamline storage activities, such as archiving, backup, and recovery, because they can combine multiple network storage devices virtually into a single storage device.

### Network virtualization

Any computer network has hardware elements such as switches, routers, and firewalls. An organization with offices in multiple geographic locations can have several different network technologies working together to create its enterprise network. Network virtualization is a process that combines all of these network resources to centralize administrative tasks. Administrators can adjust and control these elements virtually without touching the physical components, which greatly simplifies network management.

The following are two approaches to network virtualization.

#### Software-defined networking

Software-defined networking (SDN) controls traffic routing by taking over routing management from data routing in the physical environment. For example, you can program your system to prioritize your video call traffic over application traffic to ensure consistent call quality in all online meetings.

#### Network function virtualization

Network function virtualization technology combines the functions of network appliances, such as firewalls, load balancers, and traffic analyzers that work together, to improve network performance.

### Data virtualization

Modern organizations collect data from several sources and store it in different formats. They might also store data in different places, such as in a cloud infrastructure and an on-premises data center. Data virtualization creates a software layer between this data and the applications that need it. Data virtualization tools process an application’s data request and return results in a suitable format. Thus, organizations use data virtualization solutions to increase flexibility for data integration and support cross-functional data analysis.

### Application virtualization

Application virtualization pulls out the functions of applications to run on operating systems other than the operating systems for which they were designed. For example, users can run a Microsoft Windows application on a Linux machine without changing the machine configuration. To achieve application virtualization, follow these practices:

- **Application streaming** – Users stream the application from a remote server, so it runs only on the end user's device when needed.
- **Server-based application virtualization** – Users can access the remote application from their browser or client interface without installing it.
- **Local application virtualization** – The application code is shipped


### Desktop Virtualization Explained in Simple Terms

Desktop virtualization is a technology that allows you to run different desktop operating systems (like Windows, Linux, or MacOS) on a single physical computer or from a remote server. Here's an easy way to understand it:

#### Imagine Your Computer is a Building

1. **Your Physical Computer is a Building**: Think of your physical computer as a building with many rooms.
2. **Virtual Desktops are the Rooms**: Each room in the building can be set up differently. One room might have a Windows setup, another might have a Linux setup, and so on.
3. **Virtualization Software is the Architect**: This software designs and manages these rooms, making sure each one runs smoothly without interfering with the others.

#### Types of Desktop Virtualization

1. **Local Desktop Virtualization**:
   - **How It Works**: You create virtual desktops (rooms) directly on your physical computer (building).
   - **Example**: You might have a Windows virtual desktop running on your Mac computer. You can switch between your Mac and Windows environments as if you’re moving between different rooms in the same building.

2. **Virtual Desktop Infrastructure (VDI)**:
   - **How It Works**: The virtual desktops are hosted on a remote server (a separate, large building), and you access them via your local device.
   - **Example**: Your company provides you with a virtual desktop that you can access from your home computer. The virtual desktop looks and feels like your work computer, but it's actually running on a server in your company's data center.

#### Benefits of Desktop Virtualization

1. **Flexibility**: Run different operating systems and applications on the same physical computer without needing separate hardware.
2. **Cost Savings**: Save money by reducing the need for multiple physical computers. Virtual desktops can share the same hardware resources.
3. **Easy Management**: IT administrators can easily manage and update virtual desktops from a central location, reducing the time and effort needed for maintenance.
4. **Remote Access**: Users can access their virtual desktops from anywhere, making remote work and collaboration easier.

#### Simple Example

- **Scenario**: You have a team of designers, developers, and customer service agents.
- **Solution with Desktop Virtualization**:
  - Designers get a virtual desktop with powerful graphics software on a Windows setup.
  - Developers get a virtual desktop with a Linux setup and development tools.
  - Customer service agents get a virtual desktop with basic software on a Windows setup.

All these virtual desktops can run on a single physical server, and each team member can access their specific virtual desktop from any device, anywhere.

# Chapter Jenkins:


Think jenkins as person who have a PC. You will provide your Source code to him. He will run commands on it that you will provide to it either in YAML or GROOVY format (those files would called pipelines). 

# Installation
Here we are using jenkins Image and will be running it in a docker container. Therefore, we are first building the Jenkins Image. It is a good practice to run jenkins in a container. By running it into a container is same as running jenkins in another PC and all your projects and pipline scripts will be run in that container. Therefore, you first have to setup and install all packages in container before running the project.

## STEP 1: Create a Dockerfile:
To build the image we will be needed a Docker file which you can create and paste the following content in it:

```bash
FROM jenkins/jenkins:2.414.2-jdk11
USER root
RUN apt-get update && apt-get install -y lsb-release python3-pip
RUN curl -fsSLo /usr/share/keyrings/docker-archive-keyring.asc \
  https://download.docker.com/linux/debian/gpg
RUN echo "deb [arch=$(dpkg --print-architecture) \
  signed-by=/usr/share/keyrings/docker-archive-keyring.asc] \
  https://download.docker.com/linux/debian \
  $(lsb_release -cs) stable" > /etc/apt/sources.list.d/docker.list
RUN apt-get update && apt-get install -y docker-ce-cli
USER jenkins
RUN jenkins-plugin-cli --plugins "blueocean:1.25.3 docker-workflow:1.28"
```

## STEP 2: Build the Jenkins BlueOcean Docker Image (or pull and use the one I built)
```
docker build -t myjenkins-blueocean:2.414.2 .

#IF you are having problems building the image yourself, you can pull from my registry (It is version 2.332.3-1 though, the original from the video)

docker pull devopsjourney1/jenkins-blueocean:2.332.3-1 && docker tag devopsjourney1/jenkins-blueocean:2.332.3-1 myjenkins-blueocean:2.332.3-1
```

## STEP 3: Create the network 'jenkins'
```
docker network create jenkins
```

## STEP 4: Run the Container
### MacOS / Linux
```
docker run --name jenkins-blueocean --restart=on-failure --detach \
  --network jenkins --env DOCKER_HOST=tcp://docker:2376 \
  --env DOCKER_CERT_PATH=/certs/client --env DOCKER_TLS_VERIFY=1 \
  --publish 8080:8080 --publish 50000:50000 \
  --volume jenkins-data:/var/jenkins_home \
  --volume jenkins-docker-certs:/certs/client:ro \
  myjenkins-blueocean:2.414.2
```

### Windows
```
docker run --name jenkins-blueocean --restart=on-failure --detach `
  --network jenkins --env DOCKER_HOST=tcp://docker:2376 `
  --env DOCKER_CERT_PATH=/certs/client --env DOCKER_TLS_VERIFY=1 `
  --volume jenkins-data:/var/jenkins_home `
  --volume jenkins-docker-certs:/certs/client:ro `
  --publish 8080:8080 --publish 50000:50000 myjenkins-blueocean:2.414.2
```


## Get the Password
```
docker exec jenkins-blueocean cat /var/jenkins_home/secrets/initialAdminPassword
```

## STEP 5: Connect to the Jenkins
```
https://localhost:8080/
```

## Installation Reference:
https://www.jenkins.io/doc/book/installing/docker/

# Practice Task 1: Running scripts in Jenkins:
Go to the dashboard > items > new items > free style projects

create a free style project and simply give it a script and click on build now. Here you will know how jenkins can run scripts etc.

All things are self descripting you just have to check some point and have to provide some information. 

![image](https://github.com/user-attachments/assets/a3049139-63fe-44f5-b52c-86e9b63fed36)

![image](https://github.com/user-attachments/assets/d1114e5d-e422-4e2e-86f3-6c2225c33efb)




# Practice Task 2: Running Python scripts from a git repo in Jenkins:

Provide the link of git repo
provide credentials if repo is private.

and again run the script.

![image](https://github.com/user-attachments/assets/4bfbba65-b055-4852-a158-43114f239ec8)

![image](https://github.com/user-attachments/assets/36a2bbf1-51b8-4ef5-b2c0-2a22401c637b)



**NOTE:** Remember! The script you are running are getting run in our container in which we are running our Jenkins image. So to run python or any other package you must have to make sure that all dependencies are setup in that container. It is same as setting a setup of tech stacks like installing python etc. before building  or running the project. So don't forget to check that. Here is how you can go into your container and install you require dependencies:

```bash
sudo docker ps -a // check currently running container and copy the name of your container

sudo docker exec -it container_name bash

// now you are in your container:

pip install packageName

// do whatever you want here to run your project


```

**NOTE:** /var/jenkins_home/workspace   this directory path in jenkins container where all your project files (freestyle, pipelines) reside. You can have access them from this directory.


# Practice task 3: Running python script from repo in a Docker cloud using Jenkins cloud agent:
Here think cloud agent as another 3rd PC in which you will be testing, running and building your scripts. 

Since we are running jenkins in a container here our cloud will also be running in another container. So there would be total 2 containers. One that will be running jenkins and other will running scripts on our project. 
### So how would container 1 that is jenkins container will communicate with container 2?
So the answer is that we will forward traffic from jenkins container to our cloud container. Here is how:


## alpine/socat container to forward traffic from Jenkins to Docker Desktop on Host Machine

https://stackoverflow.com/questions/47709208/how-to-find-docker-host-uri-to-be-used-in-jenkins-docker-plugin
```
docker run -d --restart=always -p 127.0.0.1:2376:2375 --network jenkins -v /var/run/docker.sock:/var/run/docker.sock alpine/socat tcp-listen:2375,fork,reuseaddr unix-connect:/var/run/docker.sock
docker inspect <container_id>
copy the ip address and export port (2375)
```

## Using my Jenkins Python Agent
```
docker pull devopsjourney1/myjenkinsagents:python
```

So you will get tcp://172.19.0.2:2375

# How to create a jenkins cloud agent
Now go to dashboard > manage Jenkins > Cloud > add cloud 

here I will be using Docker cloud so simply check the docker and then it will asking you for cloud details.

so in Docker Host URI you have to enter: e.g tcp://172.19.0.2:2375 (enter whatever IP of you running docker container will be that is container 2)

Enable it.
test connection.

Now create a docker agent template:
![image](https://github.com/user-attachments/assets/324a9de0-5e37-4439-a74f-78fd29402cae)

![image](https://github.com/user-attachments/assets/59549f4e-b07f-418c-9516-91a3343177ac)

![image](https://github.com/user-attachments/assets/3a638e44-ccc4-4ae9-a1f1-bd780c98e90d)


Now Your Jenkins cloud agent is ready. Now you can use this cloud agent to run your scripts, your projects etc.

# Run Python script in the above create cloud:
simple open you free style project and click on configure and check the 'Restrict where this project can be run?' and add label of whatever you want.

![image](https://github.com/user-attachments/assets/e2aff240-992b-4559-a2be-eea3a288442e)


Now simply run your script in the script tag.


# Practice Task 4: Running Jenkins pipeline on git repo using genkins cloud agent:

Go to the dashboard > add item > pipeline 

provide your repo

Now in script tag you have to either give GROOVY or YAML:

Groovy script:

```bash
pipeline {
    agent { 
        node {
            label 'my_first_jenkins_docker_cloud_agent' // here your cloud label will go
            }
      }
    stages {
        stage('Build') {
            steps {
                echo "Building.."
                sh '''
                echo "doing build stuff.."
                '''
            }
        }
        stage('Test') {
            steps {
                echo "Testing.."
                sh '''
                echo "doing test stuff.."
                '''
            }
        }
        stage('Deliver') {
            steps {
                echo 'Deliver....'
                sh '''
                echo "doing delivery stuff.."
                '''
            }
        }
    }
}
```

**NOTE:** The good practice is that you should provide a pipeline file that will be in your git repo instead of providing the hard coded pipeline in the script section.

To provide the file you have to select:

'Pipeline script from SCM' SCM means source control management

then provide git repo link.

## auto-trigger feature on jenkins
**NOTE:** If you want to run you commands on push your code to git. Then look for PollSCM and provide the time there. This would be the after which pipeline will be trigger again on pushing the code to repo.

If you want to give 5 min timer then you have that like this: */5 * * * *


# Jenkins Deploying a full stack web app using Linode, Jenkins, Docker and Blue Ocean:
Here we are going to use two servers one for Docker which will be running our Image of our application and other server would be running Jenkins that would be watching to our repo of our project. In case of any changes detected then Jenkins will run jobs (job will include running a pipeline of test, build and pushing updated image to docker hub)
Below is the architecture diagram:

![jenkins_architecture_balsamiq_diagram2](https://user-images.githubusercontent.com/10039233/190653544-48ea7cb1-bde8-4bf6-97b8-c1ff5bf854d2.png)

# Step 1: Create a Linode account and create two servers:
Here servers are nothing but are machines that will have CPU, RAM and OS.
Setup jenkins in one server and setup Docker in other server.
Make sure to install required dependencies in the servers such as Node, npm and git etc. By using SSH. (You will get SSH IP to get access to the terminal of the server where you can run commands to install dependencies)

# Setting up jenkins Server:
Install Docker, Docker Hub, Git and Blue Ocean (Blue Ocean is a modern UI to create CI/CD pipelines. It will also provide a UI to write CI/CD pipeline script without writing the code) Plugins by going into 'Manage Jenkins section'

Now Go to the dashboard you will see Blue Ocean Section go into that and give your repo link and repo access token and then create pipeline. In add step button search for git and then add step. This will create a 'jenkinsfile' in your repo that will contain all your pipeline code.

# Updating the pipeline:
till now you have create a jenkinsfile in your repo, you have created two servers. We are currently working in jenkins server.

The first stage of our Pipeline is called log and it will run the following command
```bash
ls -la
```
second stage would be the test stage and will run the following command:
```bash
cd you_app_repo_name && npm i && npm run test:unit
```

third stage would be the build step. This will create a docker image:
```bash
docker build -f curriculum-front/Dockerfile . -t fuze365/curriculum-front
```
4th step is to login into your Docker account so that you can push this updated image to your Docker hub account.

```bash
docker login -u $DOCKERHUB_USER -p $DOCKERHUB_PASSWORD
```

5th stage is to push the image to the docker hub:
```bash
docker push you_docker_hub:latest
```

# what we have done?
We have deployed the app to Dockerhub and have the app server watch for changes to the docker image. It will pull whenever there are changes. (this is what we have set up now)
