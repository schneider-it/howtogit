# Summary

## config

Configure the author name and email address to be used with your commits.  
Note that Git strips some characters (for example trailing periods) form user.name.

    git config --global user.name "Programmierer281986"
    git config --global user.email admin@schneider-it.at

## init

Create a new local repository

    git init

## clone

Create a working copy of a local repository:

    git clone /path/to/repository

For a remote server, use:

    git clone username@host:/path/to/repository
    git clone organisation/repository

## add

Add one or more files to staging (index):

    git add <filename>
    git add .
    git add *

## commit

Commit changes to head (but not yet to the remote repository):

    git commit -m "Commit message"

Commit any files you've added with git add, and also commit any files you've changed since then:

    git commit -a

## push

Send changes to the master branch of your remote repository:

    git push origin master
    git push

## status

List the files you've changed and those you still need to add or commit:

    git status

## log

If you want commits to be listed, use log:

    git log

This command also shows other useful information.

## remote

If you haven't connected your local repository to a remote server, add the server to be able to push to it:

    git remote add origin <server>

List all currently configured remote repositories:

    git remote -v

## stash

If you want to save all your local changes to a git-folder but undo them, so you have the same files as before local changes:

    git stash

You can also stash only individual files:

    git stash <filename>

## branches

Create a new branch and switch to it:

    git checkout -b <branchname>

Switch from one branch to another:

    git checkout <branchname>

List all the branches in your repository, and also tell you what branch you're currently in:

    git branch

Delete the feature branch:

    git branch -d <branchname>

Push the branch to your remote repository, so others can use it:

    git push origin <branchname>

Push all branches to your remote repository:

    git push --all origin

Delete a branch on your remote repository:

    git push origin :<branchname>

## update

Fetch and merge changes on the remote server to your working directory:

    git pull

To merge a different branch into your active branch:

    git merge <branchname>

View all the merge conflicts:

    git diff

View the conflicts against the base file:

    git diff --base <filename>

Preview changes, before merging:

    git diff <sourcebranch> <targetbranch>

After you have manually resolved any conflicts, you mark the changed file:

    git add <filename>

## tags

You can use tagging to mark a significant changeset, such as a release:

    git tag 1.0.0 <commitID>

CommitId is the leading characters of the changeset ID, up to 10, but must be unique. Get the ID using:

    git log

Push all tags to remote repository:

    git push --tags origin

## undo

If you mess up, you can replace the changes in your working tree with the last content in head:

    git checkout -- <filename>

Changes already added to the index, as well as new files, will be kept.

Instead, to drop all your local changes and commits, fetch the latest history from the server and point your local master branch at it, do this:

    git fetch origin
    git reset --hard origin/master
