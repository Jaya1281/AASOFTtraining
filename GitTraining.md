This file will have content on Git training and version control
Guide to Git & version control
Created Thursday 05 January 2023

Our goal
This course teaches beginners about version control and how to start incorporating Git for solo projects or how to contribute to other collaborative works that rely on version control.

The goal of this course is to make sure you grasp the various concepts of Git and how they can be useful. You do not need to have any prior experience with version control to follow along with this course, but some basic knowledge about terminal commands will be a significant advantage.
A guide for beginners
This course is a guide for beginners. Therefore, we will begin with the very basics and gradually move on to more complex concepts and terms. Initially, you will learn about version control and what makes Git such a popular tool for version control.

Version control is a crucial skill for every developer.
The course will explain how to set up Git configurations on your local machine. You will also learn about GitHub. In addition to providing familiarity with GitHub, this course will also teach you how to create remote repositories (more on this later) and local repositories. By the end of this course, you should have a solid grasp on several important Git concepts such as:

Commits
Branches
Merging
Rebasing
With that said, let’s proceed forward and take a more detailed look into version control.
--------------------
What Is Version Control?
This lesson dives into version control and explains why it is useful for large projects.

We'll cover the following

Why do we need version control?
Keep track of changes to the codebase
Ease in collaborative work
Version control tools

Why do we need version control?
Let’s say you create a project and have worked on it for over a month. While adding a new feature, you realize that something you did a week back won’t allow your new feature to work properly. You decide to revert those changes but aren’t sure if you have made similar changes in other files as well.

What if there was a way for you to identify what exact changes you made and where in your code you made them? That’s where version control can help you out.

Keep track of changes to the codebase
In the simplest of terms, you can consider version control to be a record of all the changes that your software code goes through. Version control systems allow you to keep track of how your project changes over time, with additional information about why and when each change was incorporated.

Ease in collaborative work
Version control systems can solve many problems that you, as a developer, will face. They keep track of how your source code changes, who is changing it, and when. It also allows you to revert those changes as you deem fit.

Because of all these advantages, version control makes collaborative work easier.


Version control makes collaborative work easier.
If you opt not to use version control for your project, sooner or later you will find yourself copying your project directory into multiple different versions. You might name them according to whichever priority you want to assign, such as ‘final_version,’ ‘latest_version,’ or something along those lines. However, it is not a sustainable approach, especially when working collaboratively with a team. Version control systems essentially formalize this process, so you don’t have to manually do it yourself.

Version control tools
Version control tools have been continuously updated over time, following the ever-changing workflows that developers choose to use. In more recent times, Git has become the tool of choice for version control.

In the next lesson, we will look into what Git is and what makes it such a widely used software for version control.
--------------------

Why Is Git So Important?
In this lesson, you will learn about Git and why it's so widely used.

We'll cover the following

What is Git?
Git snapshots
Git states
What is Git?
Git is a distributed version control software. As a result, a complete copy of the entire codebase will be available on every contributor’s computer; we can also call this codebase a local repository.

Git tracks the local repository, maintains a record of all the changes that occur within it. It removes the hassle of keeping multiple versions of the project in separate directories and also makes sharing changes to the source code between collaborators seamless and quick.

The Git logo
The distributed nature of Git makes it unique and efficient. Since every contributor or collaborator has their own ‘clone’ of the source code in their local repository, it allows Git to track, add, or revert changes very quickly. Git uses the local database to keep a record of the changes to the project files.

Distributed version control allows everyone to clone the entire codebase in 'local repositories'.
--------------------

Git snapshots
A Git snapshot is, essentially, the state of the project files at a certain point in time. In other words, instead of maintaining a record of file-based changes that occur over time, Git will store that data as a snapshot, which is the entire state of the project at that particular moment. While saving the snapshot, it will keep those files that did get updated and only keep references of files that didn’t change from the previous snapshot to avoid duplicates.

How a snapshot keeps track of new changes.
--------------------

