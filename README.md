<img
  src="/assets/img/git.png"
  width="70"
  align="right"
/>

# Git Alias &amp; BASH Command

## Translated Versions
- [বাংলা সংস্করণ](READMEbangla.md)
- [Version English](README.md)
___

## Table of contents

* [Git Commands](#git-commands)
* [BASH Commands](#bash-commands)
* [Git Alias Commands](#Git-Alias-Commands)


## About it
> Have you recently started using Git? This should give you the base commands you need to perform the most common actions in Git. If you find a command that is not here, or could be explained better, please don't hesitate in * [Contributing](#contributing). Cheers!


## Git Commands 🌟🌟🌟🌟

### 👉 Glossary

| Keywords                     | Description                                                                                                             |
| ---------------------------- | ----------------------------------------------------------------------------------------------------------------------- |
| git                          | Open-source distributed version-control system, used to store code in repositories                                      |
| GitHub, GitLab, Bitbucket    | Platform for hosting and collaborating on Git repositories                                                              |
| staging                      | Proposed files/directories that you'd like to commit                                                                    |
| commit                       | Saving all staged files/directories to your local repository                                                            |
| branch                       | An independent line of development, so you can develop features isolated from each other. Master branch is the default. |
| clone                        | Local version of a repository, including all commits and branches                                                       |
| remote                       | Common repository on eg. Github that all team members to keep that changes in sync with                                 |
| fork                         | Copy of a repository owned by a different user                                                                          |
| pull request                 | A method of submitting contributions to a repository                                                                    |
| HEAD                         | Represents your current working directory                                                                               |


### 👉 Configuration

| Key/Command                              | Description                                         |
| ---------------------------------------- | --------------------------------------------------- |
| `git config --global user.name [name]`   | Set author name to be used for all commits          |
| `git config --global user.email [email]` | Set author email to be used for all commits         |
| `git config color.ui true`               | Enables helpful colorization of command line output |


### 👉 Getting & Creating Projects

| Command | Description |
| ------- | ----------- |
| `git init` | Initialize a local Git repository |
| `git clone ssh://git@github.com/[username]/[repository-name].git` | Create a local copy of a remote repository |

### 👉 Basic Snapshotting

| Command | Description |
| ------- | ----------- |
| `git status` | Check status |
| `git add [file-name.txt]` | Add a file to the staging area |
| `git add -A` | Add all new and changed files to the staging area |
| `git commit -m "[commit message]"` | Commit changes |
| `git rm -r [file-name.txt]` | Remove a file (or folder) |


### 👉 Committing files

| Command | Description |
| ------- | ----------- |
| `git commit -m 'commit message' ` | Commit staged file(s) |
| `git commit filename -m 'commit message' ` | Add file and commit |
| `git commit -am 'insert commit message' ` | Add file and commit staged file |
| `git commit --amend 'new commit message' ` | Amending a commit |
| ` git rebase -i ` | Squashing commits together |
| `git reset --soft HEAD~number_of_commits ` | Squashing commits together using reset --soft |
| `git shortlog -s --author 'Author Name' ` | Number of commits by author |
| `git shortlog -s -n ` | List of authors and commits to a repository sorted alphabetically |
| `git shortlog -n --author 'Author Name' ` | List of commit comments by author |


### 👉 Git remote

| Command | Description |
| ------- | ----------- |
| `git remote show origin' ` | Show where 'origin' is pointing to and also tracked branches |
| `git remote -v ` |  Show where 'origin' is pointing to |
| `git remote set-url origin https://github.com/user/repo.git` |  Change the 'origin' remote's URL |
| `git remote add [NAME] https://github.com/user/fork-repo.git` |  Add a new 'origin' |


### 👉 Branching & Merging

| Command | Description |
| ------- | ----------- |
| `git branch` | List current branch |
| `git branch -a` | List all branches (local and remote) |
| `git branch -r` | Viewing remote branches|
| ` git branch -a --merged` | Viewing all branches that have been merged into your current branch, local and remote |
| `git branch -a --no-merged` | Viewing all branches that haven't been merged into your current branch, local and remote |
| `git branch [branch name]` | Create a new branch |
| `git checkout -b [branch name]` | Create a new branch and switch to it |
| `git checkout -b [branch name] origin/[branch name]` | Clone a remote branch and switch to it |
| `git branch -m [old branch name] [new branch name]` | Rename a local branch |
| `git branch -m [new-branch-name]` | Rename current branch |
| `git branch -d [branch name]` | Deleting a local branch |
| `git branch -D [branch name]` | Deleting a local branch if it hasn't been merged yet |
| `git push origin --delete [branch name]` | Delete a remote branch |
| `git checkout [branch name]` | Switch to a branch |
| `git checkout -` | Switch to the branch last checked out |
| `git checkout -- [file-name.txt]` | Discard changes to a file |
| `git merge [branch name]` | Merge a branch into the active branch |
| `git merge [source branch] [target branch]` | Merge a branch into a target branch |
| `git stash` | Stash changes in a dirty working directory |
| `git stash clear` | Remove all stashed entries |
| `git push origin branchname` | Pushing local branch to remote |



### 👉 Stashing files

| Command | Description |
| ------- | ----------- |
| `git stash` | Stash local changes |
| `git stash save "this is your custom message"` | Stash local changes with a custom message |
| `git stash apply` |  Re-apply the changes you saved in your latest stash |
| `git stash apply stash@{stash_number}` | Re-apply the changes you saved in a given stash number |
| `git stash drop stash@{0}` | Drops any stash by its number |
| `git stash pop` | Apply the stash and then immediately drop it from your stack |
| `git stash pop stash@{stash_number}` | 'Release' a particular stash from your list of stashes |
| `git stash list` | List all stashes |
| ` git stash show` | Show the latest stash changesh |
| `git diff stash@{0}` | See diff details of a given stash number |


### 👉 Checking what you are committing

| Command | Description |
| ------- | ----------- |
| `git diff` | See all (non-staged) changes done to a local repo |
| `git diff --cached` | See all (staged) changes done to a local repo |
| `git diff --stat origin/master` | Check what the changes between the files you've committed and the live repo |


### 👉 Synchronization of Changes

| Key/Command   | Description                                                                           |
| ------------- | ------------------------------------------------------------------------------------- |
| `git fetch`   | Downloads all history from the remote branches                                        |
| `git merge`   | Merges remote branch into current local branch                                        |
| `git pull`    | Downloads all history from the remote branch and merges into the current local branch |
| `git push`    | Pushes all the commits from the current local branch to its remote equivalent         |

*Tip: `git pull` is the combination of `git fetch` and `git merge`*


### Undo Changes

| Key/Command                 | Description                                                                                 |
| --------------------------- | ------------------------------------------------------------------------------------------- |
| `git checkout -- [file]`    | Replace file with contents from HEAD                                                        |
| `git revert [commit]`       | Create new commit that undoes changes made in [commit], then apply it to the current branch |
| `git reset [file]`          | Remove [file] from staging area                                                             |
| `git reset --hard HEAD`     | Removes all local changes in working directory                                              |
| `git reset --hard [commit]` | Reset your HEAD pointer to previous commit and discard all changes since then               |
| `git reset HEAD -- filename` | The version from the most recent commit              |


### Branches

| Key/Command                | Description                        |
| -------------------------- | ---------------------------------- |
| `git branch [branch]`      | Create a new branch                |
| `git checkout [branch]`    | Switch to that branch              |
| `git checkout [branch] -b` | Create and checkout new branch     |
| `git merge [branch]`       | Merge [branch] into current branch |
| `git branch -d [branch]`   | Deletes the [branch]               |
| `git push origin [branch]` | Push [branch] to remote            |
| `git branch`               | Lists local branches               |
| `git branch -r`            | Lists remote branches              |
| `git branch -a`            | Lists local and remote branches    |


### 👉 Sharing & Updating Projects

| Command | Description |
| ------- | ----------- |
| `git push origin [branch name]` | Push a branch to your remote repository |
| `git push -u origin [branch name]` | Push changes to remote repository (and remember the branch) |
| `git push` | Push changes to remote repository (remembered branch) |
| `git push origin --delete [branch name]` | Delete a remote branch |
| `git pull` | Update local repository to the newest commit |
| `git pull origin [branch name]` | Pull changes from remote repository |
| `git remote add origin ssh://git@github.com/[username]/[repository-name].git` | Add a remote repository |
| `git remote set-url origin ssh://git@github.com/[username]/[repository-name].git` | Set a repository's origin branch to SSH |

### 👉 Inspection & Comparison 👊

| Command | Description |
| ------- | ----------- |
| `git log` | View changes |
| `git log --summary` | View changes (detailed) |
| `git log --oneline` | View changes (briefly) |
| `git diff [source branch] [target branch]` | Preview changes before merging |

### History / log

| Key/Command                | Description                                                      |
| -------------------------- | ---------------------------------------------------------------- |
| `git log`                  | Show a list of all commits. shows everything commit ID, author, date and commit message                     |
| `git log --author=[name]`  | List of commits by author |
| `git log --oneline`        | Lists compressed version history for the current branch          |
| `git show [commit]`        | Outputs metadata and content changes of the specified commit     |
| `git blame [file]`         | Shows who changed what and when in file                          |
| ` git log -p`         | List of commits showing commit messages and changes                         |
| ` git log -S 'something' `   | List of commits with the particular expression you are looking for                         |
| ` git log --since=yesterday `   | Show a list of commits in a repository since yesterday |


## Useful Short Aliases 🌟🌟🌟

Git Add:

```.gitconfig
[alias]
    g = git
    st = status
    co = checkout
    ad = add
    cm = commit -m
    acm = commit -am
    ph = push
    rb = rebase -i
    fh = fetch
    df = diff
    br = branch -a
    re = reset HEAD\\^
    fu = fetch upstream
    rum = rebase upstream/master
    pom = push origin master
    list = config --get-regexp alias
    readme = !git add . && git commit -m "Update README.md" && git push origin master
    docs = !git add . && git commit -m "Update" && git push origin master
    update = !git fetch upstream && git rebase upstream/master && git push origin master

```

Git Add :

```.gitconfig
[add]
    git a = add
    git aa = add --all
    git ap = add --patch
    git au = add --update

```

Git Commit :

```.gitconfig
[Commit]
    git c = commit
    git ca = commit --amend
    git cam = commit --amend --message
    git cane = commit --amend --no-edit
    git ci = commit --interactive
    git cm = commit --message
```

Git Checkout :

```.gitconfig
[Checkout]
    git co = checkout
    git cog = checkout --guess
    git cong = checkout --no-guess
    git cob = checkout -b
```

Git Branch :

```.gitconfig
[Branch]
    git b = branch
    git bm = branch --merged
    git bnm = branch --no-merged
    git bed = branch --edit-description
    git bsd = branch --show-description (polyfill)
```

Cherry pick :

```.gitconfig
[Cherry]
    git cp = cherry-pick
    git cpa = cherry-pick --abort
    git cpc = cherry-pick --continue
    git cpn = cherry-pick -n (--no-commit)
    git cpnx = cherry-pick -n -x (--no-commit and with a message)
```

Git Log :

```.gitconfig
[log]
    git l = log
    git ll = log list with our preferred short settings
    git lll = log list with our preferred long settings
    git lg = log --graph
    git lo = log --oneline
    git lor = log --oneline --reverse
    git lp = log --patch
    git lfp = log --first-parent
    git lto = log --topo-order
```


Git Merge :

```.gitconfig
[merge]
    git m = merge
    git ma = merge --abort
    git mc = merge --continue
    git mncnf = merge --no-commit --no-ff
```
Git fetch :

```.gitconfig
[fetch]
     git f = fetch
```

Git pull :

```.gitconfig
[pull]
    git pf = pull --ff-only
    git pr = pull --rebase
    git prp = pull --rebase=preserve
```

Git Rebase :

```.gitconfig
[Rebase]
    git rb = rebase
    git rba = rebase --abort
    git rbc = rebase --continue
    git rbs = rebase --skip
    git rbi = rebase --interactive
    git rbiu = rebase --interactive @{upstream}
```

Git Remote :

```.gitconfig
[Remote]
    git rr = remote
    git rrs = remote show
    git rru = remote update
    git rrp = remote prune

```

Git Status :

```.gitconfig
[Status]
    git s = status
    git ss = status --short
    git ssb = status --short --branch

```


### Contributing
1. Fork it!
2. Create your feature branch: `git checkout -b my-new-feature`
3. Commit your changes: `git commit -m 'Add some feature'`
4. Push to the branch: `git push -u origin my-new-feature`
5. Submit a pull request
6. cheers!
