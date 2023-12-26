# Git Commands Cheat Sheet

## Setting Up a Repository

| Command | Description |
| ------- | ----------- |
| `git init` | Create a new local Git repository |
| `git clone ssh://git@github.com/[username]/[repository-name].git` | Copy a remote repository to your local machine |

## Global Git Configuration

| Command | Description |
| ------- | ----------- |
| `git config --global user.name "[name]"` | Set your global Git username |
| `git config --global user.email "[email address]"` | Configure your global Git email address |

## Basic Operations

| Command | Description |
| ------- | ----------- |
| `git status` | Check the current status of your working directory |
| `git add [file-name.txt]` | Stage a file for the next commit |
| `git add .` | Stage all new and changed files |
| `git commit -m "[commit message]"` | Record changes with a commit message |
| `git rm -r [file-name.txt]` | Remove a file (or folder) from version control |

## Branching and Merging

| Command | Description |
| ------- | ----------- |
| `git branch` | List local branches (asterisk denotes the current branch) |
| `git branch -a` | Display all branches (local and remote) |
| `git branch [branch name]` | Create a new branch |
| `git branch -d [branch name]` | Delete a local branch |
| `git checkout -b [branch name]` | Create and switch to a new branch |
| `git checkout -b [branch name] origin/[branch name]` | Clone and switch to a remote branch |
| `git branch -m [old branch name] [new branch name]` | Rename a local branch |
| `git checkout [branch name]` | Switch to an existing branch |
| `git checkout -` | Switch to the last checked-out branch |
| `git checkout -- [file-name.txt]` | Discard changes to a specific file |
| `git merge [branch name]` | Combine changes from another branch |
| `git merge [source branch] [target branch]` | Merge changes from a source branch into a target branch |
| `git push origin --delete [branch name]` | Remove a remote branch |
| `git stash` | Temporarily save changes without committing |
| `git stash clear` | Discard all saved changes |

## Collaborating and Updating

| Command | Description |
| ------- | ----------- |
| `git push origin [branch name]` | Send changes to a remote repository |
| `git push -u origin [branch name]` | Push changes to the remote repository and set upstream |
| `git push` | Push changes to the remembered branch in the remote repository |
| `git push origin --delete [branch name]` | Delete a remote branch |
| `git pull` | Update the local repository to the latest commit |
| `git pull origin [branch name]` | Retrieve changes from the remote repository |
| `git reset [fileName]` | Unstage a file while keeping its content |
| `git reset [commitId]` | Undo all commits after a specified commit, preserving changes locally |
| `git reset --hard [commitId]` | Discard all history and return to a specific commit |
| `git remote add origin ssh://git@github.com/[username]/[repository-name].git` | Connect to a remote repository |
| `git remote set-url origin ssh://git@github.com/[username]/[repository-name].git` | Update the URL of a remote repository |

## Reviewing and Comparing

| Command | Description |
| ------- | ----------- |
| `git show [commitId]` | View changes made in a specific commit |
| `git log` | Examine changes in the commit history |
| `git log --summary` | Review changes with a detailed summary |
| `git log --oneline` | Check changes briefly |
| `git diff [source branch] [target branch]` | Preview changes before merging |
