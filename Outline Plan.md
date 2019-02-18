# How to use Git

### What is version control and why is it useful?

When tackling small projects, it is possible to hold all of the information in your head at once. When working on a larger project it can be helpful to break the project down into smaller sections and work on one section at a time. Version control allows you to segment projects into small sections to work on at a time.

Sometimes we start working on a small section of a project but then decide that we want to work on something else for a bit. Version control allows you to work on a small section of a project and then put it aside for some time and work on something else and then come back to the original section later.

When collaborating with other people it is important to define roles so that two people don’t work on the same thing at once. It is also good if we can comment on and review each other’s contributions before they are combined into the project. Version control allows powerful collaboration between project contributors.

Version control is not just for computer code, it can be used for reports, papers and much more.

### What is Git?

Git is a distributed version control system. It is a program installed on your computer that sets up the file structure to allows you to store snapshots of a project at a point in time. It is good for storing text based files. It is less good for binary type files and really bad for large binary files (typically those > 10 Mb).

*Demo: Save a snapshot using the command line.*
* git init
* git add
* git commit –m “Initial commit of repo”
* git status

### Making and navigating commits

You can make changes, commit these and then switch between these different versions. For our purpose for now, treat master as a pointer to the newest commit.

*Demo: Make another commit, switch between them.*

* git log (shows ID)
* git checkout (ID)
* git checkout master

### Using a GUI

Using the command line is very powerful but can be a bit fiddly. We can use a GUI to make it easier. I recommend GitHub Desktop, it is multi-platform, relatively simple and integrates well with GitHub (discussed later).

*Demo: GitHub desktop.*

### Syncing with GitHub

This is good but still quite local. What if we want to work with multiple people or across different machines? This can be done by using on online hosting service. A good option is GitHub. They offer free accounts for everyone although the free account does not give you private repositories – everything you do is made public. This is good unless you are working one something secret. However, as a student or researcher you can register with GitHub for a free Pro account which gives you access to all features of GitHub including private accounts.

*Demo: Show my GitHub account.*

Note that there are two forms of ID here. Each git commit has an embedded name and email address but this is just a vanity thing. These can be set to anything. Your GitHub username and password are separate but will be required to authenticate you as a user on GitHub.

*Demo: Add username and email in Github Desktop.*

*Demo: Sync repository with GitHub, show how it appears online.*

### Cloning a repository

If you want to work on another machine, you can then clone the online repository to a local machine.

*Demo: Clone a repo from my account.*

### Branching

When working on very simple project on your own you can just use a single sting of commits. However, if more than one person is involved ore the repository is public, it is a good idea to have different branches for different purposes. A branch is a name given to a series of commits. The default branch is called “master”. 

*Demo: Draw a diagram of branches on a whiteboard.*

A standard arrangement of branches is to have a “master” branch which contains the snapshot of the project which you are happy to release to the public. Then a working branch called “devel” is used to commit development snapshots of the project. Commits to devel should be working and complete but not necessarily yet ready for public consumption. Day to day changes should be made to “feature” branches. A new development branch is opened for each small section of work. Commits to a development branch do not have to be complete or correct.
Branches can then be merged together. Typically, once a feature branch has been completed it is merged into devel and when a number of features have been added to devel and the project is stable and in a good condition, devel is merged into master.

*Demo: Create devel and feature branches in GitHub Desktop. Commit some work to a feature branch*

### Merging

Merging branches is done through a pull request. This is a commit which bundles up a collection of commits from one branch and commits them to another branch. 
Demo: Show creation and merging of a pull request

### Conflicts

Hopefully, having multiple branches should mostly avoid two people writing to the same file. When two branches with edits to the same file are merged this causes a merge conflict. Git will try to automatically merge the files but if the same piece of text has changed then this conflict will have to be merged manually. This cannot currently be done in GitHub desktop but can either be done from the command line or from the web interface of GitHub. 
