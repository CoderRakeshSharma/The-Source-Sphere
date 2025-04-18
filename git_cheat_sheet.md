
# Git Cheat Sheet

## Setup & Configuration
```bash
git config --global user.name "Your Name"
git config --global user.email "your.email@example.com"
git config --list                                    # List all configurations
```

## Repository Operations
```bash
git init                                            # Initialize a new repository
git clone <repository-url>                          # Clone a repository
git remote add origin <repository-url>              # Add remote repository
git remote -v                                       # List remote repositories
git remote remove <name>                            # Remove a remote
git remote rename <old> <new>                       # Rename a remote
```

## Basic Commands
```bash
git status                                          # Check repository status
git add <file>                                      # Add file to staging area
git add .                                           # Add all files to staging area
git commit -m "commit message"                      # Commit staged changes
git push origin <branch>                            # Push commits to remote
git push -u origin <branch>                         # Push and set upstream tracking
git pull origin <branch>                            # Pull changes from remote
```

## Branch Operations
```bash
git branch                                          # List local branches
git branch -a                                       # List all branches (local + remote)
git branch <branch-name>                            # Create new branch
git checkout <branch-name>                          # Switch to branch
git checkout -b <branch-name>                       # Create and switch to new branch
git checkout -                                      # Switch to the previous branch
git merge <branch-name>                             # Merge branch into current branch
git branch -d <branch-name>                         # Delete local branch
git push origin --delete <branch-name>              # Delete remote branch
git branch -m <new-name>                            # Rename current branch
git branch -m <old-name> <new-name>                 # Rename specific branch
```

## History & Differences
```bash
git log                                             # View commit history
git log --oneline                                   # Compact commit history
git diff                                            # Show unstaged changes
git diff --staged                                   # Show staged changes
git diff <commit1> <commit2>                        # Compare two commits
git show <commit>                                   # Show changes in a specific commit
git blame <file>                                    # Show who changed what and when
```

## Undo Operations
```bash
git reset <file>                                    # Unstage file
git reset --soft HEAD~1                             # Undo last commit, keep changes
git reset --hard HEAD~1                             # Undo last commit, discard changes
git revert <commit>                                 # Create new commit that undoes changes
git restore <file>                                  # Discard changes in working directory
git restore --staged <file>                         # Unstage a file (like `git reset <file>`)
```

## Stash Operations
```bash
git stash                                           # Stash changes
git stash list                                      # List stashes
git stash apply                                     # Apply most recent stash
git stash pop                                       # Apply and remove most recent stash
git stash drop                                      # Delete most recent stash
git stash save "message"                            # Stash with a message
git stash show -p                                   # Show patch of most recent stash
git stash branch <branch-name>                      # Create branch from stash
```

## Advanced Operations
```bash
git rebase <branch>                                 # Rebase current branch
git rebase -i HEAD~n                                # Interactive rebase (edit/reorder commits)
git cherry-pick <commit>                            # Apply specific commit to current branch
git reflog                                          # Show history of all HEAD changes
git tag <tag-name>                                  # Create lightweight tag
git tag -a <tag-name> -m "message"                  # Create annotated tag
```

## Cleanup Operations
```bash
git clean -n                                        # Show what will be deleted
git clean -f                                        # Delete untracked files
git gc                                              # Cleanup unnecessary files
git prune                                           # Remove unreachable Git objects
```

## Help
```bash
git help <command>                                  # Get help for a command
git <command> --help                                # Alternative way to get help
```
