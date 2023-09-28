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

  NOTE:
   - Git pull is also used when you want to pull changes from a single branch.
   - Git fetch is used when you want to fetch all the changes from all the branch.
   - Git clone is used to copy whole repository.

- HOw to view origin url/remote repository ?

      git remote -v

  <img width="498" alt="image" src="https://github.com/ManishNegi963/Git-GitHub-interview-questions/assets/124788172/1a24adf9-2c61-4150-8eb4-b0ccd2455b3a">


- Now go to setting in github > developer setting > personal access token > generate new token > check the rights you want to give and then copy the token.

  <img width="757" alt="image" src="https://github.com/ManishNegi963/Git-GitHub-interview-questions/assets/124788172/f992915f-9589-49fc-b6d5-b06ccbe29ba5">



-   Now if we try to push using username and password is not safe practice.

   <img width="494" alt="image" src="https://github.com/ManishNegi963/Git-GitHub-interview-questions/assets/124788172/743a12b1-ef37-4893-8d8e-51e5b7c66ad3">

  - Adding the token into url

         git remote set-url --add origin https://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@github.com/ManishNegi963/git-fetch-practice.git

    <img width="848" alt="image" src="https://github.com/ManishNegi963/Git-GitHub-interview-questions/assets/124788172/07b9429a-1dba-4c7f-bf82-42916ae34815">


- NOw we have 2 url for push, delete the old url

      git remote set-url --delete origin https://github.com/ManishNegi963/git-fetch-practice.git

<img width="851" alt="image" src="https://github.com/ManishNegi963/Git-GitHub-interview-questions/assets/124788172/8e25093e-eb45-418e-903f-ac6831ad4bde">


- Push the changes to the GIthub repo.

      git push origin main

<img width="815" alt="image" src="https://github.com/ManishNegi963/Git-GitHub-interview-questions/assets/124788172/5b368b4f-cd67-4e8a-a325-0044ac2d88ae">


-  Sample.txt have been pushed to GitHub repo.

  <img width="697" alt="image" src="https://github.com/ManishNegi963/Git-GitHub-interview-questions/assets/124788172/e10a23ac-3fdd-4147-9d90-ccb7c5221e5e">


