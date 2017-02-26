# Git workflow workshop for two programmers



<!-- ***********************************************************-->
## Workshop summary

An exercise to practice git workflow skills. The workshop should be carried out by two programmers, working on two separate computers. The skills practiced include:

- cloning a repository
- creating branches
- switching branches
- adding changes to staging area
- committing changes
- pulling latest version from the remote master branch
- merging master branch into recently created branch
- resolving merge conflicts
- pushing to remote repository
- creating a pull request on Github
- merging a pull request to remote master branch



<!-- ***********************************************************-->
## OK, let's start :rocket:

Your client has just called you and asked to improve their [company website](https://piotrberebecki.github.io/git-workflow-workshop-for-two/).

There are two issues that when resolved will make their site super cool:

1. Spelling mistake in the heading.
1. The name of the css class in the heading needs to be updated.

You decide that one of you (Programmer 1) will resolve issue number 1 while the other person (Programmer 2) will resolve issue number 2.



<!-- ***********************************************************-->
## Step 1 - Programmer 1 forks this repository

1. Programmer 1 [forks](https://help.github.com/articles/fork-a-repo/) this repository.

  <img src="https://help.github.com/assets/images/help/repository/fork_button.jpg" width="500" height="auto">

2. Programmer 1 goes into settings of the newly forked repository and adds Programmer 2 as a [contributor](https://help.github.com/articles/inviting-collaborators-to-a-personal-repository/).

  <img src="https://help.github.com/assets/images/help/repository/repo-settings-collab-autofill.png" width="500" height="auto">

3. Programmer 2 accepts the invitation to the new repository via their email.



<!-- ***********************************************************-->
## Step 2 - Programmer 2 Enables GitHub pages and reports 2 issues

1. Programmer 2 goes into repository settings and enables [GitHub pages](https://help.github.com/articles/configuring-a-publishing-source-for-github-pages/).

  <img src="https://help.github.com/assets/images/help/pages/select-gh-pages-or-master-as-source.png" width="500" height="auto">

2. Programmer 2 goes into repository settings and makes sure that the [issues](https://guides.github.com/features/issues/) feature is enabled.

  <img src="https://help.github.com/assets/images/help/issues/issues_settings_remove_from_repo.png" width="500" height="auto">

3. Programmer 2 creates the following two [issues](https://help.github.com/articles/creating-an-issue/):

  `Fix spelling typo in <h1> heading`

  `Correct the class name of <h1> heading to match the existing class name in the css file`



<!-- ***********************************************************-->
## Step 3 - Both programmers clone the forked repository

1. Both programmers [clone](https://help.github.com/articles/cloning-a-repository/) the forked repository using their terminal.

  <img src="https://help.github.com/assets/images/help/repository/https-url-clone.png" width="500" height="auto">

  ```sh
  $ git clone 'PASTE THE URL OF YOUR REPOSITORY HERE'
  ```

2. Both programmers navigate to the newly created directory.

  ```sh
  $ cd git-workflow-workshop-for-two
  ```



<!-- ***********************************************************-->
## Step 4 - Both programmers create one branch each

1. Both programmers create one [branch](https://help.github.com/articles/about-branches/) each. Unique and descriptive branch names work best, for example, `fix-typo-heading` (Programmer 1) and `update-class-heading` (Programmer 2).

  ```sh
  # Programmer 1:
  $ git branch fix-typo-heading

  # Programmer 2:
  $ git branch update-class-heading
  ```



<!-- ***********************************************************-->
## Step 5 - Both programmers open the `index.html` file and make one requested change each

1. Programmer 1 fixes only the spelling typo in the heading (Workshow -> Workshop).

  ```html
  <h1 class="nice-heading">Git Workflow Workshop</h1>
  ```

1. Programmer 2 updates only the class name of the heading (`nice-heading` -> `page-heading`).

  ```html
  <h1 class="page-heading">Git Workflow Workshow</h1>
  ```



<!-- ***********************************************************-->
## Step 6 - Both programmers save the `index.html` file and check status

1. Both programmers save the file and check the [status](https://git-scm.com/docs/git-status) to confirm that `index.html` file has been modified.

  ```sh
  $ git status
  ```



<!-- ***********************************************************-->
## Step 7 - Both programmers add the modified `index.html` file to the staging area

1. Both programmers add the modified `index.html` file to the [staging area](http://softwareengineering.stackexchange.com/questions/119782/what-does-stage-mean-in-git).

  ```sh
  $ git add index.html
  ```



<!-- ***********************************************************-->
## Step 8 - Both programmers commit their changes.

1. Both programmers [commit](http://stackoverflow.com/questions/27˜Ω45076/what-are-the-differences-between-git-commit-and-git-push) the changes. Before closing the commit message with a quote symbol you can press enter on your keyboard to continue typing in the new terminal line. The text in the second line can be used as an additional message. It is a good practice to link your commit to an existing issue by typing  `Relates #1`. Thanks to using the hash symbol followed by the relevant issue number your commit will be [automatically linked to an existing issue](https://help.github.com/articles/autolinked-references-and-urls/).

  ```sh
  # Programmer 1:
  $ git commit -m 'Fix typo in page heading
  > Relates #1'

  # Programmer 2:
  $ git commit -m 'Update class name in heading
  > Relates #2'
  ```
