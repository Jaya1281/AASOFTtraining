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

BRANCHES
Branches
Created Friday 06 January 2023

Why are branches useful?
Let’s say you are working on a project with a team. You’ve been working on a significant feature that requires a lot of changes to the codebase, and, all of a sudden, one of your team members tells you that there is a major bug, and you need to prioritize it and fix it.

You will find yourself in a confusing situation. Not only will you need to switch context completely by focusing on the new issue at hand, but where will you store all the code you have been working on for the unfinished feature? The bug has nothing to do with the unfinished feature. Fixing the bug along with the feature is going to create a lot of confusion for everyone.

You will somehow need to go back to a state or snapshot of the source code before you started making changes to it for the feature, fix the bug, and then go back to work from where you had left off. This scenario is precisely where Git branches can work in your favor.
--------------------
Branches in Git
In Git, you start with the one, primary branch called the master. This name is the default, given to the branch the moment you create your very first commit.

All the other commits you make from that point on are made on the master branch. Git, however, allows you to create as many other branches as you like.

You can create a separate branch that diverts away from the master and continue to do your work from there. The changes you make from that point forward and the commits you create will only be reflected in this branch and will not affect the source code in the master branch.

When you decide to create a new branch, what Git essentially does is create a new pointer to the current snapshot or commit to your project.

Therefore, the master branch has its pointer, and when you take a new branch out from the master branch, your new branch will have its pointer separate from the master.
--------------------

The ability to create different branches allows you to work freely on the source code without affecting any other person’s work or the actual code in the master branch.

All the changes you make will be restricted to your branch and will not spill over to alter things you do not intend to alter.

This also allows you to switch back and forth between contexts without having to worry about what will happen to each branch once you move to another. Git is super flexible in this regard and has made working in collaborative environments extremely easy and convenient.

Branches out of other branches
Git lets you create a branch from any other branch. A new branch doesn’t necessarily have to come out of the master branch.

CREATING A BRANCH

Creating a branch
Created Friday 06 January 2023

	Creating a Branch
	Learn how Git lets us create branches seamlessly and quickly.

	The git branch command
	The git branch command is a useful, multi-purpose tool that lets us do a lot of different things. When used as is (without any other options appended), the command will print out all the branches present in the repository and point out which branch we are currently on.
	--------------------
	The git branch command will print out the master branch with a prepended asterisk. The asterisk denotes that this also happens to be the branch that is currently active in our repository. In other words, we are currently using the master branch. If there were more branches, their names would also be listed.
Eg: git branch
*master

After you create the new branch, enter the plain git branch command to double-check that it works. You will know if it works because the name will now be printed along with the master branch. One critical point to realize if you want to create a new branch in this manner is that you will still be using the parent branch in your working directory. That should be easy to identify, given the asterisk (*) next to the master branch name.

This is a significant point that you shouldn’t ignore. If you want to now switch to the newly created branch from the master, that is where the git checkout command will help you.

RENAMING A BRANCH

Renaming branches
Created Friday 06 January 2023

you might find yourself in a situation where you have to rename the new branch you’ve created. Git provides a very convenient way to do so.

We will, once again, rely on the git branch command to rename an existing branch.

Let’s say you have been working on a significant feature. You want to add authentication to your application. The branch that you are making all the relevant changes to is called new_branch. The name new_branch is not related to what you are doing in any way. No one else will be able to identify what this branch is about, either. It is a better idea to call it something like authentication_feature.

Renaming a branch you are currently on#
Switch over to the branch you have to rename with the following command:
git checkout new_branch
Use the git branch command appended with the -m flag to provide the new name:
git branch -m authentication_feature

--------------------
To verify that you were able to rename the branch, use the plain git branch command to print out the list of branches and you will be able to see that the current branch you are on is now called authentication_feature instead of just new_branch.

Renaming a branch without switching over to it
What if you want to rename the branch but want to remain on the branch that you are originally using at that moment? The git branch command can do that too.

The general syntax for doing so is:

git branch -m old_name new_name
Therefore, if you want to rename new_branch as authentication_feature but also want to remain on the master branch, you would enter this command in the terminal:

git branch -m new_branch authentication_feature

SWITCHING BETWEEN BRANCHES

Switching between branches
Created Friday 06 January 2023

