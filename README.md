# GitHub Informational Guide 

## Author
[Jayden Shaw](mailto:jayden.shaw@stridemgmt.com)
Web Developer, [Stride Management Corp.](https://www.stridemgmt.com/) 

## GitHub 101
[GitHub]() is a web-based version control system which uses Git, the open-source version control software. To put it simply, GitHub is an online hosting hub for git repositories and project. It lets you and other team members work on a project together from anywhere. You can collaborate, learn new skills, and manage projects in one easy-to-use interface. 

## Getting Started
GitHub is completely free, 

### Requirements

### Dictionary 

**Repository**:
Also known as a *Repo*, repositories are the essential elements of GitHub. Repositories contain all of the files and revision histories of each project. Repos can be either public or private, and multiple users can work collaboratively within a project's repository. 

**Branch**:
Each repository can contain multiple copies of the same project. Each seperate version is a *branch* of the original project, and changes made to individual branches can be merged into the primary branch if desired. 

Upon creation of a new repository a singluar branch known as the **Master** branch is created. 

**Clone**:
A copy of a repository that is hosted locally on a user's device.

**Commit**:
A record of change made to a file or files in the repository. Every commit has a unique ID for tracking purposes and can contain a user-defined message that describes the changes that were made. 

**Fork**:
*Forking* is when you copy another user's repository to your own account. You can then make any changes you want to your forked copy, leaving the original unaffected. However, forks retain a connection to their original source, giving you the option to update your copy with changes made to the original at a later date if necessary. 

**Issues**: 
Issues are essentially used to help you organize your GitHub project. They're mainly used to track bugs, but they can also be used to collect user feedback and organize tasks. You have the ability to assign issues to colleagues, put them in milestones, project boards, or reference them in pull requests. 

**Project Boards**:
For an even greater organizational view, GitHub has project boards! Made up of issues, pull requests, and notes, project boards organize your work into a kanban view. These can be used for complex feature work, release checklists, or more comprehensive roadmaps. 

**Pull/Push**:
Merging changes made to the repository files into the local copy you are working on is called *pulling*. A *push* is the opposite, this is when the repository of files is updated with the changes you have made to your local files. 

**Pull Request**: 
When you want to make changes to a repository you are working on as a part of a collaborative project you send a *pull request*. The other users can then approve or deny your request, or contain them in a seperate branch. Pull requests are generally where you'll find feedback during the development cycle. Other developer review your code, find bugs, suggest changes, and discuss its quality and implementation. 

**Versioning**:
This refers to recording and tracking the revisions made to a project, the saved copies of different stages or iterations of that project, and the tags and naming conventions used to differentiate its various versions. 

### Best Practices 
1. Don't push straight to master
As the name suggest, the master branch is the main source of your GitHub project. It is best to push commits to the master branch through pull requests. 

2. Don't leak secrets onto GitHub
Regardless of whether you are pushing to a private or public repository it is essential to keep API keys, private tokens, and SSH keys private. It is recommended to inject secrets as environment variables externally from a secure store. In most cases GitHub bots will alert you if a secret has been pushed to your GitHub repository, if this occurs it is highly recommended to make the necessary changes as soon as possible.

3. Don't commit dependencies into source control
Pushing dependencies such as NPM Packages into your remote origin will cause an increase in the repository size. Remove any project dependencies included in your repositories and let your package manager download them in each build. 

4. Don't commit local files into source control 
It is strongly recommended against commiting local config files to version control. These are usually private configuration files that you do not want to push to remote because they hold secrets, personal preferences, history, or general information that should only be in your local environment. 

5. Create a meaningful git ignore file
A .gitignore file is a must in each repository to ignore predefined files and directories, such as the afformentioned local files. This will help you prevent secret keys, dependencies, and other possible discrepancies in your code. 

6. Enable security alerts
Security alerts are another feature of GitHub, the gist is that GitHub tracks reported security vulnerabilities in some dependencies and can suggest fixes for you. With public repositories, this is enabled by default, however, for private repositories this must be enabled manually. 

## Working with Github

### Command Line Integration (CLI)

### Dreamweaver 

## Further Reading and References
- [GitHub Docs](docs.github.com/en)
- [GitHub Cheat Sheet](https://education.github.com/git-cheat-sheet-education.pdf)
- [More Best Practices](https://resources.github.com/videos/github-best-practices/)