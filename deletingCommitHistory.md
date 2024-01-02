# Creating and Updating Default Branch (main) in Git

To create or update the default branch in your Git repository, follow these steps:

1. **Checkout/Create Orphan Branch:**
   ```bash
   git checkout --orphan latest_branch
   ```
2. **Add All Files to the Newly Created Branch:**
   ```bash
   git add -A
   ```
3. **Commit the Changes:**
   ```bash
   git commit -am "commit message"
   ```
4. **Delete Default (main) Branch (This step is permanent):**
   ```bash
   git branch -D main
   ```
5. **Rename the current branch to main:**
   ```bash
   git branch -m main
   ```
5. **Finally, All Changes Are Completed on Local Repository, force update your remote repository:**
   ```bash
   git push -f origin main
   ```