Switching Between Branches
Learn how Git allows us to quickly switch between different branches. This lesson also discusses an alternative way to create a new branch with Git.
The git checkout command
Using the git branch command lets us create new branches seamlessly. However, the problem is that even though we get to create new branches, we still don’t actually know how to switch over to those branches and use them. The git checkout command lets us do just that.

Once you create a new branch (let’s call it new_branch), use the following command while still currently on the master branch, to switch over to that new branch:

git checkout new_branch

To verify that you did switch to the master branch, use git branch to list all the branches in your repository. You will see the asterisk next to master, indicating that you are using the master branch once again.

Creating new branches with git checkout
Right now, we need to rely on entering two separate commands to create a branch and then switch over to it.

What if we could create a new branch that is a child of the branch that we are currently on and directly switch over to it with just one command? Well, git checkout lets us do that too.

**The -b flag**
Using the -b flag along with git checkout provides us with a convenient way to first implicitly execute git branch and then run git checkout to switch over to the newly created branch immediately. As an example, enter the following command in the terminal below:

git checkout -b new_branch

DELETING A BRANCH

Deleting a branch
Created Friday 06 January 2023

Deleting a Branch
--------------------

Learn how to delete a branch from your local repository in this lesson.
Using git branch to delete a branch
We can use the git branch command to create, list, rename, and delete a branch. In this lesson, we will take a look at how we can delete a branch from our repository.

The -d flag
The syntax for deleting a branch is fairly simple:

git branch -d <branch_name>

As always, to double-check that the deletion process has been executed successfully, you can rely on the simple git branch command to verify this. The branch that is deleted should no longer be listed in the output.

Note: You can’t delete the branch you are currently on. You will need to switch over to another branch and then delete it.

GIT STASH

Git Stash
Created Friday 06 January 2023

Learn how to use the git stash command to stash uncommitted changes in this lesson.

The git stash command
Often, you will be working on your separate branch and making some changes that you don’t want to commit just yet, but you will be required to switch over to another branch to do something else in between.

You don’t want to get rid of the changes but also don’t want to commit them either. This exact scenario is where you can use the git stash command.

git stash temporarily stores the staged and modified files in a kind of a cache, all the while making the working branch directory clean.

You could either stash all of the uncommitted changes you have made in the branch or stash individual files.

git stash

When to use git stash
Let’s say you are currently working on a branch called new_branch and you made some changes to the file1.txt. You can verify which branch you are on by using the command git branch and check which files have changed using the command git status.

Now, for some other task, you are required to move to the master branch. However, the changes to file1.txt aren’t ready to be committed yet, but you also don’t want to lose the changes.

Ideally, you want to switch to the master branch where the changes you have made to file1.txt do not exist. Once you are done working with the master branch, you want to go back to new_branch and continue working on the changes you had started.

Here is what you will need to do:

Enter the command git stash while you are still on new_branch.
Enter the command git checkout master to switch to the master branch.
After you have done whatever you needed to do on the master branch, you will, once more, enter git checkout new_branch to switch back again.
You want your changes to be present once again, so you will enter the command git stash apply.
Enter git status to verify if your changes are back or not.
And there you have it. The uncommitted changes you had made are all back again in your working directory, and you will be able to continue with your work uninterrupted once more. You didn’t have to commit your unfinished work, and you were able to switch branches and still keep your changes! A win-win situation.
--------------------
Had you decided not to use git stash, Git would have prevented you from switching over to any other branch if the other branch had changes that would be overwritten with the new uncommitted changes (since the changes in the other branch would be out of context). You would have to do one of the following:

Commit your unfinished work, switch branches, do your work, switch back to new_branch, and revert the most recent commit.
Completely get rid of the changes you had made, switch branches, do your work, switch back to new_branch, and start all over again.
In case the altered file does not conflict with the branch you plan to switch to, Git will let you switch over without errors and the uncommitted changes would still be present in that branch as well.

GIT MERGE

GitMerge
Created Monday 09 January 2023

Git Merge
Learn how Git allows the merging of different branches with one another in this lesson.

Git allows us to create separate branches and work on them independently without interference from changes in other branches. The option to create different branches enables a very convenient workstream where you, or a group of people can work on new features and ship them out only when they are complete.

Creating new branches is only one part of the complete workflow. Git is a convenient version control tool because not only can we create new branches, but we can also merge a branch with another as well. Once we have finished working on a new feature on a separate branch, we can then merge or combine this branch into the master branch. All the changes we made in the feature branch will now be present in master as well.
--------------------

