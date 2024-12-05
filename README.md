Live URL: https://idolwave.github.io/GitHub/


<h1>GitHub:</h1>
GitHub is a web-based platform that uses Git, a version control system, to host and manage software development projects. It enables collaboration, tracks changes, and provides tools for managing the development workflow.

<h2>Core Concepts:</h2>

<li>Repository (Repo): A repository is a storage space for a project, containing all files and their revision history. Repos can be public (visible to everyone) or private (restricted access).</li>

<li>Branch: A branch is an independent line of development within a repo. The default branch is typically main or master. Developers create branches to work on features or fixes without affecting the main codebase.</li>


<li>Commit: A commit is a snapshot of changes made to files in a branch. Each commit has a unique identifier (hash) and often includes a message describing the changes.</li>


<li>Pull Request (PR): A pull request is a proposal to merge changes from one branch into another. It allows for code review, testing, and and collaboration before merging the changes into the target branch.</li>

<li>Code Review: Team members can review the changes, provide feedback, and suggest improvements to ensure code quality and consistency. Testing: Changes can be tested in a controlled environment to confirm they don't introduce bugs or break existing functionality. Collaboration: Developers can discuss and refine the changes through comments or by committing additional improvements to the branch. A pull request acts as a safeguard to ensure only well-reviewed and tested code is integrated into the main branch or another target branch.</li>

<h1>Git Command Line Cheat Sheet</h1>

