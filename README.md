# Outlier-Engineering-Git-Challenge

here are the steps that will let you add both changes to the `master` branch by using `git rebase`:

1. First, ensure you are on the `master` branch:

    ```bash
    git checkout master
    ```

2. Then pull the latest commits from the remote repository to update your local `master`:

    ```bash
    git pull origin master
    ```

3. Next, check out the branch containing the `add base64 endpoint` commit:

    ```bash
    git checkout base64-endpoint-branch
    ```

4. Perform a rebase operation to shift changes from `base64-endpoint-branch` directly on top of the `master` branch:

    ```bash
    git rebase master
    ```

5. After resolving possible conflicts, switch back to the `master` branch to merge the `base64-endpoint-branch`:

    ```bash
    git checkout master
    git merge base64-endpoint-branch
    ```

6. Now repeat the process for the `add user-agent endpoint` commit. Check out the branch containing this commit:

    ```bash
    git checkout user-agent-endpoint-branch
    ```

7. Then again, rebase it onto `master`:

    ```bash
    git rebase master
    ```

8. After resolving possible conflicts, switch back to the `master` and merge `user-agent-endpoint-branch`:

    ```bash
    git checkout master
    git merge user-agent-endpoint-branch
    ```

Your `master` branch will now contain all three commits in the specified order. 