Merging a branch with the master branch
Let’s try out the git merge command with a scenario.

You have a master branch and another branch called the feature_branch.

In the master branch, you will have file1.txt, and, in the feature_branch, you will create another commit where you will add another file, file2.txt.

Once you decide to merge the feature_branch with the master, the master branch should have both file1.txt and file2.txt.

The steps mentioned above have already been executed in the terminal provided later in the lesson. You can verify which branch contains which files by switching to each branch and entering the terminal command ls to identify the file names.

Now, from this point forward, this is what you will need to do:

Switch to the branch in which you want to contain the merging branch that you would like to merge. For example, if we want to merge the feature_branch into the master, we will switch to the master branch so that it is the active one. Use git branch to verify which branch you are currently on.
git checkout master
Now that you are using the branch that will contain the merging branch, we will move on to the git merge command. The basic syntax for it is as follows:
git merge <branch_to_be_merged>
Therefore, for this example, we will enter the following command:
git merge feature_branch

--------------------
Verifying after merging
You can also verify if the commit and changes from the feature_branch are accessible in the master using the commands ls and git log. Using ls should list both file1.txt and file2.txt. Moreover, git log should list the commits from the master branch and the feature_branch.

MERGE CONFLICTS

merge conflicts
Created Monday 09 January 2023

Merge Conflicts
Learn about merge conflicts and how they occur by reading through this lesson.

What is a merge conflict?
Merge conflicts occur, most commonly, when more than one contributor is working on a project. A merge conflict takes place when a file changes at the same line in different branches or if a file is deleted in one branch, but in another, its contents are updated. When the branches are merged, Git won’t be able to infer which change it should keep and which one it should discard. At this point, it becomes necessary for a developer to resolve this merge conflict.

--------------------
How a merge conflict can occur
Let’s look at an example of how a merge conflict can occur. We will create a new branch called feature_branch and switch over to it from master using the following command:

git checkout -b feature_branch
Now that we’re at the feature_branch, we will update file1.txt.

echo 'Updated file1 in feature_branch' > file1.txt
Next, we will create a new commit and make sure that the change in file1.txt becomes part of the snapshot by entering this command:

git commit -m 'updated contents of file 1 in feature_branch'
We will then switch back over to master and update file1.txt again:

echo 'Updated file1 in master' > file1.txt
We will proceed to create another commit that will contain the new change but this time for the master branch.

git commit -m 'updated contents of file 1 in master' 
Try entering the commands mentioned above in the terminal provided below. You are already provided with a working project directory and initial commit:

Now that we have two branches, with both containing commits that have changes affecting the same file, we can try to see what will happen when the two branches are merged. Enter the following command in the terminal below. All of the commands mentioned above have already been executed in that terminal, so you only have to merge the branches:

git merge feature_branch
Make sure that you are currently on the master branch and that the working directory is clean and has no modified files.
If a merge conflict occurs, the image below shows what it will look like:

# CONFLICT (content) : Merge conflict in file1.txt
Automatic merge failed; fix conflicts and then commit the results

When you try to merge 'feature_branch' with master, this is the expected output you should get.

RESOLVE MERGE CONFLICTS

resolving merge conflicts
Created Monday 09 January 2023

Resolving Merge Conflicts
This lesson will teach you ways in which you can resolve merge conflicts.

In the previous lesson, we looked at how merge conflicts can occur and worked with an example to create a merge conflict. We made changes to the same file, file1.txt, in two different branches and tried to merge them. Git can’t decide on its own which change should remain so a developer would have to resolve the conflict themselves.

In the terminal below, we have a merge conflict that has taken place when we try to merge a branch called feature_branch with master.

What to do when a merge conflict occurs
In the terminal provided above, our merge process was halted because of a conflict. We need to make sure that the conflict no longer exists so that the merge can be completed.

Identify a merge conflict in the code
We made changes to file1.txt in both branches, so what does Git view as a conflict, and how does it depict it? Well, if you open up file1.txt in any text editor of your choice, you would see that Git has highlighted what it considers as a conflict in a syntax similar to this.

<<<<<<< HEAD
=======
>>>>>>> feature_branch
We can try to view the contents of the file using nano, vim, or simply using cat <file_name>, and we will note that the contents of the file have somewhat changed.

