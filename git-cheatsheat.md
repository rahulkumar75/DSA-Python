# Daily Git Cheat Sheet

## Repository Basics

```bash
git status              # Check working tree status
git branch              # Show current branch
git branch -a           # Show all branches
git checkout <branch>   # Switch branch
git checkout -b <new>   # Create and switch to new branch
```

## Pull Latest Changes

```bash
git pull                        # Pull latest changes
git pull origin main           # Pull from specific branch
git pull --rebase origin main  # Pull with rebase
```

## Add and Commit Changes

```bash
git add .                              # Stage all changes
git add <file>                         # Stage specific file
git commit -m "your commit message"   # Commit staged changes
```

## Push Changes

```bash
git push                    # Push current branch
git push origin <branch>   # Push specific branch
```

## Stash Changes

```bash
git stash             # Save uncommitted changes
git stash list        # List stashes
git stash pop         # Reapply last stash
git stash apply       # Apply stash without deleting
```

## View History

```bash
git log --oneline --graph --all   # Compact commit history
git diff                          # Show unstaged changes
git diff --staged                 # Show staged changes
```

## Undo Changes

```bash
git restore <file>           # Discard changes in file
git restore --staged <file>  # Unstage file
git reset --soft HEAD~1      # Undo last commit, keep changes
git reset --hard HEAD~1      # Undo last commit, discard changes
```

## Handle Remote Branches

```bash
git fetch --all                     # Fetch all remotes
git branch -r                      # List remote branches
git checkout -b <branch> origin/<branch>   # Track remote branch
```

## Resolve Conflicts

```bash
git status               # See conflicted files
# Edit files manually
git add .
git commit -m "resolve conflicts"
```

## Useful Cleanup

```bash
git clean -fd            # Remove untracked files/folders
git branch -d <branch>   # Delete local branch
git remote -v            # Show remotes
```

## Safe Daily Workflow

```bash
git status
git pull --rebase origin main
git add .
git commit -m "message"
git push origin <branch>
```

## If Local Changes Exist Before Pull

```bash
git stash
git pull --rebase origin main
git stash pop
```
