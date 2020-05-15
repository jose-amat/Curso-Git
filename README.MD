GIT
===

## Help

### General
	git help
	
### A specific command
	git help <qualquer_comando_git>

	example:
	git help commit
	

## Configuration

### Set a user
	git config --global user.name <username>

#### Example:
	git config --global user.name jose.amat

### Set an email
	git config --global user.email <user-email>

#### Example:
	git config --global user.email jose.alc.luis@gmail.com

### List settings
	git config --list


Local Repository
================

### Create a new repository

	git init

### Check file/directory status

	git status

### Add file/directory to staged area

#### Add an specific file

	git add <my-file.extension>

#### Add an specific directory

	git add <directory>

#### Add all files/directories
	
	git add .	
	
	
### Commit a file/directory

#### Commit a file
	
	git commit <my-file.extension>

#### Commit multiple files

	git commit <my-file-1.extension> <filename-2.extension>
	
#### Commit with a message

	git commit <my-file.extension> -m "my commit message"

#### Accessing a commit

    git checkout <commit-id>

### Remove a File/Directory

#### Remove a file

	git rm <my-file.extension>

#### Remove a directory

	git rm -r <directory>

### View Commit History

#### View the history
	
	git log
	
#### View a particular author's story

	git log --author=<username>




Remote Repository
=================

### View remote repositories

	git remote
	
### View remote repositories address (URL)	
	git remote -v

### Link local repository with a remote repository

	git remote add <repository-name> <remote-repository>

#### Example:
	git remote add origin git@github.com:jose-amat/Curso-Git.git

### View information from remote repositories

	git remote show <repository-name>
	
### Rename a remote repository 

	git remote rename <old-repository-name> <new-repository-name>
	
### Unlink a remote repository
	
	git remote rm <repository-name>

### Send files/directories to remote repository

The first ``push`` of a repository is:
	
	git push -u <repository-name> <branch-name>

#### Example: 
	git push -u origin master
	
The other ``pushes`` do not need this information

	git push
	

### Update local repository according to remote repository

#### Update files in the current branch

	git pull
	
#### Search for changes, but do not apply them to the current branch

	git fetch
	
### Clone an existing remote repository

	git clone git@github.com:jose-amat/Curso-Git.git
	
	
### Branches

The ``master`` is the main branch of GIT.

The ``HEAD`` is a special pointer that indicates which ``branch`` is current. By default, ``HEAD`` points to the main branch, the ``master``.

#### Creating a new branch

	git branch <new-branch>
	
#### Switching to an existing branch

	git checkout <branch-name>
	
In this case, the main pointer ``HEAD`` is pointing to the branch called bug-123.

#### Create a new branch and switch

	git checkout -b <new-branch>
	
#### Back to the main branch (master)

	git checkout master
	