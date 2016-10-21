# rebase-workflow
Some commands that I use during a rebase workflow


- `git checkout <your branch>` if you’re not on it already.
- `git fetch origin` to download any new work that's been done on the remote repository.
- `git rebase -i origin/master` starts an interactive rebase session, rebasing your changes on top of master.
- In the interactive rebase view, use `r` to rewrite message, `f` to squash and throw away message, `s` to squash into previous commit, `p` to use the commit as is.
- The view uses an editor called vi.  To edit the text in vi, use `i` for insert mode, `ctrl-c` to exit insert mode, `:wq` to save and quit.
- In the next view, it’ll ask you to use vi again to rewrite any messages from `r` or `s` commits.  Use `i`, `ctrl-c` and `:wq`.
- You should get a message saying rebase was successful.  If not, stop there and review what you’ve done.
- `git log -3` to look at your new commit history after you’ve rebased (`q` to exit the log command if necessary).  Pay attention to not only your own commits but that the commits before yours match what is remote master.
- `git diff` to look at the code diff of the newly rebased code (`q` to exit the diff command if necessary).
- `git push --force origin <your branch>` to upload your rebased code to the remote repository.
