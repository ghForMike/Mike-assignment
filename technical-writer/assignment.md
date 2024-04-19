## Overview

This is a technical writing and editing project as part of your interview.

This project is designed to take between 1 - 2 hours.
Please take the time to carefully review the [writing style guide](../styling-guide-snippet.md).

## Instructions

Create a new GitHub repository with the following content (See [content](#content)) as the first commit. Make a branch and open a PR to edit the text for clarity, and include any questions about the content's meaning, as if you were editing a colleague’s work. 

 **Any changes that you think will improve the text and explain the concepts better are welcome**. If anything in the text doesn’t match your opinion on a best practice, feel free to correct the meaning of the text. The result should be a document that you, as a technical writer, would be comfortable sharing with end-users.


Construct your PR to teach the author:
- Make atomic commits.
- Write your commit messages to show your rationale for edits.
- Please construct your commits, commit messages, and PR description as you would for an actual PR as if you were collaborating with a team.
- It is best to edit the files on your local machine and push with the `git` command or a desktop Git application rather than editing directly on the GitHub.com website.

Edit the text so that it is easy to read:
- Correct errors.
- Put the text in active voice and present tense.
- Address the reader as you, not we.
- Phrase statements as positive rather than negative.
- Make the language simple and plain. 
- Avoid euphemisms.
- Structure the text so it has a logical flow. 

Once you're finished with your edits, send the PR link to the HashiCorp recruiter.

**NOTE**: DO NOT FORK THE PROJECT. MAKE A COPY OF ALL FILES, CREATE YOUR OWN FRESH REPOSITORY AND SUBMIT A PULL REQUEST TOWARDS YOUR OWN PROJECT. DO NOT MERGE THE PULL REQUEST.

---

## Content

### Using <code>push</code>, <code>pull</code>, <code>fetch</code>, and <code>merge</code>

Transfer file changes/updates between your local workspace and a remote repository with the following commands:

- **`git push`** – updates the remote repository with changes from your local or tracking branch
- **`git pull`** – retrieves changes from one branch and merges them into the current branch
- **`git fetch`** – imports the latest updates in a remote repository to your tracking branch
- **`git merge`** – combines specified changes from the tracking branch into the remote branch

> **Note**: A tracking branch is a local branch that has a direct origin/master relationship with a remote branch. When you use the commands listed above on a tracking branch, Git automatically knows from where to fetch and the target to merge it with.

The **push** command fetches the latest changes from the remote repository, then compares these with your local branch. If there is divergence —— the commits are out of sync, i.e. the local branch is missing changes in the remote branch —— the push fails, throwing an error, and the conflicts identified must first be reconciled before merging can proceed.

The **pull** command, by contrast, runs `git fetch` with any parameters you specify. Then, depending on the configuration options or command line flags you include, either `git rebase` or `git merge` is called automatically to reconcile any divergence between the two branches. However, merging divergent branches may lead to conflicts that cannot be resolved automatically, especially if changes have been made to the same file in both branches. When this happens, Git will ask you to resolve the conflicts manually.

Invoking `git fetch` updates the local repository with the latest changes from the remote repository. Although the changes are not merged into the current working branch, they are available for merging. Use the **fetch** command when you want to see any changes made to the remote repository since you last fetched or you want to update your local repository with the latest changes from a remote repository that you are not currently working on.

Using `git merge` combines changes from two or more branches into a single branch or multiple sequences of commits into one unified history. When you merge two branches, Git creates a new commit that represents the merge —— a merge commit —— which allows you to track the history of your repository. Merge conflicts that are not resolved automatically require you to manually edit the content before then committing your changes.