Edit the file with the conflict
Now that we know where the merge conflict is, let’s see what we can do to fix the issue. The conflict in file1.txt occurred because both branches had modified the text in it, and Git isn’t sure which version to keep. The changes that each branch made are separated by line:

=======
It is up to us to decide which change should be kept. Since we are still on the master branch, we can proceed with keeping the text:

Updated file1 in master
After our updates, file1.txt should look something like this:

Resume the merge process
Now that we have updated file1.txt, we can proceed with making sure that the feature_branch is officially merged with the master. From this point on, the process is fairly straightforward. While making the necessary changes to the file, we inevitably modified it. Therefore, we will need to make sure Git marks these changes and adds file1.txt to a staged state. We can do that with the command:

git add file1.txt
Now, we simply need to create a new snapshot or commit that will contain our new changes.

Let’s create a new commit with the command:

git commit -m 'fixed merge conflict in file1.txt'

You can verify that the merge worked by viewing the contents of file1.txt and also by using git log. The most recent commit will contain a special line that tells us that this was a merge commit. It will begin with the word Merge.

Summary
And there you have it. You should now have a fairly good idea of what to do when a merge conflict arises.

Update the files that contain the conflicts
Use git add to add the updated files to staging
Create a new commit that contains the files which have been updated to resolve the conflicts

REMOTE REPOSITORIES
What is github
Created Monday 09 January 2023

A code hosting platform
GitHub is a code hosting platform. Git creates a local repository on every contributor’s computer, which contains the entire codebase and its revision history. You can consider GitHub as a platform that stores the whole codebase in a remote repository.

By enabling the creation of remote repositories, GitHub allows developers to have a unified source of truth for their source code. They can treat that as the main version from which every other contributor creates local repositories.


If your codebase is in a remote repository on GitHub:

Every other contributor who wants to work on the project will know that they can get the code from the remote repository.
Any updates that they make and then want to share can push those changes to the remote repository instead of sending each contributor the updates one by one.
While Git is a convenient command-line tool that you can utilize to manipulate and update the repository, GitHub serves as an interactive interface where you can navigate through your codebase and the revision history it has gone through effortlessly.

Creating an account
To create your repositories on GitHub or contribute to other open source projects, you will need to create a personal account on GitHub.

Open source projects are those software whose source code is available for free. GitHub has one of the largest communities of open-source projects.

Once you have your own GitHub account with your unique username and ID, you will be able to contribute to a plethora of public repositories and projects. You will also be able to create your own repositories.

CREATING REMOTE REPOSITORIES

Creating remote repository
Created Monday 09 January 2023

Creating your first repository on GitHub
Let’s see how you can now create a repository on GitHub. Once you are logged in and are on the homepage, you will notice a button on the top left side titled ‘New’

Once you click on the ‘New’ button, GitHub will redirect you to a different page where you will have to provide a name for the repository. Additionally, you can add a description of your repository. You may provide the sample information given below for your first repository:

Name: test_project
Description: “The first repository that I will use to learn Git commands.”
Public and private repositories
Besides providing a name and description, you need to choose whether you want your repository to be public or private.

As the name suggests, a public repository is accessible to anyone who wants to look it up. Anyone is able to see the codebase and clone this repository to their local machine for use.

A private repository, on the other hand, is only visible to people who you have chosen. No other person is able to view it.

Since you are creating your first repository and will only be using it to learn Git and GitHub, it would be wise to opt for a private repository.

--------------------
The README file
Another decision you will have to make while creating a new repository is whether or not you’ll create a README file.

The README file contains necessary information about the repository. For example, it might include the following information:

Instructions on how to clone and run the source code on local machines
A basic guide on how to use the library or package that the repository contains
What to do if you come across certain kinds of bugs
Licensing and copyright information
Contact information about people who contributed to the code
For now, let’s opt to create a repository that won’t have a README. GitHub will provide you with the option to choose to initialize a project with or without a README:
--------------------

The .gitignore file
Finally, you will be able to choose whether or not you want a .gitignore file with your repository. The purpose of the .gitignore file is to filter out files and subdirectories in your repository that you do not want Git to keep track of. Therefore, any changes you make to files contained in a .gitignore file will not be marked as modified, staged, or committed by Git.

Here is an example of a .gitignore file:

# if you dont want to track a single file
abc.txt

