# Git Instruction   

## Introduction

Git is a fast distributed revision control system. It allows software developers to cooperate in their work and use siple commands to share their work results with co-workers.

You can always use 
> **git --help** to get the list of the commands, but lets talk about the workflow.
## 1. Initialize git repository

To initialize a new git repository create a new folder, enter a commandline in this folder and call **_git init_** command.
This will create a hidden _.git_ folder with multiple usefull files inside.

## 2. Adding changes to your project

After adding some file changes in your project  (creating files with some text inside) you are ready to make your first commit.
for that purpose you will need two more commands:

* **_git add_**
* **_git commit_**

> git add _filename_
Selects the files to commit, using _-A_ key after command allows to add all files to commit
> git commit 
adds a new coomit cord to your work log
Amonk multiple additional keys one of the most important is _-m_, which adds a commit message, which is essential for understanding which changes were made.

more advanced _-am_flag allows to combine _git add -a_ into _git commit_ command and use only one instead of two.

## 3. Repository status ang work log

> git status

a usefull commang to get repository status with list of modfied files.

> git log

shows the actual repository log with all commits

## 4. Branches

Branches are usefull for adding some changes to existing project without a possibility to break it.
The main branch of the project is called **_master_**. Other branches usually named after the expected modifications, taskID, etc.
a new branch creates a copy of the actual master (or trunk).

A single command with various keys and options is used for working with branches:
> git branch
without arguments chows the list of available branches

> git branch _name_
creates a new branch. Sending this command with_-D_ key before branch name removes this branch (e.g _git branch -D uselessbranch_)

## 5. Moving between branches
after a branch is created you need jump to it (or _checkout_ it to your workspace). For that purpose you need to use 

> git checkout _branch_name_
after that you are ready to make more changes that will not affect "main" code.

_**DO NOT FORGET to save files, add them to commit and commit!!!**_

_This will save you much time :)_


## 6. Adding changes to MASTER

After the changes in separate branch are made and you are sure they are ok you need to add them to your "main".

For that purpose you need to jump back to trunk using _git checkout master_ commang and then call 

> git merge _branch.name_

Git is smart so it will try to merge the changes without your help.
This works well when there are no conflicts between the branches.
If the conflicts occur you will need to merge the changes manually. Git extensin for VSCode allows you no make it easy and fast.

_**DO NOT FORGET to save files, add them to commit and commit!!!**_

_This will save you much time :)_

## 7. Working with remote repo
As a first step you need to create an account on some cloud-based git sevice, e.g. [GitHub](https://github.com).
It contains thousands of user repos from all over the world.

Basically you can download contens of someone's repository from github or any other remote repository. But working with remote repo has it's specific rules. You can't just commit and push your changes to someone's repoitory. 

At first you need to login into git and fork a repository. This will create a copy of the user's repository within your github account. Ater that you can start working with it.
Fork sign looks like this: ![fork](img/fork.jpg)

After forking a repository you can clone forked repository (not the original one) to your pc and start working with it:

 > git clone \<repository url>

 after that you can branch the repository using _git branch \<branch.name>_ 
 _git checkout_ new branch and make some changes

 After that you can make and commit the changes you have made.

 You can send the local changes to remote repository by using 
> git push

You can also update your local repository with uptodate from remote repository changes using 
> git pull

This command is very usefull when several developers wor with the same project.
