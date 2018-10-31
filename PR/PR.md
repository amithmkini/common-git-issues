# Pull request issues

Issues often happen when a pull request is created to some other repo and they merge it. Some of them are discussed here.

### Your branch is `x` commits ahead, `y` commits behind owner:master

This occurs when you have created a pull request containing multiple commits and the owner has decided to "squash and merge" your commits.  
In "squash and merge", multiple commits are combined into one single commit. When this happens in the owner's repository, that single commit
will be counted as a new commit and your multiple commits are considered as commits not belonging to the master branch, even though
they are included in the owner's repo. 

To resolve this:
- In the local system, pull your forked version of the repository.
- Add the upstream URL for the repo as the owner's repo URL. `git remote add upstream https://github.com/<owner>/some-repo`
- Now rebase your local copy with the owner's copy. `git rebase --onto upstream/master`
- Now you have a repo which has identical history to the owner's repo, but not your remote repo.
- Finally, execute the following: `git push --force origin master`