- Use Case of git revert

  Suppose you created a bug in the application and you want to revert that code (don't delete the file as it will delete the functionality also",
  use git revert to revert the commit.

- Create a good feature 

<img width="544" alt="image" src="https://github.com/ManishNegi963/Git-GitHub-interview-questions/assets/124788172/437b8990-9c24-4163-8ec3-3ddab5d59c5e">

- NOw added bug

  <img width="585" alt="image" src="https://github.com/ManishNegi963/Git-GitHub-interview-questions/assets/124788172/f185fbae-652d-4a7d-a9ff-6ff0ff1f2fb9">

- View feature2 file

  <img width="476" alt="image" src="https://github.com/ManishNegi963/Git-GitHub-interview-questions/assets/124788172/17046e13-46a4-40bb-ac43-317e0a3a566b">

 - Reverting the bug commit

       git revert f54cafd

<img width="493" alt="image" src="https://github.com/ManishNegi963/Git-GitHub-interview-questions/assets/124788172/ee562dee-3849-4171-a759-38c68d767e19">

  git revert also create a commit for revert, only the bug commit will be reverted and functionality remains same.


- Bug feature in feature2 file has been removed

  <img width="427" alt="image" src="https://github.com/ManishNegi963/Git-GitHub-interview-questions/assets/124788172/c8980125-63bc-4137-a58d-013a9b79c599">

- Use case of git reset

  Suppose you have keys commited to git and now you have remove those keys from git, for that we will use git reset to untrack changes.

  - Commit keys with feature3 and 
 
        git add .

 Ths will commit all the untracked files.

 <img width="422" alt="image" src="https://github.com/ManishNegi963/Git-GitHub-interview-questions/assets/124788172/672743e9-48be-4df5-b48e-4214c832c6e5">

- added more fucnc and keep working on it.

<img width="514" alt="image" src="https://github.com/ManishNegi963/Git-GitHub-interview-questions/assets/124788172/6603ff0b-c08a-4bea-ac95-3fc5515bedd5">

- now use git reset to reset to the last commit where keys were not tracked/commited.

      git reset 28878ad

gti reset removed the logs and untracked the changes.

<img width="497" alt="image" src="https://github.com/ManishNegi963/Git-GitHub-interview-questions/assets/124788172/afd1dcf6-4637-429f-8240-5741be5033c4">

- Now you have the keys untracked.

<img width="571" alt="image" src="https://github.com/ManishNegi963/Git-GitHub-interview-questions/assets/124788172/28a34ea3-039e-4720-89b3-3056fb08b35a">

- Use case of .gitignore

  Suppose you want a file not to be committed/tracked for example keys, then we can put that file in .gitignore

  <img width="228" alt="image" src="https://github.com/ManishNegi963/Git-GitHub-interview-questions/assets/124788172/84d921a3-91d5-48de-8679-adf4d84107b1">

- commit .gitigore file

  <img width="566" alt="image" src="https://github.com/ManishNegi963/Git-GitHub-interview-questions/assets/124788172/32a62371-0bcb-4d89-901c-4b16399f66f9">

- view git status

  <img width="392" alt="image" src="https://github.com/ManishNegi963/Git-GitHub-interview-questions/assets/124788172/17a5d289-1166-4f0c-8c02-62c2aa9f7f01">

- Use case git rebase vs git merge

  SUppose you went to holiday and now to get all the changes in sequential manner you can use git rebase.

  There were some changes in master branch in GItHUb while you were on holidays, then use git pull origin master --rebase in local, it will take all the log history in sequential manner in your local.

      git pull origin master --rebase

  but if you use git merge then it will pull the last head from github.

 - Use case of cherry-pick
 
   - suppose you added a feature6 for later use in dev branch and then added fesature7.

<img width="484" alt="image" src="https://github.com/ManishNegi963/Git-GitHub-interview-questions/assets/124788172/8325d3d9-3f4d-467c-b325-44dcfdf2f4be">


  - then you go to master branch and want feature6 only, then we can use git cherry-pick

            git cherry-pick 32b9fac

  <img width="421" alt="image" src="https://github.com/ManishNegi963/Git-GitHub-interview-questions/assets/124788172/4f86d022-7ea3-4959-ac52-bccb06f061f9">


- Use case of git stash

  Suppose you are working on feature8 and then in middle of work you go to another branch staging and in that feature8 you have half work and you don't want to commit that half work
  then you can temporarily store that work into stash by using git stash.

   - Added half work but didnt want to commit the half work
 
 <img width="517" alt="image" src="https://github.com/ManishNegi963/Git-GitHub-interview-questions/assets/124788172/c75b51e9-b980-4b20-9371-66055928ea6b">

  - use git diff to see the half work/not commited

    <img width="455" alt="image" src="https://github.com/ManishNegi963/Git-GitHub-interview-questions/assets/124788172/78f6816c-5a93-4d2e-a826-e3660fe1c439">

- store the work in temporary by using git stash

      git stash

<img width="540" alt="image" src="https://github.com/ManishNegi963/Git-GitHub-interview-questions/assets/124788172/a2a0afe7-10c7-4503-8411-a70db27b4903">

- Pop out the stashed work

      git stash pop

  <img width="587" alt="image" src="https://github.com/ManishNegi963/Git-GitHub-interview-questions/assets/124788172/76938c0e-d619-40a9-8325-133c8bc26c3d">

- How to resolve merge conflict?

- Editing a file in local feature-6.txt and commit

  <img width="563" alt="image" src="https://github.com/ManishNegi963/Git-GitHub-interview-questions/assets/124788172/df9b941c-b397-4fbd-9336-6cc1546a15d6">

  - Now go to the same file in dev branch in Github an edit the same lines and commit
 
    <img width="588" alt="image" src="https://github.com/ManishNegi963/Git-GitHub-interview-questions/assets/124788172/8a4fdadd-e9be-4ad6-ae1b-e98cca40b367">

- Now local and remote both have made changes to the same lines in same file and it create a conflict to which code to use when we do git pull origin dev.

       git pull origin dev
 
<img width="562" alt="image" src="https://github.com/ManishNegi963/Git-GitHub-interview-questions/assets/124788172/d3c82de9-2b1c-4abe-8886-8afbc7935d0a">

- Now we can merge both code using --ff(fast forward)

       git pull origin dev --ff

- NOw check the status as both are modified.

  <img width="565" alt="image" src="https://github.com/ManishNegi963/Git-GitHub-interview-questions/assets/124788172/5f1aae14-31ea-4347-9015-d46152bb19c6">

- NOw edit the file feature-6.txt and choose which code to use

<img width="629" alt="image" src="https://github.com/ManishNegi963/Git-GitHub-interview-questions/assets/124788172/996e430d-b747-4db3-8034-05121452082c">

- Using github code

  <img width="550" alt="image" src="https://github.com/ManishNegi963/Git-GitHub-interview-questions/assets/124788172/a9c5b6df-969e-4636-b0cf-f1f25f931767">

