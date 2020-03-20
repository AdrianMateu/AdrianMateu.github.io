---
layout: post
title: Git Support
---

*{{ page.date | date: "%B %e, %Y" }}*

Create local branch

~~~
# Git checkout on the branch from which you want to create the branch
git checkout develop

# Check for the latest changes
git fetch
git pull

# Create branch
git checkout -b feat/new-feature
~~~

Remove a file from the staging area

~~~
git reset HEAD -- <file>
~~~

Undo changes to files that are in the working directory (not yet uploaded to the staging area)

~~~
git checkout .
~~~

Git amend

~~~
# allows you to change the most recent commit message.
git add <file1> <file2>

git commit --amend

git push origin <branchname> -f
~~~

Reset your local branch to whatever is on origin

~~~
git reset —hard origin/branch 
~~~

Delete local & remote branch

~~~
git push -d origin feat/feature-branch
git branch -D feat/feature-branch
~~~

Stash the changes in a dirty working directory away

~~~
# Save
git stash

# Remove a single stashed state from the stash list and apply it on top of the current working tree state
git stash pop

# Like pop, but do not remove the state from the stash list.
git stash apply
~~~

Search a Git repository by commit message

~~~
git log --all --grep='Build 0051'
~~~

Create tags

~~~
git tag -a 3.26.0 -m "Version 3.26.0”

git push origin 3.26.0
~~~

Delete tags

~~~
# Remote:
git push --delete origin tagname

# Local:
git tag --delete tagname
~~~


[close]({{ site.baseurl }}/)