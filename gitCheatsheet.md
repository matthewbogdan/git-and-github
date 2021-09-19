# Git Cheatsheet


Status
git status

## remove a file
git rm NAME


## Commit
git commit -amend 
## launch default editor with amended history
git commit -am “New commit message” 
# amend changes with a new commit message
git commit -amend —no-edit 
# leaves message the same as in the last commit

## Log
get log
### visually easier to see all logs
get log --oneline

## Reset
git reset hashid(from log)
get rest --hard hashid(from log)

## Rebase
### taking commits from one branch and applying to another git rebase <branch>/<commit>
git rebase --interactive <branch>/<commit>
git rebase -i HEAD-#
git rebase -i --root

## Branching
# look at all branches in repository
git branch

## git switch
### make copy of exiting branch
git switch -c "NAME"
### Legacy version of switch
gIt checkout -b "NAME" 

## Merging
git merge <branch>

## Delete Branch
git branch --delete NAME
### use -d if branches are free of conflicts branch will be deleted
git branch -d NAME
### use -D will ignore conflicts & delete branch 
git branch -D NAME 

## Stashing Code
### view list of what has been stored
git stash list
### allows to apply a stashed set of changes
git stash apply
### will remove the git stash from the list
git stash pop

## Clean
### removing old files that you don't need anymore
git Clean 
### would remove NAME file
git clean -n # dry run # n
### would remove NAME directory
git clean -dn # directories
git clean -d # directories
### Removing Name files/directories
git clean -f # force

## Remotes
git remote add NAME URL
git remote remove NAME
git rename OLDNAME NEWNAME
git remote -v

## Git Push
git push REMOTE BRANCH
git push --set-upstream-to origin main (-u)
git push -u origin main # --set-upstream
### push all branches
git push --all
git branch --set-upstream-to <orgin/remote-branch>