# Git Cheatsheet

# Table of Contents

- [Git Cheatsheet](#git-cheatsheet)
- [Commands](#commands)
- [Examples](#examples)

# Commands

| Command                    | Description                              |
| -------------------------- | ---------------------------------------- |
| `git init`                 | Initialize a new Git repository          |
| `git clone <url>`          | Clone a repository                       |
| `git status`               | Show the working tree status             |
| `git add`                  | Add files to staging area                |
| `git commit`               | Commit changes to repository             |
| `git push`                 | Push changes to remote repo              |
| `git pull`                 | Fetch and merge changes from remote repo |
| `git checkout <branch>`    | Switch to a branch                       |
| `git checkout -b <branch>` | Create a new branch                      |
| `git merge <branch>`       | Merge a branch into the current branch   |
| `git branch`               | List all branches                        |
| `git branch -d <branch>`   | Delete a branch                          |
| `git log`                  | Show commit history                      |
| `git reset <file>`         | Unstage a file                           |
| `git revert <commit>`      | Revert a specific commit                 |
| `git stash`                | Stash changes                            |
| `git stash pop`            | Apply stashed changes                    |
| `git remote -v`            | Show remote repositories                 |
| `git fetch`                | Fetch changes from remote repository     |

# Examples

## Repository initilization:

```bash
git init
```

This command will create a `.git` folder containing all the information about your repository (branches, commits, etc)

## Repository cloning

```bash
git clone https://github.com/ItsMeViipeR/git-cheatsheet
```

This command will create a new folder (here `git-cheatsheet`) in you working directory (in UNIX, you can see the path with the `pwd` command).

To start editing, go in this folder, make your changes and use [`git commit`](#committing-changes) and [`git push`](#repository-pushing).

## Repository status

The repository status contains the informations about the file that git is tracking (added files, modified files, deleted files, etc).

```bash
git status
```

## Adding file to a git repository

To add a file to the staging area in your Git repository, use the `git add` command followed by the file name. For example, if you want to add a file named `example.txt`, you would run:

```bash
git add example.txt
```

This command tells Git to start tracking changes to the specified file and prepares it for the next commit. You can also use `git add .` to stage all changes in the current directory.

## Committing changes

To commit changes in your Git repository, use the `git commit` command followed by the `-m` flag and a message describing the changes. For example:

```bash
git commit -m "Add example.txt with initial content"
```

This command creates a new commit in the repository with the staged changes and associates it with the provided message. The commit message should be concise yet descriptive, summarizing the purpose of the changes.

## Pushing changes

To push changes to a remote repository, use the `git push` command followed by the name of the remote (usually `origin`) and the branch name. For example, to push changes from the `main` branch, you would run:

```bash
git push origin main
```

This command uploads your local commits to the specified branch on the remote repository. Ensure you have the necessary permissions and that your branch is up-to-date with the remote branch to avoid conflicts.

## Pulling changes

To pull changes from a remote repository and merge them into your current branch, use the `git pull` command followed by the name of the remote (usually `origin`) and the branch name. For example, to pull changes from the `main` branch, you would run:

```bash
git pull origin main
```

This command fetches the latest changes from the specified branch on the remote repository and merges them into your local branch. It is a combination of `git fetch` and `git merge`. Ensure your local branch is up-to-date and free of conflicts before pulling changes.

## Switching branches

To switch to an existing branch in your Git repository, use the `git checkout` command followed by the branch name. For example:

```bash
git checkout feature-branch
```

This command updates your working directory to match the specified branch.

## Creating a new branch

To create and switch to a new branch, use the `git checkout -b` command followed by the branch name. For example:

```bash
git checkout -b new-feature
```

This command creates a new branch named `new-feature` and switches to it.

## Merging branches

To merge a branch into your current branch, use the `git merge` command followed by the branch name. For example:

```bash
git merge feature-branch
```

This command integrates the changes from `feature-branch` into your current branch.

## Listing branches

To list all branches in your repository, use the `git branch` command:

```bash
git branch
```

This command displays a list of all branches, with the current branch highlighted.

## Deleting a branch

To delete a branch, use the `git branch -d` command followed by the branch name. For example:

```bash
git branch -d old-feature
```

This command deletes the branch named `old-feature`.

## Viewing commit history

To view the commit history of your repository, use the `git log` command:

```bash
git log
```

This command displays a list of commits, including their hashes, authors, dates, and messages.

## Unstaging a file

To unstage a file that was added to the staging area, use the `git reset` command followed by the file name. For example:

```bash
git reset example.txt
```

This command removes the file from the staging area but keeps the changes in your working directory.

## Reverting a commit

To revert a specific commit, use the `git revert` command followed by the commit hash. For example:

```bash
git revert abc1234
```

This command creates a new commit that undoes the changes introduced by the specified commit.

## Stashing changes

To temporarily save your changes without committing them, use the `git stash` command:

```bash
git stash
```

This command saves your changes and reverts your working directory to the last commit.

## Applying stashed changes

To apply the most recently stashed changes, use the `git stash pop` command:

```bash
git stash pop
```

This command restores the stashed changes and removes them from the stash list.

## Viewing remote repositories

To view the remote repositories associated with your local repository, use the `git remote -v` command:

```bash
git remote -v
```

This command displays the URLs of the remote repositories.

## Fetching changes

To fetch changes from a remote repository without merging them, use the `git fetch` command:

```bash
git fetch
```

This command downloads the latest changes from the remote repository but does not apply them to your local branch.
