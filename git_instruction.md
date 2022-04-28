![Git-logo](gitlogo.png)
# Work with GIT
## 1. Check Git install status
In terminal insert: `git version`

If **Git** is installed, you will see a message window with programme version. 
If not, an '`error`' message will be displayed.
## 2. Install Git
Upload the last **Git** version from https://git-scm.com/download

Install with default settings
## 3. Git settings
During a first use of **Git**, you need to log in to the system. Enter 2 commands:
```
git config --global user.name «Your name»

git config --global user.email "Your e-mail"
```
## 4. Initialise repository
In terminal go to folder where you want to create a repository. Enter command `git init`.

In source folder you will see a hidden folder *.git*.  
## 5. Record changes in repository
Each file in working folder can have two version controls - tracked and untracked. Tracked files can be unchanged, changed or ready to commit. 

To see a file status in repository you need to enter a command: 
```
git status
```
To start tracking a new file use a command: 
```
git add <file name its extension>
```
It is a multifunctional command used to add new files for version control, to prepare to fix changes.  
To fix changes use a command:
```
git commit -m "commit name - enter description of changes made in file"
```
To see a difference between a current folder and the last commit enter a command: 
```
git diff
```
## 6. Review commits history
To review commits history use a command
```
git log
````
This command lists commits with hash code, name and e-mail of originator, cretion date and commit message. 
By default, the last commits are placed in the upper part.  
To quit from  history review mode use a key button "q". 
## 7. Move between commits
To switch between commits use a command:
```
git checkout <A name of the commit>
````
## 8. Ignore files
To remove from tracking definite files or folder in repository, need to create a file ***.gitignore*** and include there its name. 
## 9. Create branches in Git
Branch is a simple move between branches. 
By default, a name of basic branch in Git is a "*master*".

A branch can be created by command:
```
git branch <A name of a new branch>
```
A new indicator to the current commit is created.
Use a command `git branch` to see a list of branches in repository. 

To switch between branches use a command:
```
git checkout <A name of the branch>
```
To move directly to the branch during its creation you can use commands:
```
git checkout -b <A name of the new branch>
```
or
```
git switch -c <A name of the new branch>
```
## 10. Merge branches and resolve conflicts
To merge a selected branch with the current one enter a command:

    git merge <A name of selected branch>

If the same part of file was changed in two branches, it can cause a conflict of branches which can be resolved by a user. Git will propose resolve options.
```
git merge <A name of selected branch>
```
If the same part of file was changed in two branches, it can cause a conflict of branches which can be resolved by a user. 
Git will propose resolve options.

To resolve a conflict need to select one of the options or to merge the content. 
## 11. Delete branches
After merge the non-required branch can be deleted by command: 
```
git branch -d <A name of the branch> 
```
## 12. Ignore files
To hide files and folders in **Git** use a command:
```
.gitignore
```
This function is used to hide configured files (especially containing passwords), temporary files and folders. 
## 13. Work with remoted repository
Created commits are stored in repository linked to the specified folder in our computer, they are called local. But if you need to open an access to the file or send a code to the server you need to connect to the remoted repository. To link a local repository with the remoted, enter a command:
```
git remote add origin <URI-address>
```
Now we can send a commit to the server as we connected to the remoted repository by entering a command:
 ```
 git push origin <A name of the branch>
 ```
If a user needs to clone a remoted repository, a command *clone* is used:
 ```
 git clone <URI-address>
 ```
 If a user needs to get an information on changes made, he uses a command:
 ```
 git pull origin "A name of the branch"
 ```
