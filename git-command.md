# 📘 Git Commands Reference (Days 22–25)

This document covers **core Git commands** learned from Days **22 to 25**, organized by category for quick reference and revision.

---

## 1️⃣ Setup & Configuration

```bash
git config --global user.name "Your Name"
git config --global user.email "you@email.com"
git config --list

Purpose

Configure Git identity

Verify current Git settings

2️⃣ Basic Workflow
git status
git add <file>
git add .
git commit -m "commit message"
git log
git log --oneline
git log --oneline -4
git diff
git diff --staged

Purpose

Track file status

Stage changes

Commit snapshots

View history

Inspect changes

3️⃣ Branching
git branch
git branch <branch-name>
git switch <branch-name>
git switch -c <new-branch>
git checkout <branch-name>
git branch -d <branch-name>
git branch -D <branch-name>

Purpose

Create and manage branches

Switch between branches

Delete merged/unmerged branches

4️⃣ Remote Operations
git clone <repo-url>
git remote -v
git fetch
git pull
git push
git push -u origin <branch>
Fork Workflow (Concept)

Fork repo on GitHub

Clone your fork

Add upstream remote

git remote add upstream <original-repo-url>
git fetch upstream
git merge upstream/main

Purpose

Sync with remote repositories

Collaborate safely using forks

5️⃣ Merging & Rebasing
Merge
git merge <branch-name>
git merge --squash <branch-name>

Combines branches

May create merge commit

Rebase
git rebase <branch-name>
git rebase -i HEAD~3

Replays commits on top of another branch

Rewrites history (local only)

6️⃣ Stash & Cherry-Pick
Stash
git stash
git stash list
git stash apply
git stash pop
git stash drop

Use

Temporarily save uncommitted changes

Cherry-Pick
git cherry-pick <commit-hash>

Use

Apply a specific commit from another branch

7️⃣ Reset & Revert
Reset (Local History Rewrite)
git reset --soft HEAD~1
git reset --mixed HEAD~1
git reset --hard HEAD~1
Mode	What Happens
--soft	Removes commit, keeps changes staged
--mixed	Removes commit, unstages changes
--hard	Removes commit and discards changes

⚠️ Do not use reset on pushed commits

Revert (Safe Undo)
git revert <commit-hash>
git revert --continue
git revert --abort

Purpose

Safely undo a commit by creating a new commit

Recommended for shared branches

🔑 Golden Rules

Local mistake → reset

Pushed/shared mistake → revert

Feature work → branch

Cleanup before push → rebase

Emergency fix → hotfix / cherry-pick

🧠 One-Line Memory

Reset rewrites history, Revert preserves history





# 📘 Git Commands Reference (Days 22–25) — Table Format

| Category | Command | Description | When to Use | Example |
|--------|--------|-------------|------------|---------|
| **Setup & Config** | `git config --global user.name` | Set Git username | First-time setup | `git config --global user.name "Sana"` |
| | `git config --global user.email` | Set Git email | First-time setup | `git config --global user.email "sana@mail.com"` |
| | `git config --list` | View config | Verify settings | `git config --list` |
| **Basic Workflow** | `git status` | Show repo status | Before/after changes | `git status` |
| | `git add <file>` | Stage a file | Before commit | `git add file.txt` |
| | `git add .` | Stage all changes | Multiple files | `git add .` |
| | `git commit -m` | Save snapshot | After staging | `git commit -m "Add feature"` |
| | `git log --oneline` | View commit history | Quick history view | `git log --oneline` |
| | `git diff` | View unstaged changes | Review edits | `git diff` |
| | `git diff --staged` | View staged changes | Before commit | `git diff --staged` |
| **Branching** | `git branch` | List branches | Check branches | `git branch` |
| | `git branch <name>` | Create branch | New feature | `git branch feature-1` |
| | `git switch <name>` | Switch branch | Change context | `git switch main` |
| | `git switch -c <name>` | Create + switch | Start work | `git switch -c login` |
| | `git branch -d <name>` | Delete branch | After merge | `git branch -d login` |
| **Remote** | `git clone` | Copy remote repo | Start project | `git clone repo-url` |
| | `git remote -v` | View remotes | Check origin | `git remote -v` |
| | `git fetch` | Download changes | Sync without merge | `git fetch origin` |
| | `git pull` | Fetch + merge | Update branch | `git pull origin main` |
| | `git push` | Upload commits | Share work | `git push origin main` |
| **Merging & Rebasing** | `git merge <branch>` | Combine branches | Integrate work | `git merge feature-1` |
| | `git merge --squash` | Squash commits | Clean history | `git merge --squash feature-1` |
| | `git rebase <branch>` | Replay commits | Linear history | `git rebase main` |
| | `git rebase -i` | Edit commits | Cleanup before push | `git rebase -i HEAD~3` |
| **Stash** | `git stash` | Save work temporarily | Switch tasks | `git stash` |
| | `git stash list` | View stashes | Manage stashes | `git stash list` |
| | `git stash pop` | Apply + delete stash | Resume work | `git stash pop` |
| **Cherry-Pick** | `git cherry-pick <hash>` | Apply specific commit | Hotfix | `git cherry-pick a1b2c3` |
| **Reset** | `git reset --soft` | Undo commit, keep staged | Edit commit | `git reset --soft HEAD~1` |
| | `git reset --mixed` | Undo commit, unstage | Re-stage changes | `git reset --mixed HEAD~1` |
| | `git reset --hard` | Delete commit + changes | Discard work ⚠️ | `git reset --hard HEAD~1` |
| **Revert** | `git revert <hash>` | Safe undo commit | Shared branch | `git revert a1b2c3` |
| | `git revert --continue` | Finish revert | After conflict | `git revert --continue` |
| | `git revert --abort` | Cancel revert | Abort operation | `git revert --abort` |

---



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


