## CI with a Full-Stack App using GitHub Actions

In this exercise, you will demonstrate how to set up a Continuous Integration pipeline using GitHub Actions for a simple full-stack application. 

### Business Scenario

Suppose you are working for a small start-up, Uda-Crafts, that sells handmade crafts. The development team has been tasked to develop a full-stack application for listing products on the website. The backend service is built with Node.js, and the frontend with basic HTML and JavaScript.

### Your Job

To ensure quality and avoid deployment of broken code, you have been asked to implement a CI pipeline using GitHub Actions that will automatically build, test, and lint (code quality check) the application whenever changes are pushed to the main branch.

Follow the steps below to complete the exercise:

## Part 1: The Application Files

The initial application-related files and folders are available in the Lesson Workspace in the `lesson-3-exercise/CI-FullstackApp`directory.

* **Create a new repository using your GitHub account - **
You can name this repository "CI-FullstackApp".
* **Create a new repository on the command line - **
From the Lesson Workspace terminal, navigate to the `CI-FullstackApp` root directory : 

```undefined
cd */CI-FullstackApp
```

From the `CI-FullstackApp`directory, execute the following set of bash commands:

```
git init
git add .
git commit -m "First Commit"
git branch -M main
git remote add origin https://github.com/<YOUR_GITHUB_USERNAME>/CI-FullstackApp.git
git push -u origin main
```

**Important:** To paste code in the Lesson Workspace, use Shift + Command + V for a Mac or Shift + Control + V for a Windows.

## Part 2: Execute a GitHub Actions Workflow

* **Create a GitHub Actions workflow file:**
* Provide a descriptive name for the workflow.
* The workflow should run on any push to the main branch **and** every Sunday at midnight (0.00). Hint: use the `cron` keyword. Hint: <a href="https://pubs.opengroup.org/onlinepubs/9699919799/utilities/crontab.html#tag_20_25_07" target="_blank">check out this documentation.</a>
* The build job should use a matrix strategy to run on Node.js versions 16.x and 18.x.
* The workflow steps should include installing dependencies, running tests, and linting. 
* Print the following message at the completion of the run: "Hello [username of the user who initiated the run]. You pushed to [repository_name] at [date]." Hint: <a href="https://docs.github.com/en/actions/learn-github-actions/contexts#job-context" target="_blank">Check out the official documentation for GitHub Actions variable/context documentation</a>.


