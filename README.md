# Forking a GitHub Repository and Making Local Changes with VS Code Terminal

This guide outlines the process of forking a GitHub repository, cloning it to your local system, making changes using the integrated terminal in Visual Studio Code (VS Code), and then pushing those changes to your forked repository.

## Step 1: Fork the Repository on GitHub

1.  **Navigate to the Repository:** Open your web browser and go to the GitHub repository you want to contribute to.

2.  **Click the "Fork" Button:** In the top-right corner of the repository page, you'll see a button labeled "Fork." Click this button.

3.  **Choose Your Account:** GitHub will ask you where you want to fork the repository. Select your personal GitHub account.

4.  **Wait for Forking:** GitHub will create a copy of the original repository under your account. You'll be redirected to your forked repository, which will have a URL like `https://github.com/YourUsername/OriginalRepositoryName`.

## Step 2: Clone Your Forked Repository to Your Local System

1.  **Open VS Code:** Launch Visual Studio Code.

2.  **Open the Integrated Terminal:** Go to "Terminal" in the top menu and select "New Terminal." This will open a terminal panel within VS Code.

3.  **Navigate to Your Desired Directory:** Use the `cd` command in the VS Code terminal to navigate to the directory where you want to store the cloned repository. For example:
    ```bash
    cd Documents/GitHub
    ```

4.  **Get the Clone URL:** On your forked repository page on GitHub (the one under your username), click the green "Code" button. A dropdown menu will appear. Make sure "HTTPS" is selected and copy the URL provided.

5.  **Clone the Repository:** In the VS Code terminal, use the `git clone` command followed by the URL you copied:
    ```bash
    git clone [https://github.com/YourUsername/OriginalRepositoryName.git](https://github.com/YourUsername/OriginalRepositoryName.git)
    ```
    This will download a copy of your forked repository to your local machine in a new directory named `OriginalRepositoryName`.

6.  **Navigate into the Cloned Repository:** Use the `cd` command in the VS Code terminal to enter the newly created directory:
    ```bash
    cd OriginalRepositoryName
    ```

## Step 3: Make Changes Using Visual Studio Code (VS Code)

1.  **Open the Repository in VS Code (if not already open):** If you haven't already, go to "File" > "Open Folder..." in VS Code and then navigate to the cloned repository directory and select it.

2.  **Make Your Changes:** Use VS Code's editor to modify the files in the repository as needed. You can create new files, edit existing ones, etc.

3.  **Save Your Changes:** After making your modifications, save the files in VS Code (File > Save or Ctrl+S / Cmd+S).

## Step 4: Commit Your Changes Using VS Code Terminal

1.  **Open the Integrated Terminal (if closed):** Go to "Terminal" in the top menu and select "New Terminal."

2.  **Check the Status of Your Changes:** Use the `git status` command in the VS Code terminal to see which files have been modified or are untracked:
    ```bash
    git status
    ```
    Modified files will be listed under "Changes not staged for commit," and new, untracked files will be listed under "Untracked files."

3.  **Stage Your Changes:** Use the `git add` command to stage the files you want to include in your commit.
    * To stage all modified and untracked files:
        ```bash
        git add .
        ```
4.  **Commit Your Changes:** Use the `git commit` command to record your staged changes with a descriptive message:
    ```bash
    git commit -m "Your concise and informative commit message"
    ```
    Replace `"Your concise and informative commit message"` with a clear description of the changes you made.

## Step 5: Push Your Local Commits to Your Forked Repository on GitHub

1.  **Push Your Commits:** Use the `git push` command in the VS Code terminal to upload your local commits to your forked repository on GitHub. You'll typically need to specify the remote name (`origin`) and the branch name:
    ```bash
    git push 
    ```
2.  **Verify on GitHub:** Go to your forked repository on GitHub in your web browser. You should see your new branch and the commits you just pushed.

## Step 6: Create a Pull Request (Optional, for Contributing to the Original Repository)

If your goal is to contribute your changes back to the original repository, you'll need to create a Pull Request (PR):

1.  **Navigate to Your Forked Repository on GitHub:** Open your forked repository in your web browser.

2.  **Click the "Compare & pull request" Button:** You should see a button prompting you to create a pull request. If not, you can go to the "Pull requests" tab and click the "New pull request" button.

3.  **Select the Base and Compare Branches:**
    * **Base repository:** This should be the original repository you forked from.
    * **Base:** This is the branch in the original repository you want to merge your changes into (usually `main` or `dev`).
    * **Head repository:** This should be your forked repository.
    * **Compare:** This is the branch in your forked repository that contains your changes (e.g., `your-new-branch-name`).

4.  **Write a Descriptive Title and Body:** Provide a clear and concise title for your pull request and a detailed description of the changes you've made and why they are beneficial.

5.  **Click "Create pull request":** This will submit your changes to the maintainers of the original repository for review. They may provide feedback or merge your changes.
