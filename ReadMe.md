<!-- COMPILED BY @THEAM01 -->
# Git Beginner’s Cheat Sheet

Everything you need to survive Git as a beginner.
Try to clone this repo to your local machine and play around with Git.

---

## Starting a Project
| Command | Meaning |
|----------|----------|
| `git init` | Start a new Git repo in the current folder (creates a hidden `.git` folder). |
| `git clone <repo-url>` | Copy (download) an existing remote repo to your machine. Example: `git clone https://github.com/user/project.git`. |

---

## Tracking Files
| Command | Meaning |
|----------|----------|
| `git add <file>` | Stage one file for commit. |
| `git add .` | Stage *all* changed files in the folder. |
| `git status` | Show what’s changed, staged, or untracked. |
| `git rm --cached <file>` | Unstage a file (remove from staging, not delete it). |

---

## Saving Changes
| Command | Meaning |
|----------|----------|
| `git commit -m "message"` | Save (commit) all staged changes with a message. |
| `git commit -am "message"` | Shortcut: add *and* commit all tracked files in one go. |
| `git log` | Show commit history. |
| `git log --oneline` | Compact commit history. |

---

## Connecting to GitHub
| Command | Meaning |
|----------|----------|
| `git remote add origin <url>` | Link your local repo to a remote one. |
| `git remote -v` | View connected remotes. |
| `git push -u origin main` | Push your branch to GitHub and set upstream (`-u` remembers the path). |
| `git push` | Push new commits (after upstream is set). |
| `git pull` | Fetch + merge new commits from the remote branch into your local one. |

---

## Branches
| Command | Meaning |
|----------|----------|
| `git branch` | Show all branches and highlight the current one. |
| `git branch <branch-name>` | Create a new branch. |
| `git checkout <branch-name>` | Switch to a branch. |
| `git checkout -b <branch-name>` | Create and switch to a new branch. |
| `git merge <branch-name>` | Merge the given branch into your current branch. |
| `git branch -d <branch-name>` | Delete a branch (safe). |
| `git branch -D <branch-name>` | Force delete a branch. |

---

## Updating & Syncing
| Command | Meaning |
|----------|----------|
| `git fetch` | Get latest changes from remote but don’t merge them yet. |
| `git pull` | Fetch + merge changes automatically. |
| `git push` | Upload your commits to the remote repo. |

---

## Undoing Things
| Command | Meaning |
|----------|----------|
| `git restore <file>` | Undo local changes to a file (go back to last commit). |
| `git reset <file>` | Unstage a file. |
| `git reset --hard` | Reset everything to the last commit (⚠️ wipes uncommitted changes). |
| `git revert <commit-hash>` | Undo a specific commit safely by making a new opposite commit. |

---

## Quick Daily Workflow
```bash
git init                        # Create repo
git add .                       # Stage all
git commit -m "first commit"    # Save snapshot
git branch -M main              # Rename default branch to main
git remote add origin <url>     # Link to GitHub
git push -u origin main         # Push it
```

Then each day:
```bash
git pull                        # Get updates
git add .                       # Stage
git commit -m "your message"    # Commit
git push                        # Push changes
```
