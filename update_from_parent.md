To update your fork with the latest changes from the parent repository, follow these steps:

1. **Add the parent repository as an upstream remote (if you haven’t already):**

   Open your terminal, navigate to your fork's directory, and run:

   ```bash
   git remote add upstream https://github.com/buildfastwithai/gen-ai-experiments.git
   ```

   Replace the URL with the actual URL of the parent repository.

2. **Fetch the latest changes from the parent repository:**

   ```bash
   git fetch upstream
   ```

   This command downloads the commits and branches from the parent repository without modifying your working files.

3. **Merge (or rebase) the changes into your local branch:**

   If you want to merge the changes into your local branch (commonly the main or master branch), first switch to that branch:

   ```bash
   git checkout main
   ```

   Then merge the changes:

   ```bash
   git merge upstream/main
   ```

   (If the parent repository uses `master` as the default branch, replace `main` with `master` in the commands.)

   Alternatively, if you prefer a rebase instead of a merge:

   ```bash
   git checkout main
   git rebase upstream/main
   ```

   Rebasing makes your branch history linear but requires careful handling if there are conflicts.

4. **Push the updated branch to your fork on GitHub:**

   After merging or rebasing, push your changes to your GitHub fork:

   ```bash
   git push origin main
   ```

   If you rebased and encounter push errors, you may need a force push:

   ```bash
   git push origin main --force
   ```

   Note: Use force push with caution as it rewrites history on the remote branch.

These steps will update your fork with the latest changes from the parent repository.