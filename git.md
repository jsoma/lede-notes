# Using `git`

`git` is cool! `git` is fun! `git` will do your dishes if you only remember a few simple commands. If it's a repository that you've already made (like your **Notes** one) you can skip down to adding files and making commits.

## Creating a repository + connect to the remote repository

Do you already have a respository in that folder? Did you set it up earlier? If not..

First, you want to get your local repo (a.k.a. the copy on your machine) initialized.

    git init

Then you'll want to connect it to the remote on you made on github.

    git add remote origin https://github.com/yourusername/reponame.git

**Don't cut just and paste that!** You'll go to prison. Instead, make sure you're using your username and repository name - it's the same URL as in your browser, but with a `.git` at the end. You can also get it by clicking on the right hand side of your page where it says "HTTPS clone URL."

**NEXT UP:** You probably want to add your files

## Add new files

Unlike something like Dropbox, `git` doesn't pay attention to new files unless you tell it to. You can tell it to pay attention by using `git add`. You'll want to walk through and add the files one at a time.

    git add somemarkdown.md
    git add pythonstuff.py
    git add anotebook.ipynb

There's a way to add them all at one, but *I'm not telling you how*.

**NEXT UP:** You'll also need to **commit** them in order to get them to *actually* save.

## Saving changes

Whether you're adding new files or just changing existing ones git knows about, you'll need to commit your changes.

    git commit -m "Saving some files"
  
Make sure you don't put a space after the `m`! And be careful with your quotation marks, it's easy to forget to close them.

Even though you've saved your changes locally, you still want them to be up on GitHub!

    git push

The first time you run this on a new repo you'll need to specify `git push -u origin master` so it knows where to send it (Remember when we did `remote add origin`? Yeah, it's related to that.).

**NEXT UP:** What about changes already on GitHub? 

## Pulling from GitHub

Let's say something else made a change and pushed it to GitHub, or maybe you edited a file from their editor window. Your computer isn't up to date! It'll probably yell if you try to `git push`. You'll want to download the changes from GitHub using

    git pull

## Copying other repositories

Let's say you really like my repository, and you'd like to stay in touch! You'd like to be able to use `git pull` to pull down any edits and get any new files I've made. To copy a repository to your computer, you use the command

    git clone https://github.com/theirusername/theirreponame.git

and it'll create a new folder with all of the contents.

**DO NOT DO THIS INSIDE OF ONE OF YOUR REPOSITORIES.** (please)

## Review

`git init` to initialize a new local repo

`git remote add origin https://github.com/username/repo.git` to connect to GitHub from your local repo

`git add filename.py` to tell `git` to track changes for a new file

`git commit -m "Here are my comments"` to save changes to your local repo

`git push` to push your changes up to git

`git pull` to download other peoples' changes from git
