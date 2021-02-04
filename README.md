# GitHub Informational Guide 

## Author
[Jayden Shaw](mailto:jayden.shaw@stridemgmt.com)
Web Developer, [Stride Management Corp.](https://www.stridemgmt.com/) 

## GitHub 101
[GitHub](https://github.com/) is a web-based version control system which uses Git, the open-source version control software. To put it simply, GitHub is an online hosting hub for git repositories and project. It lets you and other team members work on a project together from anywhere. You can collaborate, learn new skills, and manage projects in one easy-to-use interface. 

## Getting Started

### Requirements
- Create a free [GitHub Account](https://github.com/join?ref_cta=Sign+up&ref_loc=header+logged+out&ref_page=%2F%3Cuser-name%3E&source=header) 
- Watch the [Introduction to GitHub](https://youtu.be/sz6zfrQpCQg) video (21 minutes)
	- Note: in the video it mentions that Private Repositories require a paid account, this is inaccurate as of [January 2019](https://github.blog/2019-01-07-new-year-new-github/)

### Dictionary 

**Repository**:
Also known as a *Repo*, repositories are the essential elements of GitHub. Repositories contain all of the files and revision histories of each project. Repos can be either public or private, and multiple users can work collaboratively within a project's repository. 

**Branch**:
Each repository can contain multiple copies of the same project. Each seperate version is a *branch* of the original project, and changes made to individual branches can be merged into the primary branch if desired. Upon creation of a new repository a branch known as the **Master** branch is created. 

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

7. Write meaningful commit messages
When committing new code to Git it is essential to write meaningful commit messages. A well-crafted Git commit message is the best way to communicate context about a change in the code to other developers, and also your future self. There are several conventions used to write good commit messages, but a few tips are: 
	- Specify the type of commit (feat, fix, style, refactor, test, doc)
	- Remove any whitespace errors
	- Remove unecessary punctuation marks
	- Do not end the commit message with a period or special character, add a a space at the end of the message
	- Capitalize
	- Do not assume the reviewer understands what the original problem was, ensure you add it
	- Do not think your code is self-explanitory
	- Follow the convention used by your team 

## Working with Github
GitHub offers a variety of ways to interact with remote repositories. The most common is with the Command Shell/Line. However, [GitHub Desktop](https://desktop.github.com/) allows you to manipulate GitHub with a GUI. 

### Command Line Integration (CLI)
You can easily work with GitHub using the built-in command shell (aka terminal, command prompt, or command line) of your computer. 

**Install Git**:
- Open the command line and run: `git --version` 
If the command is not recognized, you'll need to install [Git](https://docs.gitlab.com/ee/topics/git/how_to_install_git/index.html)
**Configure Git**:
- Add your GitHub Username: `git config --global user.name <YOUR USERNAME>`
- And your email address: `git config --global user.email <YOUR EMAIL>`
- Check the configuration: `git config --global --list`

**Add a remote repository**:
- Add a remote repository to your local environment: `git remote add origin <REMOTE URL>`

**Download the Changes to Local**:
- Pull the files from a remote repository: `git pull <REMOTE URL> <NAME OF BRANCH>`

**Working with Branches**
- Create a new branch: `git checkout -b <NAME OF BRANCH>`
- Switch to the master branch: `git checkout master`
- Switch to an existing branch: `git checkout <NAME OF BRANCH>`

**Viewing Git Changes**
- View your remote repositories: `git remote -v`
- View untracked/changed files on local repository: `git status`
- View differences between local, unstaged, and repository versions: `git diff`

**Add and Commit Local Changes**:
- Stage changes to be pushed to repository: `git add <FILE NAME/FOLDER NAME>` or `git add .` to add all files
- Write Commit message for changes staged files: `git commit -m "<YOUR MESSAGE WITHIN QUOTES>"`

**Push Changes to GitHub**:
- Push all staged commits to remote branch: `git push <REMOTE> <NAME OF BRANCH>`
- Push all staged commits to master branch: `git push origin master`

**Merge a Branch**:
- Merge a branch with master: `git checkout <NAME OF BRANCH>` then `git merge master`

These are only a few of the most common git CLI commands, for more checkout the [Git Cheat Sheet](https://education.github.com/git-cheat-sheet-education.pdf).

### Dreamweaver 
Dreamweaver has Git integration allowing you to edit files and manage version control within a unified interface. You can pull and push changes, write (meaningful) commit messages, view differences, and perform merges. 

**Account Setup**:
- Create a new Dreamweaver Site
- Create a local site folder
- Select *Associate a Git repository with this site* 
- Select *Clone existing Git repository* if applicable 
- Enter the *https://* URL of your repository
- Enter GitHub username
- Enter your GitHub password

![GitHub Sign In](https://www.computerhope.com/issues/pictures/dreamweaver-git-site-config.jpg)

- Use *Test* to verify that it is working
- Click *Save* 

**Work Flow**:
- **Prior to editing files** perform a *Git Pull*, this will sync your local repository with the remote, giving you all of the new work completed since your last pull
- Save your changes to the Dreamweaver files
- After you have edited and saved a file, it will be listed as an *unstaged file*. Unstaged files are not currently being tracked by Git and are not part of a commit
- To stage a file you have modified, check the box next to the file name

![Dreamweaver Add](https://www.computerhope.com/issues/pictures/dreamweaver-git-stage.jpg) 

- When you are ready to commit your changes, click the *Commit* button

![Dreamweaver Commit](https://www.computerhope.com/issues/pictures/dreamweaver-git-commit-ren1.jpg)

- Enter a meaningful commit message describing your changes and click *OK*
- When you are ready to push your changes to the remote repository click *Git Push* 

![Dreamweaver Push](https://www.computerhope.com/issues/pictures/dreamweaver-git-push.jpg)

## Further Reading and References
- [GitHub Docs](docs.github.com/en)
- [GitHub Cheat Sheet](https://education.github.com/git-cheat-sheet-education.pdf)
- [GitHub Learning Lab](https://lab.github.com/)
- [More Best Practices](https://resources.github.com/videos/github-best-practices/)