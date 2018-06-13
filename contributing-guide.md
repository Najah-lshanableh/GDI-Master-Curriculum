# GDI Contribution Guide :two_women_holding_hands:
Our community it's continuously growing, and our chapters do so much to adapt, collaborate and enhance our curriculum as they prepare for workshops and teaching events. It's absolutely necessary to Girl Develop It's work to create superior curriculum and resource sharing. We ask you to contribute your work back to the GDI master curriculum repository and use the documentation below as guidance.

Included in this file is information about:
* The GDI Open Source Community
* Contributing Guidelines for Issues or Pull Requests
* Using Labels Appropriately
* Contributor Expectations

---
# The Community :tada:
We have broken down the GDI open source community as follows:

* Owner: GDI HQ team
* Maintainers (write access to the repository): Chapter Leaders
* Contributors (everyone who can open and have a pull request merged into a project): Chapter Leaders, Teachers, TA's
* Community Members (users who often use and care deeply about GDI curriculum and are active in discussions to enhance our curriculum): Chapter Leaders, Teachers, TA's, Students

---
# Contributing Guidelines: Issues and Pull Requests :bookmark:
We welcome and highly encourage active collaboration from all the GDI chapters. Contributing back should take the form of issues or pull requests depending on the nature of the contribution. Workshops-related feedback or questions should be submitted via GDI helpdesk.

## Create an Issue :scream_cat:
If you find a bug in a class curriculum, documentation or resources (and you don’t know how to fix it) if have higher-level questions about the scope or sequence of a lesson, or have a general question about the curriculum, create an issue!

Here are a few tips when creating an issue:
  * Check if there are existing issues for your issue. Duplicating an issue is slower for both parties so search through open and closed issues to see if what you’re running into has been addressed already.

  * Be clear about your feedback or question by using a label and thorough details in your issue description: what lesson were you using? what should have happened that didn't happen? how would you change a week? etc.

  * Include error messages, logs, or screenshots

  * Paste error output or logs in your issue or in a Gist. If pasting them in the issue, wrap it in three backticks so that it renders nicely.

## Create a Pull Request :raising_hand:
Pull request is an excellent tool for fostering collaboration among our members.  A pull request is simple a proposal of suggested code/content changes.  Once you submit your pull request, there could also create an opportunity for reviewing, discussing with other collaborators about the potential changes.

If you’re able to patch the bug, create a new lesson, or correct some syntax/spelling yourself – wonderful! Make a pull request with your changes! Be sure you’ve read our styleguide and follow accordingly as it will speed up the merging process. Once you’ve submitted a pull request, the owners and maintainers will carefully review your code/suggestions to determine whether or not more action is needed or the request should be merged or closed.

Here are a few tips when creating a pull request:
  * All pull requests should be submitted from a feature branch on your local fork, straight to [GDI Master Curriculum](https://github.com/girldevelopit/GDI-Master-Curriculum).

  * Before submitting a pull request, please make sure your local feature branch is up to date with [GDI Master Curriculum](https://github.com/girldevelopit/GDI-Master-Curriculum):

  ```
  $ git remote add upstream git@github.com:girldevelopit/GDI-Master-Curriculum
  $ git fetch --all
  $ git checkout -b my-feature-branch upstream/master
  ```

  * Contribute in the style of this repository to the best of your abilities. This may mean using indents, semi colons or comments differently than you would in your own repository, but makes it easier for the maintainer to merge, others to understand and maintain in the future. Again, look at our styleguide for more information.

  * If you're submitting a new lesson, or resource, create a feature branch for each individual resource. Lesson branch naming should follow the same naming style and convention we use for folders. For example:

    ```
    $ git checkout master
    On branch master
    nothing to commit, working directory clean

    $ git checkout -b intro-to-javascript
    Switched to a new branch intro-to-javascript
    ```

  * If a lesson/resources both have the exact same name, just denote which with -lesson or -resource.
    ```
    $ git checkout -b responsive-design-lesson
    ```
    ... or ...

    ```
    $ git checkout -b responsive-design-resource
    ```

  * Again, if submitting a new lesson or resource, please make sure the lessons are in the standard curriculum templates.

  * If pull request is new to you or want to learn more, here are helpful reading resources:
    * [About Pull Requests - Github](https://help.github.com/articles/about-pull-requests/)
    * [Creating a Pull Request - Github](https://help.github.com/articles/creating-a-pull-request/)
    * [Requesting a Pull Request Review](https://help.github.com/articles/requesting-a-pull-request-review/)


### Open Pull Requests
Once you’ve submitted a pull request, a discussion may start around your proposed changes. Other contributors and users may have questions or suggestions, but ultimately the decision is made by the maintainer(s) and the owner. You may be asked to make some changes to your pull request, if so, add more commits to your branch and push them – they’ll automatically go into the existing pull request.

If your pull request is merged – great! If it is not, no worries, it may not be what the project maintainer had in mind, or they were already working on it.

## Labels (WIP) :pencil2:
Labels help us to keep our work organize and well prioritized. Please use labels to make it easier for owners and maintainers to work through and address issues and merge pull requests. Take a look at the labels and label use cases below:

  * admin:

  * Newbies Friendly: Issues that new or beginners can easily work on

  * advanced-issue:

  * content:

  * typos:

  * epic:

  * Bug Fix: Used by contributors for either pull requests that contain solutions or issues reporting a bug

  * Help Wanted: Used by maintainers, owners, or contributors to invite others to collaborate; this will be used in conjunction with assignment

  * Discussion/Question: Used by maintainers, owners, or contributors on issues for higher-level discussions or questions about the curriculum

  * Duplicate: Used by maintainers or owners to classify duplicate issues or pull requests

  * Enhancement/Suggestion: Used by contributors to suggest changes in an issue or enhance a lesson for various reasons

  * Needs Review: Used by maintainers or owners to call for technical support or a second set of eyes

  * Needs Revision: Used by maintainers or owners to notify contributors that more work is needed before a merge

  * New Resource: Used by contributors to submit a new lesson or resource

## Contributors Expectations(WIP) :point_up_2:

The outcome of the issue or pull request is likely to fall into one of three buckets:

  * Merged / Addressed - The feedback, solution, new resource, or bug fix is merged in or addressed immediately. Bug fixes will take priority and, as long as merge conflicts are not an issue, will be merged, immediately.

  * Prioritized for Planning Sprint - If the feedback or pull request cannot be addressed in the time dedicated each week, but the owners and maintainers acknowledge the immediate impact, the pull request or issue will be brought to the next planning meeting (these occur every X weeks) and appropriate time will be budgeted to address and work through the issue or pull request.

  * Logged into the feedback log - If the feedback or pull request cannot be addressed in the time dedicated, and the owners and maintainers do not see the immediate value in prioritizing this feedback, it will be closed and logged into the product feedback log to be used for future iterations and releases of the curriculum.

Expect all your issues or pull requests to be commented on by an owner or maintainer. If after a X week, a dialogue does not ensue and further detail or action is needed, the issue or pull request may be closed.
