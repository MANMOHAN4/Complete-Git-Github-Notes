# Complete Git and GitHub Tutorial

## Table of Contents

1. [Introduction and Course Overview](#introduction-and-course-overview)
2. [Version Control System (VCS) Fundamentals](#version-control-system-vcs-fundamentals)
3. [Understanding Source Control](#understanding-source-control)
4. [Git Installation and Setup](#git-installation-and-setup)
5. [Git Command Line Interface (CLI) Basics](#git-command-line-interface-cli-basics)
6. [Initializing a Git Repository](#initializing-a-git-repository)
7. [Adding Files to Version Control](#adding-files-to-version-control)
8. [Understanding Commits](#understanding-commits)
9. [Staging Area](#staging-area)
10. [Viewing Commit History](#viewing-commit-history)
11. [Reverting Changes](#reverting-changes)
12. [Collaboration with Git](#collaboration-with-git)
13. [Git Remote and Remote Repositories](#git-remote-and-remote-repositories)
14. [Branching](#branching)
15. [Assignments](#assignments)

---

## Introduction and Course Overview

This is a comprehensive crash course on Git and GitHub. This tutorial covers everything from basic concepts to intermediate level understanding of Git and GitHub. By the end of this course, you will understand what Git is, what GitHub is, what version control systems are, and how to use Git for managing your version control system.

The course covers fundamental concepts including version control systems, source control, Git basics, branching, staging areas, commits management, merging, reverting commits, collaboration, and much more.

---

## Version Control System (VCS) Fundamentals

### What is a Version Control System?

A Version Control System, also known as Source Control, is a system that allows you to manage, track, and maintain code changes over time. It provides the capability to track how your code evolves and changes.

### The Problem VCS Solves

Consider a simple scenario where you have a code file like `index.js`. Initially, your code might look like this:

```javascript
const a = 24;
```

Over time, as you work on larger projects, your code undergoes many changes. You might add features, refactor code, and make various modifications:

- One developer might add: `const name = "Piyush"`
- Another developer might create a function: `function getName() { return name; }`

Without a version control system, it becomes very difficult to track:

- How your code has changed over time
- Who made specific changes
- When changes were made
- What the code looked like at previous points in time

### How VCS Solves These Problems

With a Version Control System, you can create a timeline of your code's evolution. For example:

1. **Initial State**: `const a = 24`
2. **After first change**: Added `const name = "Piyush"`
3. **After second change**: Added `function getName() { return name; }`

Each of these states represents a snapshot of your code. VCS allows you to:

- Track each change with detailed information about who made it and when
- Revert to any previous state if you discover a bug
- Maintain a complete history of all modifications
- Understand the progression of your codebase

### Why VCS is Essential

In large codebases with multiple developers working simultaneously, managing code becomes extremely complex without a VCS. Version Control Systems make it possible to:

- Manage code changes systematically
- Maintain consistency across the development team
- Track the evolution of the software
- Recover from mistakes by reverting to previous versions

---

## Understanding Source Control

Source Control is synonymous with Version Control. It refers to the practice of tracking and managing changes to your source code. There are several types of Version Control Systems available in the market:

- **Git**: The most widely used and popular VCS
- **Apache Subversion**: Another popular VCS option
- **Mercurial**: A distributed version control system
- **Bazaar**: Another VCS option

Almost all companies, whether service-based, product-based, startups, or enterprises, use Git as their primary version control system.

---

## Git Installation and Setup

### What is Git?

Git is a free and open-source distributed version control system. It is the most widely used VCS in the industry today. Git is not the only VCS available, but it has become the de facto standard for software development.

### Installing Git

To work with Git, you need to install it on your local machine. The process is straightforward:

1. Go to the official Git website: `https://git-scm.com`
2. Download the binary for your operating system (Windows, macOS, Linux)
3. Run the installer with the default settings by clicking Next repeatedly
4. Complete the installation

### Verifying Git Installation

Once Git is installed, you can verify it by opening your terminal and typing:

```bash
git
```

This command will display various Git options and commands, confirming that Git is installed.

You can also check the installed version:

```bash
git --version
```

For example, you might see output like: `git version 2.39.3`

The exact patch version (like 2.39.3 vs 2.43) is not critical as long as the major version (2) remains the same. Different patch versions work fine for this tutorial.

---

## Git Command Line Interface (CLI) Basics

### Understanding the CLI

The Command Line Interface (CLI) is how you interact with Git through your terminal or command prompt. All Git operations are performed through text commands.

### Global Configuration Setup

Before starting to work with Git, you should configure it globally with your identity. This configuration tells Git who you are, which is important because every commit will be attributed to you.

#### Setting Your Name

```bash
git config --global user.name "Your Name"
```

For example:

```bash
git config --global user.name "Piyush Garg"
```

#### Setting Your Email

```bash
git config --global user.email "your.email@example.com"
```

#### Verifying Configuration

To check your configured name:

```bash
git config user.name
```

This will display the name you configured globally.

### Why Configuration Matters

When you work in a large company with multiple developers contributing to the same codebase, every line of code includes information about:

- Who wrote it
- When they wrote it
- What commit it was part of

For example, if you add this line of code:

```javascript
const dateOfBirth = "01-01-2000";
```

Git will record that this line was added by "Piyush Garg" with the email "piyush@example.com" at a specific time. This is why proper configuration is essential.

### Optional Configuration

You can also enable color output in Git for better terminal readability:

```bash
git config --global color.ui true
```

---

## Initializing a Git Repository

### Creating Your First Project

To start tracking a project with Git, you need to initialize a Git repository in that project directory.

1. Create a project folder:

```bash
mkdir git-crash-course
cd git-crash-course
```

2. Open the folder in your code editor (VS Code):

```bash
code .
```

### Initializing Git

To enable Git version control in your project directory, use the `init` command:

```bash
git init
```

This command will output:

```
Initialized empty Git repository in /path/to/your/project/.git
```

### What Happens During Initialization

When you run `git init`, Git creates a hidden folder named `.git` in your project directory. This folder contains all the configuration and version control information for your project.

### Understanding the `.git` Folder

The `.git` folder is a hidden directory (starts with a dot) that contains:

- The complete version control history of your project
- All commits, branches, and configuration data
- Internal Git tracking information

**Important**: You should never manually edit or delete anything inside the `.git` folder. This is where Git stores all critical information about your project's history.

To view hidden folders like `.git` in your file system, you can use:

```bash
ls -la
```

Or on macOS, use: `Cmd + Shift + .` to show hidden files in Finder.

---

## Adding Files to Version Control

### Creating Files in Your Project

Once your Git repository is initialized, you can create files in your project:

1. Create a new file like `index.js`:

```javascript
const a = 24;
```

2. Create additional files like `script.js` or organize them in folders:

```javascript
function hello() {
  console.log("Hello, I am a new function");
}
```

### Tracking File Status

You can check the status of your files with:

```bash
git status
```

When files are newly created and not yet tracked by Git, they appear with a status of **Untracked**.

### Adding Files to Tracking

To add a specific file to Git tracking:

```bash
git add filename.js
```

For example:

```bash
git add index.js
```

### Adding All Files at Once

To add all modified and new files in your project to Git tracking:

```bash
git add .
```

The dot (`.`) represents the current directory and all its contents, so this command stages all changes in your project.

### Understanding Staged vs Untracked Files

After using `git add`, files move from Untracked to Staged status. This means Git is now tracking these files and will include them in the next commit.

If you check `git status` after adding files, you will see them listed as "Changes to be committed".

### Removing Files from Tracking

If you accidentally added a file to tracking and want to remove it:

```bash
git rm filename.js
```

---

## Understanding Commits

### What is a Commit?

A commit is a snapshot of your project at a specific point in time. It captures the state of all tracked files at that moment. Think of commits as points in your project's timeline:

- **Commit 1**: Initial code state - `const a = 24`
- **Commit 2**: After adding a variable - `const name = "Piyush"` added
- **Commit 3**: After adding a function - `function getName() { return name; }` added

Each commit serves as a checkpoint in your project's history.

### Creating a Commit

Once you have added files using `git add`, you create a commit with:

```bash
git commit -m "Your commit message"
```

The `-m` flag allows you to add a commit message directly in the command.

For example:

```bash
git commit -m "Initial code added"
```

### Commit Messages Best Practices

Good commit messages should:

- Be concise and meaningful
- Describe what changes were made
- Use imperative mood (e.g., "Add feature" rather than "Added feature")
- Be relevant to the changes included in that commit

Examples of good commit messages:

- `git commit -m "Added isAbove18 function"`
- `git commit -m "Remove unnecessary function"`
- `git commit -m "Changes in utils file"`

### Understanding the Full Commit Process

The complete workflow for committing changes is:

1. **Modify your code** - Make changes to your files
2. **Stage changes** - Use `git add` to stage the files you want to commit
3. **Create a commit** - Use `git commit -m "message"` to create a snapshot

### Commit Authorship

When you create a commit, Git automatically records:

- Your name (from global configuration)
- Your email (from global configuration)
- The exact time of the commit
- The commit message you provided
- All changes included in that commit

---

## Staging Area

### What is the Staging Area?

The staging area is an intermediate zone between your working directory (the actual files on your disk) and your repository (the Git history). It allows you to choose which changes to include in your next commit.

### The Three States of a File

Every file in a Git repository exists in one of three states:

1. **Modified**: You have changed the file in your working directory, but it's not staged for commit yet
2. **Staged**: You have marked the file to be included in the next commit using `git add`
3. **Committed**: The changes have been saved in the Git history through a commit

### Understanding the Workflow with Staging Area

Consider this scenario:

You have two files with changes:

- `index.js` - You want to commit these changes now
- `utils.js` - You're still working on this and don't want to commit yet

You can use the staging area to control this:

1. Stage only `index.js`:

```bash
git add index.js
```

2. Check status to see what's staged vs unstaged:

```bash
git status
```

Output will show:

```
Changes to be committed:
  modified: index.js

Changes not staged for commit:
  modified: utils.js
```

3. Commit only the staged changes:

```bash
git commit -m "Changes in index.js"
```

This commit will only include changes to `index.js`, not `utils.js`.

### Why the Staging Area is Useful

The staging area gives you fine-grained control over what goes into each commit. This helps you:

- Organize commits logically
- Keep commit history clean
- Avoid committing incomplete or unrelated changes
- Review changes before committing them

### Viewing Changes Before Commit

To see what changes are in your working directory:

```bash
git diff
```

This shows:

- Lines starting with `+` (additions)
- Lines starting with `-` (deletions)
- The files that were modified

### Staging All Changes

If you have multiple files with changes and want to stage all of them at once:

```bash
git add .
```

---

## Viewing Commit History

### Understanding Git Log

The `git log` command displays your project's commit history. It shows all commits in reverse chronological order (newest first).

### Basic Log Viewing

```bash
git log
```

This will display detailed information for each commit:

- **Commit SHA**: A unique identifier for the commit (40-character hexadecimal string)
- **Author**: The name and email of the person who made the commit
- **Date**: When the commit was made
- **Commit message**: The message describing the changes

### Viewing Compact Log

To view commit history in a more compact format (one line per commit):

```bash
git log --oneline
```

This shows only the abbreviated commit SHA and the commit message, making it easier to scan through history.

### Viewing Specific Commit Details

To see the exact changes made in a specific commit:

```bash
git show <commit-sha>
```

For example:

```bash
git show a1b2c3d
```

You can use just the first 7 characters of the commit SHA for brevity.

This will display:

- The commit metadata (author, date, message)
- The exact lines that were added (+)
- The exact lines that were removed (-)
- Which files were changed

### Blaming Code with Git Blame

The `git blame` command shows who made changes to each line of a file:

```bash
git blame filename.js
```

This is extremely useful in large projects where you want to know:

- Who wrote a specific line of code
- When that line was added
- Which commit introduced that line

For example:

```bash
git blame utils.js
```

Will show each line of `utils.js` with the commit SHA, author name, timestamp, and the actual code.

---

## Reverting Changes

### Understanding Revert vs Reset

There are two primary ways to undo changes in Git:

1. **Reset (`git reset`)**: Moves the HEAD pointer to a previous commit, effectively removing commits from history
2. **Revert (`git revert`)**: Creates a new commit that undoes changes from a previous commit while keeping history intact

### Using Git Reset

**Warning**: `git reset` is a powerful command that removes commits from your history. Use it with caution, especially in shared repositories.

If you have made a commit that introduces a bug or unwanted code, you can reset to a previous state:

```bash
git reset --hard <commit-sha>
```

For example, if you want to go back to a previous commit:

```bash
git log --oneline
```

Find the commit SHA you want to revert to, then:

```bash
git reset --hard a1b2c3d
```

This will:

- Move the HEAD pointer to that commit
- Remove all commits after that point from your history
- Restore your files to their state at that commit

### The Problem with Reset

If you reset to a previous commit, all subsequent commits are lost from the history. This is problematic in collaborative environments because:

- It rewrites history
- Other developers who have pulled those commits will have conflicts
- It makes collaboration difficult

### Using Git Revert

A safer approach, especially in shared repositories, is to use `git revert`:

```bash
git revert <commit-sha>
```

For example:

```bash
git revert a1b2c3d
```

This command:

- Creates a **new commit** that undoes the changes from the specified commit
- Keeps all history intact
- Is safe to use in shared repositories
- Makes it clear when and why changes were undone

### How Git Revert Works

When you revert a commit:

- If lines were added in that commit, they are removed in the revert commit
- If lines were removed in that commit, they are added back in the revert commit
- If lines were modified, the revert commit restores the original state

### Example Workflow

Suppose you have this commit history:

```
Commit 1: Initial code
Commit 2: Added isAbove18 function
Commit 3: Removed some code (bug introduced)
Commit 4: Made other changes
```

If you discover a bug was introduced in Commit 3, you can:

```bash
git revert <sha-of-commit-3>
```

This creates a new commit that undoes the changes from Commit 3, while keeping Commits 1, 2, and 4 in history. Your history now looks like:

```
Commit 1: Initial code
Commit 2: Added isAbove18 function
Commit 3: Removed some code (bug introduced)
Commit 4: Made other changes
Commit 5: Revert "Removed some code" (undo Commit 3)
```

---

## Collaboration with Git

### The Need for Collaboration

In real-world development, you rarely work alone on a project. Teams of developers work together on the same codebase. Without a proper system, collaboration becomes chaotic:

- Developer A has version of code with `const a = 24`
- Developer B has version of code with `const a = 28`
- Both developers have different local versions with no way to sync

### Single Source of Truth

To solve this problem, teams need a **single source of truth** - a central repository where all code is stored and synchronized. This could be:

- A dedicated server in your company
- A cloud-based service like GitHub
- Any remote Git server

### Basic Collaboration Workflow

The collaboration workflow involves:

1. **Push**: Developer A makes changes and pushes commits to the central server
2. **Pull**: Developer B pulls those changes from the server to their local machine
3. **Sync**: Both developers now have the same code

### Commit Timeline with Collaboration

Consider this scenario:

- **12:00 PM**: Developer A makes a commit changing `const a = 24` and pushes to server
- **12:15 PM**: Developer B pulls the changes, now has `const a = 24` in their code
- **2:00 PM**: Developer B makes a commit changing it to `const a = 28` and pushes to server
- **2:15 PM**: Developer A pulls the changes, now has `const a = 28` in their code

Both developers stay synchronized through the central server, and they can see the complete history of who made what changes and when.

### Benefits of Centralized Collaboration

This approach provides:

- **Consistency**: All developers have access to the same code
- **History**: Complete record of all changes with timestamps and author information
- **Traceability**: Easy to see who made what changes and why
- **Revert capability**: Can revert to any previous state if needed

---

## Git Remote and Remote Repositories

### What is a Remote?

A remote is a link to a remote server that hosts your Git repository. It allows your local Git repository to communicate with a central server.

### Remote Naming Convention

Remotes are given user-friendly names. By convention, the primary remote is called **origin**:

```bash
git remote add origin <repository-url>
```

You can also create multiple remotes with different names if needed.

### Adding a Remote

Once you have created a repository on a remote server (like GitHub), you need to link your local repository to it:

```bash
git remote add origin https://github.com/username/repo-name.git
```

For example:

```bash
git remote add origin git@github.com:piyush-garg/git-crash-course.git
```

### Listing Remotes

To see what remotes are configured in your repository:

```bash
git remote
```

This lists all remote names (usually just "origin").

To see the URLs associated with each remote:

```bash
git remote -v
```

Output will show:

```
origin  git@github.com:piyush-garg/git-crash-course.git (fetch)
origin  git@github.com:piyush-garg/git-crash-course.git (push)
```

### Pushing to Remote

Once a remote is configured, you can push your local commits to it:

```bash
git push origin main
```

This pushes commits from your local `main` branch to the `origin` remote's `main` branch.

**Note**: Branch names will be discussed in detail in the branching section.

### Why Remotes Are Important

Remotes enable:

- Sharing your code with other developers
- Backing up your repository to a server
- Collaboration on shared projects
- Access to your code from multiple machines

---

## Branching

### Understanding Branches

Branches are parallel lines of development within a single repository. Think of branches like tree branches - each branch can grow independently and later be merged back to the main trunk.

### Why Use Branches

Branches allow multiple developers to work on different features simultaneously without interfering with each other:

- Developer A works on Feature A in one branch
- Developer B works on Feature B in another branch
- Both work independently without affecting the main codebase
- Features can be merged when ready

### The Main Branch

By default, Git creates a branch called `main` (previously called `master`). This is the primary branch of your project.

### Creating a Branch

To create a new branch:

```bash
git branch branch-name
```

For example:

```bash
git branch feature-new-login
```

### Switching Between Branches

To switch to a different branch:

```bash
git checkout branch-name
```

For example:

```bash
git checkout feature-new-login
```

### Creating and Switching in One Command

You can create a new branch and switch to it in a single command:

```bash
git checkout -b branch-name
```

### Checking Current Branch

To see which branch you are currently on:

```bash
git branch
```

This will show all local branches with the current branch marked with an asterisk (\*).

### Branching Naming Conventions

Good branch naming conventions include:

- `feature/feature-name` - For new features
- `bugfix/bug-name` - For bug fixes
- `refactor/what-was-refactored` - For refactoring work
- `docs/what-documentation` - For documentation updates

For example:

- `feature/user-authentication`
- `bugfix/login-validation`
- `refactor/database-queries`

### Understanding the Branch Structure

When you work on a branch and make commits:

1. The main branch continues its own history
2. Your feature branch has its own history
3. Both branches exist independently
4. They can be merged together when the feature is complete

### Branch Lifecycle

```
Main Branch: Commit1 -> Commit2 -> Commit3 -> Commit4
             |
             +-- Feature Branch: Commit3A -> Commit3B -> Commit3C
```

### Merging Branches

Once you complete work on a feature branch, you merge it back to the main branch.

#### Merge Strategy 1: Squash Merge

A squash merge combines all commits from the feature branch into a single commit before merging:

```bash
git checkout main
git merge --squash feature-branch-name
git commit -m "Merge feature description"
```

This approach:

- Takes all commits from the feature branch
- Combines them into one commit
- Adds that single commit to the main branch
- Results in a cleaner history

#### Merge Strategy 2: Regular Merge

A regular merge preserves all commits from the feature branch:

```bash
git checkout main
git merge feature-branch-name
```

This approach:

- Keeps all commits from the feature branch
- Maintains the full history
- Shows the complete evolution of the feature

### Deleting Branches

Once a branch is merged and no longer needed:

```bash
git branch -d branch-name
```

---

## Assignments

To solidify your understanding of Git, complete the following hands-on assignments:

### Assignment 1: Basic Repository Setup

1. Create a new folder for a test project
2. Initialize it as a Git repository using `git init`
3. Create several files (JavaScript, Python, or any language you prefer) with simple code
4. Make changes to different files at different times
5. Create at least 8-10 commits with meaningful commit messages
6. Practice `git log` and `git log --oneline` to view your commit history

### Assignment 2: Understanding the Staging Area

1. Create a new file and modify an existing file
2. Use `git status` to see the current state
3. Stage only one of the files using `git add filename`
4. Commit only the staged changes
5. Verify that the unstaged file is still modified but not committed
6. Practice switching between adding all files and adding individual files

### Assignment 3: Version Control Visualization

1. Install the Git Graph extension in VS Code (recommended: "Git Graph by mhutchie")
2. Create several commits in your repository
3. Open the Git Graph view to visualize your commit history
4. Understand how commits are represented in the graph
5. Navigate through different commits to see the evolution of your code

### Assignment 4: Commit History Navigation

1. Use `git show <commit-sha>` to examine specific commits
2. Identify which files were changed in each commit
3. Use `git blame` on one of your files to see which commits introduced each line
4. Practice using abbreviated commit SHAs (first 7 characters)
5. Understand the metadata associated with each commit

### Assignment 5: Reverting Changes

1. Create a commit with intentional changes
2. Create another commit on top of that
3. Use `git revert` to undo one of the commits
4. Observe how the revert creates a new commit rather than removing history
5. Verify that the reverted changes are undone while maintaining commit history

### Assignment 6: Branching Practice

1. Create multiple feature branches from your main branch
2. Switch between different branches and make commits in each
3. Use `git log` to see different histories in different branches
4. Merge a feature branch back to main using both:
   - Squash merge (combining all commits into one)
   - Regular merge (preserving all commits)
5. Delete the merged branches

### Assignment 7: Git Visualization Tools

1. Use `git log --graph --oneline --all` to visualize your branch history in the terminal
2. Experiment with the Git Graph extension to see visual representations
3. Create branches, make commits, and observe how the graph evolves
4. Practice understanding the visual representation of your repository structure

### Key Takeaways

Through these assignments, you will gain practical experience with:

- Initializing and managing Git repositories
- Creating and organizing commits effectively
- Using the staging area strategically
- Understanding commit history and navigation
- Reversing and undoing changes safely
- Working with branches for feature development
- Visualizing repository structure and history

Remember that the best way to learn Git is through hands-on practice. Start with basic operations and gradually work your way toward more complex scenarios involving multiple branches and merges.
