Git Cheatsheet


Status
git status

git rm NAME
# remove a file

Commit
git commit -amend 
# launch default editor with amended history
git commit -am “New commit message” 
# amend changes with a new commit message
git commit -amend —no-edit 
# leaves message the same as in the last commit

Log
get log
get log --oneline
# visually easier to see all logs

Reset
git reset hashid(from log)
get rest --hard hashid(from log)

Rebase
# taking comits from one branch and applying to another git rebase <branch>/<commit>
git rebase --interactive <branch>/<commit>
git rebase -i HEAD-#
git rebase -i --root

Branching
git branch
# look at all branches in repository

git switch
git switch -c "NAME"
   # make copy of exiting branch
gIt checkout -b "NAME" 
   # Legacy version of switch

Merging
git merge <branch>

Delete Branch
git branch --delete NAME
git branch -d NAME
# use -d if branches are free of conflicts branch will be deleted
git branch -D NAME 
# use -D will ignore conflicts & delete branch 

Stashing Code
git stash list
# view list of what has been stored
git stash apply
# allows to apply a stashed set of changes
git stash pop
# will remove the git stash from the list

git Clean 
# removing old files that you don't need anymore
git clean -n # dry run # n
# would remove NAME file
git clean -dn # directories
# would remove NAME directory
git clean -d # directories
git clean -f # force
# Removing Name files/directories