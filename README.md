The whole purpose of this file is to practice how to use git in the terminal.

I installed git using: "brew install git" command. Because I tried installing it on my Mac M1, it initally would work because Homebrew is not configured to work on this processor. So I enabled the "Open using Rosetta" checkbox in the Get Info dialogue box for Terminal. Rosetta is a translator tool that allows Homebrew to work on an M1 ARM-64 processor.

Here are some of the commands I used:

git init

Use this tool to set up git in the current directory. It will set up some invisible files in the directory. You can see the by entering ls -a in the current directory in Terminal. The files are labeled "." , ".." and ".git". The ".git" file is used to track any changes to the files in the directory.

git add example.html

This is used to add a file to staging area. The purpose of the staging area is that you can add small changes to files, and then commit all of them at once.

git commit -m "My first commit."

This is used to commit all the files kept in the staging area. The purpose of the "-m" flag is to add a message to the commit, in this case: "My first commit."

I tried using "git commit ." instead of "git commit -m "MESSAGE"" but it prompted me with a dialogue box in the to enter the message. The problem was that I couldn't escape the dialogue box after I entered the message. There is nothing to explain how to exit in instructions. Online it said to press esc and then enter "wq" to write and quit, but that doesn't work. I wonder is it like this because I'm using the integrated terminal in VS.

EDIT: I tried it in an independent terminal, same problem.

git status

This command shows the current status of git for that directory. If everything has been committed, it should display: "On branch master
nothing to commit, working tree clean"

It can also display what files have been added to the staging area, as well as new files that have been created but not yet added or committed to git.

git log

This command diplays all the previous commits for the current branch. It will display the name and email of the committer, as well as a serial number for that commit, the time and date, and the message left by the committer.

You can exit the log by hitting the q key.

git remote

This command will display the name of the remote repository. Usually its' default name is "Origin".

You can use git remote -a to list the exact url of the remote repository.

git remote remove <remote name>

This command will remove any remotes associated with the local repository. By default, the remote name should be 'origin'.

git push

This command will push all commits up to the remote repository online, in this case GitHub.

git pull

This command is the opposite to git push. It will pull any changes to the remote repo and overwrite them on the local repo.

Niall Harrington, 29/1/2022
