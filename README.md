## GIT WORKFLOW

```
         ┌── hotfix─────────┐
master──────────────────────────────────────────────────────────────────tag(release-v1.0)─────────────────────── -
 └── develop──────────────────(merge)───(merge)───(merge)─────tag(qa-v1.0)─────────┘─────────────────────── -
     ├── feature1────────────────┘        │        │                     └── feature4───── - 
     ├── feature2───────────────(mrege)───┘        │               
     │            └── feature2.1───┘               │
     └── feature3──────────────────────────────────┘

```
Master branch will be used for production and making releases.

Our default branch is develop. We can create branches from it. We will develop features and merge and test it. and on every 25 day of the month we merge the develop branch to master and tag it with the release version.

No developer can directly merge on master. developers can create feature branches from the develop branch, develop features and create pull requests to merge them to develop branch.

Developers create pull requests(PR) for code review, Then after reviewing code, administrators merge it to develop branches and create tags for qa.

QA Tags to be tested by QA team or might need multiple recursions to fix. Final tag to be released to production(master). fix for issues will follow the same branching strategy as feature branches.

hotfix branches are used to quickly patch production releases. Hotfix branches are a lot like release branches and feature branches except they're based on master instead of develop.

