# Commits

# add

Before you can commit your local changes you have to add your changes to the git working tree. You can do this with this command:

    git add .

# commit

After adding changes to the working tree, you can make a commit:

    git commit -m "<some message>"

However, this commit is only on your local machine, not in the remote git repository.

# push

If you want to push your local commits, use this command:

    git push

Usually this command is the last command you execute after working on something.

# pull

If you want to copy remote commits to your local repository and integrate them into the working tree, use this command:

    git pull

Usually this command is the very first command you will execute before working.

# clone

If a remote repository doesn't exist locally yet, use this command to copy the repository to your local machine:

    git clone <URL of repository>

For example, if you want to get the remote repository schneider-it locally, use this command:

    git clone https://github.com/schneider-it/schneider-it

# fetch

If you want to copy remote commits to your local repository but you don't want them to be integrated in your working tree, use this command:

    git fetch

# revert
