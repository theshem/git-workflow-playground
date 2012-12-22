Git workflow playground
=======================

* adding some changes _by_ the **owner**.
* some changes by a contributor.
* yet another change _by_ the **owner**.
* yet another change by a contributor.
* final change _by_ the **owner**.
* final change by a contributor.

## Contributing to a project

**The first time you start contributing:**

1. Fork the repo on github.   
2. `git clone https://github.com/<your-username>/repo.git`   
3. `cd /path/to/repo`   
4. Add a remote called e.g. `upstream` points to the original repo:   
`git remote add upstream https://github.com/<repo-owner>/repo.git`   
5. Assuming the main branch of original repo is `master`, pull repo before editing:   
`git pull upstream master`   
6. Create a new branch called e.g. `topic-branch` to develop and test features without putting your main project at risk.   
`git checkout -b topic-branch master`   
7. Do some changes.   
8. Commit snapshots of those changes into your repo (use `-a` flag to add files on the stage `git add .`):   
`git commit -a -m "your commit message here"`   
9. Push `topic-branch` commits to your remote repo stored on GitHub, using `origin` remote.   
`git push origin topic-branch`   
10. Send a [pull request](https://help.github.com/articles/sending-pull-requests).

- - -

**Now and later on:**

1. Make "master" the active branch.   
`git checkout master`   
2. Pull original repo before editing:
`git pull upstream master`   
3. Make "topic-branch" the active branch.   
`git checkout topic-branch`  
4. Use `rebase` or `merge` to make sure that your commits go on top of the "master" branch:
`git rebase master` or `git merge --no-ff master`   
5. Do some changes.   
6. Commit snapshots of those changes into your repo (use `-a` flag to add files on the stage `git add .`):   
`git commit -a -m "your commit message here"`   
Push commits to your remote repo stored on GitHub. If you want to keep all branches up-to-date, do NOT add `topic-branch` at the end of the code below:   
7. `git push origin`   

I hope this approach will be helpful for you ;)
