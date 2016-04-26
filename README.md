# gitscripts

These are scripts that I use to streamline my github workflow.  These scripts assume two things:

1.  You're working off of a fork of a master repo and you've set the master repo as a remote called 'upstream' (using a command like `git remote add upstream https://github.com/willfulbard/gitscripts.git`).
2.  You have a pull request template located at repo/.github/PULL_REQUEST_TEMPLATE.md
3.  You have your $EDITOR variable set in your shell to your preferred text editor

## Requirements

git and github's command line interface hub.  You can find installation instructions for hub here:

https://github.com/github/hub

(tl;dr - just run `brew install hub`)

## Installation

Add the folder to your $PATH.  To test you can run `gitcommands` or `gitscripts` to see the help for the scripts.

## Usage

1.  In your repository on the master branch, use `gitstart mybranchname` to start new work on a branch by that name.
2.  Once you've finished and completed some work you'd like to push up, use the `gitprep` command
3.  If the rebasing in `gitprep` worked, then your ready to create a pull request using `gitpullreq`
4.  At this point, a frew different things could happen:
    * If you need to amend your pull request, commit your changes in the branch and run `gitprep` to re-push your changes to your fork.
    * If you want to start new work, then `git checkout master` and start at number 1
5.  Once your pull request has been merged, checkout the branch associated with your pull request and run `gitfinish`.  WARNING: This will delete the branch both locally and remotely.

Have fun!

##TODO
