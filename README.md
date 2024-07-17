# Git Commands Guide

This guide provides essential Git commands for managing your repositories, branches, and commits effectively.

## Repository Setup

- **Initialize a new Git repository**
  ```sh
  git init
  ```

- **Clone an existing repository**
  ```sh
  git clone <repository-url>
  ```

## Basic Operations

- **Check the status of your repository**
  ```sh
  git status
  ```

- **Add files to the staging area**
  ```sh
  git add <file>     # Add a specific file
  git add .          # Add all changes in the current directory
  ```

- **Commit changes**
  ```sh
  git commit -m "Your commit message"
  ```

- **Push changes to a remote repository**
  ```sh
  git push origin <branch-name>
  ```

- **Pull changes from a remote repository**
  ```sh
  git pull origin <branch-name>
  ```

## Branching and Merging

- **Create a new branch**
  ```sh
  git branch <branch-name>
  ```

- **Switch to a different branch**
  ```sh
  git checkout <branch-name>
  ```

- **Create and switch to a new branch**
  ```sh
  git checkout -b <branch-name>
  ```

- **Merge a branch into the current branch**
  ```sh
  git merge <branch-name>
  ```

- **Delete a branch**
  ```sh
  git branch -d <branch-name>        # Delete a local branch
  git push origin --delete <branch-name> # Delete a remote branch
  ```

## Remote Repositories

- **Add a remote repository**
  ```sh
  git remote add <remote-name> <repository-url>
  ```

- **View remote repositories**
  ```sh
  git remote -v
  ```

- **Remove a remote repository**
  ```sh
  git remote remove <remote-name>
  ```

## History and Diffs

- **View commit history**
  ```sh
  git log
  ```

- **View the difference between commits**
  ```sh
  git diff
  ```

- **View the difference between staged and working directory**
  ```sh
  git diff --cached
  ```

## Undoing Changes

- **Revert changes in a file (unstage changes)**
  ```sh
  git checkout -- <file>
  ```

- **Discard all local changes (WARNING: this will delete your uncommitted changes)**
  ```sh
  git reset --hard
  ```

- **Unstage a file**
  ```sh
  git reset <file>
  ```

## Stashing

- **Stash changes temporarily**
  ```sh
  git stash
  ```

- **Apply stashed changes**
  ```sh
  git stash apply
  ```

- **List stashes**
  ```sh
  git stash list
  ```

- **Drop a stash**
  ```sh
  git stash drop
  ```

## Tags

- **Tag a commit**
  ```sh
  git tag <tag-name>
  ```

- **View tags**
  ```sh
  git tag
  ```

- **Delete a tag**
  ```sh
  git tag -d <tag-name>
  ```

## Help and Documentation

- **Get help with a command**
  ```sh
  git <command> --help
  ```

- **View the Git documentation**
  ```sh
  git help
  ```

Feel free to modify this guide based on your project's specific needs or workflows.
