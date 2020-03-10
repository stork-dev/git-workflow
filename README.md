## GIT WORKFLOW

```

master──────────────────────────────────────────────────────────────────tag(release-v1.0)─────────────────────── -
└── develop────────────────────merge────merge────merge─────tag(qa-v1.0)─────────┘─────────────────────── -
    ├── feature1────────────────┘        │        │                     └──feature4───── - 
    ├── feature2────────────────mrege────┘        │               
    │            └── feature2.1───┘               │
    └── feature3──────────────────────────────────┘

```
Master branch will be used for produnction and making relases.

Our default branch is develop. We can create branches from it. We will develop features and merge and test it. and on every 25 day of month we merge the develop branch to master and tagged it with release version.

No developer can do directly merge on master. developers can create feature branches from the develop branch and merge them to develop branch.

Developers create pull request(PR) for code review, Then after reviewing code, administrator merge it to develop branch and create tag for qa.

QA Tags to be tested by qa team or might need multiple recursion to fix. Final tag to be released to production(master). fix for issues will follow same branching strategy as feature branches.
