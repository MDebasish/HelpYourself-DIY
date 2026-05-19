
## Steps to take while syncing Remove and Local Repo
### Check Branches
```
git branch -a
```
### Checking Your Remote

To see which remote your repo is connected to:
```
git remote -v
```
### Recommended Workflow
```
git checkout main      # or master, or your working branch
git pull origin main
```
> [!TIP]
> Replace main with the branch you want to update.

### If You Want Your Local Branch to Exactly Match the Remote

If you want to discard all local changes and make your branch identical to the remote:
```
git fetch origin
git reset --hard origin/main
```
This will:
> [!CAUTION]
> Remove all uncommitted changes
> Discard local commits that are not on the remote

### If You Have Local Changes You Want to Keep

Use:
```
git pull --rebase
```
This will:
> [!CAUTION]
> Reapply your local commits on top of the latest remote changes