```
# Configure Git (Run these once per system or repo setup)
git config --global user.name "Your Name"        # Set your Git username
git config --global user.email "your.email@example.com"  # Set your Git email

# Initialize a new Git repository
git init                                          # Initialize a local Git repo

# Clone an existing GitHub repository
git clone https://github.com/username/repo.git    # Clone a remote repo to your system

# Check repository status
git status                                        # Show status of changes in the working directory

# Add files to staging area
git add file_name                                 # Stage a specific file
git add .                                         # Stage all changes in the directory

# Commit staged changes
git commit -m "Commit message"                   # Commit with a descriptive message

# Connect a local repo to a remote GitHub repo
git remote add origin https://github.com/username/repo.git

# Push changes to GitHub
git push origin branch_name                      # Push changes to a specific branch (e.g., main)

# Pull changes from GitHub
git pull origin branch_name                      # Update local branch with changes from remote

# Create a new branch
git branch branch_name                           # Create a new branch
git checkout branch_name                         # Switch to the new branch
git checkout -b branch_name                      # Create and switch to a new branch

# Merge a branch into the current branch
git merge branch_name                            # Merge a specified branch into the current one

# View commit history
git log                                          # Show commit history

# Discard changes
git checkout -- file_name                        # Revert file changes in the working directory
git reset HEAD file_name                         # Unstage a file
git reset --hard                                 # Reset to the last committed state

# Delete a branch
git branch -d branch_name                        # Delete a local branch
git push origin --delete branch_name             # Delete a remote branch


# Initialize a new Git repository
git init                                          # Initialize an empty Git repository

# Configure user details
git config --global user.name "Your Name"        # Set global username
git config --global user.email "your.email@example.com"  # Set global email

# Clone a repository
git clone https://github.com/username/repo.git    # Clone a remote repository
git clone -b branch_name https://github.com/username/repo.git  # Clone a specific branch

# Check repository status
git status                                        # Show the status of your working directory

# Stage changes
git add file_name                                 # Add a specific file to the staging area
git add .                                         # Add all files and changes to the staging area

# Commit changes
git commit -m "Commit message"                   # Commit staged changes with a message
git commit --amend -m "Updated commit message"   # Modify the most recent commit

# View commit history
git log                                          # Show commit history
git log --oneline                                # Display history in one line per commit
git log -p                                       # Show detailed changes for each commit

# Branch management
git branch                                       # List all branches
git branch branch_name                           # Create a new branch
git checkout branch_name                         # Switch to an existing branch
git checkout -b branch_name                      # Create and switch to a new branch
git branch -d branch_name                        # Delete a local branch

# Merge branches
git merge branch_name                            # Merge a branch into the current branch

# Rebase branches
git rebase branch_name                           # Reapply commits on top of another base branch

# Push changes to a remote repository
git push origin branch_name                      # Push changes to a specific remote branch
git push -u origin branch_name                   # Set upstream for the branch and push

# Pull changes from a remote repository
git pull origin branch_name                      # Pull updates from a remote branch
git pull --rebase                                # Rebase local commits on top of remote changes

# Undo changes
git reset HEAD file_name                         # Unstage a file
git reset --soft HEAD~1                          # Undo last commit, keep changes staged
git reset --hard HEAD~1                          # Undo last commit and discard changes

# Stash changes
git stash                                        # Save changes temporarily
git stash list                                   # List all stashes
git stash apply                                  # Apply the most recent stash
git stash pop                                    # Apply and remove the most recent stash

# Tagging commits
git tag tag_name                                 # Create a lightweight tag
git tag -a tag_name -m "Tag message"             # Create an annotated tag
git push origin tag_name                         # Push a specific tag to the remote
git push origin --tags                           # Push all tags to the remote

# Resolve conflicts
# Edit files manually, then:
git add conflicted_file                          # Stage the resolved file
git commit                                       # Commit the resolved merge

# Remove files
git rm file_name                                 # Remove a file and stage the deletion
git rm --cached file_name                        # Unstage a file but keep it in the working directory

# Show changes
git diff                                         # Show unstaged changes
git diff --staged                                # Show staged changes
git diff branch1..branch2                        # Show differences between two branches

# View remote repositories
git remote                                       # List configured remote repositories
git remote -v                                    # Show URLs of remotes
git remote add origin https://github.com/username/repo.git  # Add a remote repository

# Delete a remote branch
git push origin --delete branch_name             # Delete a branch on the remote

# Work with submodules
git submodule add https://github.com/username/submodule_repo.git  # Add a submodule
git submodule update --init --recursive          # Initialize and update all submodules

# Clean up
git clean -n                                     # Show files that would be removed
git clean -f                                     # Force remove untracked files


# Initialize a new Git repository
git init                                           # Start a new Git repository
git init --bare                                    # Create a bare repository (no working directory)

# Clone a repository with depth
git clone --depth 1 https://github.com/username/repo.git  # Clone only the latest history

# Configure Git settings
git config --list                                 # List all current Git configurations
git config user.name "Local User Name"           # Override global username for the repo
git config user.email "local.email@example.com"  # Override global email for the repo

# Working with files
git mv old_file_name new_file_name               # Rename a file and stage the change

# Advanced log and history options
git log --graph --oneline                        # Visualize commit history as a graph
git log --stat                                   # View changes summary per commit
git blame file_name                              # Show who changed each line of a file
git show commit_hash                             # Show changes in a specific commit

# Reset and revert
git reset --mixed                                # Reset staging area but keep working directory changes
git reset --merge                                # Reset merge conflicts
git revert commit_hash                           # Undo a specific commit by creating a new commit

# Cherry-pick specific commits
git cherry-pick commit_hash                      # Apply changes from a specific commit to the current branch

# Interactive staging
git add -i                                       # Interactive mode for staging changes
git add -p                                       # Stage changes selectively (patch mode)

# Tagging advanced options
git tag -d tag_name                              # Delete a tag locally
git push origin :refs/tags/tag_name              # Delete a tag from the remote repository

# Squash commits
git rebase -i HEAD~n                             # Interactive rebase for the last `n` commits
# Use `pick` for commits to keep or `squash` to merge commits

# Working with remotes
git remote rename old_name new_name              # Rename a remote
git remote remove remote_name                    # Remove a remote repository

# Fetch updates
git fetch                                        # Fetch changes from the remote without merging
git fetch --all                                  # Fetch all branches from all remotes

# Archive and export
git archive --format=zip HEAD > archive.zip      # Export the latest commit as a ZIP file

# Bisect for debugging
git bisect start                                 # Start a binary search for bad commits
git bisect bad                                   # Mark the current commit as bad
git bisect good commit_hash                      # Mark a known good commit
git bisect reset                                 # End the bisect session

# Working with subtrees
git subtree add --prefix=subtree_dir https://github.com/username/repo.git branch_name  # Add a subtree
git subtree pull --prefix=subtree_dir https://github.com/username/repo.git branch_name # Pull subtree updates
git subtree push --prefix=subtree_dir https://github.com/username/repo.git branch_name # Push subtree updates

# Saving and applying patches
git format-patch HEAD~n                          # Create patches for the last `n` commits
git apply patch_name.patch                       # Apply a patch to the working directory

# Credential management
git credential-cache                             # Manage Git credentials
git credential-cache exit                        # Remove stored credentials from the cache

# Reflog (undo almost anything)
git reflog                                       # Show a log of all references in your repo
git reset --hard HEAD@{n}                        # Reset to a specific point in the reflog

# Hooks (Automation)
# Hooks are custom scripts that run during specific Git events
# Add scripts to the .git/hooks directory
pre-commit                                       # Runs before a commit
post-merge                                       # Runs after a merge

# Linting/Staging with hooks
npx lint-staged                                  # Lint and stage code before committing (requires setup)

# Working with large files
git lfs install                                  # Initialize Git Large File Storage (LFS)
git lfs track "*.psd"                            # Track specific file types (e.g., Photoshop files)
git lfs untrack "*.psd"                          # Stop tracking specific file types

# Garbage collection
git gc                                           # Optimize the repository
git gc --aggressive                              # Perform a more thorough cleanup

# Display info
git shortlog                                     # Summarize commits by contributor
git diff --name-only                             # Show only file names that have changed
git diff --cached                                # Show differences between staged changes and HEAD

# Aliases
git config --global alias.st status             # Create an alias for a command (e.g., `git st` for `git status`)

# Worktrees
git worktree add ../path/to/new_branch branch_name  # Create a new worktree for a branch
git worktree list                                # List all worktrees
git worktree remove ../path/to/new_branch       # Remove a worktree
```
