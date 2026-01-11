# Git, GitHub, and GitHub Desktop: Complete Guide

## Table of Contents

1. [Understanding Git, GitHub, and GitHub Desktop](#understanding-git-github-and-github-desktop)
2. [Getting Started with GitHub](#getting-started-with-github)
3. [Setting Up GitHub Desktop](#setting-up-github-desktop)
4. [Signing In and Configuring GitHub Desktop](#signing-in-and-configuring-github-desktop)
5. [Creating Your First Repository](#creating-your-first-repository)
6. [Understanding the GitHub Desktop Interface](#understanding-the-github-desktop-interface)
7. [Adding Files to Your Repository](#adding-files-to-your-repository)
8. [Understanding Commits](#understanding-commits)
9. [Publishing Your Repository to GitHub](#publishing-your-repository-to-github)
10. [Viewing Your Repository on GitHub](#viewing-your-repository-on-github)
11. [Managing Files with Git](#managing-files-with-git)
12. [The .gitignore File](#the-gitignore-file)
13. [Tracking Modifications](#tracking-modifications)
14. [Deleting Files](#deleting-files)
15. [Reverting Changes](#reverting-changes)
16. [Introduction to Branching](#introduction-to-branching)
17. [Creating and Working with Branches](#creating-and-working-with-branches)
18. [Merging Branches](#merging-branches)
19. [Pull Requests and Team Collaboration](#pull-requests-and-team-collaboration)
20. [Best Practices](#best-practices)

---

## Understanding Git, GitHub, and GitHub Desktop

It's important to understand the differences between these three related but distinct tools, as they can get kind of confusing!

### Git

Git is the actual version control software. It was originally meant to run on the command line, and a lot of developers run Git this way. Git is the underlying technology that powers version control.

### GitHub Desktop

GitHub Desktop is a program that runs Git on your computer and allows you to do most of the Git command line commands, just through a more visual program interface. Instead of typing commands in a terminal, you interact with Git through a graphical user interface (GUI).

**Note for Beginners**: A lot of people like using the command line to run Git commands. However, for beginners, it's generally easier to use a tool like GitHub Desktop. If you're already familiar with Git and GitHub, you can of course use whichever tool you prefer.

### GitHub

GitHub is a website where you can host your Git repositories, collaborate with other users, and discover other open source repositories. GitHub was acquired by Microsoft and is free to use. GitHub is the most popular place to store your remote repository.

---

## Getting Started with GitHub

### Creating a GitHub Account

If you don't have a GitHub account yet, you can go to **GitHub.com** and sign up for a new account. The process is straightforward and free.

### Why You Need GitHub

Once you're signed up, we're going to use the GitHub Desktop app to run GitHub on our computer. The most popular place to store your remote repository is GitHub. It's owned by Microsoft and is free to use, making it an excellent choice for both personal and professional projects.

---

## Setting Up GitHub Desktop

### Downloading GitHub Desktop

To download GitHub Desktop, go to **desktop.github.com** and download and install the program. Follow the installation wizard with default settings, and the application will be installed on your computer.

### First Steps

Once you've installed the app, go ahead and run it. The first thing you'll want to do in GitHub Desktop is to sign in to your GitHub account.

---

## Signing In and Configuring GitHub Desktop

### Signing In to Your GitHub Account

1. Go to **File > Options** in GitHub Desktop
2. Navigate to the **"Accounts" tab**
3. Click the **"Sign in" button**
4. A window will prompt you to sign in using your browser
5. Click **"Continue with browser"**

### Browser Authentication

Your default browser on your computer will try to log in to your GitHub account. Log in to GitHub if it's prompting you to. If you get a pop-up window that says "Choose an application to open the x-github-desktop-auth link," make sure **GitHubDesktop** is selected.

### Verifying Successful Sign In

Once you're signed in, your computer should go back to GitHub Desktop. To make sure everything worked:

1. Go back to **File > Options > Accounts**
2. You should see your GitHub username and profile picture on the right side

If you see your information, you're successfully signed in!

### Setting Up Global Git Configuration

Next, we want to set up our Global Git configuration:

1. In the Options, go to the **"Git" tab**
2. You should see:
   - Your GitHub username listed under **Name**
   - A `users.noreply.github.com` email under **Email**
   - A **"Default branch"** option

### Configuring the Default Branch

Under "Default branch" select either **main** or **master**.

**Important Note**: Master used to be the default branch on Git, but currently GitHub and other places are using "main" as the default, and it's the recommended standard to use going forward.

### Saving Your Settings

Once your settings are set, make sure to click the **"Save" button**, even if you didn't make any changes on this screen. GitHub Desktop automatically populated these fields when you logged in, but you'll still need to manually save them.

---

## Creating Your First Repository

### Initiating Repository Creation

Now, we're going to walk through the basics of a Git workflow with a test project. Feel free to follow along!

To create your repository:

1. Go to **File > New repository**
2. Fill in the repository details in the dialog that appears

### Repository Details

#### Name Field

In the **Name** field, write the name of your test project. GitHub repos need to be named a string without spaces. Usually, you would use hyphens between words.

Example: `test-repo` (not "test repo")

#### Description Field

The **Description** field will let people who see your repository on GitHub know what it's about. This is optional but recommended.

#### Local Path

The **Local path** is the folder where you want to create your repository.

**Example**: If you use Windows, you might put your repos in the `Documents/GitHub` folder. You can choose another location if you prefer.

#### README File

Check the box asking if you want to initialize this repository with a **README file**. This file lets you write a more detailed description about your project that will show up on GitHub, and you can always edit it later. This is optional but generally it's a good idea to have one.

#### Git Ignore

The **Git ignore** field lets you select types of files that you don't want to add to the repository. You can usually leave this at "None" and then ignore files later on while you're coding. We'll get to that later in this guide.

#### License

The **License** field tells people what they are allowed to do with your code in the repository. Since a lot of open source exists on GitHub, most people select the **MIT License** which allows people to copy, distribute, and modify your code. If you leave it blank, your project will be licensed with standard copyright.

**Additional Resource**: You can read more about open source licensing at **ChooseALicense.com**

### Creating the Repository

Once all your options are selected, click **"Create repository"**. It may take a few seconds, but GitHub Desktop should create and automatically load the repository.

---

## Understanding the GitHub Desktop Interface

### The Repository Bar

At the top under the menu bar, you'll see another bar with information about your repository:

- **Left side**: The current repository that's open
- **Next to it**: What branch you're currently on (we'll talk more about branches later, but know that a branch is one version of the codebase, and you can have multiple branches)
- **Right end**: Information about publishing this repository to GitHub

### The Main Panel

Under the repository bar is the main panel which has a left sidebar with important tabs and information.

### The Left Sidebar

The sidebar has two main tabs:

#### Changes Tab

The **Changes tab** shows all the modifications you've made to your repository that haven't been committed yet. This is currently blank since we haven't added any files or made any code changes yet.

#### History Tab

The **History tab** shows your commit history. It displays an "initial commit" with the files generated by GitHub Desktop when we created this repo.

### The Commits Panel

If you have the "Changes" tab selected, at the very bottom of the sidebar is the **commits panel**. A commit is the "save point" that you can create during development that includes a set of code changes that you want to track. We'll use this panel to create commits.

---

## Adding Files to Your Repository

### Creating Your First File

Let's start making some code changes to see what happens in Git. In your VS Code:

1. Go to **File > Open Folder**
2. Select the location where you created your GitHub repository

### Git Installation Prompt

If you see an alert message from VS Code saying "Git not found," this is asking if you want to download the original version of Git that runs on the command line. You can either dismiss the alert, or if you think you might use Git on the command line at some point, you can click the "Download Git" button to download and install it.

#### Git Installation Settings

If you do decide to download and install Git for the command line, here are the recommended settings:

1. For most of the settings, go with whatever is pre-selected
2. **Most importantly**, for the default editor used by Git, set that to **VS Code** instead of Vim
3. For the name of the initial branch when you're making a new repo, override the default branch name and use **"main"**
4. For everything else, just hit the "Next" button and then finish installing

### Creating an HTML File

Now let's create a new file:

1. Click the **"New file" icon** in the left sidebar of VS Code
2. Create an **index.html** file

In the file, type an exclamation point and press Tab to use Emmet to create boilerplate HTML markup:

```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Document</title>
  </head>
  <body></body>
</html>
```

Then save the file.

---

## Understanding Commits

### What Happens When You Add a File

If you go back to GitHub Desktop, you'll see that in the left sidebar under the "Changes" tab will be the **index.html** file. There's a **green plus icon** on the other side of the filename. This means that Git has detected a new file, and wants to add it to your repository and track any future changes.

On the right panel you'll see the actual code changes that you made in the index.html file. Right now we've added new code, which is why the lines of code are highlighted in green.

### Staging Files

You'll also see a **checked checkbox** to the left of the filename. Checking this box will **"stage"** the file, which means that you want to include this file change in your next commit.

### Creating Your First Commit

Let's create our commit to add the index.html file to the repository:

1. In the bottom commit section, there is a field where you can add what we call a **commit message** describing what the change is
2. GitHub Desktop has automatically populated the field with text saying "Create index.html"
3. You can keep this as your commit message, or write your own
4. There's also a larger **description field** under it, where you can optionally write a longer description
5. At the bottom is a button saying **"Commit to main"**

This means that clicking it will create a commit on your main branch.

### Executing the Commit

Click the button to create the commit.

### After Committing

After we commit, the "Changes" tab is empty. And if we click on the "History" tab in the left sidebar, we'll see that commit that we just made, along with the code changes from that commit.

---

## Publishing Your Repository to GitHub

### The Publish Panel

You may have noticed up at the top on the right a panel that says **"Publish this repository to GitHub."** Since we created this repository locally, it won't exist on GitHub until we publish it.

### Publishing the Repository

Click the button to publish it. A window will pop up, with:

- The name of the repository
- The description
- A checkbox for if you want to keep the repo private

For testing purposes, you might want to keep this private since it's not for any real code. Then click **"Publish repository"** and it will get published to your GitHub account.

---

## Viewing Your Repository on GitHub

### Accessing Your Repository on GitHub

Let's go to the GitHub website and see how our repository looks.

1. Go to **GitHub.com**
2. Login if it prompts you to
3. Click on your **avatar** in the top right
4. Navigate to **"Your repositories"**
5. Click on the **"test-repo"** repository

### Repository Page Layout

Let me point out a few things that are good to get familiar with:

#### Repository Path

In the top left is your username, followed by a slash, then "test-repo." This tells you what repository you're currently in, and it will also be listed in the URL.

#### Recent Commit Information

In the main part of the webpage, GitHub will load the most recent commit message which should be "Create index.html." And it has a **6-digit code** that is the hash for that specific commit.

### Understanding Commit Hashes

Every time you create a commit, Git will automatically create a random hash, which is a long string of letters and numbers, that serves as the **unique ID** for that commit.

#### Viewing Full Commit Hash

If you click on the 6 digit code, it will load that commit, and you can see the really long string in the URL and on the right side of the page.

### Repository Statistics

Going back to the test-repo repository, next to the hash:

- There's how long ago the commit was made
- Then at the end is the total number of commits

### Files in Repository

Under the top bar, GitHub will also display the files currently in the repository, which right now is only the index.html file. As we add more files you'll see them all in this area.

### Viewing and Editing Files on GitHub

If you click on the filename, GitHub will load the actual code in that file. You can even edit and delete the file right in GitHub.

**Important Note**: I wouldn't actually recommend doing this since it's better to manage your code in VS Code. But it's nice that the access is there.

---

## Managing Files with Git

### Files You Don't Want to Track

There might be files and folders that you create that you actually don't want Git to track. Let's say you're keeping some notes or something in a text file called `random.txt` that's in your project. You want those notes there but you don't want them to be public in your repository.

### Unchecking Files

In GitHub Desktop, what you can do is uncheck that box. That will make sure that the file won't be included in any commits. However, it can be kind of annoying to keep seeing that filename all the time.

---

## The .gitignore File

### What is .gitignore?

So you can actually have Git ignore files and folders. This is done through a special file called **.gitignore**.

### Creating .gitignore Entries

If you right-click a file in GitHub Desktop and select **"Ignore file (add to .gitignore)"** you'll see that the file has disappeared from the changes list. And there's a new file that Git has detected and wants to add to the repository: **.gitignore**.

In the right panel we can see that it contains the filename you wanted to ignore.

### Viewing the .gitignore File

If we look in VS Code and open the .gitignore file, we'll see the line with the filename you ignored.

### Adding Multiple Entries

In gitignore files, you can ignore individual files and folders by adding each one on a separate line:

```
random.txt
random123.txt
config.json
```

### Testing .gitignore

Let's test this out. In the gitignore file, add another line that says `random123.txt` and save it. Then in VS Code create a file with that exact file name.

Going back to GitHub Desktop, it has not added the `random123.txt` file since we ignored it. This proves that the .gitignore file is working correctly.

### Using Wildcards

As you might imagine, it can get a bit tedious to have to manually write each file name in the gitignore file. One thing that can help with that is that you can use the **wildcard** when writing the filename.

So let's go back to the gitignore file and delete everything that's there. Then add `*.txt` to ignore all text files:

```
*.txt
```

Now in GitHub Desktop, we don't have either of the text files showing up, and we can see the wildcard in the gitignore file.

### Wildcard Caution

**Important**: Just be very careful when using the wildcard to ignore file types, in case you might want to include a file of that type in the future sometime.

### Committing .gitignore Changes

Let's make a new commit with a commit message that says "Ignore text files". Then double-check to make sure the .gitignore file is checked, and click "Commit to main."

### Pushing Changes

In the top on the right we can see the panel saying **"Push origin."** What "origin" is, is it refers to the **remote repository** that we published on GitHub. So when we push commits in our local repo to origin, they will get pushed to the origin repository which is on GitHub.

Let's click **"Push origin."** It usually takes a few seconds.

### Verifying on GitHub

Now let's go back to GitHub and the main "test-repo" repository page. We can see that it looks a bit different now! The most recent commit is the "Ignore text files" one, and it has a new hash. And the total number of commits has gone up. And we can see the .gitignore file is now on GitHub too.

---

## Tracking Modifications

### Adding Content to Files

We've covered adding new files to the Git repository. Another thing Git will keep track of is changes made to existing files. Let's see how this looks.

In VS Code, open the index.html file and let's add some content to the body:

```html
<h1>Hello here is our website</h1>
<p>Here is some cool new content!</p>
```

Save it, and let's see what this looks like in GitHub Desktop.

### Detecting Modifications

Now, in the left sidebar the index.html file is showing up, and instead of that green plus icon that we saw when adding new files, there's a **yellow dot icon**. This signifies that Git has detected modifications in that file.

### Viewing Changes

In the right panel we can see the new text that we just added. And it's highlighted in green, meaning that it's code that has been added.

### Committing Modifications

So let's make a commit. We'll make the commit message something like "Added content to index.html."

Now we'll commit it to the main branch, and push to origin.

### Verifying Changes on GitHub

And if we look in GitHub, we'll see that commit we just made, and clicking on it will show us again, the green highlighted code we added to index.html.

### Git's Line-by-Line Tracking

One thing to note about Git is that it tracks changes on each line of code. If we click on the "History" tab we can see the 4 commits that we have in this repo, with the most recent on top. And if we go back to GitHub.com to the repository page, we can see the same history up there if we click on the "4 commits" link on the right side, again with the newest commits on top, and the oldest ones on the bottom.

---

## Deleting Files

### Deleting Files in Your Project

Git will also track if you delete files. Let's test this out. In VS Code, go ahead and delete the index.html file!

### Detecting Deletions

Now, going back to GitHub Desktop, we see the index.html file is showing up under "Changes." It has a **red minus symbol icon** to indicate that this file has been deleted. And in the right panel all the code in the file is highlighted in red, meaning it's been removed.

### Committing Deletions

Let's make a commit, with the commit message saying that we deleted index.html. Commit it, and then push to origin.

### Verifying Deletion on GitHub

If we check out GitHub, it'll show that most recent commit, and clicking on the commit, it tells us that the file was indeed deleted.

---

## Reverting Changes

### The Problem: Accidental Deletions

But what if we realize that we really need that index.html file?! Not to worry, this is one of the ways that Git can really save your life.

### Using Revert

In GitHub Desktop, in the "History" tab, right-click the commit where we deleted index.html. And select **"Revert changes in commit."**

### What Happens After Revert

Now we see that Git has automatically created a new commit saying that it has reverted the previous commit. And looking at more details in the right panel, it tells us the hash of the commit that was reverted, and it's added back the index.html file and all its lines of code.

### Pushing Reverted Changes

Now if we click the "Push origin" button, everything will be back to normal. In VS Code, the index.html file will be back. And in GitHub if we refresh, we can see the commit reverting it, and the index.html file is also back where it belongs.

---

## Introduction to Branching

### What is a Branch?

Now there is one more area in Git that I'd like to cover. And that is **branching**. In Git a branch is one version of the codebase, and a repo can have multiple branches going at the same time.

### Working on the Main Branch

So far, all the work that we've done in Git, and all the commits that we've made have been on the one main branch. If you're just working by yourself you can probably get away with doing everything on main. But if you're on a team with multiple developers all working on the same codebase, it would be quite chaotic to have everyone working on the same branch, especially if more than one person makes changes to the same file.

### Why Teams Use Multiple Branches

So most teams will separate work into different branches. You might have one developer fixing a bug on the homepage working in a branch called `homepage-bug`. Then there might be another developer building a new feature on the careers page working in another branch called `careers`.

Each of those branches will be created off the main branch, so they will have the most up to date code from main. Then they'll each work on their own branches locally. When the developers are done with their work, they will merge their branch back into the main branch.

### Best Practice Workflow

This type of workflow is considered **best practice** when you're working on a team. So even though in this course we can do all our work on the main branch, it's important to show you a little bit of what working with different branches looks like, as this is what you'll be doing in real-world development.

---

## Creating and Working with Branches

### Creating a New Branch

In GitHub Desktop, in the top menu, navigate to **Branch > New branch**. Let's give it a name of "feature-1". And you'll notice under the Name field is a note saying that the new branch will be based on the current branch, which is main. Then click **"Create branch"**.

### Switching to the New Branch

Now up at the top GitHub Desktop has the feature-1 branch listed as our current branch.

### Making Changes in a Branch

Let's make some demo code changes in this branch. In VS Code, create a new file called "feature1.html" to keep things simple. And in the file hit exclamation point and enter to use the Emmet shortcut to add boilerplate HTML. Then save the file.

### Committing in a Branch

And back in GitHub Desktop, we want to add feature1.html to our repo. In the commit panel at the bottom we'll just leave that default commit message of "Create feature1.html" and hit the button to commit this change to the feature-1 branch.

### Branch Isolation

Now, in GitHub Desktop, let's switch our current branch back to the main branch. If we go back to VS Code, the feature1.html file won't exist. This is because it was created in the feature-1 branch, and so it doesn't exist yet on the main branch. Git will keep the codebase files updated depending on what branch you are currently on.

This is one of the most powerful aspects of branching: each branch can have completely different code, and switching between branches updates your local files accordingly.

---

## Merging Branches

### The Merge Process

Let's pretend that we've now finished all the development work on the feature-1 branch, and we want to deploy it to our website. We need to add our changes from the feature-1 branch to the main branch in what's called a **merge** in Git.

### Merging into Main

To merge feature-1 into main, in GitHub Desktop:

1. First make sure that you are currently in the **main branch**
2. In the top menu, navigate to **Branch > Merge into current branch**
3. Select the **feature-1 branch**

This is saying that we will merge all the commits from the feature-1 branch into the main branch.

### Creating a Merge Commit

Click the button saying **"Create a merge commit"**. This will merge in the code from feature-1 into main, and the change will be automatically put into a new commit on the main branch.

### Verifying the Merge

Now if we load the History tab, we can see the "Create feature1.html" commit message listed as the most recent commit on the main branch. The file is now part of the main branch's history.

### Pushing Merged Changes

Now click the **"Push origin"** button up at the top to update GitHub.

### Verifying on GitHub

In GitHub, if we load the repository page, we can now see that the commit creating feature1.html is the most recent commit, and the file exists on the main branch.

---

## Pull Requests and Team Collaboration

### What Are Pull Requests?

One last thing to note: if you're working on a team that uses GitHub, new branches are typically merged into the main branch through a feature on GitHub called **pull requests**. This allows other people on the team to check the code changes and approve them before merging them into main. This helps to prevent any mistakes from being added.

### Pull Request Workflow

So what you would do is:

1. Make your code changes and commit onto the feature-1 branch
2. Instead of merging feature-1 into main in GitHub Desktop like we did last time, you would **publish the feature-1 branch** up to GitHub
3. Then on GitHub you would **create the pull request** for other people on your team to review
4. Team members can either approve or suggest code changes
5. If the changes are approved, your team member can then **merge your changes into main**

### Team Best Practice

This workflow ensures code quality and prevents mistakes from reaching the main branch. It's the standard practice in most professional development environments.

### Important Note

This is mainly if you're on a team. We're not going to be working with multiple branches or pull requests in this course. But it's important to know that they exist because they're common practice when you're working on a team.

---

## Best Practices

### Summary of Key Practices

Based on everything we've covered in this guide, here are the key best practices for using Git and GitHub:

1. **Use Meaningful Commit Messages**: Your commit messages should clearly describe what changes were made. This makes it easier for you and your team to understand the project history.

2. **Commit Frequently**: Make small, logical commits rather than one giant commit. This makes it easier to understand what changed and why.

3. **Use Branches for Features**: When working on a team, use separate branches for different features. This prevents conflicts and allows multiple developers to work simultaneously.

4. **Use .gitignore**: Keep your repository clean by ignoring files that shouldn't be tracked (like node_modules, configuration files, or personal notes).

5. **Review Before Merging**: If working on a team, always use pull requests to review code before merging branches into main.

6. **Push Regularly**: Keep your local repository synced with the remote repository by pushing commits regularly.

7. **Keep Main Branch Stable**: The main branch should always contain stable, working code. Don't push unfinished or broken code to main.

8. **Test Before Pushing**: Make sure your code works before committing and pushing to GitHub.

### Setting Up Your Project

Next up, we'll be setting up your project files for actual development! We'll be showing you how to set it up from a blank folder and create a new Git repo for it, so you won't be needing this test-repo one anymore.

---

## Conclusion

And that's it for the basics of Git and GitHub! You now have a solid foundation in:

- Creating and managing repositories
- Making commits and tracking changes
- Using branches for different features
- Ignoring files with .gitignore
- Reverting changes when needed
- Understanding the basics of team collaboration

As you continue your coding journey, you'll find that Git and GitHub become indispensable tools in your development workflow. The concepts you've learned here will scale as you work on larger projects and with bigger teams.

Keep practicing these concepts, and soon they'll become second nature. Good luck with your coding journey!
