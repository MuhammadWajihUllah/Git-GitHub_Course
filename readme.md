# Git and GitHub Course
# First Lecture by Ammar Tufail
https://www.youtube.com/watch?v=iJAGwErBFrU
https://www.youtube.com/watch?v=qeXnsqbzBCU

## Understanding the `.git` Folder

### 1. How the `.git` Folder is Created
When you run the `git init` command in your terminal, Git creates a special directory named `.git` inside your project folder. This folder acts as the "brain" of your repository, storing all version control data, commit histories, remote repository links, and configurations.

### 2. Why is it Hidden?
In Linux (including Linux Mint), any file or folder that starts with a dot (`.`) is automatically hidden by the operating system. 
* **Protection:** It keeps your history safe from accidental modification or deletion.
* **Cleanliness:** It prevents workspace clutter so you only focus on your source code.

### 3. How to Access the `.git` Folder in Linux Mint
* **Via Terminal:** Run `ls -a` (the `-a` flag tells Linux to list all files, including hidden ones).
* **Via File Manager (Nemo):** Open your folder and press `Ctrl` + `H` to toggle the visibility of hidden files.

### 4. Moving or Changing Repositories
If you accidentially initialize a repository in the wrong folder (or want to stop tracking a folder completely), you must delete this hidden folder first. 
To completely reset or change your repository via the terminal, use:
```bash
rm -rf .git
```
*Warning: This will permanently delete your local git configurations and commit history for that specific folder.*


### 5. Managing Repositories directly from VS Code

Instead of using the terminal, you can manage, initialize, and reset repositories directly through the Visual Studio Code interface.

#### Initializing a Repository in VS Code
1. Open the folder you want to track by going to **File** > **Open Folder...**
2. Click on the **Source Control** icon on the left sidebar (or press `Ctrl` + `Shift` + `G`).
3. Click the blue **Initialize Repository** button. Git will automatically create the hidden `.git` folder inside your opened workspace.

#### Changing or Disconnecting a Repository in VS Code
If VS Code is tracking too many files (e.g., your whole Home directory) and you want to switch folders:
1. Open your workspace folder in the **Explorer** view (`Ctrl` + `Shift` + `E`).
2. Press `Ctrl` + `H` inside your file browser to show hidden files, or ensure your VS Code settings allow hidden files to be seen.
3. Right-click the `.git` folder in the explorer panel and select **Delete** (or move it to the trash).
4. The Source Control panel will instantly refresh and stop tracking those files.
5. Go to **File** > **Open Folder...**, choose your new directory (like your Documents folder), and click **Initialize Repository** again to start fresh.
