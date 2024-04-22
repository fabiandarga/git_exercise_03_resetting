# Exercise: Reverting a commit with git reset (soft, mixed, and hard)

Through this exercise, you can learn the difference between the various reset modes (`soft`, `mixed` and `hard`)
and understand how they affect the commit history, the staging area, and the working directory.

## Step 1

Initialize a new Git repository in an empty directory using the command:
```
git init
```

## Step 2

Create a new text file using a text editor or the command line. Name the file `example.txt` and add any text content.

## Step 3

Add the new text file to the staging area and commit it using the following commands:

```
git add example.txt
git commit -m "example.txt hinzugefügt"
```

## Step 4

Delete the file example.txt, add the change to the stage, and create a new commit with the message "deleted example.txt". Check that the working directory is clean using `git status`.

## Step 5

Execute the command `git log` to display the commit history and copy the SHA-1 hash of the first commit.

## Step 6

Now, try `git reset --soft` and `git reset --mixed` one after the other to see the difference:

```
git reset --soft <Commit-Hash>
```
```
git reset --mixed <Commit-Hash>
```

Check the status of your Git repository after each reset command and reissue commands to stage and commit so that there are 2 commits in the history again.

## Step 7

Now use `git reset --hard` to completely undo the deletion of the file.

```
git reset --hard <Commit-Hash>
```

