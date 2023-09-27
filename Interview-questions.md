# Git and GitHub Interview Questions & Answers

- DIfference between Centralised and Distributed version control system.

<img width="634" alt="image" src="https://github.com/ManishNegi963/Git-GitHub-interview-questions/assets/124788172/b2bb7eea-3fc8-42f9-874e-46c8daf26df0">


  CVCS: In CVCS, their is a central repo which stores entire histroy and version of all prjects and devlopers checkout copies of the code and commit changes back to the central respository.

  We can work offline, but in order to commit the changes we will need network to access the centralised repository.

<img width="678" alt="image" src="https://github.com/ManishNegi963/Git-GitHub-interview-questions/assets/124788172/a9731a56-3fee-41f2-8740-5892e9309e83">


  DCVS: IN DCVS, every developer can take a copy of the entire project and version history and commit changes on the local copy of that and then push it to the main repository.

  We can work offline and commit the changes into the local repository as evryone has a entire copy of the repositiry in local.

- What is a fork?

   It is a entire copy of the source code/repository in GitHUb, where you can copy the entire public repository of anyone into your Github account. 

- What is the difference between Git & GitHub?

  Git: Git is version control system where it allows to track changes in the code over time.


- How to track any directory and initialize empty git repository?

      git init

  <img width="605" alt="image" src="https://github.com/ManishNegi963/Git-GitHub-interview-questions/assets/124788172/bfa323b1-2dbe-400c-8016-61342ea7d48e">
When we use git init in any directory that directory becomes root directory and evry file in that directory in now tracked.

- How to unstage the file?

      git rm --cached

  <img width="669" alt="image" src="https://github.com/ManishNegi963/Git-GitHub-interview-questions/assets/124788172/23bf37d5-6e59-4654-998c-47d5f63b0de2">

- How to restore a file(commited) that is deleted?

      git restore commands.txt 

<img width="536" alt="image" src="https://github.com/ManishNegi963/Git-GitHub-interview-questions/assets/124788172/2e3b7682-5a54-4cfa-a510-b437e87efb43">

-  How to config git?

        git config --global user.name ""

        git config --global user.email ""

  Enter the user name and email address of the GitHub.

- How to unstage a file?

      git restore --staged README.md

<img width="569" alt="image" src="https://github.com/ManishNegi963/Git-GitHub-interview-questions/assets/124788172/df1de0ba-5b8d-441e-b4bc-5ad04bb8d1e2">

- Difference between main and master branch.

  Main is default branch in the GitHub and master is default branch in the local.

- 

