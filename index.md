# Git and GitHub Tutorial

Git is the free and open source distributed version control system that's responsible for everything GitHub
related that happens locally on your computer.

INSTALLATION & GUIS STAGE & SNAPSHOT
With platform specific installers for Git, GitHub also provides the
ease of staying up-to-date with the latest releases of the command
line tool while providing a graphical user interface for day-to-day
interaction, review, and repository synchronization. Working with snapshots and the Git staging area
GitHub for Windows
https://windows.github.com
GitHub for Mac
https://mac.github.com
For Linux and Solaris platforms, the latest release is available on
the oﬃcial Git web site.
Git for All Platforms
http://git-scm.com
git status
show modified files in working directory, staged for your next commit
git add [file]
add a file as it looks now to your next commit (stage)
git reset [file]
unstage a file while retaining the changes in working directory
git diff
diﬀ of what is changed but not staged
git diff --staged
diﬀ of what is staged but not yet committed
SETUP
Configuring user information used across all local repositories
git commit -m “[descriptive message]”
commit your staged content as a new commit snapshot
git config --global user.name “[firstname lastname]”
set a name that is identifiable for credit when review version history
git config --global user.email “[valid-email]”
set an email address that will be associated with each history marker
git config --global color.ui auto
set automatic command line coloring for Git for easy reviewing
BRANCH & MERGE
Isolating work in branches, changing context, and integrating changes
git branch
list your branches. a * will appear next to the currently active branch
git branch [branch-name]
create a new branch at the current commit
SETUP & INIT
Configuring user information, initializing and cloning repositories
git checkout
switch to another branch and check it out into your working directory
git init git merge [branch]
initialize an existing directory as a Git repository merge the specified branch’s history into the current one
git clone [url] git log
retrieve an entire repository from a hosted location via URL show all commits in the current branch’s history
INSPECT & COMPARE SHARE & UPDATE
Examining logs, diﬀs and object information Retrieving updates from another repository and updating local repos
git log git remote add [alias] [url]
show the commit history for the currently active branch add a git URL as an alias
git log branchB..branchA git fetch [alias]
show the commits on branchA that are not on branchB fetch down all the branches from that Git remote
git log --follow [file] git merge [alias]/[branch]
show the commits that changed file, even across renames merge a remote branch into your current branch to bring it up to date
git diff branchB...branchA git push [alias] [branch]
show the diﬀ of what is in branchA that is not in branchB Transmit local branch commits to the remote repository branch
git show [SHA] git pull
show any object in Git in human-readable format fetch and merge any commits from the tracking remote branch
IGNORING PATTERNS git stash
Preventing unintentional staging or commiting of files Save modified and staged changes
logs/
*.notes
pattern*/ git stash list
Save a file with desired patterns as .gitignore with either direct string
matches or wildcard globs. git stash pop
git config --global core.excludesfile [file] git stash drop
system wide ignore pattern for all local repositories discard the changes from top of stash stack
