# git-comands





Here’s a list of commonly used Git and GitHub commands categorized by their purpose. Since you already have experience with Git and GitHub, I’ll include useful commands for beginners and advanced users alike. Let me know if you want additional details on any of these commands!  

---

## **Basic Git Commands**
1. **Setup and Configuration**
   - `git config --global user.name "Your Name"`: Set your name.
   - `git config --global user.email "youremail@example.com"`: Set your email.
   - `git config --list`: View your Git configuration.

2. **Initialize a Repository**
   - `git init`: Initialize a new Git repository in the current directory.

3. **Clone a Repository**
   - `git clone <repository-url>`: Clone a remote repository to your local machine.

4. **Add and Track Changes**
   - `git status`: Show the status of changes in your working directory.
   - `git add <file>`: Stage a file for commit.
   - `git add .`: Stage all changes in the current directory.

5. **Commit Changes**
   - `git commit -m "Your commit message"`: Commit staged changes with a message.
   - `git commit -a -m "Your commit message"`: Stage and commit tracked files in one step.

---

## **Intermediate Git Commands**
1. **Branching**
   - `git branch`: List all branches in the repository.
   - `git branch <branch-name>`: Create a new branch.
   - `git checkout <branch-name>`: Switch to a different branch.
   - `git switch <branch-name>`: An alternative for `git checkout` for switching branches.

2. **Merging**
   - `git merge <branch-name>`: Merge changes from another branch into the current branch.

3. **Remote Repositories**
   - `git remote -v`: Show remote repositories.
   - `git remote add origin <repository-url>`: Add a remote repository named `origin`.

4. **Push and Pull**
   - `git push origin <branch-name>`: Push your changes to a remote repository.
   - `git pull origin <branch-name>`: Pull updates from a remote repository.

5. **Viewing Logs**
   - `git log`: View the commit history.
   - `git log --oneline`: View a compact commit history.

---

## **Advanced Git Commands**
1. **Stashing**
   - `git stash`: Save uncommitted changes for later use.
   - `git stash list`: List stashed changes.
   - `git stash apply`: Apply stashed changes back to the working directory.

2. **Rebasing**
   - `git rebase <branch-name>`: Reapply commits on top of another branch.

3. **Tagging**
   - `git tag`: List all tags.
   - `git tag <tag-name>`: Create a new tag.
   - `git push origin <tag-name>`: Push a tag to the remote repository.

4. **Undoing Changes**
   - `git reset <file>`: Unstage a file.
   - `git reset --hard`: Revert changes to the last commit.
   - `git revert <commit-hash>`: Revert a specific commit.

5. **Cherry-pick**
   - `git cherry-pick <commit-hash>`: Apply a specific commit from another branch.

---

## **GitHub-Specific Commands**
1. **Forking and Pull Requests**
   - Fork a repository on GitHub via the GitHub web interface.
   - `git fetch upstream`: Sync changes from the original repository.
   - `git pull upstream main`: Merge upstream changes into your fork.
   - Use the GitHub interface to submit a pull request.

2. **Collaborating**
   - `git clone <repository-url>`: Clone a repository to collaborate on.
   - `git push`: Push your changes to GitHub for review.

3. **GitHub CLI (gh) Commands**
   - `gh auth login`: Log in to GitHub via the CLI.
   - `gh repo clone <repository>`: Clone a GitHub repository using the CLI.
   - `gh issue create`: Create a new issue in a GitHub repository.
   - `gh pr create`: Create a new pull request from the CLI.
   - `gh pr view`: View pull requests on GitHub from the CLI.

---

Would you like me to create a cheat sheet for easy reference or provide examples of specific workflows?







┌─[mrs@parrot]─[~/program/python-project]
└──╼ $git fetch upstream
fatal: 'upstream' does not appear to be a git repository
fatal: Could not read from remote repository.

Please make sure you have the correct access rights
and the repository exists.











The error indicates that the remote repository named `upstream` hasn't been configured in your local Git repository. Here’s how you can fix it:

---

### **1. Check Existing Remotes**
Run the following command to see the remotes currently configured for your repository:
```bash
git remote -v
```
This will list all the remote repositories associated with your local repository, such as `origin` (typically the primary remote).

If `upstream` is not listed, it needs to be added.

---

### **2. Add the `upstream` Remote**
You need to add the correct URL of the upstream repository. This is typically the main repository that your fork was created from.

```bash
git remote add upstream <URL-of-upstream-repository>
```
Replace `<URL-of-upstream-repository>` with the HTTPS or SSH URL of the repository you want to use as the upstream. For example:
```bash
git remote add upstream https://github.com/owner/repository.git
```

---

### **3. Verify the Remote**
After adding the `upstream` remote, verify that it was added successfully:
```bash
git remote -v
```
You should see an entry for `upstream` in addition to `origin`, like this:
```bash
origin    https://github.com/your-username/your-fork.git (fetch)
origin    https://github.com/your-username/your-fork.git (push)
upstream  https://github.com/owner/repository.git (fetch)
upstream  https://github.com/owner/repository.git (push)
```

---

### **4. Fetch from `upstream`**
Now you can fetch changes from the `upstream` repository:
```bash
git fetch upstream
```

---

### **5. Merge or Rebase (Optional)**
After fetching, you can merge or rebase the changes into your local branch:
- To merge:
  ```bash
  git merge upstream/main
  ```
  Replace `main` with the default branch name of the upstream repository (e.g., `main`, `master`, etc.).

- To rebase:
  ```bash
  git rebase upstream/main
  ```

---

If you still face issues, let me know, and I’ll guide you through troubleshooting!




