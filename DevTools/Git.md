# Git Notes
### what's Git?
>Git is a distributed **version control** system designed to *handle everything* from small to very large projects with speed and efficiency
Official webpage of [Git](https://git-scm.com)

### Git Usages
* History (Versions)
* Code storage
* Teamwork
* Monitoring projects

## Setting up Git
Display the installed **version** of Git:
``` 
git --version 
``` 
also verifies the correct install of Git

Going to the ***user configuration***,
```
git config --global user.name "john doe"
git config --global user.email "johndoe@example.com"
```
where `--global` is an argument so the setting remains in the whole system and not only in the current project. In addition accessing to the object **user**. 

Setting VS Code as main editor
``` 
git config --global core.editor "code --wait"
```
The argument `--wait` makes the terminal waiting till the VS Code window is closed

To show the configuration file:
```
git config --global -e
```
Configurationr for compability between Windows and linux/mac
```
git config --global core.autocrlf true/input
```
Use `true` if is a windows user and `input` if is a linux/mac user. [More Info](https://youtu.be/VdGzPZ31ts8?t=764)

---
___

## WORKFLOW 
### **1. Local**
On this stage is where the programmer creates, modify or delete files. All these changes remain on the local area.
With `git add` moves a file into the staging area.

### **2. Stage**
Is used as a filter to verify the files and changes to go to the server. With `git commit` pack all the changes and send it to the commit stage. 

### **3. Commit**
Are the packages of changes that are going to the server/repository. This can be accomplished with the command `git push`

### **4. Server**
Is where all the coude is kept, also know as repository. 

[more info](https://youtu.be/VdGzPZ31ts8?t=1461)

---
___

## Commands 
### Terminal Commands
|  Command  | Arguments | Action |
| :---: |:---|:---: |
| `ls`  | [ option ]    |list all the directories in the current path |
| `pwd` |     |return the current path |
| `cd`  | [ directory ] |change the current directory |
| `mkdir` | [ name ] | creates a new folder in the path |
| `rmdir` | [ option, name ] |removes a folder of the path |
| `rm` | [ option, name ] |removes a file of the path |
| `mv` | [ name, new file ] | moves or rename a file of the path |


### Git commands
Initialize a new project
```
git init
```
**Note**: it's importat to be in the correct folder to initialize the project

Shows the current state of the repository, additions, modifications, etc.
```
git status
```
Untracked files are those ones which are new

Adds a file to the staging area
```
git add <file>
```
It is possible to add all files at once with `git add .`, although it is considered a bad practice. Adding more that one file can be performed spliting the files with commas

Commits all the changes in the staging stage
```
git commit -m "this is a message"
```
With `-m` is added a message to describe the commit, without this argument, git opens a new window in **VS Code** to introduce the message manualy

Returning files from the staging stage
```
git restore --staged <file>
```
Removing the argument `--staged` will discard all changes in the file

you can add `git` to the terminal commands to safe time in the command line, for example: 
```
git rm <file>
git mv <file> <new file>
```
Use `git rm` to remove a file and send it to the staging area, and `git mv` to rename or move a file

Show the differences with the last commit to the actual files
```
git diff 
```

Displays the history of commits of the repository
```
git log
```
add the argument `--oneline` to make the return more compressed


## Git Ignore
it is a file `.gitignore` located in the main folder, which gives to git instructions of which files should be ignored



## References
Youtube channel [Hola Mundo](https://www.youtube.com/watch?v=VdGzPZ31ts8)