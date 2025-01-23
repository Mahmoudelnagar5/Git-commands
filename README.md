# Ultimate Git Guide: Master Version Control 🚀

A comprehensive guide to Git commands with detailed notes for better understanding. Use this guide to master Git like a pro! 🛠️

---

## 1. Set Up Git 👤

Configure your identity for commits:

| **Description**                     | **Command**                                      |
|-------------------------------------|-------------------------------------------------|
| Set your username                   | `git config --global user.name "<username>"`    |
| Set your email address              | `git config --global user.email <email address>`|

**Notes**:
- Replace `<username>` and `<email address>` with your actual name and email.
- These settings are global and apply to all repositories on your machine.
- Use `git config --list` to view all your Git configurations.
- To set configurations for a specific repository, omit the `--global` flag.
- Always configure your identity before making commits to ensure proper attribution.

---

## 2. Working with Commits 💾

Stage and save changes to your repository:

| **Description**                     | **Command**                                      |
|-------------------------------------|-------------------------------------------------|
| Stage a specific file               | `git add <file name>` 📂                        |
| Stage all files                     | `git add .` 📂                                  |
| Commit changes with a message       | `git commit -m "MSG"` 💾                        |
| Initialize a new Git repository     | `git init` 🆕                                   |

**Notes**:
- Use `git add <file name>` to stage specific files for the next commit.
- Use `git add .` to stage all changes in the current directory and subdirectories.
- Always write clear and descriptive commit messages. For example: `git commit -m "Add login feature"`.
- Use `git init` to create a new Git repository in the current directory. This creates a hidden `.git` folder.
- Commits are snapshots of your project at a specific point in time. Make frequent, small commits for better tracking.

---

## 3. Check Status & History 📜

Monitor the state of your repository and view commit history:

| **Description**                     | **Command**                                      |
|-------------------------------------|-------------------------------------------------|
| Check the status of files           | `git status` 📊                                 |
| View the commit history             | `git log` 📜                                    |

**Notes**:
- `git status` shows the current state of your working directory, including untracked, modified, and staged files.
- Use `git log --oneline` for a compact view of the commit history.
- Use `git log --graph` to visualize the commit history with branches.
- Use `git log -p` to see the changes made in each commit.
- Use `git log --author="<name>"` to filter commits by a specific author.

---

## 4. Undo Changes 🔄

Revert or reset changes in your repository:

| **Description**                     | **Command**                                      |
|-------------------------------------|-------------------------------------------------|
| Remove the last N commits           | `git reset (--hard \|\| --soft) HEAD~N`         |
| Revert to a specific commit         | `git reset <commit ID>` ⏪                       |
| View all actions (including resets) | `git reflog` 🕒                                  |
| Reset to a specific commit          | `git reset --hard <commit ID>` 🔄               |

**Notes**:
- `--soft` keeps changes in the staging area, while `--hard` discards all changes.
- Use `git reflog` to recover lost commits or branches. It shows a history of all actions, including resets.
- Be cautious with `git reset --hard` as it permanently discards changes.
- Use `git revert <commit ID>` to create a new commit that undoes the changes of a specific commit.
- Use `git checkout <commit ID>` to temporarily switch to a specific commit.

---

## 5. Branching 🌿

Create, manage, and switch between branches:

### Types of Branches:
- **Local branch** 🏠: Exists in your local repository.
- **Remote branch** 🌐: Exists in the remote repository.
- **Remote tracking branch** 🔄: A copy of the remote branch used for merging.
- **Local tracking branch** 📡: Local branches that track remote branches.

### Branch Commands:
| **Description**                     | **Command**                                      |
|-------------------------------------|-------------------------------------------------|
| List all local branches             | `git branch` 🌿                                 |
| Create a new branch                 | `git branch <branch name>` 🌿                   |
| List all branches (local & remote)  | `git branch -a` 🌿                              |
| List remote branches only           | `git branch -r` 🌿                              |
| Push a branch to remote             | `git push origin <branch name>` 🌐              |
| Delete a branch (safe)              | `git branch -d <branch name>` 🗑️               |
| Force delete a branch               | `git branch -D <branch name>` 🗑️               |
| Delete a remote branch              | `git push origin --delete <branch name>` 🗑️    |
| Rename a branch                     | `git branch -M <new branch name>` ✏️            |

**Notes**:
- Use `git branch -d` to delete a branch only if it has been merged.
- Use `git branch -D` to force delete an unmerged branch.
- Use `git push origin --delete <branch name>` to delete a branch from the remote repository.
- Use `git branch -M` to rename a branch. This is useful if you made a typo in the branch name.
- Always create branches for new features or bug fixes to keep the `main` branch stable.

---

## 6. Remote Repositories 🌐

Connect and interact with remote repositories:

