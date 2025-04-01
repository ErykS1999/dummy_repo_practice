# How to Fork, Clone, and Create a Pull Request

This guide explains how to **fork a repository, clone it, make changes, and submit a pull request (PR)**.

## Step 1: Fork the Repository
Since you may not have direct write access to the original repository, you need to **fork** it first.  

1. **Go to the original repository** on GitHub.  
2. Click the **Fork** button (top right corner).  
3. This creates a **copy** of the repository under your GitHub account.

## Step 2: Clone Your Forked Repository
After forking, you need to **clone your forked version** to your local computer.  

1. Copy the **URL of your forked repository** (not the original one).  
2. Open your terminal or command prompt and run:  
   ```bash
   git clone <your-forked-repo-url>
   ```
   Example:
   ```bash
   git clone https://github.com/your-username/repo-name.git
   ```
3. Move into the project folder:
   ```bash
   cd repo-name
   ```

## Step 3: Create a New Branch
Before making changes, create a new branch to work in.

```bash
git checkout -b new-branch
```
Replace `new-branch` with a meaningful name (e.g., `add-new-files`).

## Step 4: Add Three New Files
Now, create three new files inside the project folder.

```bash
touch file1.txt file2.txt file3.txt
```
To add content to the files, you can use:

```bash
echo "This is file 1" > file1.txt
echo "This is file 2" > file2.txt
echo "This is file 3" > file3.txt
```

## Step 5: Create a README File
```bash
touch README.md
echo "# Project Title" >> README.md
echo "This project was modified by adding three new files." >> README.md
```

## Step 6: Stage and Commit the Changes
Now, save your changes and commit them:

```bash
git add .
git commit -m "Added three new files and README"
```

## Step 7: Push Your New Branch to Your Forked Repository
Since you don’t have permission to push to the original repo, you need to push to your forked repo:

```bash
git push origin new-branch
```

## Step 8: Create a Pull Request (PR)
Now, you need to merge your changes into the original repository.

1. Go to your forked repository on GitHub.
2. Click the **"Compare & pull request"** button (it appears after pushing a new branch).
3. Make sure it says:
   - **Base repository**: Original repo (where you got the project from).
   - **Head repository**: Your fork.
   - **Compare branch**: `new-branch` (the one you just pushed).
4. Add a title and description for your PR.
5. Click **"Create pull request."**

## Step 9: Wait for Review
Now, the owner of the original repo will review your PR and decide whether to merge it. You may need to make changes based on their feedback.
