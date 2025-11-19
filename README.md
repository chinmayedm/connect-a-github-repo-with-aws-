# Connect a GitHub Repo with AWS
![repo](https://github.com/chinmayedm/connect-a-github-repo-with-aws-/blob/main/Screenshot%202025-11-19%20at%2020.57.33.png?raw=true)

# What is GitHub?

GitHub is a platform for version control and collaboration, allowing developers to store and manage their code repositories.
In today’s project, I used GitHub to host my project, track changes, collaborate, and push updates from my local Git repository to the cloud.

One thing I didn’t expect in this project was the need to set up a GitHub token for authentication when pushing code. It added an extra layer of security but was unexpected compared to using a password for the first time.

# Git and GitHub

Git is a version control system that tracks changes in your projects and helps in collaboration.

I installed Git using the following commands:

``` 
sudo dnf update -y

sudo dnf install git -y
```

GitHub is a platform for hosting and managing code.
I used GitHub in this project to track file changes, collaborate easily, and view updates in a user-friendly way. It simplifies teamwork by enabling shared codebases, reviews, and version control.
![git and github](https://github.com/chinmayedm/connect-a-github-repo-with-aws-/blob/main/Screenshot%202025-11-19%20at%2020.58.08.png?raw=true)

# My Local Repository

A Git repository is a storage space where your project’s files and their change history are tracked. It helps manage versions, collaborate with others, and roll back to previous states if needed.

I initialized a new Git repository using:

```
git init
```

After running git init, the terminal confirmed that a new Git repository was initialized.
![local repo](https://github.com/chinmayedm/connect-a-github-repo-with-aws-/blob/main/Screenshot%202025-11-19%20at%2020.58.41.png?raw=true)

# Branches

A branch in Git is a separate line of development that lets you work on features or fixes independently without affecting the main codebase.

# Pushing Local Changes to GitHub

To push local changes to GitHub, I ran three commands:

1. git add
```
git add .
```

This adds all changes to the staging area, where updates are prepared before committing.

2. git commit
```
git commit -m "message"
```

This saves the staged changes to the repository with a message describing the update.

3. git push
```
git push -u origin master
```

This uploads the committed changes to the GitHub repository.
The -u flag sets the upstream branch so future pushes can be done with just:

```
git push
```
# Authentication

When I committed changes to GitHub, Git asked for my credentials to verify my identity and ensure I had permission to push updates. This maintains the security and integrity of the shared codebase.

# Local Git Identity

Git needs my name and email because it uses them to track the changes I make.
Running:

```
git log
```


showed a detailed history of all commits, including commit hashes, author information, dates, and messages.

# GitHub Tokens

GitHub authentication failed when I entered my password because GitHub no longer supports password-based authentication for Git operations.
Instead, it requires a Personal Access Token (PAT) for secure authentication.

A GitHub token is a secure access key that allows authentication without using a password. I used one in this project because GitHub requires tokens instead of passwords for better security.

I set up a GitHub token by going to my GitHub account settings, opening Developer Settings, selecting Personal Access Tokens, and generating a new token with the required repository permissions.

# Making Changes Again

I updated the index.jsp file in the project, but I couldn’t see the changes in my GitHub repo initially because I had not committed and pushed them yet.

I finally saw the changes after running:

```
git commit -m "Updated index.jsp"
```

and then:

```
git push -u origin master
```


This uploaded the updates to the remote repository successfully.
