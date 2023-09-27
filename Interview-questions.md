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

## IMPORTANT QUESTION:

- Difference between git fetch and git pull.

 - Let's first create repository in GitHub and a file named as commands.txt having text as git init & git push

  <img width="441" alt="image" src="https://github.com/ManishNegi963/Git-GitHub-interview-questions/assets/124788172/86b9737f-c6b3-4ec6-8bbd-a3eab0d7bd90">

 - Now clone the repository into the local.

      git clone https://github.com/ManishNegi963/git-fetch-practice.git

<img width="691" alt="image" src="https://github.com/ManishNegi963/Git-GitHub-interview-questions/assets/124788172/d5474da1-976c-49be-bc6a-8b3a1ea4681f">

 - Now edit the commands.txt in the GitHub with text git pull git fetch

   <img width="348" alt="image" src="https://github.com/ManishNegi963/Git-GitHub-interview-questions/assets/124788172/2d424568-f453-49b8-a16b-9d1496acfd82">

- In the local, use git fetch

      git fetch origin

  <img width="487" alt="image" src="https://github.com/ManishNegi963/Git-GitHub-interview-questions/assets/124788172/5780d846-fa5f-49fd-9a54-848d7c69d406">

Git fetch will retreive the changes from the remote repository to the local but won't merge those changes, we can check the log or git diff to decide if we want to apply those changes or not.

- Check the changes by using git log --all

      git log --all 

<img width="572" alt="image" src="https://github.com/ManishNegi963/Git-GitHub-interview-questions/assets/124788172/eb73758d-1cac-4f4c-8e6f-f8e9a6d59de3">

Now we can see that the head is on create commands.txt and head of origin on update commands.txt

- CHeck the changes by using git diff main origin/main

      git diff main origin/main

  <img width="574" alt="image" src="https://github.com/ManishNegi963/Git-GitHub-interview-questions/assets/124788172/e13a116a-4def-4e85-bdbc-b0e6511ccc67">

- NOw use git merge to merge those changes into local

      git merge origin/main

<img width="556" alt="image" src="https://github.com/ManishNegi963/Git-GitHub-interview-questions/assets/124788172/10207a2e-4337-4aca-b0b3-a0fce1276204">

- NOw head of local and remote are same.

      git log

  <img width="651" alt="image" src="https://github.com/ManishNegi963/Git-GitHub-interview-questions/assets/124788172/638cceac-f9bd-46a4-b529-ef603c041f49">

- Now , in case of git pull

  let's edit the commands.txt and add text git log

  - Using git pull
 
        git pull origin main

    It will auto merge the changes from the remote repository to the local.

<img width="533" alt="image" src="https://github.com/ManishNegi963/Git-GitHub-interview-questions/assets/124788172/86984190-b097-4ff6-b5c9-2216bd75b6f6">


