READ ME FILE:::::::::CONFIGURE TOOLING
Configure user information for all local repositories
Sets the name you want attached to your commit transactions
$ git config --global user.name "Michael Kelem"
Sets the email you want attached to your commit transactions
$ git config --global user.email michaelkelem@me.com
Sets up credential helper
$ git config --global credential.helper osxkeychain
Enables helpful colorization of command line output
$ git config --global color.ui auto

CREATE REPOSITORIES
Create a repository (folder):
Mkdir repos/git-basics
Navigate to that folder and create a new local repository:
$ git init 
Check status of the folder:
$ git status 

Opt: Download a project and its entire version history:
$ git clone [url]

MAKE CHANGES
Review edits and craft a commit transaction
Lists all new or modified files to be committed
$ git status
Show file differences not yet staged:
$ git diff
Snapshots the file in preparation for versioning
$ git add [file] don’t use brackets, obviously
$ git add *.html
$ git add .
Opt: Shows file differences between staging and the last file version
$ git diff --staged
Opt: Unstages the file, but preserve its contents
$ git reset [file]
COMMIT:
Commit: Record file snapshots permanently in version history:
Do a git status before every commit.
To unstage a file:
$ git rm –cached <file>
Commmit:
$ git commit -m "[descriptive message]"

You’re now in VIM!
Write a message, like: Initial commit.
Then hit esc followed by :wq to escape VIM

GROUP CHANGES 
Name a series of commits and combine completed efforts 
$ git branch 
Lists all local branches in the current repository 
 $ git branch [branch-name]
Creates a new branch 
 $ git checkout [branch-name]
Switches to the specified branch and updates the working directory 
 $ git merge [branch]
Combines the specified branch’s history into the current branch 
 $ git branch -d [branch-name]
Deletes the specified branch 
REFACTOR FILENAMES 
Relocate and remove versioned files 
 $ git rm [file]
Deletes the file from the working directory and stages the deletion 
 $ git rm --cached [file]
Removes the file from version control but preserves the file locally 
 $ git mv [file-original] [file-renamed]
Changes the file name and prepares it for commit 
SUPPRESS TRACKING 
Exclude temporary files and paths 
 *.log
 build/
 temp-*
A text file named .gitignore suppresses accidental versioning of files and paths matching the specified patterns 
 $ git ls-files --other --ignored --exclude-standard
Lists all ignored files in this project 
SAVE FRAGMENTS 
Shelve and restore incomplete changes 
$ git stash 
Temporarily stores all modified tracked files 
 $ git stash pop
Restores the most recently stashed files 
 $ git stash list
Lists all stashed changesets 
 $ git stash drop
Discards the most recently stashed changeset 
REVIEW HISTORY 
Browse and inspect the evolution of project files 
$ git log 
Lists version history for the current branch 
 $ git log --follow [file]
Lists version history for a file, including renames 
 $ git diff [first-branch]...[second-branch]
Shows content differences between two branches 
 $ git show [commit]
Outputs metadata and content changes of the specified commit 
REDO COMMITS 
Erase mistakes and craft replacement history 
 $ git reset [commit]
Undoes all commits after [commit], preserving changes locally
$ git reset --hard [commit]?
Discards all history and changes back to the specified commit 
SYNCHRONIZE CHANGES 
Register a repository bookmark and exchange version history 
 $ git fetch [bookmark]
Downloads all history from the repository bookmark 
 $ git merge [bookmark]/[branch]
Combines bookmark’s branch into current local branch 
 $ git push [alias] [branch]
Uploads all local branch commits to GitHub 
$ git pull 
Downloads bookmark history and incorporates changes 


