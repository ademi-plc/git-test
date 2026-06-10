# Basic Git commands

    git init                     - create a new repository
    git status                   - show file status
    git add                      - add files (stage changes for commit)
    git commit                   - save changes
    git log                      - show history
    git diff                     - show differences (what changed since last time)

## git commit and its flags

    git commit                   - create a new commit
    git commit -m "<message>"    - flag for a message (briefly describe what changed)
        --amend                  - amend or modify the last commit
    git commit -a                - add all changed and deleted files to the commit
    git commit --allow-empty     - create a commit with no changes

## git diff - shows what changed since the last commit

    +++  - added lines
    ---  - deleted lines

## Additional commands

    git log --oneline            - quickly view history (briefly)
    git diff --staged            - see what's in the staging area
    git restore file             - undo changes in a file
    git branch -r                - view remote branches
    git rm --cached file         - stop tracking a file

## Git branch creation and switching commands

    git branch soski             - create branch "soski"
    git checkout soski           - switch to branch "soski"
    git checkout -b soski        - create and immediately switch to branch "soski"
    git branch -d soski          - delete branch "soski" (after merging, the branch is no longer needed)
    git branch -M piski          - rename current branch to "piski"

## Interesting naming convention

Branches are named like `feature/readme-update` — the slash does **not** mean a
file inside a `feature` branch; it is the full name. This is done for better
clarity: the first word is the development group (feature, bugfix, hotfix) and
the second part is the specific task in that branch (readme-update, new-button,
etc.).

## Merging branches

To merge a branch into, say, `master`, we first switch to `master` and then run
the merge command:

    git merge <branch-name-to-merge>

## The coolest Git command

    git remote add origin <github-url> - this literally means "now we will
    connect to a remote repository"

## Push and tracking

Now comes something brilliant. You can push the `main` branch to the `main`
branch on GitHub so that it permanently remembers where to push `main` to
GitHub. The same works for every branch:

    git push -u origin main     - set up tracking between local main and GitHub main
    git branch -vv              - show all branch tracking relationships
    git pull                    - fetch all new changes from the remote repo to your local machine
