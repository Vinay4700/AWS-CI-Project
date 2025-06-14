AWS Continuous Integration Project

This project demonstrates a **Continuous Integration (CI)** setup using **AWS CodePipeline**, **CodeBuild**, and **GitHub** for a Python application. It automates building, testing, and deploying code changes from GitHub using AWS Developer Tools.

1. Set Up GitHub Repository

To begin, create a GitHub repository for your Python application:

1. Go to [GitHub](https://github.com) and sign in.
2. Click the "+" icon (top-right) → **New repository**.
3. Enter a repository name and description.
4. Choose visibility (public/private).
5. Initialize with a README (optional).
6. Click **Create repository**.

2. Create an AWS CodePipeline

Follow these steps to set up AWS CodePipeline:

1. Open AWS Console → **CodePipeline**.
2. Click **Create pipeline**.
3. Name your pipeline and proceed.
4. Choose **GitHub** as the source provider.
5. Connect GitHub and select your repository and branch.
6. For the build stage, select **AWS CodeBuild**.
7. Click **Create project** to define a new build project.
8. Configure build settings: runtime, build commands, artifacts.
9. Return to CodePipeline, finish the setup, and click **Create pipeline**.

3. Configure AWS CodeBuild

Set up CodeBuild to build and test your application:

1. Open AWS Console → **CodeBuild**.
2. Click **Create build project**.
3. Name the project.
4. Choose **AWS CodePipeline** as the source.
5. Set environment options: OS, runtime, compute.
6. Add build commands (e.g., install dependencies, run tests).
7. Configure build artifacts.
8. Click **Create build project**.

4. Trigger the CI Process

To test your CI pipeline:

1. Make a code change in your GitHub repo (e.g., bug fix, new feature).
2. Commit and push to the target branch.
3. Open **AWS CodePipeline** and view your pipeline.
4. It should automatically detect the changes and run the build process.

Once configured, CodePipeline automates everything—from pulling the latest code to building and deploying it, providing a streamlined CI experience.

Technologies Used

- AWS CodePipeline
- AWS CodeBuild
- GitHub
- Python
- (Optional) AWS Elastic Beanstalk or other deployment services
