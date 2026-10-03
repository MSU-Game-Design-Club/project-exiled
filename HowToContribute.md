# How to Contribute

All working changes will be pull requested to the `dev` branch, with releases being pull requested to `main`.

## Don't Push to Main or Dev
When working on this project, the only changes allowed to be made to the `main` and `dev` branches will be through pull requests that have to be reviewed before being merged.

## Issue Driven

Development will be issue driven, meaning all changes or code added to `dev` should come from an issue.

GitHub supports Issues where you can post an issue. Issues are things that need to be worked on, such as adding a feature or fixing a bug.

When an issue is created, you will have the option to assign someone to the issue and create a branch for it. 
Issue branch names should always be of the form:

```text
#-issue-name
```

where `#` is the issue number and `issue-name` is the title of the issue branch.

GitHub will automatically create branches in this form when you press the *Create branch* button while viewing an issue.

Issues also act as threads, so you can use an issue as a conversation and work on it while developing on the issue branch. You can also use the issue to ask for feedback during development.

## Issue Scoping
If the scope of an Issue is large then we should take a problem and break it down into smaller issues such that the compleition of the smaller issues helps to resolve the whole issue. 

You can refer to existing issues using `#number` syntax within a GitHub issue post. For example,
if there exists an issue like `2-create-weapons`, then there should also exist sub issues that issue #2 references, such as `3-create-ranged-weapons` and `4-create-melee-weapons`.

Each sub issue should have its own branch, and those branches should be merged into the parent issue's branch rather than directly into dev.

So with our example changes created in issues #3 and #4 should be merged into issue #2's branch. Once issue #2 is fully resolved, its changes can then be merged into the `dev` branch, and eventually `main`. 

This way, we can trace the development of features in a chronological way.

## General Workflow
For a normal issue, the workflow is:
1. Find or create the issue you are working on.
2. Assign the issue to yourself or others interested with working on this issue.
3. Create the issue branch using GitHub's *Create branch* button.
4. Clone the repository or switch to the issue branch locally.
5. prior to working run `git pull` to get the lastest changes. 
6. Make your changes.
7. Push your changes to the issue branch.
8. Create a Pull Request targeting `dev` or the issue's parent branch.
9. Have the Pull Request reviewed.
10. Merge the Pull Request once it has been approved.

If you are working on an ongoing branch, always ensure that your branch is up to date with its target branch before creating a Pull Request.
Rebasing can be used to keep the branch up to date and reduce the chance of having large merge conflicts.
