[![Review Assignment Due Date](https://classroom.github.com/assets/deadline-readme-button-22041afd0340ce965d47ae6ef1cefeee28c7c493a6346c4f15d667ab976d596c.svg)](https://classroom.github.com/a/GvXCZgfk)
[![Open in Visual Studio Code](https://classroom.github.com/assets/open-in-vscode-2e0aaae1b6195c2367325f4f02e2d04e9abb55f0b24a779b69b11b9e10269abc.svg)](https://classroom.github.com/online_ide?assignment_repo_id=15317578&assignment_repo_type=AssignmentRepo)
# SE-Assignment-4
Assignment: GitHub and Visual Studio
Instructions:
Answer the following questions based on your understanding of GitHub and Visual Studio. Provide detailed explanations and examples where appropriate.

Questions:
Introduction to GitHub:
What is GitHub, and what are its primary functions and features? Explain how it supports collaborative software development.

- Github-cloud-based platform where you can store, share, and work together with others to write code.
- Primary functions and features-Allow developers to work together remotely on the software and also track changes made.
        - Features-repositories, Banching and merging, pill requests, Integrations, collaboration tools
-It supports collaborative software development by allowing developers to collaborate on a project at the same time.


Repositories on GitHub:
What is a GitHub repository? Describe how to create a new repository and the essential elements that should be included in it.

- Github repositories- a place in github where you can code, store your files and revise your file history. (https://docs.github.com/en/repositories/creating-and-managing-repositories/about-repositories)

- Elements of the repositories- README.md, License, pull request,commits, Actions

Version Control with Git:
Explain the concept of version control in the context of Git. How does GitHub enhance version control for developers?

- It enhances VS by allowing developers to keep track of changes made by indidual deevelopers. This increases productivity and allow for smooth collaboration between the developers.(https://resources.github.com/software-development/what-is-version-control/) 


Branching and Merging in GitHub:
What are branches in GitHub, and why are they important? Describe the process of creating a branch, making changes, and merging it back into the main branch.

- Branches- A parallel version of your code that is contained within the repository, but does not affect the primary or main branch. Allows developers to create a space where they can test their codes without affecting the main branch.

ProcesS
- Navigate to Your Repository on GitHub
- Click on the "Branch: main" dropdown.
- Type a new branch name in the "Find or create a branch" field.
- Press "Enter" to create the new branch.

- To make chnages, Navigate to the newly created branch in your repository.
- Click on the file you want to edit.
- Make your changes directly in the GitHub editor.
- Add a commit message describing your changes.
- Click "Commit changes."

- Navigate to your repository on GitHub.
- Click the "Pull requests" tab.
- Click the "New pull request" button.
- Select your new branch from the "compare" dropdown and ensure the base branch is set to main (or the branch you want to merge into).
- Add a title and description for your pull request.
- Click "Create pull request."

- To merge, Click the "Merge pull request" button.
- Confirm the merge by clicking "Confirm merge."


Pull Requests and Code Reviews:
What is a pull request in GitHub, and how does it facilitate code reviews and collaboration? Outline the steps to create and review a pull request.

- This a way that Github informs developers collaborating in the same project that chnages has been made to the repositories. This allows them to discuss the changes before they can merge the changes into the main branch.

- On GitHub.com, navigate to the main page of the repository.
- In the "Branch" menu, choose the branch that contains your commits.
- Click "Compare & pull request" to create a pull request
- Under your repository name, click  Pull requests
- To request a review, click  Reviewers
- Type the username of the person or the name of the team you're asking to review your changes
- Once your pull request is reviewed, navigate to Reviewers in the right sidebar and click  next to the reviewer's name whose review you'd like.


GitHub Actions:
Explain what GitHub Actions are and how they can be used to automate workflows. Provide an example of a simple CI/CD pipeline using GitHub Actions.

- A platform in Github that allows you to build, test, and deploy your pipeline.
- It allows you to create workflows that you can automate development processses.(https://www.freecodecamp.org/news/automate-open-source-projects-with-github-actions/#:~:text=It%20lets%20you%20create%20custom,for%20everyone%20contributing%20to%20it).

- Simple CI/CD pipeline

name: Node.js CI/CD Pipeline

on:
  push:
    branches:
      - main  # Trigger the workflow on push events to the main branch

jobs:
  build:
    runs-on: ubuntu-latest

    steps:
      - name: Checkout code
        uses: actions/checkout@v2  # This action checks out your repository's code

      - name: Set up Node.js
        uses: actions/setup-node@v2  # Sets up Node.js environment

      - name: Install dependencies
        run: npm install  # Install Node.js dependencies

      - name: Run tests
        run: npm test  # Run tests using npm test script

  deploy:
    runs-on: ubuntu-latest

    needs: build  # Ensure 'build' job completes successfully before deployment

    steps:
      - name: Checkout code
        uses: actions/checkout@v2

      - name: Set up Node.js
        uses: actions/setup-node@v2

      - name: Install dependencies
        run: npm install

      - name: Deploy to production
        run: |
          npm run build  # Example build step
          npm run deploy  # Example deployment script or command


Introduction to Visual Studio:
What is Visual Studio, and what are its key features? How does it differ from Visual Studio Code?

- Visual studio- It's a comprehensive integrated development environment (IDE) that you can use to write, edit, debug, and build code. (https://learn.microsoft.com/en-us/visualstudio/get-started/visual-studio-ide?view=vs-2022). It differs from Visual Studio code in that is it full-fledged IDE while VS code is Lightweight Source Code Editor


- Features- Code editor, Run and debud, Extensions, Github pull request, customizable setting


Integrating GitHub with Visual Studio:
Describe the steps to integrate a GitHub repository with Visual Studio. How does this integration enhance the development workflow?

- Fork your repository in your Github account
- Open Gitbash and follow the below commands
        - clone URL(from gihub assigment)
        - cd repositoryname
        - code .
- It will take you to VS code
- Once in VS Code, click on terminal>new terminal
- Ensure that your teminal is on Gitbash
- Write the below commands  to integrate VS code with Github
        - git add .
        - git commit -m "commit message"
        - git push

Debugging in Visual Studio:
Explain the debugging tools available in Visual Studio. How can developers use these tools to identify and fix issues in their code?

- Debugging tools in VS- use to identify and fix issues in the code. e.g Python debugger
- How to to do that:
        - Set breakpoints at the point in your code where you suspect the issue might be.
        - Click on "Run and Debug"
        - Choose debug configuration and run

Collaborative Development using GitHub and Visual Studio:
Discuss how GitHub and Visual Studio can be used together to support collaborative development. Provide a real-world example of a project that benefits from this integration.

- Github has pull request option that notify developers working in the same project of the changes made on the collaborative project.
- Example of real-life project is the E-commerce project. This is collaborative project that involve Front-end and back-end developers and the DevOps team. The whole team provide support to making the project successfull.

Submission Guidelines:
Your answers should be well-structured, concise, and to the point.
Provide real-world examples or case studies wherever possible.
Cite any references or sources you use in your answers.
Submit your completed assignment by [due date].
