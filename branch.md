# Branches

## branch

    git branch

With this command you can get the local branches and the information on which branch you are currently.

## checkout

    git checkout <branch>

Use this command to checkout to another branch.

For example, if you want to checkout from your dev branch to your main branch, just type:

    git checkout main

## merge

Before you merge checkout to the branch you want to merge into.  
After that use:

    git merge <branch>

For example, if you want to merge the dev branch into the merge branch, use these commands:

    git checkout main
    git merge dev
