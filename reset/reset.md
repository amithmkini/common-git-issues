# Reset in Git

Considered as one of the high risk commands, there are high chances that there are unintended side effects to this command. Please use this with care.

### Oh no! I accidentally made a commit that broke my application.

Do this only if you have not pushed the code to GitHub

- Use the command: `git log` to find the list of commits. 
- Now, copy atleast the first 8 characters of the commit hash you want to revert to: (looks like `f417a5630ebf1f5152c1b88adafaa99607420420`)
- If you do not wish to keep the newer changes, do: `git reset --hard f417a563`
- If you want to keep the changes as an uncommited changes, do: `git stash`, `git reset --hard f417a563`, `git stash pop`

If you have pushed the code, use revert instead:
- `git revert <commit hash 1>..<commit hash n>`
- `git commit` to confirm the commit. Revert creates commits that essentially undo the older commit changes, but keeps the older commit, thus not breaking the flow of the commit tree.