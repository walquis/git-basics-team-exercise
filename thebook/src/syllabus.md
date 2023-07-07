# Syllabus for Collaborating with git

### Goals
1. Read a repo's commit graph, and use git commands confidently to make it look like you want.
1. Clearly and efficiently communicate changes with your team using git commands, and Github workflow tools such as Pull Requests.
1. Capably manage the state of your local changes using basic git commands such as `git add`, `git commit`, and `git reset` to move them among __The Three Trees__.
1. When using git commands in real-life scenarios, know their effects in terms of __The Three Objects__ of git's data model.
1. Make changes confidently, knowing specifically how git has your back with commands such as `git reflog`.
 

### Objectives

By the end of this course, students will be able to...

#### Demonstrate these skills:
- Use Pull Requests to deliver changes for review by one or more members of your team
- Work as a team to deliver changes to a chosen remote and branch
- Manage commits with `git reset` and `git rebase` - including undo, modify, move operations
- Resolve merge collisions
- Stash work and return to it

#### Explain these terms and concepts:
- sha
- content-addressable filesystem
- blob, tree, commit
- working tree, index, HEAD
- symbolic ref
- branch
- remote
- fetch vs. pull
- fast-forward merge
- 'detached HEAD' state

#### Use these commands, and understand them in terms of the 3 objects/3 trees:
- git add
- git status
- git diff \[\--staged\]
- git show
- git commit
- git reset \[\--soft, \--mixed, \--hard \]
- git branch
- git merge
- [git stash](https://git-scm.com/book/en/v2/Git-Tools-Stashing-and-Cleaning) - "I need to save what I'm working on and come back to it later"
- git cherry-pick
- [git rebase -i](https://git-scm.com/book/en/v2/Git-Branching-Rebasing) - clean up commit history before pushing
- (stretch goal) [git bisect](https://git-scm.com/book/en/v2/Git-Tools-Debugging-with-Git) - find a bad commit
 
#### Identify and explain these components of a repo graph (as seen with "git log \--all \--decorate \--oneline \--graph"):
- HEAD
- main
- origin/main
- shas
- the lines along the left side
- branch/merge points

## Three Objects

Git is a brilliantly simple data model surrounded by a dense constellation of commands and options.  Once you know the model, you know how the graph should look.  Then you are equipped to find the command that does want you want.

[Git Objects](https://git-scm.com/book/en/v2/Git-Internals-Git-Objects) at git-scm.com is good reading.

- __Commit__ and its attributes
- __Tree__ and its attributes
- __Blob__ and its attributes

## Three Trees

The word "reset" is loaded with many connotations. In a git context, you can read `git reset` as "set-current-branch-to-an-existing-commit".  We'll explore how this works for managing local changes.

git-scm.com's [Reset Demystified](https://git-scm.com/book/en/v2/Git-Tools-Reset-Demystified) is also good reading.

These are the three trees:

- __HEAD__ - pointer to the current branch, which points to a commit
- __Index__ - the place you add to; the staging area for commits
- __Working Tree__ - the files checked out on disk (not including the git repo itself - that would be too meta)
