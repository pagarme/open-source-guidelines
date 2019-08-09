# Contributing

There are many ways to contribute to this repository. You can:

- [Create Issues](#Creating-an-Issue) reporting bugs, suggesting new features or enhancements;
- [Create Pull Requests](#Creating-a-Pull-Request) fixing bugs, adding features or enhancements.

Both are equally important :blush: 

## Creating an Issue

To create an Issue go to [here](https://github.com/pagarme/INSERT-REPOSITORY-NAME/issues/new).

Add a sucint title describing the subject, being either a bug, feature, etc.

Describe with more detail below what it is about, and if possible add the following things:

### If it is a bug/problem

- Information about which conditions the situation happens, like the Operating System;
- How it was actually achieved, like which terminal commands where used to get there.

This helps to understand how to replicate the issue for whoever is going to solve it.

### If it is a feature/suggestion

- How is the enhancement like;
- How it should behave;
- Edge cases, if found.

The more information you give, it will make the life easier of whoever is going to implement it :slightly_smiling_face:


## Creating a Pull Request

To create a Pull Request, first you will need to do the following steps:

1. Make a fork of this repository and clone it in your computer;
2. Make a new branch based of `master` (`git checkout -b fix/button-size`, for example);
3. Make your changes, creating commits that group these changes;
4. Send your branch to your fork (`git push origin fix/button-size`, for example);
5. Now you can finally create the Pull Request :tada: [here](https://github.com/pagarme/INSERT-REPOSITORY-NAME/compare). You will have to change the `compare` branch to your branch (`fix/button-size`, for example).

### Guidelines

To make the repository be sane to work with, we use a guideline of rules that define how the code, commits, etc should be.

Usually we enforce some of them via Continuous Integration (TravisCI/CircleCI for example).

Take a look at some of them:

- [JavaScript Style Guide](https://github.com/pagarme/javascript-style-guide)
- [Git Style Guide](https://github.com/pagarme/git-style-guide)

### Out of date branch

Sometimes a Pull Request is made, and the `master` branch ends up getting updated before the merge of it. When that happens the branch of the Pull Request should get updated to continue for a possible merge.

We usually do that update via `git rebase`. In this scenario do the following:

1. Add our `"upstream"` as remote: `git remote add upstream https://github.com/pagarme/INSERT-REPOSITORY-NAME`. You can do the same with `ssh` instead of `https`, it doesn't matter :wink:
2. Get the updates from `"upstream"`: `git fetch upstream`;
3. Do the rebase of your branch: `git rebase upstream/master <your-branch>` (without `<>`);
4. Resolve the conflicts if necessary, and use `git rebase --continue` to continue, commit by commit;
5. Do the force push in your fork: `git push origin <your-branch> --force-with-lease` (without `<>`).