#if you dont want to track files with a certain extension
*.pyc

# if you d

For now, you can opt not to create a .gitignore file with your repository. Once you fill in all the options, you will be ready to create your GitHub repository.

PUSHING CODE TO GITHUB

Pushing code to github
Created Monday 09 January 2023

When you create a remote repository on GitHub, it will initially be empty. You will need a way to get your local repository to the remote repository on GitHub.

Git provides a convenient way to make this happen:

You will need to add the link of the remote repository to a local repository.
You will then push your code in the local repository to the remote one.
The git remote and git push commands let us do this, respectively.

Note: When you’re done configuring the new remote GitHub repository, you will be redirected to a page that will contain all the relevant links you will need to set up the repository locally.
--------------------
The git remote command#
The git remote command allows Git to track remote repositories and connects local repositories to those remote ones. When we create a new remote repository on GitHub, we can provide its link to our local Git repository along with a reference name to that link, which we can use for our convenience.

For example, let’s say we want to add our remote repository to the local one. Therefore, the command we will enter in the terminal will be:

git remote add <name> <url_to_remote_repository>
We will name our remote repository link origin:

git remote add origin <url_to_remote_repository>
Note: The name origin is essentially a more human-readable way to link to the remote repository instead of always having to use the actual URL. origin is simply a conventional name, but we can use any other name as well.

To verify that the remote link works, we can use the plain command git remote, and it will list all the remote repositories we have added. If the name origin is present in the list, we will know that the remote repository is accessible for us to retrieve or send code for our local repository.
--------------------
The git push command
Once we have added the remote repository URL to our local one, we will want to push or upload our local code and its revision history to the remote repository. This can be done using git push.

The git push command will update the remote repository code with all the updates that were made in the local repository.
You can make changes to a local branch and create several commits. Once you are done, you can push your changes to the remote repository.

For example, if you are working on the master branch and have added a remote repository and given it the name origin, you will need to enter the following command to push your changes to the remote repository:

git push origin master
In other words, the basic syntax for pushing a branch to a remote repository is:

git push <remote_repository> <branch_name>
And there you have it. You have successfully pushed your code to a remote repository.

GIT CLONE

GitClone
Created Monday 09 January 2023

Git Clone
Learn how to clone remote repositories to your local machine in this lesson.The git clone command
We can use the git clone command to clone or copy the entire codebase of a project from a remote repository and set it up as a local repository on our machines.

While cloning the project, two more actions occur as well:

The git clone command will also create a remote link to the remote repository being cloned and name it origin. This is similar to manually entering the command git remote add origin <remote_repository_url>.

It will copy and set up the primary branch, which is the master branch in most cases, as the active branch in the working directory.

You can test this command out yourself in the terminal provided at the end of the lesson. You can look up a repository on GitHub that you like and clone it.

git clone <link_to_repository>
--------------------
Shallow cloning
Sometimes, we might come across a remote repository that we want to clone, but its commit history might be too long, resulting in longer times to download and clone. This occurs when the project is very large and has a very large commit history. You can opt to clone the commit history up to a certain point by using the --depth flag.

Try the following command in the terminal provided below:

git clone <repository_url> --depth 1
You can change the depth number according to your requirement.

Try it yourself
In the terminal provided below, try out the commands to clone a repository from GitHub on your own. You can clone a repository that you’ve created or clone any other repository you want. As an example, try cloning this repository:

https://github.com/githubteacher/github-slideshow.git
This is a simple public repository for getting familiar with GitHub. You don’t need to worry about the contents of the repository itself.

You will need to enter the following command:

git clone https://github.com/githubteacher/github-slideshow.git
--------------------
When you successfully clone the project, all of the project’s files will be available to you locally in a separate directory. Use the ls command to view the directory name. You will need to switch to the project directory using the cd command and verifying the contents.

Try entering other Git related commands as well, such as git log and git branch, to test various aspects of the newly cloned repository.

GIT FETCH

GitFetch
Created Monday 09 January 2023

The git fetch command
git fetch is used to download the updated changes from a remote repository. If you are working in a collaborative environment and want to see how other people might have updated the remote repository between now and the last time you viewed it, you will need to use the git fetch command.

The benefit of git fetch is that it merely downloads the latest changes and does not affect your local codebase and updates. The git fetch command is useful if you want to know how the remote repository has changed but don’t want those changes to alter your local setup.

