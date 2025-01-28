# GIT-commit-and-restore-Version-implementation




Here’s a step-by-step breakdown of how to create a local Git repository, modify an index.html file, perform commits, and restore versions of the file:

#### Step 1: Create a Local Git Repository
1. Open Terminal (or Command Prompt) on your system.
2. Navigate to your desired directory or create a new one:
```yml
    mkdir my-git-repo
    cd my-git-repo
```
3. Initialize the Git repository:
```yml
    git init
```
### Step 2: Create index.html and Perform the First Commit
1. Create the index.html file:
  ```yml
    <!DOCTYPE html>
    <html lang="en">
    <head>
        <meta charset="UTF-8">
        <meta name="viewport" content="width=device-width, initial-scale=1.0">
        <title>My Webpage</title>
    </head>
    <body>
        <h1>Welcome to my webpage!</h1>
        <p>This is the first line.</p>
    </body>
    </html>
```

2. Stage and commit the file:

 ```yml
    git add index.html
    git commit -m "Initial commit with 2 lines in index.html"
```

### Step 3: Modify index.html and Perform Another Commit
1. Modify the index.html file by adding two more lines:
```yml
    <p>This is the second line.</p>
    <p>This is the third line.</p>
```

2. Stage and commit the changes:
   
```yml
    git add index.html
    git commit -m "Added 2 more lines to index.html"
```

### Step 4: Modify index.html Again and Commit
1. Modify the file again by adding two more lines:
```yml
    <p>This is the fourth line.</p>
    <p>This is the fifth line.</p>
```

2. Stage and commit the changes:

 ```yml
    git add index.html
    git commit -m "Added 2 more lines to index.html (lines 4 and 5)"
```

### Step 5: Restore Earlier Version with 4 Lines
1. View the commit history to find the commit with 4 lines:
```yml
    git log --oneline
```

  *You should see output like this:*

    fba9fcd Added 2 more lines to index.html (lines 4 and 5)
    3c9e2d2 Added 2 more lines to index.html
    7d983a0 Initial commit with 2 lines in index.html

2. Checkout the commit with 4 lines (the second commit) and restore the file:
```yml
    git checkout 3c9e2d2 -- index.html
```

3. Stage and commit the restored file:
```yml
    git add index.html
    git commit -m "Restored index.html to the version with 4 lines"
```

### Step 6: Modify the File Again and Commit
1. Modify the index.html file by adding three more lines:
```yml
    <p>This is the sixth line.</p>
    <p>This is the seventh line.</p>
    <p>This is the eighth line.</p>
```

2. Stage and commit the changes:
```yml
    git add index.html
    git commit -m "Added 3 more lines to index.html (lines 6, 7, and 8)"
```

#### Step 7: Restore 4-Line Version Again
1. Restore the 4-line version again by checking out the relevant commit:
```yml
    git checkout 3c9e2d2 -- index.html
```
2. Stage and commit this restored version:
```yml
    git add index.html
    git commit -m "Restored index.html to the version with 4 lines again"
```

Final Verification
1. View the final commit history:
```yml
    git log --oneline
```
  *The output will look something like this:*

    <latest commit hash> Restored index.html to the version with 4 lines again
    <commit hash> Added 3 more lines to index.html (lines 6, 7, and 8)
    <commit hash> Restored index.html to the version with 4 lines
    <commit hash> Added 2 more lines to index.html (lines 4 and 5)
    <commit hash> Added 2 more lines to index.html
    <commit hash> Initial commit with 2 lines in index.html

## Summary of Commands Used
- Initialize Git repository: git init
- Stage file: git add index.html
- Commit changes: git commit -m "commit message"
- View commit history: git log --oneline
- Restore a file version: git checkout <commit-hash> -- index.html

*With these steps, we've created a local Git repository, committed changes, modified files, and restored versions as needed.*















<br>
<br>
<br>
<br>



**👨‍💻 𝓒𝓻𝓪𝓯𝓽𝓮𝓭 𝓫𝔂**: [Suraj Kumar Choudhary](https://github.com/Surajkumar4-source) | 📩 **𝓕𝓮𝓮𝓵 𝓯𝓻𝓮𝓮 𝓽𝓸 𝓓𝓜 𝓯𝓸𝓻 𝓪𝓷𝔂 𝓱𝓮𝓵𝓹**: [csuraj982@gmail.com](mailto:csuraj982@gmail.com)





<br>
