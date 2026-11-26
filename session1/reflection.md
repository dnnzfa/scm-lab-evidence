Part 5: Reflection and Evidence

1.	Why is a commit history useful when maintaining software? Give one concrete maintenance situation (for example finding when a bug appeared) and refer to your own commits.
-	A commit history records every saved change along with a message showing what was done, which makes maintaining software much easier over time. If a bug or broken feature appears, I can check the log to see which recent change caused it and trace back to what happened. For example, in scm-lab-evidence, I made separate commits like "Add README for SCM evidence repository", "Add student name to README", and "Add .gitignore" so each step is clear. If a bad update were later added to README.md or .gitignore, I could inspect the history and see exactly when that line changed instead of guessing.
2.	Explain the difference between Git and GitHub, using your two repositories (the exercise repository and scm-lab-evidence) as examples.
-	Git is the version control tool running locally on the user's computer in Git Bash (~/Documents/scm/scm-lab-evidence). It tracks file snapshots in the user's local .git database, supports local branches such as session1-notes, performs merges, and lets the user inspect history (git log) or discard local edits (git restore).
-	GitHub is the cloud-based hosting and collaboration platform where remote repositories live (https://github.com/dnnzfa/scm-lab-evidence.git) and the user's GitHub Skills exercise repository. It stores remote copies of branches, provides a web interface for creating files/edits or pull requests, and acts as a shared hub for syncing code across machines or teammates.
3.	In the GitHub Skills exercise you worked on a branch and used a pull request instead of changing main directly. What risk does this reduce?
-	Working on a separate branch and opening a pull request instead of committing directly to main reduces the risk of breaking the main/working codebase with incomplete, buggy, or unreviewed changes and overwriting teammates' work without coordination. It isolates experimental edits, allows diff review and checks before merging, and keeps main in a clean, reliable state.
4.	State which of your commands changed only your computer and which changed GitHub.
-	Commands like git init, git add, git commit, git switch, git merge, git branch -d, and git restore only changed files, branches, or local history on the user's computer. Even git remote add origin only saved the GitHub URL in the local Git setup, while git clone and git pull only brought data from GitHub down to the user's computer. The command that actually changed GitHub was git push, which uploaded my local commits to the remote repository.

## Concept Table from Part 1

| Term | Definition |
| --- | --- |
| Repository | A project folder along with its complete commit history. |
| Working tree (working directory) | The actual files in the folder that a person views and edits. |
| Staging area (index) | The list of changes selected to go into the next commit. |
| Commit | A saved snapshot of project changes with a message, author, and timestamp. |
| Branch | A movable pointer to a line of commits used for working on changes separately. |
| Merge | Combining changes from one branch into another. |
| Remote | A version of the repository hosted elsewhere, such as `origin` on GitHub. |
| Push / Pull / Clone | Uploading commits to a remote (`push`), downloading and merging remote changes (`pull`), or copying a remote repository onto a machine (`clone`). |