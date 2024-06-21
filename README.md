# Cloning a GitHub Template Repository into Your Current Repository

To clone a GitHub template repository into your current repository, follow these steps:

## Create a New Repository on GitHub

1. Go to your GitHub account.
2. Click on the "+" sign in the top right corner and select "New repository".
3. Name your repository and set the necessary settings, then click "Create repository".

## Initialize Your New Repository Locally

1. Open a terminal or command prompt.
2. Navigate to the directory where you want to initialize the repository.
3. Run the following commands to initialize a new Git repository and link it to your GitHub repository:

    ```sh
    git init
    git remote add origin https://github.com/your-username/your-repo-name.git
    ```

## Clone the Template Repository

To clone the template repository's content into your current repository, you can use a combination of the `git fetch` and `git merge` commands. Assuming you have the URL of the template repository, follow these steps:

1. Add the template repository as a remote:

    ```sh
    git remote add template https://github.com/rayaanr/shadcn-nextjs-template.git
    ```

2. Fetch the template repository's content:

    ```sh
    git fetch template
    ```

3. Merge the template repository's content into your current repository:

    ```sh
    git merge template/main --allow-unrelated-histories
    ```

   Replace `https://github.com/user/template-repo.git` with the URL of the template repository, and `main` with the default branch name of the template repository if it is different (e.g., `master`).

## Resolve Any Merge Conflicts

If there are any merge conflicts, resolve them manually by editing the conflicting files, then stage and commit the resolved files:

    ```sh
    git add .
    git commit -m "Resolve merge conflicts"
    ```

## Push Changes to Your GitHub Repository

Finally, push the merged content to your GitHub repository:

    ```sh
    git push origin main
    ```

   Replace `main` with the default branch name of your repository if it is different.

This process clones the content of the template repository into your current repository, allowing you to use the template's structure and files as a starting point.
