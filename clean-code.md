# Clean Code

## Principles

- we micromanage technical details and code, not people!

- we mainly judge engineers on how good they following the development process, because if they follow the process well, good results will always follow! The focus should be on good process (and continues improving), not just good code!

- make sure you read and understand the task (issue) before you start writing code. We prefer engineer re-read task description (with sub-tasks, comments, etc) multiple times to make sure nothing missed before any code written

- we are not interested our engineers to do task faster in the expense of getting it done right!

- before implement some components or modules, make sure:

  a) such components/modules not exists yet (in our codebase or as an open-source project you can use)  
  b) if nothing exists and you are going to build new one, make sure to think if such component/module can be done more generic way and used in other parts of the system you are building. For example "notes" or "notifications" modules could probably be used in 100x places all over any software or even in multiple software. So if you need to create EmployeeNotes, CandidateNotes, ProductNotes, etc, make sure you create generic "Nodes" instead and use it everywhere.
  
## Code

1) Watch spacing vs tabs in your commits / PRs. Sometimes developer did not make any real changes in the source file, but we can see the changes from space to tabs or back. Please avoid that!

2) For JS/TS based projects, if you use VS Code please setup [DeepScan Extension](https://marketplace.visualstudio.com/items?itemName=DeepScan.vscode-deepscan).

3) For .NET projects, if you use VS 2019 please setup [ReSharper](https://www.jetbrains.com/resharper) (ask manager about license).

4) Watch out for errors from DeepScan, CircleCI build reports or other tools we are using after you push your code and fix them as soon as possible.

5) Make sure you push code DAILY (to feature branch of course), even if you working long time on some large Epic!

6) On "removing" of some code. Basically, people say that it's great when you can remove a lot of code and make your code base simpler / smaller. And it's true and normally part of the process called "Refactoring". What is not acceptable however, is when you remove the code you do NOT understand (yet), for example, when you try to do your task or fix some issues, etc. You may think: "hm, I don't understand that few lines of code (or thousands lines, does not matter), so let's just remove it" and this is where you basically make a huge mistake because you just remove some FEATURE ... So, please DO NOT EVER REMOVE EVEN SINGLE LINE OF CODE UNLESS YOU ABSOLUTELY UNDERSTAND WHY IT WAS ADDED THERE AND WHY IT'S NOT NEEDED ANYMORE. We see this happens mostly for beginners / juniors, rare for Senior Developers (unless by mistake of course, sh..t happen to everyone).

7) Let's avoid Typos! Use https://marketplace.visualstudio.com/items?itemName=streetsidesoftware.code-spell-checker or similar extension for your IDE to check spelling! 

8) DRY - do not repeat yourself - do NOT copy / paste code multiple times!

## Branching

1) When developer pushed some large commits to new `feature` branch, it's best to create **Draft Pull Request** from `feature` branch to `develop` branch (note: Draft, not regular!). That way we can be sure nobody will remove feature branch by incident plus it will be able easy to review code changes directly on Github.

2) It's best to make sure developer pulls the latest from `develop` branch daily before starting new `feature` branch. If developer already working on some feature branch, it's best to merge from `develop` branch into the `feature` branch on a daily bases. It's very important to avoid large merge issues later!

3) Make sure branches and PRs named like `feat/#333-time-management-page`, where #333 is number of issue on Github (Note: instead of `feat` you can use `fix`, `docs`, `refactor` and other keywords).

4) ALWAYS base your feature branch on `develop` branch!

5) Be careful when you merge to not lost your own changes or other developers changes. Ask more senior developers to help with merging if you not completely sure how to do it safely.

6) To Summarize, the flow to starting work on new feature or fix is following:

 - First checkout develop `git checkout develop`
 - Pull latest `git pull`
 - Now create your feature or fix branch `git checkout -b feat/#ticket-number-and-some-more-branch-name`
 - Write your code
 - Now commit, push and make PR from your feature branch `feat/#ticket-number-and-some-more-branch-name` into `develop` branch
 - For a different feature or fix repeat steps above again :)

7) Enable automatic rebase / stash

`git config --global pull.rebase true`  
`git config --global rebase.autoStash true`

## Github Issues and PRs

1) We recommend to install https://www.zenhub.com/extension for better project management on Github

2) It's best to make sure every Github PR or Issue has a short video or screenshots, especially for complex features. Today lots of software available for video recording (both paid and free), including:
- https://www.loom.com
- [Vimeo Record](https://chrome.google.com/webstore/detail/vimeo-record-screen-webca/ejfmffkmeigkphomnpabpdabfddeadcb)
- https://getsharex.com
- https://obsproject.com
- [Snagit](https://www.techsmith.com/screen-capture.html)
- https://www.screencastify.com/
- https://www.getcloudapp.com
- https://www.apowersoft.com/free-online-screen-recorder
