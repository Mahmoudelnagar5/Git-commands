# Git Commands Cheat Sheet 🚀

This guide provides a quick reference to essential Git commands, organized by category. Use this cheat sheet to streamline your Git workflow! 🛠️

---

## 1. Tell Git Who You Are 👤

Configure your identity for commits:

| **Description**                     | **Command**                                      |
|-------------------------------------|-------------------------------------------------|
| Configure the author name           | `git config --global user.name "<username>"`    |
| Configure the author email address  | `git config --global user.email <email address>`|

---

## 2. Commits & Staging 💾

| **Description**                     | **Command**                                      |
|-------------------------------------|-------------------------------------------------|
| Stage a specific file               | `git add <file name>` 📂                        |
| Stage all files                     | `git add .` 📂                                  |
| Commit changes with a message       | `git commit -m "MSG"` 💾                        |
| Initialize a new Git repository     | `git init` 🆕                                   |

---

## 3. Log & Status 📜

| **Description**                     | **Command**                                      |
|-------------------------------------|-------------------------------------------------|
| Show the status of files            | `git status` 📊                                 |
| Show the commit log                 | `git log` 📜                                    |

---

## 4. Removing Commits 🔄

| **Description**                     | **Command**                                      |
|-------------------------------------|-------------------------------------------------|
| Remove the last N commits           | `git reset (--hard \|\| --soft) HEAD~N`         |
| Revert to a specific commit         | `git reset <commit ID>` ⏪                       |
| Show history of all actions         | `git reflog` 🕒                                  |
| Reset to a specific commit          | `git reset --hard <commit ID>` 🔄               |

---

## 5. Checkout & Switching Branches 🌿

| **Description**                     | **Command**                                      |
|-------------------------------------|-------------------------------------------------|
| Move to a specific commit           | `git checkout <commit ID>` ⏩                   |
| Switch to a branch                  | `git checkout <branch name>` 🌿                 |
| Create and switch to a new branch   | `git checkout -b <branch name>` 🌿              |
| Switch to another branch            | `git switch <branch name>` 🔄                   |
| Create and switch to a new branch   | `git switch -c <branch name>` 🔄                |

---

## 6. Branching 🌿

### Types of Branches:
- **Local branch** 🏠: Exists in your local repository.
- **Remote branch** 🌐: Exists in the remote repository.
- **Remote tracking branch** 🔄: A copy of the remote branch used for merging.
- **Local tracking branch** 📡: Local branches that track remote branches.

### Branch Commands:
| **Description**                     | **Command**                                      |
|-------------------------------------|-------------------------------------------------|
| Show all local branches             | `git branch` 🌿                                 |
| Create a new branch                 | `git branch <branch name>` 🌿                   |
| Show all branches (local & remote)  | `git branch -a` 🌿                              |
| Show remote branches only           | `git branch -r` 🌿                              |
| Push a branch to remote             | `git push origin <branch name>` 🌐              |
| Delete a branch (dry run)           | `git branch -d <branch name>` 🗑️               |
| Force delete a branch               | `git branch -D <branch name>` 🗑️               |
| Delete a remote branch              | `git push origin --delete <branch name>` 🗑️    |
| Rename a branch                     | `git branch -M <new branch name>` ✏️            |

---

## 7. Remote Repository 🌐

| **Description**                     | **Command**                                      |
|-------------------------------------|-------------------------------------------------|
| Link local repo to remote           | `git remote add origin <repo link>`             |
| Push changes and set up tracking    | `git push -u origin main` 🌐                    |

---

## 8. Rebase & Cherry-pick 🔄

| **Description**                     | **Command**                                      |
|-------------------------------------|-------------------------------------------------|
| Rebase current branch               | `git rebase <source branch>` 🔄                 |
| Apply changes from a specific commit| `git cherry-pick <commit ID>` 🍒                |

---

## 9. Miscellaneous 🛠️

| **Description**                     | **Command**                                      |
|-------------------------------------|-------------------------------------------------|
| Show tracked files in staging area  | `git ls-files` 📂                               |
| Merge changes from a branch         | `git merge <source branch>` 🔄                  |
| Remove untracked files (dry run)    | `git clean -dn` 🧹                              |
| Delete untracked files              | `git clean -df` 🧹                              |
| Discard changes in a file           | `git restore <file name>` 🗑️                   |
| Discard all changes                 | `git restore .` 🗑️                             |
| Unstage a file                      | `git restore --staged <file name>` 🗑️          |
| Delete a file                       | `git rm <file name>` 🗑️                        |

---

## 10. Stashing 📦

| **Description**                     | **Command**                                      |
|-------------------------------------|-------------------------------------------------|
| Temporarily save changes            | `git stash` 📦                                  |
| Restore saved changes               | `git stash apply` 📦                            |
| Show list of saved changes          | `git stash list` 📋                             |
| Restore a specific stash            | `git stash apply <stash ID>` 📦                 |
| Delete a specific stash             | `git stash drop <stash ID>` 🗑️                 |
| Delete all saved changes            | `git stash clear` 🗑️                           |
| Save changes with a message         | `git stash push -m "message"` 📦                |
| Restore and delete recent stash     | `git stash pop` 📦                              |

---

## 11. Pulling Changes 🔄

| **Description**                     | **Command**                                      |
|-------------------------------------|-------------------------------------------------|
| Fetch and merge changes             | `git pull` 🔄                                   |

---

## 12. GitHub Specific Commands 🐙

| **Description**                     | **Command**                                      |
|-------------------------------------|-------------------------------------------------|
| Clone a repository                  | `git clone <repo link>` 📥                      |

---

## Corrections & Notes 📝

1. **`git reset <commit ID>`**: Moves the HEAD to a specific commit. To restore a deleted commit, use `git reflog` to find the commit ID and then `git checkout <commit ID>`.
2. **`git branch -d <branch name>`**: Deletes a branch only if it has been merged. Use `git branch -D <branch name>` for unmerged branches.
3. **`git push origin --delete <branch name>`**: Deletes a branch from the remote repository. Ensure you’ve deleted it locally first.
4. **`git rebase <source branch>`**: Ensure you’re on the branch you want to rebase before running this command.
5. **`git cherry-pick <commit ID>`**: Ensure you’re on the correct branch before running this command.

---

Enjoy using Git like a pro! 🎉
