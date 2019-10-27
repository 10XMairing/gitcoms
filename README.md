### Common Linux Bash Commands

	
| command | description  |
|--|--|
| `cd dirname` | go to dirname in current directory  |
| `cd ./dirname` | go to dirname in current directory |
|`cd ..`|go back one level down (back)|
|`cd ../dirname`|go to dirname on level down(back)|
|`touch {filename.extension}`| create file with name.ext eg:: `touch index.html`|
|`rm filename.extension`| remove file with given name|
|`rm *`| remove all files in current directory|
|`rm -rf foldername`| remove folder|
|`mv fromDir toDir` |move folder fromDir to toDir, can also be used for renaming files and folders |
|`cp fromDir toDir`| copy files |
|`ls `|list files and folders in your current dir|
|`ls -a`|list all files including *hidden* files : in linux hidden files/folders start with a dot eg `.file`|
|`pwd`|show current working dir|

`.gitignore` This is not a command -- this is a *hidden* file(starts with a dot) where the names of all the files should be stored which you want to ignore in your commits and hence it is ignored and not recorded, pushed , or pulled eg : `node_modules` . this file should be in the same dir as your `.git` folder


*make sure you set your config settings before trying to use git*

## Configuration settings

`git config --global user.name "your username"`

`git config --global user.email "youremail@domain.com"`

``git config --global http.proxy http://proxyUsername:proxyPassword@proxy.server.com:port``

`git config --global http.proxy https://proxyUsername:proxyPassword@proxy.server.com:port`

`git config --list --global`  to list your current global settings

**This config is usually stored in your home folder in a hidden file called `.gitconfig` You can manually edit this file to change config. If you are using college proxy and want to remove it for some reason set proxy as an empty string `""` if you dont your proxy might still be active**


### Common git commands

| command     | description|
| --      | -- |
| `git init `| initialize a git repository in the current directory: **important**  it creates a hidden folder called `.git` in your working dir and this is where all your commit logs will be saved. all your commits will be deleted if u deleted this folder | 
|`git add filename`        | set a file as ready for commit |
|`git add .`|set all files in current dir as ready for commit|
|`git commit -m "any message here"`| commit the current state of files in the logs.This means that your current state of files has been recorded |
|`git status`|check your current status of files and your branch , uncommited files etc|
|`git log`|check your commit history *partial*|
|`git checkout commitid/branchname`|go back to a certain commit with id `commitid` or branch `branchname`|
|`git reflog`|check your *overall* commit history|
|`git remote add origin https://yourremoteorign/username/projectname`|adds your remote repository addresss locally for easy access - ``origin`` is the name of the variable where this addr is stored. it can be any name like origin2, hub etc|
|`git remote remove originName`|remove remote will name `originName`|
|`git remote -v`|list all your locally stored remote names and their address|
|`git branch `| list your branches : your current branch is marked in green : your default branch is called ***master***|
|`git branch Test`| create a new branch called Test : your current branch will be cloned to Test|
|`git merge Test` while in *master*| pull changes from Test branch and commit in master|
|`git branch -D Test`| Delete test branch|
|`git push origin master`|push all your commits to your remote repository `origin` in branch `master`|
|`git pull origin master`|fetch and merge all your changes in your remote `origin` from branch `master`|
|`git revert commitid`|undo a commit|
|`git reset commitid`|go back to a previous commit|