Git states
Git has three primary states that it allows the project’s files to acquire. The three states are:

Modified - files that have been changed, but the changes have not yet been marked by Git. These changes won’t become part of the next snapshot.
Staged - the changes have been tracked by Git and will be marked as such in the next snapshot.
Committed - the changed files that have successfully become part of the latest snapshot.

How a file changes states.
Before we move on to learn more about Git, let’s briefly go over how you can use the terminal to edit text files using text editors and terminal commands.
--------------------
Basic Terminal-Based Text Editors
A basic summary of how you can edit files or make changes using terminal commands or terminal-based text editors.

We'll cover the following

Using the echo command
Using nano

The goal of this course is to cover the necessary Git commands and concepts. To do that, we will have to alter the content of some files as we go along. We have a variety of options to opt for in this regard. Since you will be able to test out all the commands within the lessons, it’s going to be beneficial if you have an idea about how you can modify plain text files using the terminal itself.

Normally, we use fancy text editors and notepad applications, but, for this course, we will opt to use plain terminal-based commands and terminal-based text editors to make changes and updates.

Using the echo command
We can add text to a file using the echo command which is shown below:

echo "Hello world!" >> file1.txt
Note: The echo command can’t be used to add text in arbitrary points in the file. It will, instead, append the text at the end of the text file.

Try out the command in the terminal provided below. The terminals in this lesson already have a file called file1.txt, which is present in the working directory test_project. You can verify this by using the command ls.

To view the contents of the file itself, use the command cat file1.txt, or you can opt to use one of the terminal-based text editors, such as nano, which is discussed later in this lesson.
--------------------
This is a very simple and straightforward way to add text to a file.

Using nano
nano is a very simple terminal-based text editor that comes installed as a default with Linux. Click anywhere on the terminal widget below, and then execute the following command.

1
nano file1.txt
Terminal 1
Terminal
From this point forward, you will simply enter any text you plan to add to the file. By using the commands provided at the end of the terminal window, you can save those changes and exit the editor.

Note the ^ key. It represents the ctrl key on your keyboard.

In order to get help on the commands, press ctrl + g (hold down the control key while hitting g).
If you want to exit nano, press ctrl + x. If there are unsaved changes, nano will prompt you to save those changes before exiting.
Note: The ^ is the control key on the MAC keyboard and Ctrl key on Windows.

The image shown below is of the user interface you will encounter when you use the nano command.


nano <file_name>
That is more or less the gist of the very basics you will need to know about terminal-based text editors for this course. Alternatively, if you are comfortable with using any other text editor such as Vim, feel free to use that as well.
--------------------

This is test line
Creating a new project with git
Created Thursday 05 January 2023

1. Let’s start by creating a new working directory or folder in the terminal. We’ll call the new working directory test_project. You can create a new directory by using the following command: mkdir test_project
2. Once we have created the new directory, we will need to set that as the current working directory. We will do that by entering the following command: cd test_project
3. Once the test_project directory becomes the working directory, which will be initially empty, we will create a plain text file. Let’s call it file1.txt. We will create the new file using this command: touch file1.txt
4. To verify that the file was created, enter the plain command ls in the terminal window below. It should print all the folders and files present within the working directory, which, in our case, is file1.txt.

GIT INIT COMMAND

The git init command
Now that we have a working project directory with a file in it, we can initialize Git to track this project and its contents:
the git init command simply creates an empty repository. Therefore, your project will not automatically come under the ambit of version control with this command alone. What git init does, however, is create a .git directory. The .git directory will contain all the metadata that Git will require for tracking the project.

The subdirectory .git will contain several files and more subdirectories that Git will use to keep track of changes in the project.

--------------------
The git add command

Now that we have a project that has a file and an empty Git repository set up, we want Git to track the contents of the entire project.

At this point, the git add command will help us. Enter the following command in the test_project directory: git add .( dot)
--------------------
The git status command
To verify what state your files in the repository are in, you can use the git status command. It doesn’t change or update anything. Instead, it prints out which files are modified, staged, or untracked.
Git commit
Created Thursday 05 January 2023

