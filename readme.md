# Git & GitHub Crash Course with extension
* https://www.youtube.com/watch?v=SWYqp7iY_Tc
* https://www.youtube.com/watch?v=ugN-IYV1NTM

## Basic Commands 

### Local Commands 
```
git init
git add <file>
git status
git commit
```

### Network Commands
```
git push
git pull
git clone
```

```
$ git --version
git version 2.18.0.windows.1
```

--- Git Bash Here ??? 

```
git init 
```


### Show hidden folders in VSCode tree UserSettings
```
"files.exclude": {
     "**/.git": false
}
```

#### SOME VS CODE shortcuts 

- VS CODE > CTRL+P - file open
- VS CODE > CTRL+D select next Multi cursor
- VS CODE > CTRL+K & CTRL+D  --- CTRL+ALT+UP/DOWN


### Basic commands flow 

* Adding Email and Address To Config
```
git config --global user.name 'Mark Pet'
git config --global user.email 'me@test.com'

q - to get out from help mode 

git config --list
```

* add single file 
```
git add index.html
```

* remove from staging area
```
git rm --cached index.html
```

* add all with type
``` 
git add *.html
```
* add all
```
git add .
```

* Commit Changes to Repository 
```
git commit -a -m 'Initial Commit'
```

* Ignoring files is with 
```
.gitignore 
```

* -m message for Commit
```
git commit -m 'New change '
```

### Branching 

* create branch
```
git branch login
```

* Quick create empty file
```
touch login.html
```

* Switch to LOGIN branch
```
git checkout login

touch login.html
git add .
git commit -m 'Loging Form in Login branch'
git status
```

* Upon return to MASTER branch login.html file is gone!
```
git checkout master
```

* Merge to obtain login branch and login.html file  
```
git merge --message 'AddedLogin' login
```

### LOGs
* to see all changes and commits
```
git log 
```

* shortened only names and hashes in one line
```
git log --pretty=oneline
git log --pretty=format:"%h - %an, %ar : %s"
git log --pretty=format:"%h %s" --graph
git log --since=2.weeks
git log -S function_name
```

* [Amend changes to last commit](https://medium.com/@igor_marques/git-basics-adding-more-changes-to-your-last-commit-1629344cb9a8)
```
git commit --amend    >>> i or :wq or :q
git commit --amend --no-edit
```


### Remoting to GitHub and push changes
```
git remote
git remote add origin https://github.com/oodboo/Git-lectures.git
git remote
git push -u origin master
```


### Deleting GitHub Repository

--> Your project --> Settings Tab --> "Danger Zone" (Botom of the Page) --> [Delete This Repository]
 

### Fixhing with forcing the push
 >   ! [rejected]        master -> master (non-fast-forward)
 >   error: failed to push some refs to 'https://github.com/oodboo/Git-lectures.git'
 >   hint: Updates were rejected because a pushed branch tip is behind its remote
 >   hint: counterpart. Check out this branch and integrate the remote changes
 >   hint: (e.g. 'git pull ...') before pushing again.
 >   hint: See the 'Note about fast-forwards' in 'git push --help' for details.
 >> https://stackoverflow.com/questions/10298291/cannot-push-to-github-keeps-saying-need-merge

```
git push -f origin master
```
