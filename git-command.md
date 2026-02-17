Setup & Config
git config --global user.name

What it does: Sets your name for all Git commits on this system.
Example:

git config --global user.name "sana"

git config --global user.email

What it does: Sets your email for all Git commits on this system.
Example:

git config --global user.email "aqibkhan@gmail.com"

git config --global --list

What it does: Shows all global Git configuration settings.
Example:

git config --global --list
 Basic Workflow
git init

What it does: Creates a new Git repository in the current folder.
Example:

git init

git status

What it does: Shows the current state of files (modified, staged, untracked).
Example:

git status

git add

What it does: Adds file changes to the staging area.
Example:

git add file.txt


Add everything:

git add .

git commit

What it does: Saves staged changes as a snapshot in the repository.
Example:

git commit -m "Initial commit"

👀 Viewing Changes
git log

What it does: Shows the history of commits.
Example:

git log


Short version:

git log --oneline

git diff

What it does: Shows differences between working directory and staging area.
Example:

git diff

git branch

Shows all local branches and highlights the current one.

git branch branch-name

Creates a new branch.

Example:

git branch feature-login

git checkout branch-name

Switches to an existing branch.

Example:

git checkout feature-login

git checkout -b branch-name

Creates a new branch and switches to it.

Example:

git checkout -b fix-bug

git switch branch-name

Switches to a branch (modern and simpler command).

Example:

git switch main

git switch -c branch-name

Creates a new branch and switches to it (modern way).

Example:

git switch -c new-feature

git branch -d branch-name

Deletes a branch after it is merged.

Example:

git branch -d feature-login

git branch -D branch-name

Force deletes a branch (even if not merged).

Example:

git branch -D temp-branch

git merge branch-name

Merges a branch into the current branch.

Example:

git merge feature-login

git log --oneline --graph

Shows branch history in a visual graph format.
~
~
~
~
~
~
~
~
~
~
~
~
~
~
~
~
~
~
~
~
~
~
~
~
~
~
~
git-command.md [unix] (02:09 18/02/2026)                                                        0,1 All
-- INSERT --

