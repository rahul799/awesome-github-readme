# Contribution Guidelines

Please ensure your pull request adheres to the following guidelines:

- Alphabetize your entry.
- Search previous suggestions before making a new one, as yours may be a duplicate.
- Suggested READMEs should be beautiful or stand out in some way.
- Make an individual pull request for each suggestion.
- New categories, or improvements to the existing categorization are welcome.
- Keep descriptions short and simple, but descriptive.
- Start the description with a capital and end with a full stop/period.
- Check your spelling and grammar.
- Make sure your text editor is set to remove trailing whitespace.
- Use the `#readme` anchor for GitHub READMEs to link them directly

Thank you for your suggestions!

# How to contribute
Geeks who are eager to contribute, must read it. 

## Creating Issues

- Make sure you have a GitHub account.
- Search GitHub and Google to see if your issue has already been reported
        - Create an issue in GitHub, assuming one does not already exist.
	- Clearly describe the issue including steps to reproduce when it is a bug.
	- Make sure you fill in the earliest version that you know has the issue.

## Getting Started

1. Goto the [awesome-github-readme](https://github.com/rahul799/awesome-github-readme/) repository
2. Click on the Fork button in the upper right corner.

Introduce your self to GIT, make sure you use an email associated with your GitHub account.
```
git config --global user.name "John Doe"
git config --global user.email johndoe@example.com
```

Make sure you clone the forked repository.
```
git clone https://github.com/<your username>/awesome-github-readme.git
```

Switch awesome-github-readme to your fork
```
git remote set-url origin https://github.com/<your username>/awesome-github-readme.git
```

Setup awesome-github-readme to be able to fetch from the master
```
git remote add upstream https://github.com/The-Codesis/awesome-github-readme.git
```

## Adding Features

When you add a new feature always create an issue first, this allows others to comment and give you tips. It will also help us keep track of what people are adding and with new releases helps us to write new release notes and give you credit for your work.

Secondly, always work in a branch, never work on the master branch. Keep your master branch in sync with the master of the official Simple-Static-Website repository. This makes the pull requests (you do want your work to be in the main branch right?) easier for us.

Finally, try to keep your branches focused on fixing/adding only one feature and try not to fall in the trap of doing a lot of things in a single branch. This will not only make it harder for us to process your pull request but makes it take longer before you can submit your pull request. Small pull requests are more likely to be looked at faster and pulled into the main branch faster.

Here is a simplified workflow on how to add a new feature:

### Syncing with fork

Syncing your forked repository to the original repository is an important step before submitting any pull request to the original repository. So, it goes something like, you fetch from the original repository (Upstream Repository) to your working area (your local copy) and merge it with the fork's master branch and then you push it to your forked Github repository.

You can see all your remotes with ```git remote -v```, if you don't have upstream set as ```https://github.com/rahul799/awesome-github-readme.git```, set up  the original repository as your upstream.
```
git remote add upstream https://github.com/rahul799/awesome-github-readme.git
```
By now, you have set the upstream as the original repository i.e. ```https://github.com/rahul799/awesome-github-readme.git``` and the origin as the forked repository i.e. ```https://github.com/<your username>/awesome-github-readme.git```.

Now, fetch all of the changes from the original repository (note that commits to the original repository will be stored in a local branch called, upstream/master).
```
git fetch upstream
```
Since you want fork's master branch and the original's master branch should be synced, so make sure you are on fork's master branch and merge the changes from the upstream/master into your fork's local master branch (you may need to resolve the conflicts).
```
git checkout master
git merge upstream/master
```
At this point, your local branch is synced to the original repository's master branch. To update your forked Github repository, you need to push your changes to the forked Github repository.
```
git push origin master
```

