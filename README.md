# Git-Gitlab
Here is a comprehensive list of Git and GitLab CLI commands, covering basic usage, advanced operations, and configuration.

### **Git CLI Commands**

#### **1. Basic Commands**

- **Check Git version:**
  ```bash
  git --version
  ```

- **Configure Git username and email:**
  ```bash
  git config --global user.name "Your Name"
  git config --global user.email "your.email@example.com"
  ```

- **Initialize a new Git repository:**
  ```bash
  git init
  ```

- **Clone a repository:**
  ```bash
  git clone REPOSITORY_URL
  ```

- **Check the status of the working directory:**
  ```bash
  git status
  ```

- **Add changes to the staging area:**
  ```bash
  git add FILE_NAME
  git add .
  ```

- **Commit changes to the repository:**
  ```bash
  git commit -m "Commit message"
  ```

- **View commit history:**
  ```bash
  git log
  ```

- **Show the difference between working directory and index:**
  ```bash
  git diff
  ```

- **Show the difference between index and last commit:**
  ```bash
  git diff --cached
  ```

#### **2. Branch Management**

- **List all branches:**
  ```bash
  git branch
  ```

- **Create a new branch:**
  ```bash
  git branch BRANCH_NAME
  ```

- **Switch to a branch:**
  ```bash
  git checkout BRANCH_NAME
  ```

- **Create and switch to a new branch:**
  ```bash
  git checkout -b BRANCH_NAME
  ```

- **Merge a branch into the current branch:**
  ```bash
  git merge BRANCH_NAME
  ```

- **Delete a branch:**
  ```bash
  git branch -d BRANCH_NAME
  ```

- **List all remote branches:**
  ```bash
  git branch -r
  ```

#### **3. Remote Repository Management**

- **Add a remote repository:**
  ```bash
  git remote add REMOTE_NAME REPOSITORY_URL
  ```

- **List remote repositories:**
  ```bash
  git remote -v
  ```

- **Fetch changes from a remote repository:**
  ```bash
  git fetch REMOTE_NAME
  ```

- **Pull changes from a remote repository:**
  ```bash
  git pull REMOTE_NAME BRANCH_NAME
  ```

- **Push changes to a remote repository:**
  ```bash
  git push REMOTE_NAME BRANCH_NAME
  ```

- **Remove a remote repository:**
  ```bash
  git remote remove REMOTE_NAME
  ```

- **Rename a remote repository:**
  ```bash
  git remote rename OLD_NAME NEW_NAME
  ```

#### **4. Tag Management**

- **List all tags:**
  ```bash
  git tag
  ```

- **Create a new tag:**
  ```bash
  git tag TAG_NAME
  ```

- **Push a tag to a remote repository:**
  ```bash
  git push REMOTE_NAME TAG_NAME
  ```

- **Delete a tag:**
  ```bash
  git tag -d TAG_NAME
  ```

#### **5. Stashing and Cleaning**

- **Stash changes:**
  ```bash
  git stash
  ```

- **List stashed changes:**
  ```bash
  git stash list
  ```

- **Apply the most recent stash:**
  ```bash
  git stash apply
  ```

- **Drop a stash:**
  ```bash
  git stash drop STASH@{0}
  ```

- **Clean untracked files and directories:**
  ```bash
  git clean -f
  git clean -fd
  ```

#### **6. Configuration and Help**

- **Show Git configuration:**
  ```bash
  git config --list
  ```

- **Edit Git configuration:**
  ```bash
  git config --global -e
  ```

- **Get help for a Git command:**
  ```bash
  git help COMMAND_NAME
  ```

### **GitLab CLI Commands**

GitLab primarily interacts through its API or Git commands. However, GitLab also provides a CLI tool (`glab`) for easier interaction.

#### **1. Basic GitLab Commands (Using `glab`)**

- **Install `glab`:**
  ```bash
  # For macOS using Homebrew
  brew install glab

  # For Linux using a binary release
  curl -s https://api.github.com/repos/profclems/glab/releases/latest \
  | grep "browser_download_url.*linux_amd64.tar.gz" \
  | cut -d : -f 2,3 \
  | tr -d \" \
  | xargs curl -LO \
  && tar xf glab_*_linux_amd64.tar.gz \
  && sudo mv glab /usr/local/bin
  ```

- **Authenticate with GitLab:**
  ```bash
  glab auth login
  ```

- **List GitLab projects:**
  ```bash
  glab repo list
  ```

- **Create a new issue:**
  ```bash
  glab issue create -t "Issue Title" -d "Issue description"
  ```

- **List issues:**
  ```bash
  glab issue list
  ```

- **Show an issue:**
  ```bash
  glab issue view ISSUE_ID
  ```

- **Create a merge request:**
  ```bash
  glab mr create -t "Merge Request Title" -d "Merge request description"
  ```

- **List merge requests:**
  ```bash
  glab mr list
  ```

- **Show a merge request:**
  ```bash
  glab mr view MR_ID
  ```

- **Merge a merge request:**
  ```bash
  glab mr merge MR_ID
  ```

- **Delete a project:**
  ```bash
  glab repo delete PROJECT_NAME
  ```

#### **2. GitLab CI/CD Commands**

- **Trigger a pipeline:**
  ```bash
  glab pipeline trigger --ref BRANCH_NAME
  ```

- **List pipelines:**
  ```bash
  glab pipeline list
  ```

- **Show pipeline details:**
  ```bash
  glab pipeline view PIPELINE_ID
  ```

### **Summary**

This list covers essential Git and GitLab CLI commands for managing repositories, branches, remotes, and configurations. It also includes advanced commands for stashing, cleaning, and using GitLab’s CLI tool `glab` for interacting with GitLab projects and issues. This comprehensive set of commands will help streamline version control and project management workflows.