For example, let’s say you are working on the master branch, and in the meantime, other collaborators have made a few changes to the remote repository. You want to take a look at those changes but don’t want them to interfere with your branch just yet. Therefore, you can use the following command:

git fetch origin
origin, in this case, is the name of the remote repository. You will be able to view the updated commit history and the latest commits as well.
--------------------
ou can switch over to the fetched branch using the git checkout origin/master command.

Once you’ve decided to merge those changes with your local master branch, you can use the following command:

git merge origin/master
The git merge origin/master command will make sure that the latest changes in the remote branch are merged with the local version of the branch as well.
--------------------
In the terminal provided below, the GitHub repository we cloned in the previous lesson is available to you. Enter the following command to verify which branch you are currently on:

git branch
You will notice you are currently on the master branch. Try entering the following command:

git fetch origin master
Followed by:

git merge origin/master

The Already up-to-date message means that the local branch and the remote one have no pending changes and are identical.

GIT PULL

GitPull
Created Monday 09 January 2023

The git pull command
Similar to git fetch, the git pull command also downloads the latest updates from the remote repository. In many ways, it does what git fetch also does but with the added function of merging the newly downloaded remote repository with the latest commits into the local version of the branch.

Let’s say you’ve been working on creating a new feature for your project on a branch with another team member. Both you and the teammate have been working tirelessly, and making changes and committing them regularly. There will be countless times when you will need to make sure that your branch is in sync with your teammate’s branch.

Both of you will push your commits to the remote repository and pull each other’s changes. This is where the git pull command comes in handy.

git pull origin branch_name
The command above will download the latest changes from the remote repository and merge them into your local branch, ultimately updating your branch HEAD to point to the latest commit in that branch.
--------------------
In the terminal provided at the end of the lesson, the GitHub repository discussed in the previous two lessons is available to you. Enter the following command to check which branch you are currently on:

git branch
You will note that the currently active branch is master. Now, enter the following command to pull the remote master branch locally:

git pull origin master
You will notice an immediate difference between how the git fetch command worked and how the git pull command downloaded the remote branch. While it took two steps to download and merge the remote branch, you got the very same result with only one command using git pull.
While the git fetch command only downloaded the remote branch, the git pull command downloaded and merged the remote branch into the local one as well.

GIT REVERT

Reverting to ealier commit
Created Monday 09 January 2023

Remember the git reset command which is useful in cases where you want to undo a recent change? Well, it is only useful when you wish to make changes to your commit history locally. However, this command is not helpful if we have pushed our commits to a remote repository. Changing the commit history on a remote repository will result in a history conflict with everyone who has a clone of that repository. The remote commit history will begin to differ from theirs.

We can add a new commit to the remote repository that contains content from an older commit instead of the commit which contains any mistakes to address this issue.
--------------------
The git revert command
In order to set an old commit, which is free from any known flaw, and have it set as our latest commit, we can use the following command:

git revert HEAD~1
git revert will add another commit on top of the commit that contains flaws in your code.

PULL REQUESTS

Pull Requests
Created Monday 09 January 2023

What are pull requests
Pull requests are a way to formally contribute to a project without disrupting the workflow of the other team members and also a way to maintain a check and balance of the contributions added to the project source code.

Platforms such as GitHub have a straightforward and convenient way to create pull requests. These allow other contributors to review and evaluate your submitted work and provide comments and suggestions accordingly.

Go over to the project repository on GitHub
Switch to the pull requests tab
Click on the ‘New pull request’ button on the top right
Select the appropriate base branch (the branch with which the other one is meant to be merged) and the branch you want to compare changes with
And that’s it! You’ve created your own pull request!

Think of pull requests as the intermediate step before you can merge your contribution into the source code. Pull requests serve as barriers for the source code not to be polluted with modifications that are not vetted. Once the pull request is approved, the changes in the pull request are merged with the source code.

Pull requests are a user-friendly way of keeping a record of all the modifications that your project’s source code goes through, the discussions that took place regarding the proposed changes, and also who the responsible stakeholders were for each change that was incorporated.
--------------------
Pull requests are not restricted to Git
Pull requests aren’t specific to Git, and there is no special command that is used to create pull requests. They are simply a method or process that is extremely beneficial to developers working on projects with teams or for open source projects. You can create pull requests on GitHub, Bitbucket, or any other similar platform.

