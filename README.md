# DevOps Git Project
Git and GitHub
==============
what is version control system?
A Version Control System is a tool that helps developers track, manage, and control changes to code or files over time. It allows multiple people to work on the same project simultaneously, without overwriting each other’s work — and keeps a complete history of all changes made.
A version control system records every change made to files so that you can go back to a previous version, compare changes, and collaborate safely with others.
Key Functions:
1.Track Changes:
Keeps a history of who changed what and when.
2.Collaboration:
Many developers can work together on the same project.
3.Backup and Restore:
You can revert to an older version if something breaks.
4.Branching and Merging:
Developers can create separate branches to experiment, then merge back to the main code.
5.Conflict Management:
Helps detect and resolve code conflicts between team members.

There are two type of version control systems:

1. Centralized Version Control System (CVCS)

In a centralized VCS, there is one central server that stores all project files and the entire version history.
Developers connect to this central server to get the latest code and to commit their changes.
Example: SVN (Subversion), CVS, Perforce

How it works:
One main server (repository) stores all versions.
Developers check out code from the server.
Developers commit changes back to the same server.

2. Distributed Version Control System (DVCS)

In a distributed VCS, every developer has a full copy of the entire repository — including the complete history.
There’s no single point of failure because each local copy is a full backup.
Example: Git, Mercurial

How it works:
Each developer has a local repository with full history.
They can commit, branch, and merge locally without needing a network connection.
They push changes to a shared remote repository (like GitHub) when ready.

What is a Fork in Git / GitHub?

A fork is a copy of someone else’s repository (project) that you make under your own GitHub account.
It allows you to freely experiment, modify, and improve the project without affecting the original one.
A fork is like creating your own version of another person’s project — you can make changes safely, and later suggest your updates to the original project.

How It Works:
You find a repository on GitHub that you want to work on.
Click the “Fork” button (top right).
GitHub creates a copy of that repository in your account.
You can now:
Edit code
Add new features
Fix bugs
Push your changes to your fork
If you want your changes to be added to the original project, you can create a Pull Request.

Fork = Copy someone else’s repo to your GitHub
Clone = Copy a repo (yours or others’) to your computer


git vs git hub
==============

Feature	          Git	              GitHub

Definition	Git is a version      GitHub is a cloud
                control system — a    platform that hosts
                tool used to track    Git repositories                                                                     
                 changes in code.       online	

Type           Software/Command-line   Web-based service
                tool

Where it runs   On your local         On the internet 
                computer (offline).    (remote).

Purpose         Manage versions,      Store, share, and      
                commits, branches,    collaborate on Git 
                merges locally.         repositories.

Usage           Used by developers    Used to host Git 
                to manage code        projects and   
                   history             collaborate with  
                                       others  

Integration     Works with many       Specific to GitHub, 
                platforms (GitLab,    but also supports 
                 Bitbucket, etc.)      git commands  


first connect to your ec2
run the command to install git (ex: apt install git)

run the [git init] command to initialize the git 
when you run the git init commend then a git repository is created 

[git status] is the command used to check the status of your current repository  

[git add file_name] this command will add the file to git repository and maintain its versioning 

[git diff] this is the command used to know what exact changes have made from previous  version to present version

[git commit -m "this is my first version"] this command will tell the which version is it to git

[git log] it will maintains all the commits. it track all the commits

you made commit two time and you two versions but now you have to come to previous version  
use the command [git commit] it will show all versions wit commit id copy the commit id of version you want 
[git reset --hard commit_id] by using this version you will come to previous version

[git checkout file_name] it will remove all changes

[git branch branch_name] it will create a new empty branch

[git checkout -b branch_name] it will create a new branch with all existing code in main branch 

[git branch] it will show all branches 

git checkout is used to switch between the branches [git checkout branch_name]

you have made changes in the branch and you need to add it back to main branch. go to branch you created give command like git log
and copy the commit id and come to main branch and use the command to merge [git cherry-pick commit_id]
note: it is used when less commits or less changes 

[git merge branch_name] it will combine two branches. Keeps full commit history (creates a merge commit).Safe and best for shared branches. History looks non-linear.

[git rebase branch_name]Moves your branch commits on top of another branch. Rewrites history (no merge commit). Gives clean, linear history. Use for local branches before pushing.

if you want to create a distributed system:
the GitHub or self hosted git or bitbucket come into picture
steps:
Create a new repository on GitHub.
Link your local repo to GitHub:
git remote add origin https://github.com/username/repo-name.git

Push your code to GitHub:
git push -u origin main

Branching Strategy
==================

what is a branch?
A branch is a pointer to a specific commit (version) in Git, allowing you to work on new features, bug fixes, or experiments safely without disturbing the main code.
 
The main branch is your stable project.
When you create a new branch, you’re making a duplicate of that version to try new things.
If it works, you can merge it back into the main branch.

what is good Branching Strategy?

It’s a plan for how developers will create, name, and merge branches while working together — to keep the project organized and avoid conflicts.
Why Branching is Needed
To allow multiple developers to work at the same time.
To separate new features, bug fixes, and releases safely.
To prevent unstable code from breaking the main application.

Common Git Branching Strategies
===============================
1. Git Feature Branch Workflow

Used for: Isolating new features or tasks.
Developers create a new branch for each feature.
After the feature is complete, it’s merged back into the main branch.

2. GitHub Flow

Used for: Simple continuous deployment (CD) setups.
Only one main branch (main or master)
For each task:
Create a new branch
Make changes
Open a pull request (PR)
Merge to main after review
Deploy automatically

3.Release Branching Strategy

The Release Branching Strategy is a Git workflow where a separate branch is created for preparing a new release version of the software. It helps teams stabilize the code, fix bugs, and prepare documentation before deploying to production.

used for:When a project is close to release
You want to freeze new feature development.
Focus only on testing, bug fixes, and polishing.
Keep the develop branch open for the next version of development.
  

example:
Git Branching Workflow Explanation

We start with a master (main) branch that contains our stable production code — for example, code that performs addition and subtraction operations.
Whenever we want to add a new feature, such as division, we create a feature branch from the master branch.
We develop and test the new functionality in that branch.
After successful testing, we merge the feature branch back into the master branch and then delete the feature branch to keep the repository clean.
We follow this process every time we add a new feature — creating a separate feature branch for each feature.
When all features for a new version are complete, we create a release branch from the master branch.
This branch is used for final testing, bug fixing, and preparing the code for deployment to customers.
After the release is tested and stable:
The release branch is merged into the master branch (production-ready version).
The release branch is then deleted.


Git commands
============
first clone the GitHub repository then do the following commands like git add, git commit, git push 






                            
