# 📘 Git Commands Reference (Days 22–25)

This document covers **core Git commands** learned from Days **22 to 25**, organized by category for quick reference and revision.

1️⃣ Setup & Configuration
---
| Command                                          | Description                       | Example                                             |
| ------------------------------------------------ | --------------------------------- | --------------------------------------------------- |
| `git config --global user.name "Your Name"`      | Set your Git username globally.   | `git config --global user.name "Sana Shaik"`        |
| `git config --global user.email "you@email.com"` | Set your Git email globally.      | `git config --global user.email "sana@example.com"` |
| `git config --list`                              | List all configured Git settings. | `git config --list`                                 |

2️⃣ Basic Workflow

| Command                          | Description                                                | Example                          |
| -------------------------------- | ---------------------------------------------------------- | -------------------------------- |
| `git status`                     | Show the status of working directory and staging area.     | `git status`                     |
| `git add <file>`                 | Stage a specific file for commit.                          | `git add index.html`             |
| `git add .`                      | Stage all modified and new files.                          | `git add .`                      |
| `git commit -m "commit message"` | Save staged changes as a commit.                           | `git commit -m "Added homepage"` |
| `git log`                        | Show full commit history.                                  | `git log`                        |
| `git log --oneline`              | Show commits in condensed single-line format.              | `git log --oneline`              |
| `git log --oneline -4`           | Show the last 4 commits.                                   | `git log --oneline -4`           |
| `git diff`                       | Show unstaged changes between working directory and index. | `git diff`                       |
| `git diff --staged`              | Show changes staged for the next commit.                   | `git diff --staged`              |

3️⃣ Branching

| Command                       | Description                        | Example                        |
| ----------------------------- | ---------------------------------- | ------------------------------ |
| `git branch`                  | List all local branches.           | `git branch`                   |
| `git branch <branch-name>`    | Create a new branch.               | `git branch feature-login`     |
| `git switch <branch-name>`    | Switch to an existing branch.      | `git switch feature-login`     |
| `git switch -c <new-branch>`  | Create and switch to a new branch. | `git switch -c feature-signup` |
| `git checkout <branch-name>`  | Switch branches (older Git style). | `git checkout main`            |
| `git branch -d <branch-name>` | Delete a merged branch safely.     | `git branch -d feature-login`  |
| `git branch -D <branch-name>` | Force delete an unmerged branch.   | `git branch -D bugfix-header`  |

4️⃣ Remote Operations

| Command                       | Description                                | Example                                      |
| ----------------------------- | ------------------------------------------ | -------------------------------------------- |
| `git clone <repo-url>`        | Copy a remote repository to local machine. | `git clone https://github.com/sana/repo.git` |
| `git remote -v`               | Show all remote repository URLs.           | `git remote -v`                              |
| `git fetch`                   | Fetch updates from remote without merging. | `git fetch origin`                           |
| `git pull`                    | Fetch and merge changes from remote.       | `git pull origin main`                       |
| `git push`                    | Push local commits to remote.              | `git push`                                   |
| `git push -u origin <branch>` | Push branch and set upstream tracking.     | `git push -u origin feature-login`           |

Fork Workflow
| Command                                       | Description                                 | Example                                                        |
| --------------------------------------------- | ------------------------------------------- | -------------------------------------------------------------- |
| `git remote add upstream <original-repo-url>` | Add the original repo as upstream.          | `git remote add upstream https://github.com/original/repo.git` |
| `git fetch upstream`                          | Fetch latest changes from upstream repo.    | `git fetch upstream`                                           |
| `git merge upstream/main`                     | Merge upstream changes into current branch. | `git merge upstream/main`                                      |

5️⃣ Merging & Rebasing

| Command                            | Description                                             | Example                            |
| ---------------------------------- | ------------------------------------------------------- | ---------------------------------- |
| `git merge <branch-name>`          | Merge another branch into current branch.               | `git merge feature-login`          |
| `git merge --squash <branch-name>` | Merge as a single commit without creating merge commit. | `git merge --squash feature-login` |