Pull requests have several functions
The image provided above shows the GitHub page for a pull request.

The pull request displays the list of commits that will be merged and also displays the branch that will be merged and the branch with which the other branch will be merged. In this case, the branch task/user-posts-in-newsfeed will be merged with master.

The pull requests page allows contributors and reviewers to start a discussion by adding comments and details regarding the changes proposed.

You can ask other contributors to review your pull requests. Pull requests make the following tasks easier, quicker, and better documented:

Merge the changes in the pull request
Approve the pull request
Request more changes
Close the pull request without merging the branch if the proposed changes aren’t needed
Pull requests also allow you to view the entire list of commits and who made the commit.

Pull requests also allow you to view the files that will be changed and how they will be changed in a convenient manner. Each line of code is colored, which represents whether that line was added, deleted, or was left unchanged. The green color shows that the new line was inserted, and a red-colored line would mean the line is meant to be removed. 

MANAGING CONFLICTS IN REBASE

Managing conflicts in rebase
Created Monday 09 January 2023

Managing Conflicts When Rebasing
What happens if the rebase operation runs into conflicts? Let's take a look.

Why conflicts can occur when rebasing
What if you decided to rebase your branch with the latest version of the parent branch, which contains new commits that have changed the same files at the same location within those files where you have also included your changes?

Do note that when a rebase is carried out, it takes place commit by commit. Therefore, what would happen if one of the parent branch’s commit conflicted with the changes one of your branch’s commit was trying to introduce? Git is not intelligent enough to decipher which changes to keep and which ones ought to be discarded.

That’s where it will prompt the rebase not to be completed and will require you to handle the conflict by picking out the changes you want to keep and discarding the rest. Once you are done with that, you can choose to continue the rebase operation that had been paused. You can also choose to completely abort the rebase operation altogether if such a situation arises. You might realize that a large number of conflicts could occur with each new commit that is applied, making it troublesome to resolve every conflict.
Let’s try to see how the example in the illustration above plays out in an actual terminal. There are two branches already created, master and new_branch.

Both branches contain commits that alter the contents of file1.txt. There is one new commit on the master branch which was added after the new_branch had already been created. This commit is not a part of new_branch's commit history.

In the terminal provided at the end of the lesson, checkout to the new_branch so that it becomes the currently active branch:

git checkout new_branch
In the working directory, enter the command:

git rebase master
You will get an error stating that the rebase could not be completed:
This is how Git will display the conflict in file1.txt, by highlighting the content from each branch allowing you to visually differentiate it and also decide what to keep:
Using any text editor you like, you can modify the contents of the file by removing changes you don’t want and keeping the ones you do. In the terminal provided below, you can either use nano or vim.

Once you are done, you will enter the command:

git add file1.txt
This will make sure that Git has added your changes to file1.txt to be staged. You can proceed with the rebase process now. Enter the following command to do so:

git rebase --continue

DIFF BETWEEN REBASE AND MERGING

Diff between rebasing and Merging
Created Monday 09 January 2023

git merge and git rebase are often used for very similar tasks. These commands are used to alter commit histories of branches and integrate one branch with another.

What is the difference between rebasing and merging?
The significant differences to note between the two operations are as follows:

Merging results in a new merge commit for the branch with which another is merged.
Rebasing doesn’t result in any new commits. It updates the rebased branch’s commit history to look like it was taken out from a more recent version of the parent branch.
--------------------
When should you merge and when should you rebase?
If more than one person is working on a particular branch, then, in that case, rebasing it would not be a good idea. Other collaborators will be routinely pulling the latest version of the branch on their local machines, unaware that someone rebased it, fundamentally altering its state and leading to inconsistent branches for everyone. However, if you’re the only person working on the branch, then rebasing is a very viable option to make sure that your branch is taken from the latest version of the parent branch.

If you don’t want to alter the commit history of a branch, you should use git merge. git merge will retain the commit history as it is and add a new merge commit instead, while rebasing a branch will alter the commit history for that branch. This will be a less intense change for people collaborating on a branch since one person merging another branch with it would result in a new commit that others can then simply pull locally from a remote repository. If the branch were rebased and pushed to the remote repository, when others pull it, the updated branch would conflict with the local one even though it would be the same branch.

Note: Reverting a rebase is a much more complicated process than reverting a merge in case there are many conflicts.