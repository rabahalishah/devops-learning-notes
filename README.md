# linux_guide
How to install Zsh and configure its themes
--> https://phoenixnap.com/kb/install-zsh-ubuntu

My Theme: Steeef
```bash
echo $PATH //This command is used to check which directory is used for executables files (Env variables)
```
**NOTE**: Any file that start with . is a hidden file. To see hidden files we can do
```bash
ls -a
```
```bash
vi path_to_file // this command is used to edit the file
```
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

here - r is for recursive
```bash
touch fileName //this command will be used to create a filef
```

```bash
## merging the content of two files in a new single file
```bash
cat hello.txt hello2.txt > myNewFile.txt (this command will be used to read all the content of hello.txt)
```

```bash
cp textfile.txt newTextFile.txt
```


**TIP**: Ctrl + X for exiting the file and Ctrl + S for saving the file
