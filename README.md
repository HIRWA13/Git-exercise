# Git Exercises

Welcome to the ultimate Git training ground! This comprehensive exercise combines essential Git skills, from manipulating history to advanced branching strategies. Hone your Git mastery through a series of practical challenges designed to solidify your understanding.

**Getting Started:**

1. **Create a New Git Repository:**
   - Head over to GitHub and create a new repository. Clone this repository to your local machine using a Git client.

2. **Initialize Your Environment:**
   - Open a terminal window and navigate to your cloned repository directory.
   - Run the following commands to create some dummy files and commit them:

   ```bash
   touch test{1..4}.md
   git add test1.md && git commit -m "Create initial file"
   git add test2.md && git commit -m "Create second file"
   git add test3.md && git commit -m "Create third and fourth files"
   ```

**Challenges (30+ total):**

**Part 1: Refining Git History (10 Challenges)**

1. **Missing File Fix:**

   - Run `git status` and `git log` to assess the current state of your repository.
   - From the status you will see that you forgot to add `test4.md` in the last commit.

   **Challenge:** Recover from this error by adding `test4.md` and amending the commit message with an appropriate description.

2. **Editing Commit History:**

   - It's crucial to maintain accurate commit messages. Let's say you want to modify the message for "Create second file".

   **Challenge:** Utilize interactive rebasing (`git rebase -i`) to edit the commit message and ensure clarity.

3. **Keeping History Tidy - Squashing Commits:**

   - Squashing combines multiple commits into a single one. Let's merge "Create second file" into "Create initial file" for a cleaner history.

   **Challenge:** Use interactive rebasing with the `squash` command to achieve this.

4. **Splitting a Commit:**

   - Imagine "Create third and fourth files" describes too much at once. Separate them for better tracking.

   **Challenge:** Leverage `git reset` to separate the files into individual commits with distinct messages.

5. **Advanced Squashing:**

   - Let's explore more complex squashing. Can you combine the last two commits ("Create third file" and "Create fourth file") into a single commit named "Create third and fourth files"?

   **Challenge:** Utilize interactive rebasing with the `squash` command to achieve this advanced squash.

6. **Dropping a Commit:**

   - We all make mistakes. Imagine needing to completely remove an unwanted commit from your history.

   **Challenge:** Use `git rebase -i` to identify and remove this commit, cleaning up your history.

7. **Reordering Commits (Bonus):**

   - Delve deeper into `git rebase -i`. Can you rearrange commits within your history using this command?

8. **Cherry-Picking Commits (Bonus):**

   - Imagine you only desire a specific commit from another branch. Research and use `git cherry-pick` to selectively bring that commit into your current branch.

9. **Visualizing Commit History (Bonus):**

   - Tools like `git log --graph` or a graphical Git client can help visualize your commit history. Explore these tools for a clearer understanding of your workflow.

10. **Understanding Reflogs (Bonus):**

   - Reflogs track Git operation history. Research `git reflog` to learn how you can navigate back to previous states in your repository if needed.

**Part 2: Branching Mastery (10 Challenges)**

1. **Feature Branch Creation:**

   - Imagine working on a new feature named `new-feature`. Let's establish a dedicated branch for it.

   **Challenge:** Create a new branch named `feature/new-feature` and switch to that branch.

2. **Working on the Feature Branch:**

   - Create a new file named `feature.txt` in this branch and add some content to it.
   - Commit these changes with a descriptive message like "Implemented core functionality for new feature".

3. **Switching Back and Making More Changes:**

   - It's common to switch between branches during development.

   **Challenge:** Switch back to the `main` branch (previously master) and create a new file named `readme.txt` with some introductory content. Commit these changes with a message like "Updated project readme".


4. **Local vs. Remote Branches (Bonus):**

   - So far, we've been working with local branches that exist on your machine. Research the concept of remote branches, which are copies of your local branches stored on a Git hosting platform like GitHub. Learn how to push your local branches to remote repositories and pull changes from them to keep your local and remote repositories in sync.

5. **Branch Deletion:**

   - After merging or completing work on a feature branch, it's good practice to remove it.

   **Challenge:** Delete the `feature/new-feature` branch once you're confident the changes are integrated into `main`.

