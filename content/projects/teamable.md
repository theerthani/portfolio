---
title: "Introducing Teamable: Empowering Users to Connect and Collaborate with Ease!"
description: "A fullstack application which helps users to update and edit their user profiles"
dateString: June 2023
draft: false
#tags: ["git", "DVA", "Certification", "Developer", "Developer Associate"]
weight: 102
cover:
    image: "static/projects/teamable/teamable-front.jpg"
---

<!-- # Credentials
### 🔗 [Certificate](https://drive.google.com/file/d/1VhFPfb1cc7ORFVqFetCvpiGLPE96ofg4/view?usp=sharing)

### 🔗 [Credly Badge](https://www.credly.com/badges/b08022fe-627a-4b78-8647-b42955f50767/public_url)

### 🎬 [YouTube Video](https://youtu.be/x88k9fuEDuE) -->

# Project Highlights

1. Setting up a Jira Board for scrum project
2. Develop the 1st version of Teamable app using HTML, CSS and vanilla JavaScript
3. Replace vanilla JavaScript of the Teamable app with Vue.js
4. Implement Backend using node.js
5. Connect backend to MongoDB database to persist data
6. Write test for teamable app
7. Package teamable application
8. Creating Linux server on a cloud platform, connect to it using SSH
9. Preparing deployment server for Teamable app
10. Deploy Teamable V1 on the server

# Background Story

My main goal was to learn and grow as a developer. Developing a web application using Agile Scrum allowed me to gain hands-on experience with industry-standard development methodologies, making the learning process more structured and effective. The idea of creating an application to manage employees resonated with me as it had real-world significance. Employee management is a crucial aspect of any company's operations, and by building this tool, I saw the potential to make a positive impact on businesses and their employees.
I was keen on understanding how Agile Scrum worked in practice. By using this methodology for the project, I aimed to experience its benefits first-hand, such as improved collaboration, adaptability to changing requirements, and the incremental delivery of features.

In addition to the before mentioned reasons, another significant motivation behind undertaking this project was the desire to gain a comprehensive understanding of the various roles within an IT team. By taking on the responsibilities of the product owner, software developer, tester, and systems administrator, I gained the ability to pivot seamlessly between tasks, troubleshoot issues efficiently, and optimize the development process.


# What is Software Development Workflows

In a project team, we don't only have Software developers, we also have other roles which are equally important in the development process. Here are the brief tasks and responsibilities of all the roles in a project team.

1. In a project team, the Product owner identifies the product requirements by talking to the customer and Translates these        requirements into tasks for the development team.
2. Next comes the Software Developer who program the application.
3. Tester tests the application extensively.
4. Finally Systems Administrator creates and configure server, runs the application on it and make it accessible to the users.They also manage and administer database, configure networking for servers.

The most important thing in Software development is collaboration. Though all the roles in a project team has different tasks and responsibilities all the tasks are connected. Product Owner needs to explain the product details to software developers in detail, otherwise the developers end up developing the product which is completely different from what the customer wants.Developers need to communicate with testers when they are done coding the feature, and tester needs to communicate to the developer regarding the bugs that they've found in testing process so the developers can fix those issues. Developer need to tell the systems administrator what the software needs, to run on the server.
Since there are multiple developers, testers and sys admins, they need to communicate with each other. so collaboration is important.

There are some online tools for collaboration between the team members such as Jira software(Issue and Project Tracking Software). Jira is widely used in software development teams. The uses of Jira is as follows: 

1. Documents the whole interactions between the team memebers
2. Other team members know about the decisions etc
3. Be able to group chat
4. Has a nice visualization overview of what features are being developed, what features are tested, and which feature/fix was released.




# Downloading Git

To download Git go to https://git-scm.com/downloads and download Git for the respective OS. Go to the command line, type git and press enter. If you get some list as shown in the below figure then Git is correctly installed in your system.

![img1](\blog\git-and-github\img1.jpg)
 
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