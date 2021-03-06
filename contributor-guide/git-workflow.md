# Git workflow

## Setting up

**Step 1:** Fork the Code Collabo repo you want to work on. We'll use [node-mongo-cli](https://github.com/code-collabo/node-mongo-cli) as example. Open up your terminal on your computer.

**Step 2:** Clone that forked version onto your computer with: `git clone git@github.com:your-github-username/node-mongo-cli.git`

If you prefer or are using https, use this instead: `git clone https://github.com/your-github-username/node-mongo-cli.git`

**Step 3:** Set original repo as upstream: `git remote add upstream git@github.com:code-collabo/node-mongo-cli.git`

You can check that your forked repo's url is set as the origin, and the original repo's url is set as the upstream with: `git remote -v`

## Updating your fork

Setting original repo as the upstream means you'll be able to update your fork, with the latest changes made to the original repo using the `git pull` command. Before you start or as you work on the code, update your fork so that you'll be working with latest changes from the original repo.

To pull changes for the develop branch for example, checkout to develop: `git checkout develop`

Then use the command: `git pull` or `git pull upstream develop`

In summary, just checkout to the branch you want to pull changes into `git checkout branch-name` and use the `git pull` or `git pull upstream branch-name` command.

## Gitflow and branches

The only time you have business with the main branch is if you choose to pull changes while in the main branch as explained in _**updating your fork**_.

{% hint style="warning" %}
You are not to make changes to **main branch**, as it contains the production-ready version of the code.
{% endhint %}

A branch with name `develop` has been created for development purpose.

{% hint style="warning" %}
Also, you are not to make changes to the _\*\*_**develop branch**. Instead, **create a feature branch** **from the develop branch** and make your changes there.
{% endhint %}

## Creating a feature branch

Checkout to develop to ensure the feature branch you will create is a copy of the develop branch: `git checkout develop` \(If the repo does not have a develop branch, then checkout to main instead\).

Create a feature branch while inside develop branch: `git checkout -b feature-branch-name-here`

{% hint style="warning" %}
Always make sure you checkout to develop branch before creating a new feature branch.
{% endhint %}

## Naming a feature branch

To help reviewers know what you are working on, give your feature branch a descriptive name containing: `issueNumber-action-description`.

* **IssueNumber:** Check the issue you are working on to get issue number. 
* **Action:** Words like `fix`,  `setup`,  `feature` etc. 
* **Description:** What you are setting up, fixing, updating etc.

So, feature branch name could look something like `7-setup-jasmine-test`, `19-update-readme`, `1001-fix-db-error` etc. You can decide to leave out action, if you like, when branch name gets too long.

## Submitting your changes

After you've made the needed changes in the feature branch you created, add, commit, push and submit a pull request.

Add changes: `git add .`

Commit changes: `git commit -m "Add your commit message here"`

Push changes from your feature branch to the remote for the first time: `git push -u origin your-branch-name`

Pushing every other time: `git push`

### Submit pull request

Next create and send a `pull request` so that your code can be reviewed. Also add description and testing checklist to your pull request. See examples of previously made pull requests for how to go about this: [pull request 11](https://github.com/code-collabo/node-mongo-cli/pull/11#issue-584788302), [pull request 50](https://github.com/code-collabo/node-mongo-cli/pull/50#issue-602381499).

## Further study

Although the sections above are what you will be needing to contribute, see [this YouTube resource](https://youtu.be/jFL228SfOmU) to help understand the git workflow term better.

