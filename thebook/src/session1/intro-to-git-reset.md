### Your Local Git repo and The Three Trees - or, "Intro to `git reset`"
When I last checked (end of March 2023), six of the [top twelve stackoverflow questions](https://stackoverflow.com/questions?tab=Votes) were git questions!!

For at least a couple of those, the answer is `git reset`. 

`git reset` is an essential command for moving changes around in your local git repo.  We'll learn to use `git reset` to move changes back and forth between the "three trees" - **working tree**, **index**, and **HEAD**.  To go more in-depth, work thru [The Objects and Trees Exercise](objects-and-trees-exercise.md).

**Vocabulary**:
- working tree, index, HEAD
- "detached HEAD" state

**Commands**: <br>`git reset --soft`, `git reset --mixed`, `git reset --hard`,<br> `git diff`, `git diff --staged`,<br> `git reflog`, `git stash`

A busy diagram, but worth pondering nonetheless.  It shows the objects as well as the trees.
![](../images/GitThreeTrees.png)

#### LAB - Commit changes and then modify them with `git reset`
Use each of `git reset`'s `--soft`, `--mixed`, and `--hard` options at least once.
> 1. Make a change and commit it (do not `git push`!).
> 1. Undo the change using `git reset`.
> 1. Make another change, and commit.
> 1. Revert, using another option of `git reset`.  Commit.
> 1. Revert, using another option of `git reset`.  Commit.

🤔 So far, we've only used `git reset` to move our current branch back one commit.  But with `git reset`, we can move our current branch anywhere we want.  When might this be useful?

**Scenario**: You accidentally make commits on `main`, but then realize you should be on a different branch--for instance, in order to push that branch and submit a Pull Request for it (we'll discuss PR's soon).

#### LAB - Simulate branching "after-the-fact"
> 1. Make 3 or 4 commits on `main`.  Then realize, "Ooops, I should be on another branch".
> 1. Make a branch at your current location.  _Hover [here](doesnotexist.jpg, "'git branch mybranch' (not 'git checkout mybranch'!  Why is that?)") for a hint._
> 1. Use `git reset` to move `main` back to where it should be.

**Key Learning Points:**

✅ `git` doesn't care as much about your working tree as you might assume.  It mostly cares about the objects in its database **and frequently uses its database to overwrite your working tree**.  That said, `git` is not reckless; it will give you warnings about `git` operations that might be destructive to your local work.

✅ If you can understand and make the round-trip through the "Managing Local Changes" diagram in the [Cheat Sheet](/cheat-sheet.md), you have a great foundation for understanding how git works!
