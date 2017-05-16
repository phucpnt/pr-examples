# Managing revert PR

Use case for doing this: when we don't want to roll-out a feature or we want to revert bad PR

### Practice yourself:

1. Clone the repo
2. Create the PR from commit-1 to master PR#1
3. Create the PR from commit-2 to master PR#2
4. Create the PR from commit-3 to master PR#3
5. After merging the PR#1, the PR#2 will have the conflict. 
6. Resolve the confict for PR#2
7. Merge the PR#2
8. Merge the PR#3

### Revert the PR
Let assume, the PR#1 is not pass the QA. And we want to do the release without PR#1. 
Follow the steps on branch `master`:

1. Get the git commit of PR#1 from the `git log`.
2. Run the command `git revert -m 1 <commitID>`
3. Resolve the conflict
4. Commit the update

Tip:
* to reset branch to commit, use `git reset --hard <commitID>`.
