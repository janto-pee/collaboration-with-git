Git is a Version Control System. A version control system is a software designed to record changes within one or more files over time. 
When developers work on a project, different files are created and changes are continuously made to parts of the code. As project grow, some of the codes result in conflict. Git enables us to rollback, revert or cancel pending changes within one or more file. Git also enables us compare the changes made to the different versions of a project. Having understood the importance of git, let's dive in

### Installation
If you don't have git already installed on your machine, you can download the latest version from git-scm website https://git-scm.com according to the version of your operating system - Windows, Mac or Linux.
if you're running a windows operating system, download the windows vesion and go to DOWNLOAD folder in file explorer.
Now double click to install and follow the prompt. once installed, lets proceed to setup.

### Configuration
You can confirm if you correctly installed git with the `git --version` On confirmation, let's proceed to configure our name and email.
```
git config --global user.name "ayobami adejumo"
git config --global user.email "aayo.software@gmail.com"
#check this 
git config --global --list
```
### Getting Started
To learn the basic git commands by practice, lets open an empty folder in a text editor such as vscode. 
Open the vscode terminal and Initialize a git repo in the current working directory with
`git init`

`git clone https://github...`
git downloads a project from a remote repository.

`git status`
displays the state the working directory. List the files which are staged, unstaged or untracked.

`git add filename`
Add file to the staging area

`git add .`
recursive add lets you add all untracked files in the working directory to the staging area.

`git commit -m "enter your commit message here"`
Create a new commit from changes added to the staging area. The commit must have a message!

`$ git rm [filename]`
Remove file from working directory and staging area.


### Reviewing Commit History

`$ git log`
List commit history of current branch.

`$ git log --oneline --graph --decorate`
An overview with reference labels and history graph. One commit
per line.

`$ git log ref..`
List commits that are present on the current branch and not merged
into ref. A ref can be a branch name or a tag name.

`$ git show commit-id`
List commit that are present on ref and not merged into current
branch.

`git diff`
show changes between working directory and staging area. This helps you compare the various changes you've made to code.

`git diff --staged [file]`
Shows any changes between the staging area and the repository.


### Revert or Undo Changes

`git checkout [filename]`
Discard changes in working directory. This operation is unrecoverable.

`git reset commit-id`
Revert your repository to a previous known working state.

`git revert HEAD`
#Revert your repository to a previous known working state.

`git revert commit-id`
#Revert your repository to a previous known working state.


### Git branching model

`$ git branch -a`
List all local branches in repository. With -a: show all branches (with remote).

`$ git branch [branch_name]`
Create new branch, referencing the current HEAD.

`$ git checkout [branch_name]`
Switch working directory to the specified branch.

`$ git checkout -b [branch_name]`
Create a newbranch and switch the working directory to the newbranch.

`$ git merge [branchname]`
Join specified [from name]` branch into your current branch (the one
you are on currently).

`$ git branch -d [branchname]`
Remove selected branch, if it is already merged into any other.

`$ git reflog`
List operations (e.g. checkouts or commits) made on local repository.
Tagging known commits
Reverting changes
Synchronizing repositories

### Tagging

`$ git tag`
List all tags.

`$ git tag [tagname]`
Create a tag reference named name for current commit.

`$ git show [tagname]`
Create a tag reference named name for current commit.

`$ git tag -d [tagname]`
Remove a tag from local repository

### Synchronizing repositories

`$ git revert [commit sha]`
Create a new commit, reverting changes from the specified commit.
It generates an inversion of changes.

`$ git fetch [remote]`
Fetch changes from the remote, but not update tracking branches.

`$ git fetch --prune [remote]`
Delete remote Refs that were removed from the remote repository.

`$ git pull [remote]`
Fetch changes from the remote and merge current branch with its
upstream.

`$ git push [--tags]` [remote]`
Push local changes to the remote. Use --tags to push tags.

`$ git push -u [remote]` [branch]`
Push local branch to remote repository. Set its copy as an upstream

### Stashing

`$ git stash`
Put current changes in your working directory into stash for later use.

`$ git stash pop`
Apply stored stash content into working directory, and clear stash.

`$ git stash drop`
Delete a specific stash from all your previous stashes