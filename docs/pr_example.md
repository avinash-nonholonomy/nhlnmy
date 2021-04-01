_warning_ this is written as a tutorial - your mileage may vary! Contact [mailto:avinash@nonholonomy.com](avinash) with any issues. 

# Introduction

## Nota Bene

Distributed Version Control is a *HARD TOPIC*. In practice anything beyond the simplest basics covered in this guide are usually handled by:
  - a) Finding the person in your company that is an expert.
  - b) Kindly asking them how to resolve the strange situation you've found yourself in.
  - c) Thanking them profusely, especially by making notes to avoid that one problem in particular in the future.

## Glossary
- repo: repository
- PR : Pull Request: A principled way to submit changes to an existing code repo.
- clone : An (often initial) direct copy of a code repo.
- pull : A one-way attempt to synchronize new code from the central repo to your local copy. May trigger a `merge`.
- commit: How you log meaningful changes to a codebase with a message describing the change. 
- push : A one-way attempt to synchronize any local changes you have made to the central repo. Should definitely be `reviewed` before your change is `pulled` into the central repo.
- branch : A way to safely make changes to a codebase without losing the original state. 
- fork: Typically the first time you `branch` off an existing repository for individual developement.
- vcs: Version Control System: a way to maintain code with all the bugs an bug fixes! There are many implementations of this out there, but they follow similar concepts to `git` which we will use in this guide.
- git: An open source version control scheme invented b

## Recommended Reading
- Much of this doc is based on this [guide](http://oss-watch.ac.uk/resources/pullrequest) by Mark Johnson.
- This [tutorial](https://git-scm.com/docs/gittutorial) is a great example of how to use `git` the package.
- Happily accepting PRs for more references! {wink-emoji-not-found-please-pr}



# Example Pull Request

- First, `clone` the repository! This is how you get the source code onto your local machine.

```bash
git clone https://github.com/avinash-nonholonomy/nhlnmy.git
cd nhlnmy
```

- You'll often be working with a repository you already cloned that may have changed before you started coding - so best practice is to  regularly `pull` the latest changes from the `main` branch. From the source directory you can run: 

```bash
git pull
```

_WARNING_ This may result in something called a `merge conflict`. This is a good thing! It means that a collaborator has made changes that change the same files you've tried to edit. *Catching these errors is a huge part of why we have Pull Request processes!!!* The git tool is great using the `diff` format to make it explicit. The `diff` format is usually something like `>>>` or `+++` for new addtions to a file, or `<<<` or `---` for things removed from a file. Your job is to resolve the changes such that none of the strange `diff` symbols remain, and then re `commit` 



# Create a new branch for the PR
```bash
git checkout -b "pr_example_00"

```

- In practice you've already cloned the repository, so *always* make sure you have the latest code by doing a `pull` before starting a new PR!

```bash
git pull
```

- Next, create/modify what you need to! For this example PR (pr_example_00) we added in this readme. But in general this is where you write the code that adds new features or fixes bugs.

- Then, you want to `push` your changes for review!
  - btw if you type `git push` with no arguments it will prompt you with the right incantation.

```bash
    git push --set-upstream origin pr_example_00



```

# The Advanced Version Caveat
The above guide assumes you have full access to a repository which is in general a terrible idea for many *many* reasons. What we usually do is a slight wrapper of the above process:

- `fork` the repository you want to make changes to
- `clone` it to your local machine
- 




