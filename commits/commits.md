# Commit issues

### *** Please tell me who you are

This issue often arises for people who just installed Git. Basically, git wants to know the name and email of the user who is creating the commits. This is to ensure that other people watching the commits gets to know who made the changes. The error message is pretty self-explanatory in solving the issue.

To resolve this:
- Open the terminal, and type: `git config --global user.name "Your Name"`
- And: `git config --global user.email "you@email.com"`
- Make sure that the email id matches with the email of your GitHub account. This will ensure easy navigation to your profile by just a click on your name.

### Editing a commit

There are chances that you may commit a error in your commit message. Or you might have forgotten to add a file in the commit. Instead of creating another commit, if you haven't pushed anything, you can amend the commit.

To do this:
- `git commit --amend`. This opens an editor where you can change the commit message.
- To add missing file, do `git add forgotten-file` and then `git commit --amend` to make the changes.