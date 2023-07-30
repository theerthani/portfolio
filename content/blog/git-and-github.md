---
title: "Git and GitHub for beginners"
description: "Mostly used git commands in the dev role"
dateString: June 2023
draft: false
#tags: ["git", "DVA", "Certification", "Developer", "Developer Associate"]
weight: 101
cover:
    image: "/blog/git-and-github/cover.jpg"
---

<!-- # Credentials
### 🔗 [Certificate](https://drive.google.com/file/d/1VhFPfb1cc7ORFVqFetCvpiGLPE96ofg4/view?usp=sharing)

### 🔗 [Credly Badge](https://www.credly.com/badges/b08022fe-627a-4b78-8647-b42955f50767/public_url)

### 🎬 [YouTube Video](https://youtu.be/x88k9fuEDuE) -->

# Introduction

So, I recently completed a course on youtube called Complete Git and GitHub Tutorial by Kunal Kushwaha. This is by far the finest and clearest course I have ever come across. I learned a lot in the simplest method imaginable. I highly recommend it to everyone who's thinking of learning Git and Github. Here is what I learnt in a nutshell.

Now let's get right into the topic...

# What are Git and Github? What are they used for?

Let's assume you have an application and you want people to collaborate on it, or you just introduced some new features to your application, but the program crashes or it's no longer operating properly, and you want to revert to the original codebase as it was before adding the new feature...how would you achieve that? How could you store your codebase such that you could access it anytime you needed it and have it exactly as it was at the time?

It's like saving the history of your project.

Let's say in open-source, hundreds and thousands of people contribute to a project How do these people share their code? If you want to add some code or some functionality to a project, How can you do that?

You can do it via Git and GitHub...

So, Git and GitHub allow us to maintain a history of your project. Git helps us to know at what particular time which person made which change, where in the project. GitHub is a platform or online website that allows us to host our Git Repositories. A Repository is a folder where all the changes are made. We'll look more into it shortly.

A simpler use-case scenario would be, Consider an email service, we have all the servers and technology, and everything happening in the backend can be related to Git. And the interfaces to use this service - to send emails to people around the world, to have a GUI where you can see all your emails like Gmail, Outlook, yahoo mail so on and so forth, can be related to GitHub. Git is the version control system and there are so many other platforms that allow us to host these folders or repositories online so that other people from around the world can share, look, and contribute to our projects like GitLab and Bitbucket, but we'll be using GitHub, as it is the most popular among all the others.

Git - Free and open-source version control system.

# What is Version Control?

1. The management of changes to documents, computer programs, large websites, and other collections of information.

2. It is a way programmers track code changes.

3. we save our initial version of code into git and when we update our code again we can save it into Git again and again and again.

4. we can look back at all of the changes that we made over time.

5. we can go back to the previous version of the code if we need to.

Some terms that we come across are

Directory—> Folder

Terminal or Command Line—> Interface for Text Commands

CLI—> Command Line Interface

Code Editor—> Word Processor for Writing Code

Repository—> (Git repository) Project, or the folder/place where your project is kept.

GitHub—> A Website to host your repositories online.

# Downloading Git

To download Git go to https://git-scm.com/downloads and download Git for the respective OS. Go to the command line, type git and press enter. If you get some list as shown in the below figure then Git is correctly installed in your system.

![img1](/blog/git-and-github/img1.jpg)
 
# Initializing a Git Repository

Create an empty directory called project on the desktop. And you will be using Git to maintain the history of this project. Everything will be saved in the history when you create a file, delete a file, or make some changes to it. So, all of these histories are stored in another folder that Git provides us which is known as Git repository and is named ".git". The dot extension files are the files that are hidden.


How do we get this folder where all this history is being saved?

Command: "git init" (Initializing an empty git repository)

![img2](\blog\git-and-github\img2.jpg)

First, we created an empty folder called project on the desktop and we changed the directory into it with the "cd" command. The "ls" command lists all the files in the project folder which is currently empty. To initialize an empty git repository we used the "git init" command. And since ".git" is a hidden file we have to use the "ls -al" command. And we can see ".git/" is created.

![img3](\blog\git-and-github\img3.jpg)

And when we "ls" into the ".git" file you can see HEAD, config, description etc..which we'll be going through it shortly in this series. And don't worry about the (master) for now. Now you'll be able to maintain the history of the project. Any change made in this project now Git will pick it up.

# Making changes to the project

Let's create a file named fnames.txt using the touch command. As there's a change in this project, now does anyone in the world know that you made this change to the project? Is this history maintained in the Git repository right now?

The answer is NO.