6. **Creating a Branch from a Commit:**

   - You can also create a branch from a specific commit in your history.

   **Challenge:** Use `git checkout -b new-branch-from-commit HEAD~2` (adjust the commit hash as needed) to create a new branch named `new-branch-from-commit` starting from the commit two positions back in your history.

7. **Branch Merging:**

   - Now that you've completed work on your feature branch, it's time to integrate it into `main`.

   **Challenge:** Merge the `new-branch-from-commit` branch into the `main` branch. Address any merge conflicts that might arise.

8. **Branch Rebasing (Optional):**

   - Rebasing is another method to integrate changes from a feature branch. It rewrites your branch history by incorporating its commits on top of the latest commit in the target branch (`main` in our case).

   **Challenge (Optional):** Try rebasing the `new-branch-from-commit` branch onto the `main` branch. Remember, rebasing rewrites history, so use it with caution, especially in shared repositories.

9. **Renaming Branches:**

   - Branch names can sometimes evolve. Let's rename `new-branch-from-commit` to a more descriptive name.

   **Challenge:** Use `git branch -m new-branch-from-commit improved-branch-name` to rename your branch.

10. **Checking Out Detached HEAD (Bonus):**

   - In specific situations, you might need to detach HEAD from your current branch. Research `git checkout <commit-hash>` (replace with the desired commit hash) to understand this concept.

**Part 3: Advanced Workflows (10+ Challenges)**

1. **Stashing Changes:**

   - Imagine you're working on some changes in the `main` branch but need to attend to something urgent. You don't want to lose your uncommitted work.

   **Challenge:** Stash your current changes in the `main` branch using `git stash`.

2. **Retrieving Stashed Changes:**

   - Later, when you're ready to resume working on those stashed changes, you can retrieve them.

   **Challenge:** Apply the most recent stash back onto the `main` branch using `git stash pop`.

3. **Branch Merging Conflicts (Continued):**

   - Merge conflicts can arise when the same lines of code are modified in both branches being merged.

   **Challenge (Optional):** Simulate a merge conflict scenario (you can create conflicting changes in a file on both `main` and a new feature branch). Then, try merging again and resolve the conflicts manually using your text editor.

4. **Resolving Merge Conflicts with a Merge Tool (Bonus):**

   - Explore using a merge tool like `git mergetool` to help you visualize and resolve merge conflicts more efficiently.

5. **Understanding Detached HEAD State (Bonus):**

   - Detached HEAD refers to a state where your working directory is not associated with any specific branch. Research the implications and how to recover from this state using commands like `git checkout <branch-name>`.

6. **Ignoring Files/Directories:**

   - You might have files or directories you don't want to track in Git. Create a `.gitignore` file to specify these exclusions.

   **Challenge:** Add a pattern like `/tmp` to your `.gitignore` file to exclude all temporary files and directories from version control.

7. **Working with Tags:**

   - Tags act like bookmarks in your Git history. Create a tag to mark a specific point in your development.

   **Challenge:** Use `git tag v1.0` to create a tag named `v1.0` on the current commit in your `main` branch.


**Part 3: Advanced Workflows (Continued)**

8. **Listing and Deleting Tags (Continued):**

   **Challenge:** Use `git tag` to list all existing tags. Then, use `git tag -d <tag-name>` to delete a specific tag (replace `<tag-name>` with the actual tag you want to remove).

9. **Pushing Local Work to Remote Repositories:**

   - Once you're happy with your local changes and branches, it's time to share them with others.

   **Challenge:** Assuming you've set up a remote repository on a Git hosting platform (like GitHub), use `git push origin <branch-name>` (replace `<branch-name>` with the actual branch you want to push) to push your local branch to the remote repository.

10. **Pulling Changes from Remote Repositories:**

   - Collaboration often involves pulling changes from the remote repository made by others.

   **Challenge:** Use `git pull origin <branch-name>` (replace `<branch-name>` with the actual branch you want to pull) to fetch changes from the remote repository's `main` branch and merge them into your local `main` branch. Address any merge conflicts that might arise.