| **Description**                     | **Command**                                      |
|-------------------------------------|-------------------------------------------------|
| Connect local repo to remote        | `git remote add origin <repo link>`             |
| Push changes and set up tracking    | `git push -u origin main` 🌐                    |

**Notes**:
- Replace `<repo link>` with the URL of your remote repository.
- The `-u` flag sets up tracking between the local and remote branches.
- Use `git remote -v` to view the list of remote repositories.
- Use `git remote remove origin` to disconnect from a remote repository.
- Use `git fetch` to download changes from the remote repository without merging them.

---

## 7. Rebase & Cherry-pick 🔄

Rewrite commit history and apply specific changes:

| **Description**                     | **Command**                                      |
|-------------------------------------|-------------------------------------------------|
| Rebase current branch               | `git rebase <source branch>` 🔄                 |
| Apply changes from a specific commit| `git cherry-pick <commit ID>` 🍒                |

**Notes**:
- Use `git rebase` to maintain a clean commit history. It moves the entire branch to a new base commit.
- Use `git cherry-pick` to apply specific commits to another branch. This is useful for picking bug fixes from one branch to another.
- Be cautious with `git rebase` as it rewrites commit history, which can cause conflicts.
- Use `git rebase --abort` to cancel an ongoing rebase.

---

## 8. Stashing Changes 📦

Temporarily save and restore changes:

| **Description**                     | **Command**                                      |
|-------------------------------------|-------------------------------------------------|
| Temporarily save changes            | `git stash` 📦                                  |
| Restore saved changes               | `git stash apply` 📦                            |
| List all stashed changes            | `git stash list` 📋                             |
| Restore a specific stash            | `git stash apply <stash ID>` 📦                 |
| Delete a specific stash             | `git stash drop <stash ID>` 🗑️                 |
| Delete all stashed changes          | `git stash clear` 🗑️                           |
| Save changes with a message         | `git stash push -m "message"` 📦                |
| Restore and delete recent stash     | `git stash pop` 📦                              |

**Notes**:
- Use `git stash` to save work-in-progress before switching branches.
- Use `git stash apply` to restore changes without removing them from the stash list.
- Use `git stash pop` to apply and remove the most recent stash.
- Use `git stash push -m "message"` to save changes with a descriptive message.
- Use `git stash list` to view all stashed changes.

---

## 9. Pulling Updates 🔄

Fetch and merge changes from a remote repository:

| **Description**                     | **Command**                                      |
|-------------------------------------|-------------------------------------------------|
| Fetch and merge changes             | `git pull` 🔄                                   |

**Notes**:
- `git pull` is a combination of `git fetch` and `git merge`.
- Use `git pull --rebase` to avoid merge commits and maintain a linear history.
- Always pull changes before pushing to avoid conflicts.
- Use `git fetch` to download changes without merging them.

---

## 10. GitHub Commands 🐙

Clone and interact with GitHub repositories:

| **Description**                     | **Command**                                      |
|-------------------------------------|-------------------------------------------------|
| Clone a repository                  | `git clone <repo link>` 📥                      |

**Notes**:
- Replace `<repo link>` with the URL of the repository you want to clone.
- Cloning creates a local copy of the remote repository.
- Use `git clone --branch <branch name> <repo link>` to clone a specific branch.
- Use `git clone --depth 1 <repo link>` to clone only the latest commit (shallow clone).

---

## 11. Cleaning Up 🧹

Remove untracked files and discard changes:

| **Description**                     | **Command**                                      |
|-------------------------------------|-------------------------------------------------|
| Remove untracked files (dry run)    | `git clean -dn` 🧹                              |
| Delete untracked files              | `git clean -df` 🧹                              |
| Discard changes in a file           | `git restore <file name>` 🗑️                   |
| Discard all changes                 | `git restore .` 🗑️                             |
| Unstage a file                      | `git restore --staged <file name>` 🗑️          |
| Delete a file                       | `git rm <file name>` 🗑️                        |

**Notes**:
- Use `git clean -dn` to preview which files will be deleted.
- Use `git clean -df` to permanently delete untracked files.
- Use `git restore` to discard changes in tracked files.
- Use `git rm` to remove files from the working directory and staging area.
- Use `git restore --staged` to unstage a file without discarding changes.

---

## 12. Merging Changes 🔄

Combine changes from different branches:

| **Description**                     | **Command**                                      |
|-------------------------------------|-------------------------------------------------|
| Merge changes from a branch         | `git merge <source branch>` 🔄                  |

**Notes**:
- Always ensure you’re on the target branch (e.g., `main`) before merging.
- Resolve merge conflicts if they occur. Use `git status` to identify conflicting files.
- Use `git merge --abort` to cancel a merge in progress.
- Use `git merge --no-ff` to create a merge commit even if the merge is a fast-forward.

---

That's it! You're now ready to use Git like a pro. 🎉
