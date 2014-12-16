# Development - A process

**This is how the *Comrades!* work.**

This is not the be-all and end-all and it will never be finished. However we find it a good place to start, because having a process that we're all familiar with means we can quickly get up and running when working together. It also means that the people we work with understand how we do things. 

To write this process we've drawn on our experiences working within teams in organisations as well things we've found works well when working in isolation.

## Stories

The task of building a website/web app should be split up into a number of stories that document the requirements of the project.

We have a Trello board containing all stories for v1, the initial version of the website that we aim to launch with. This Trello board is called the backlog. 

Each story contains a description of an individual requirement, along with a set of acceptance criteria that is used to decide when a story has been completed successfully. Where relevant, a story should also contain links to UX/designs, technical specs, form field names, validation rules, business logic or any other supporting material. 

Each story should also be ascribed to a user persona. Multiple personas have been created to associate each requirement with a particular type of user, to ensure that the work remains focused on the core aims of the project. 

Anyone can create a new story at any time as new requirements come to light. New stories should be added to the backlog.

BDD style story template. Note that in this style acceptance criteria are defined as one or more “scenarios”:


More info https://medium.com/@jonatisokon/a-framework-for-user-stories-bc3dc323eca9


## Sprints

We are building the website using an iterative process spread over multiple sprints.

Each sprint is an agreed set of time (usually two weeks) in which we select a subset of stories to work on.

In advance of each sprint, a backlog grooming session should take place, whereby the backlog is reviewed and stories prioritised to decide what will be worked on next. 

To be successful it will need business buy-in, people responsible for making decisions need to attend, or grant the power to make decisions.

To be considered for inclusion in a sprint, a story must contain the content outlined above (a description of the requirement, and acceptance criteria). It must also be signed off by the business. This is to avoid ambiguity and building to an incorrect set of requirements.

All new stories should be added to the backlog. Unless there are exceptional circumstances, and agreement from all involved, a new story should never be added into a current sprint. It can be prioritised to ensure it is at the top of the backlog ready for the next sprint. 

A sprint is not a fixed set of work. It is an estimation of the amount of work thought possible given the amount of time available. 

During a sprint, if work is progressing at a greater pace than originally anticipated, it is possible to include extra stories from the backlog. 

Likewise, if a sprint is more complex than originally thought, it may be that stories will not be completed. These stories will need to be reconsidered on an individual basis - either they are re-added to the backlog, or they can carry over into the following sprint. However, where possible this should be avoided.

## Sprints

Sprints are iterative - not a formalised process. We will collect thoughts from previous sprints to feed in to future sprints. This gives us the room to evolve the process and to learn from experience.

### At the start of each sprint
We should have a kick-off meeting where we look through the backlog (which should have been prioritised) and pick a set of stories that can be achieved in the time available. 

Developers will discuss the stories that the business/product owner has provided, discuss them in detail, add technical details and potentially split the stories up into smaller logical chunks of work.

We should decide upon the length of the sprint - we will usually default to 2 weeks unless there is a valid reason to change.

We should update a shared calendar to show who is available on which days for the sprint.

### During each sprint
We will have a daily catchup at the start of the day. This is a brief meeting to discuss progress: who is working on what and with whom; What the requirements are; If there are any blockers. No detail should be discussed - if a further conversation over a specific point is required it can be arranged here but discussed separately.

If considered relevant, we could have a mid-sprint review half way through a sprint. This is a longer meeting to discuss progress, and a good time to consider adding or removing stories from the sprint.

### At the end of each sprint
On the final afternoon of each sprint we should have a retrospective meeting. This is an important part of the process, as it is the point where we review both progress and process to decide whether changes are necessary. 

Progress - we should look through each ticket and discuss the work that has taken place.

Everyone involved in the sprint should discuss:

 - what went well
 - what didn't go so well
 - what we would do differently next time

This is an open honest discussion, it is important to learn from any mistakes and refine the process so that it works for everyone.

## Development process
### Branches
When starting a new piece of work, a new Git feature branch should be created to allow this piece of functionality to be worked on in isolation.

Always start a new branch name with `developer-name/` to show who's working on them. 

The exception being when it's something multiple developers are working on together, when we change the name to start with``feature/

Any experimental branches that are to live in the repo long-term should be renamed to start with keep/ to mark it as such.

### PRs
Where possible, a new PR should be created for each story. 

It is a good idea to create a new PR early in the process so that it can be informally reviewed throughout its lifetime, and help to identify the origin of each branch.

In the main PR description a link to the story should be provided, along with a description of the work carried out.  

No work should ever be directly merged into the main branch. All work should be peer-reviewed via a Pull Request.

While a PR is in progress, it should be marked as [DNM] (do not merge) both in the title and with a tag. 

Once a PR is ready for review, the DNM tag/title should be removed.

A developer shouldn't expect PRs to be found - when ready they should inform the team that a PR is ready for review. 

Likewise, a developer is responsible for getting their own PRs merged, so rather than waiting for it to be reviewed they should seek review.

A developer cannot review or merge their own PR.

Before a PR is merged, ensure it has been rebased to the latest version of the main branch.

Once a PR has been merged, it should be closed and the feature branch deleted.

### Testing / Continuous integration
Where relevant, tests should be written for all new pieces of functionality. (Use common sense to decide whether a test is necessary).

CI (e.g. Codeship) will run these tests.

A feature branch should only be merged if test coverage is comprehensive, and if all tests pass.

### QA
Once a developer considers a piece of work to be complete, it will have been merged into the main branch.

At this point, the story should be reviewed on the dev server once a branch has been merged, to ensure that the work is reviewed in an independent place (as opposed to on the laptop of the developer carrying out the work).

QA should be carried out by an internal member of the team.

The QA review should involve testing a piece of new functionality against the description and acceptance criteria outlined in the story. 

If a story does not pass QA, a relevant note should be added so that the relevant developer knows what further work needs to be carried out.

## Supporting services

#### Trello
Trello is used for managing stories into numerous boards. 

The Trello boards should be kept up to date at all times as it is the best place to see an overview of the latest state of the website.

#### Github
Github is used for managing the codebase.

Github PRs are used for reviewing and merging updates.

Github issues are to be used only for very specific issues related to the current codebase. All major code updates should be managed via Trello tickets so that all development work can be tracked in one place.  

#### Slack
Slack is used for day-to-day communication between the team, rather than using email.

Slack is transient in nature. As such it is easy to miss conversations. It should be used for day-to-day conversation, but any important updates should be communicated in meetings to ensure everyone is aware.

#### Email
Where possible email should be avoided for project-specific conversation. Where email is necessary, ensure everyone relevant is copied in. 

Email should be used for admin - e.g. invoicing, agreeing terms of the project/contract, etc.

## Any other business

### Working remotely

Before someone is able to work remotely, there must be agreement from all concerned. If someone is working remotely they are expected to keep to standard office hours, be present on Slack, and contactable via Skype.


