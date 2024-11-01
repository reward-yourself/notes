# Merging via command line
If you do not want to use the merge button or an automatic merge cannot be performed, you can perform a manual merge on the command line. However, the following steps are not applicable if the base branch is protected.
	
- Step 1: Clone the repository or update your local repository with the latest changes.
 ```git pull origin main```
- Step 2: Switch to the base branch of the pull request.
 ```git checkout main```
- Step 3: Merge the head branch into the base branch.
 ```git merge my-first-branch```
- Step 4: Push the changes.
 ```git push -u origin main```