How do you know what changes have been made to the project that are not currently saved in the history of the project?

Command: "git status" (changes that are not currently maintained in the history of the project)

![img4](\blog\git-and-github\img4.jpg)

Here this command is saying that someone has added the "fnames.txt" file and it is currently untracked. For example, If you share this project on GitHub no one knows that fnames.txt was added by you at this respective time.

If you want these changes to be maintained in your project history. What would you do?

let's compare this scenario to a wedding. How does the entire scenario of the Guest clicking photos with the couple play out? The First step would be for the Guests whose photograph has not been taken to go on to the stage. Then the photographer will click their picture, and then they will exit the stage. And now their picture will be saved in the history of that wedding in a photo album.

How does Git relate to this scenario?

The Guests whose photo has not been taken yet can be related to untracked files which can be shown by the git status command. You need to take a photo of these files so that you can save them in a Git repository. The only step remaining is, placing all these files whose photo has not been taken yet or whose history is not being saved in the project yet onto the stage. How do you do that?

Command: "git add ." or "git add filename" (everything in the current project directory that's untracked or currently not having its history, puts all those files in the staging area.)

![img5](\blog\git-and-github\img5.jpg)

we can also write the individual names of the files --> "git add fnames.txt".

How do we save these files to the Git repository?

Command: git commit -m "some msg here" ( -m is the message that you can add like "fnames.txt file is added".)

![img6](\blog\git-and-github\img6.jpg)

Here we added the file to the git repository and in the next command, we are checking if any other changes are made and are not saved in the repository. Here we made no changes other than creating a file so it shows that there's nothing to commit, and the working tree is clean.

How do you remove a file from the git repository?

command: git restore --staged "filename" (to remove a file from the git repository)

![img7](\blog\git-and-github\img7.jpg)

Here we added some text into the fnames.txt file and we checked the git status it shows fnames.txt in red colour which means it is not added to the git repository so we add it to the git repository with the command "git add ." And we removed a file from the git repository using the "git restore --staged fnames.txt" command. Now it again shows fname.txt in red colour.

![img8](\blog\git-and-github\img8.jpg)

Again here we added the file to the git repository and we commit the file by using the git commit -m command we can see 1 file is changed and 3 insertions were made.

Now, how do you see the entire history of the project?

command: git log (shows the entire history of the project)
![img9](\blog\git-and-github\img9.jpg)

Now let's make some more changes and commit them to the git repository.

![img10](\blog\git-and-github\img10.jpg)

Here we deleted the fnames.txt file and then commit the change to the git repository. Now let's take a look at the git log again.

![img11](\blog\git-and-github\img11.jpg)

It is updated. Now imagine you did it by mistake and you want to remove that commit. How would you do that?

You can't just remove a particular commit from the middle of the log, it has a hash id, and each commit is built on top of the other. If you want to remove the top two commits copy the hash id of the commit just below them, whatever commit you copy, all the above commits will be removed.

![img12](\blog\git-and-github\img12.jpg)

Here we can see that there's only one log in the git log, and the remaining two other commits that are on top of the existing commit are removed.

Now, you might be thinking what happened to the files that were modified, or changed in the previous commits? They are now in the unstaged area.

![img13](\blog\git-and-github\img13.jpg)

For example, if you don't want to delete these changes right now you can place them in the stash area.

Let's say you are working on a project and you have a few lines of code that you are working on, now you want to try out something new with a clean codebase. All the working files, files that you modified, you want to remove those, but you also don't want to save your progress as a separate commit. It's basically placing all your work somewhere else without making a commit and whenever you want those back you can get them back.

Command: git stash ( Getting the command to the stashing area)

![img14](\blog\git-and-github\img14.jpg)

Let us make some more changes to our project by creating surnames.txt and houses.txt files. We added all of those changes, you can see that in the git status command. Now, let's get all those changes into the stash area.

![img15](\blog\git-and-github\img15.jpg)

Now, if you can see we saved all our changes in the stash area, and if we run the git status command we can see the working tree is clean. In the log, we can only see our first commit since we didn't commit those changes, all these changes that we made are saved in the stash area.

Now if you want back all the changes that were saved in the stash, How can you do it?

Command: git stash pop (brings back all changes to the unstage area)

![img16](\blog\git-and-github\img16.jpg)

What if you want to delete all the changes that were saved in the stash area? How would you do it?

![img17](\blog\git-and-github\img17.jpg)

So, all those changes that were not committed and were saved in the stash area are now gone and we can't get those back.

So, that was how you can go back to your commits.


# That's all folks
That was all about the basic git commands Thanks a lot for reading!