Rebase

6️⃣ Stash & Cherry-Pick

| Command           | Description                           | Example                     |
| ----------------- | ------------------------------------- | --------------------------- |
| `git stash`       | Save uncommitted changes temporarily. | `git stash`                 |
| `git stash list`  | List all saved stashes.               | `git stash list`            |
| `git stash apply` | Apply a stash without removing it.    | `git stash apply stash@{0}` |
| `git stash pop`   | Apply and remove the stash.           | `git stash pop`             |
| `git stash drop`  | Delete a specific stash.              | `git stash drop stash@{0}`  |

Cherry-Pick

| Command                         | Description                                  | Example                   |
| ------------------------------- | -------------------------------------------- | ------------------------- |
| `git cherry-pick <commit-hash>` | Apply a specific commit from another branch. | `git cherry-pick 5f3e2a1` |


7️⃣ Reset & Revert

| Command                    | Description                            | Example                    |
| -------------------------- | -------------------------------------- | -------------------------- |
| `git reset --soft HEAD~1`  | Undo last commit, keep changes staged. | `git reset --soft HEAD~1`  |
| `git reset --mixed HEAD~1` | Undo last commit, unstage changes.     | `git reset --mixed HEAD~1` |
| `git reset --hard HEAD~1`  | Undo last commit and discard changes.  | `git reset --hard HEAD~1`  |

Revert (Safe Undo)

| Command                    | Description                                        | Example                 |
| -------------------------- | -------------------------------------------------- | ----------------------- |
| `git revert <commit-hash>` | Create a new commit that undoes a previous commit. | `git revert 5f3e2a1`    |
| `git revert --continue`    | Continue revert after resolving conflicts.         | `git revert --continue` |
| `git revert --abort`       | Cancel an ongoing revert operation.                | `git revert --abort`    |


## 📘 GitHub CLI (gh) Commands Referenc


| Category            | Command | Description | Example |
|---------------------|---------|-------------|---------|
| Authentication | `gh auth login` | Log in to GitHub via browser or device flow | `gh auth login` |
| Authentication | `gh auth status` | Check current login and token scopes | `gh auth status` |
| Authentication | `gh auth logout` | Log out from GitHub CLI | `gh auth logout` |
| Authentication | `gh auth refresh -h github.com -s delete_repo` | Refresh token and add required scope | `gh auth refresh -h github.com -s delete_repo` |
| Repository | `gh repo create` | Create a new GitHub repository | `gh repo create my-repo` |
| Repository | `gh repo view` | View repo details | `gh repo view` |
| Repository | `gh repo clone` | Clone a GitHub repository | `gh repo clone user/repo` |
| Repository | `gh repo list` | List repositories for a user/org | `gh repo list Sana-2026` |
| Repository | `gh repo delete` | Delete a repository (owner/admin only) | `gh repo delete user/repo --yes` |
| Issues | `gh issue create` | Create a new issue | `gh issue create --title "Bug" --body "Fix login" --label bug` |
| Issues | `gh issue list` | List issues in a repository | `gh issue list` |
| Issues | `gh issue view` | View an issue | `gh issue view 12` |
| Issues | `gh issue close` | Close an issue | `gh issue close 12` |
| Pull Requests | `gh pr create` | Create a pull request | `gh pr create --base main --head feature-1` |
| Pull Requests | `gh pr list` | List pull requests | `gh pr list` |
| Pull Requests | `gh pr view` | View PR details | `gh pr view 5` |
| Pull Requests | `gh pr merge` | Merge a pull request | `gh pr merge 5` |
| Workflow / CI | `gh workflow list` | List GitHub Actions workflows | `gh workflow list` |
| Workflow / CI | `gh workflow run` | Manually trigger a workflow | `gh workflow run deploy.yml` |
| Workflow / CI | `gh run list` | List workflow runs | `gh run list` |
| Workflow / CI | `gh run view` | View workflow run details | `gh run view 123456` |


