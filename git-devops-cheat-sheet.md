# DevOps-Focused Git Cheat Sheet

## Daily Safe Workflow

```bash
git status
git pull --rebase origin main
git add .
git commit -m "your message"
git push origin <branch>
```

## Fix Merge Conflicts

```bash
git pull --rebase origin main   # Pull latest changes
# Resolve conflicts manually in files
git add .
git rebase --continue           # Continue rebase after fixing
```

**Abort rebase if needed:**

```bash
git rebase --abort
```

## Revert a Bad Commit (Safe for Shared Branches)

```bash
git log --oneline
git revert <commit_id>
git push origin <branch>
```

This creates a new commit that reverses the bad commit.

## Reset Commits (Local Branch Cleanup)

**Undo last commit but keep changes:**

```bash
git reset --soft HEAD~1
```

**Undo last commit and unstage changes:**

```bash
git reset --mixed HEAD~1
```

**Undo last commit and discard everything:**

```bash
git reset --hard HEAD~1
```

## Reset Branch to Remote State

```bash
git fetch origin
git reset --hard origin/main
```

Useful when local branch is broken and needs fresh sync.

## Force Push (Use Carefully)

```bash
git push --force origin <branch>
```

**Safer option:**

```bash
git push --force-with-lease origin <branch>
```

Prevents overwriting others' work unexpectedly.

## Cherry-pick Specific Commit

```bash
git log --oneline
git cherry-pick <commit_id>
```

Useful for moving fixes between branches.

## Check What Changed

```bash
git diff
git diff --staged
git log --oneline --graph --all
```

## Stash Before Emergency Pull

```bash
git stash
git pull --rebase origin main
git stash pop
```

## Clean Untracked Files

```bash
git clean -fd
```

Preview before deleting:

```bash
git clean -fdn
```

## Recover Deleted Commit

```bash
git reflog
git reset --hard <commit_id>
```

Useful after accidental reset.

## Deploy / Release Tagging

```bash
git tag -a v1.0.0 -m "Release version 1.0.0"
git push origin v1.0.0
```

List tags:

```bash
git tag
```

## Branch Cleanup

```bash
git branch -d <branch>
git push origin --delete <branch>
```

## Jenkins / CI Troubleshooting

**See branch remote:**

```bash
git remote -v
```

**Fetch latest refs:**

```bash
git fetch --all
```

**Verify current commit:**

```bash
git rev-parse HEAD
```

## Production Hotfix Workflow

```bash
git checkout main
git pull origin main
git checkout -b hotfix/issue-name
# make fix
git add .
git commit -m "hotfix: issue fix"
git push origin hotfix/issue-name
```
