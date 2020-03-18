# Clean Code

## Code

1) Watch spacing vs tabs in your commits / PRs. Sometimes developer did not make any real changes in the source file, but we can see the changes from space to tabs or back. Please avoid that!

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


## Github Issues and PRs

1) It's best to make sure every Github PR or Issue has a short video or screenshots, especially for complex features. Today lots of software available for video recording (both paid and free), including:
- https://getsharex.com
- https://obsproject.com
- https://www.techsmith.com/screen-capture.html
- https://www.loom.com
- https://www.getcloudapp.com
