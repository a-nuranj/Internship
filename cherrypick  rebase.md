Cherrypick
Cherry-pick is a Git feature that lets you take a specific commit from one branch and apply it to another branch, without merging the whole branch.
First switch to the branch where you want the commit:

git checkout main

Then:

git cherry-pick <commit-id>

Example:

git cherry-pick a1b2c3d




Rebase
Rebase is used to move or replay your branch's commits on top of another branch, creating a cleaner project history
Suppose you and your friend start from the same point:

A --- B  (main)
       \
        C --- D  (feature)

While you're working, your friend adds a commit to main:

A --- B --- E  (main)
       \
        C --- D  (feature)

Now your feature branch is behind main.

If you do:

git rebase main

Git takes commits C and D and reapplies them after E:

A --- B --- E --- C' --- D'  (feature)
