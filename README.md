# A brief tutorial to use Github.

Github is the most commonly used platform for code development and sharing. It also has support in terms of plugins and community for developing software packages, libraries for languages like Python, R, Julia etc., and developing websites. Most of us would have installed packages from Github at some point or the other. 
Originally, git is a version control tool that can keep track of changes to files irrespective of their type over time.And the best part, and perhaps the most important part for us, is the fact that [there aren't any storage limits](https://docs.github.com/en/github/managing-large-files/what-is-my-disk-quota
), irrespective of whether your account is free or paid.

## Basic usage:

There are many good tutorials on what git is and how to use it. [Github's own documentation](https://docs.github.com/en/github/getting-started-with-github) is perhaps the most comprehensive resource. Other useful resources include [Tutorials point](https://www.tutorialspoint.com/git/index.htm), [Github Lab](https://lab.github.com/) and the [git-scm documentation](https://www.atlassian.com/git/tutorials/what-is-version-control). An easy to read beginner-level tutorial explaining different concepts and usage details of git is [here](https://www.atlassian.com/git/tutorials/saving-changes/git-commit). To begin with, the following steps can be used to create and maintain a github repository.

1. Create an account on github.com and create a repository. There are a few customizations you can so here including whether the repository should be private or public. For the purpose of example, let the username on github be "dummy1" and repository name be "repo1".
2. On your local machine, install git. For linux based machines, you can install it in terminal using commands like "apt-get install git". 
3. Let git know who you are, using the following commands. 
```
$ git config --global user.name "User"
$ git config --global user.email "user@email.com"
```
This allows git to maintain a track of who made changes to repositories. Therefore, these details need not be the same as your github account details. 
4. "clone" your github repository to your local machine like so:
```
$ git clone https://github.com/dummy1/repo1.git
```
This will create a copy of the repository in your current directory. If your repository is private, you will be prompted for username and password of the github account. 
5. Add files to the directory on the local machine. Once you have done that, let git know that you have added additional files and that you want git to keep a track of those files. The simplest way to do that would be 
```
$ git add -A
```
which makes git track all the files in your folder. You can also specify files to track based on your requirement. See this [documentation](https://git-scm.com/docs/git-add) for more detail. 
6. Commit changes. This lets git know that you are ready to "stage" the changes you have made to the local repository.
```
$ git commit -m "Brief description of the changes"
```
Git assigns an id to each such commit. You can restore the repository to a previous state using this id.
7. Push your changes from local repository to github repository. 
```
$ git push origin master
```
Based on the commit permissions for the repository on Github, you may be prompted to provide the github username and password. 

After the initial setup, steps 5-7 can be used to keep staging the changes to your repository. 
There can also be multiple local repositories set up on multiple machines connected to the same repository on Github. In such situations, one **must** pull the current state of the Github repository before commiting changes from the local repository. This can be done using:
```
$ git pull origin master
```

## Git is much more than just Github

Github, in all its glory, is only an implementaion of git. As mentioned earlier, git is originally a version control tool. Therefore, you can just mark a local folder on your computer with git (using the command "git init"), add files to the folder, track them and access any version of them in time whenever needed. One can also setup repositories in a machine that can be shared among the machines in the local network. Another useful feature is branching, which is useful when there are multiple collaborators and want to work on different aspects of the repository later to be merged together. 