Learn how to create your first snapshot with the git commit command.

The git commit command
Once we have a local repository that is tracking our project, we will move towards creating our very first commit.

A commit is a snapshot of the entire state that your project is in at that moment. Git keeps track of your project through a series, or chain, of commits. The most recent snapshot of your repository is referred to as the HEAD.

As soon as you create a new commit, it will directly link to the HEAD. However, since the latest commit is now the most recent one, it will be considered the HEAD instead, replacing the previous one.

The commit message
The structure of the commit command is very straight forward:
git commit -m "What changes occurred within the commit."

From the snippet above, you will notice the -m flag, followed by a string. The string is called the commit message. Usually, the commit message is a phrase that describes what changes or modifications occurred within the commit.

Our first commit
Let’s move on to creating our first commit. Since it is the first one, let’s have the commit message be “initial commit.”

Enter the following command in the terminal below and see what happens. Please note that before we create a commit, it is a wise decision to use the git status command to check which changes will be reflected in that commit.
Once you have successfully created your first commit, try entering git status again and check what has changed. All the staged files become part of your initial commit, and there are no other changes to commit anymore.

--------------------
undo a commit
Created Thursday 05 January 2023

Undo a Commit
Let’s learn how to undo or reset a commit from our local repository in this lesson.
While working on any project, it is common for us to make mistakes. For example, we might accidentally delete files, misunderstood the requirements and code up something else. Or just got stuck in some bug, and now we do not have a working copy of our code.

There are several ways to fix these problems. We can simply nuke the local repository and create a new clone. However, this approach will only work if we have a remote repository to fall back on.

Another option would be to undo all the changes that we have made. But, if our changes are present in multiple files, this process can be time-consuming. There is an easier alternative.

he git reset command
The git reset command is a useful tool to help fix past mistakes. There are a lot of ways it can be used depending on the scenario.

Unstage files
Suppose you have staged some files to be committed. But later you change your mind and decide to unstage a few or all of them. Maybe because you do not wish to commit them. To achieve this, we can simply use the following command:git reset
--------------------
The --soft flag
If you want to modify or update your changes from the previous commit but don’t want to remove them completely, you can use the following command:git reset --soft HEAD~1
he --soft flag changes the state of the committed files to “staged." You can see more clearly what happens when you run the command in a terminal. Note how the output that the git status command produces will change after you reset the most recent commit using the --soft flag. This flag preserves the changes.

The --hard flag
If you want to completely get rid of the changes that were part of the recent commit, you can use the --hard flag instead. It will reset the changes and not preserve them. 
git reset --hard HEAD~1

The git reset command can prove to be very useful if we want to update or revert changes made in older commits. The examples shown above dealt with reverting only the most recent commit. You will have noticed the reset commands used in this lesson had the HEAD~1 portion. The number indicates how many commits you want to go back.

If you’re going to reset several older commits, you can change the number to how many commits you want to be reverted, and that will land you back to an earlier snapshot of your project. For example:

git reset --soft HEAD~2
//GIT LOG//
Git log
Created Thursday 05 January 2023

The git log command
Git tracks changes to a project by maintaining a chain of snapshots or commits. If you are working on a collaborative project, you will find that your repository will have commits from different contributors. The git log command lets you view the commit history for your project.

Entering the git log command in your terminal will allow you to view a list of commits or snapshots that will be sorted based on the time they were created with the latest one at the very top.

Each log will contain information about the author of the commit, displaying their username and email that we set with the git config command (discussed in one of the previous lessons).

The log will also contain a timestamp of when each commit was created along with the commit message.

One more critical piece of information that the log will show is the 40-characters-long unique hash. The hash is vital because it helps identify commits and acts as an excellent way to secure the commit.

The commit hash uses the cryptographic hash function SHA-1. The hash key allows each commit to have integrity. If the hash were to change, we would be able to identify that the commit has been tampered with.
