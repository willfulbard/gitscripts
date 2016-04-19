# gitscripts

These are scripts that I use to streamline my git workflow.  These scripts assume that you're working off of a branch of a master repo and that you've set the master repo as a remote by the name of 'upstream' (using a command like `git remote add upstream https://github.com/willfulbard/gitscripts.git`).

## Requirements

git and github's command line interface hub.  You can find installation instructions for hub here:

https://github.com/github/hub

(tl;dr - just run `brew install hub`)

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
*  Change vim to $EDITOR or whatever the variable is that git uses to indicate the editor
