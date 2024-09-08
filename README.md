# Git Commands Guide

This guide provides essential Git commands for managing your repositories, branches, and commits effectively.

## Configuration

- **Set your username**
  ```sh
  git config --global user.name "Your Name"
  ```
  
- **Set your email**
  ```sh
  git config --global user.email "your.email@example.com"
  ```

- **Set default text editor (VS Code)(Optional)**
  ```sh
  git config --global core.editor "code --wait" # This command tells Git to use VS Code as the editor and to wait until you close the editor window before it continues.
  ```

- **Edit Global Git Configuration**
  ```sh
  git config --global --edit # Open the global Git configuration file in your default text editor.
  ```
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

## Alias

- **Alias Commands**
  ```sh
  git config --global alias.co checkout  # Create alias for checkout

  git config --global --unset alias.co # Remove alias
  ```
    
- **Using Aliases**
  After creating the alias, use `git co` instead of `git checkout`. For example:

  ```sh
  git co my-branch # Use the alias to checkout a branch
  ```

  This command is equivalent to:

  ```sh
  git checkout my-branch # also use the standard 'checkout' command
  ```

- **Listing All Git Aliases**

  To list all the aliases you have configured in Git, use the following command:

  ```sh
  git config --get-regexp ^alias\.
  ```
  To simplify the process of listing all Git aliases, you can create an alias named `alias`:

  ```sh
  git config --global alias.alias "config --get-regexp ^alias\."
  ```

  With this alias, you can now simply type:

  ```sh
  git alias
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
