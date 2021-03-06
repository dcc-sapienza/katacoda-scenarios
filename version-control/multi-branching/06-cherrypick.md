As you work on different features of the projects, changes get committed to one branch or another. As the project exolves, you might want to reorganise the commit history and reposition individual commits. 

---

Using `merge` will bring all commits from a branch into another. Commits remain, however, individual. One or more commits from a different branch can be brought into the currently checked-out one using `git cherry-pick <commit>`, where `<commit>` indicates a commit identifier (which can be shortened).

**Running `git log --oneline` shows the shortened version of the commit identifiers. In this case, since you might want the log of another branch (the one you want to cherry-pick from), you could use `git log --oneline <branch>` or `git log --oneline --all`.**

> *Note that `<commit>` can also be a **range** of commits, specified as `<commit1>..<commit2>`, but this is prone to conflicts. It can also be a branch name: this would cherry-pick all commits – but in this case, a merge is probably the best option.*

One instance in which this is particularly useful is when a commit is accidently made to the wrong branch. You can switch to the correct branch and cherry-pick the commit to where it should belong.

The cherry-picked commits are automatically committed to the new branch, with the same commit message. To modify this behaviour, `git cherry-pick` accepts the `-e` option to allow edits of the commit message, or the `-n` option to avoid committing the changes.

## Exercise

**Some collaborator created a *model.py* file, which is vital for our project. However, they created it in the wrong branch.**  
**From `master`, create a new `model` branch, then use `git cherry-pick` to apply the commits regarding *model.py* to that branch.**