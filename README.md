# A process

**This is how the *Comrades!* work.**

This is not the be-all and end-all and it will never be finished. However we find it a good place to start, because having a process that we're all familiar with means we can quickly get up and running when working together. It also means that the people we work with understand how we do things and we can work together to make great things. 

To write this process we've drawn on our experiences working within teams in organisations as well things we've found works well when working on projects together. You'll notice a lot of ideas taken from *Agile* and *Scrum*, but there also ideas that just came from a common sense approach to tackling web development projects. We're also heavily inspired by the transparency and scope of [Hanno's 'Playbook'](http://playbook.hanno.co) and [North's project guide](https://github.com/north/north).

This guide is structured in a somewhat chronological form from project start to finish, however depending on the project some parts may not be applicable. 

## First contact

When we are approached by potential clients/partners we try and garner as much information about a project via email first. If any of the *Comrades!* think the project is something they or any of the other *Comrades!* can help with, then a face to face meeting or video chat will be arranged. 

During the first meeting we'll discuss the following:

- The project's goals, timings and current state.
- How many *Comrades!* might be needed and for how long.
- Are we going to be part of a bigger team or our own isolated unit.
- Will we be based on site or remote.
- Who will be our main contact and what is their position within the organisation.


## Project planning

If your project is starting from scratch we can come in a help get things going. We'll use user stories and personas to try define the product requirements.

### User personas

A key to developing a good digital product is to understand the target user(s). We find it helpful to define basic fictional user personas to describe the different subsets the products potential user base. Persona's allow the whole team to understand the top level objectives of the product.

An example persona might be:

> Dave is a tech savvy user who wants to use yacht-r-us.com to buy his first ocean going yacht.

### User stories

Persona's will inform user stories. Each story describes a specific task that a user may want to undertake.

A story contains a description of an individual requirement, along with a set of acceptance criteria that is used to decide when a story has been completed successfully. Where relevant, a story should also contain links to UX/designs, technical specs, form field names, validation rules, business logic or any other supporting material. 

A story title should always include the persona name and define a small focussed requirement like so:

> Dave should be able to pay for his yacht with his Mastercard.

More info on writing good user stories: [https://medium.com/@jonatisokon/a-framework-for-user-stories-bc3dc323eca9]()


We use Trello boards to track stories. We'll work with all product stakeholders to agree on a set of stories to go into a intial or next release and place them in the [backlog](http://guide.agilealliance.org/guide/backlog.html) for that version.

Anyone can create a new story at any time as new requirements come to light. New stories should be added to the overall product backlog. Where they can be [groomed](http://guide.agilealliance.org/guide/backlog-grooming.html) by the stakeholders and potentially be selected for future versions.


## During the project

Once a first release has been agreed the project can get underway. [Sprints](http://scrummethodology.com/scrum-sprint/) are used to work through the version backlog.

### Sprints

A sprint is an agreed set of time (usually two weeks) in which we select a subset of stories to work on. 

In advance of each sprint, a backlog grooming session should take place, whereby the backlog is reviewed and stories prioritised to decide what will be worked on next. 

To be successful it will need business buy-in, people responsible for making decisions need to attend, or grant the power to make decisions.

To be considered for inclusion in a sprint, a story must contain the content outlined above (a description of the requirement, and acceptance criteria). It must also be signed off by the business. This is to avoid ambiguity and building to an incorrect set of requirements.

All new stories should be added to the backlog. Unless there are exceptional circumstances, and agreement from all involved, a new story should never be added into a current sprint. It can be prioritised to ensure it is at the top of the backlog ready for the next sprint. 

A sprint is not a fixed set of work. It is an estimation of the amount of work thought possible given the amount of time available. 

During a sprint, if work is progressing at a greater pace than originally anticipated, it is possible to include extra stories from the backlog. 

Likewise, if a sprint is more complex than originally thought, it may be that stories will not be completed. These stories will need to be reconsidered on an individual basis - either they are re-added to the backlog, or they can carry over into the following sprint. However, where possible this should be avoided.

#### At the start of each sprint
We should have a kick-off meeting where we look through the backlog (which should have been prioritised) and pick a set of stories that can be achieved in the time available. 

Developers will discuss the stories that the business/product owner has provided, discuss them in detail, add technical details and potentially split the stories up into smaller logical chunks of work which can be recorded as tasks on Trello.

We should decide upon the length of the sprint - we will usually default to 2 weeks unless there is a valid reason to change.

We should update a shared calendar to show who is available on which days for the sprint.

#### During each sprint
We will have a daily catchup/standup at the start of the day. This is a brief meeting to discuss progress: who is working on what and with whom; What the requirements are; If there are any blockers. No detail should be discussed - if a further conversation over a specific point is required it can be arranged here but discussed separately.

If considered relevant, we could have a mid-sprint review half way through a sprint. This is a longer meeting to discuss progress, and a good time to consider adding or removing stories from the sprint.

#### At the end of each sprint

##### Sprint review

At the end of the sprint it's good to showcase what's been achieved in that sprint to the product stakeholders. A good way to do this is to go through the list of finished tickets and discussing the work that has taken place. 

##### Retrospective

After each sprint a [retrospective](http://www.mountaingoatsoftware.com/agile/scrum/sprint-retrospective) allows the sprint to be reviewed in terms of it's process. This an important part of the process, as it is the point where we review both progress and process to decide whether changes are necessary. 

Everyone involved in the sprint should discuss:

 - what went well
 - what didn't go so well
 - what we would do differently next time

This is an open honest discussion, it is important to learn from any mistakes and refine the process so that it works for everyone.

### Development process
#### Branches
When starting a new piece of work, a new Git feature branch should be created to allow this piece of functionality to be worked on in isolation.

Always start a new branch name with `developer-name/` to show who's working on them. 

The exception being when it's something multiple developers are working on together, when we change the name to start with `feature/`

Any experimental branches that are to live in the repo long-term should be renamed to start with `keep/` to mark it as such.

#### Pull requests

No work should ever be directly merged into the main branch. All work should be peer-reviewed via a pull request (PR). Developers on the team should aim to keep the number of changes/commits in the PR to a minimum. 

In the main PR description a link to the story should be provided, along with a description of the work carried out. Disucssion within the PR should be kept to specifics covered in the changed/new code within that PR.

While a PR is in progress and is not ready to be merged, it should be marked as [DNM] (do not merge) both in the title and with a tag. Once a PR is ready for review, the DNM tag/title should be removed.

A developer shouldn't expect PRs to be found - when ready they should inform the team that a PR is ready for review. Likewise, a developer is responsible for getting their own PRs merged, so rather than waiting for it to be reviewed they should seek review. A developer cannot review or merge their own PR.

Before a PR can be merged, ensure it has been rebased to the latest version of the main branch. Once a PR has been merged, it should be closed and the feature branch deleted.

#### Testing / Continuous integration
Where relevant, tests should be written for all new pieces of functionality. (Use common sense to decide whether a test is necessary). Continuous integrations (e.g. Codeship) will run these tests.

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


