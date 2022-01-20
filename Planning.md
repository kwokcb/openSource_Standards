Version 1: January 19, 2022

# Exposure and Tracking of Contributions

Depending on the site your working and the complexity you
will probably want to keep track of issues and tasks.

In this article, we'll take a look at this using `github` which has progressively been trying to provide more "tooling" in this area. We will keep things as
simple as possible by using all tooling available locally to the repo.

# Issues

A common way to track a "work item" is to create an `issue` for this.

This can be a proposal to do some piece of work or it could be something like a fix to a defect you've encountered. Once logged than it's open for feedback and discussion.

Assuming you know your scope, then I refer you to the article about some suggestions on how to document it. `github` has a built in "issues" section for each repo with native `MarkDown` support for descriptions. Using this instead of
an external attached file allows for a straight-forward and easilty readable way
to work with others. 

Below is a snapshot from this repo showing some example issues. Categorization /
labels, project association and milestones are some ways to organize. And of course
assignement let's folks your actually doing the work.

![image](https://user-images.githubusercontent.com/49369885/149637211-f1ab2b1d-0588-40f1-a7e0-d81583781e8f.png)

In many cases issues can be logged but the additional meta-data may not be
entered unless the repo owner adds them in. It does not hurt to suggest this :).

One alternative is to keep track of issues in your own fork -- which gives you full control. In this case you can cross reference the original repo's issue with your fork onw.

# Synchronization Multiple Tracking Systems 

Using `github` to track issues for a given repo is fairly common. Unfortunately in some cases you may have to contend with multiple tracking systems. This can come up if your working for a company contributing open source but may have it's own tracking system.  

One example is a company JIRA and a public github repo. One rule-of-thumb
folks can use is, where is the "ground-truth". This should the public location.
If you fork from a repo, then you can keep this public in your own fork.

# Projects and Boards

Depending on the number of issues you may have and the requirement to see things holistically, `github` itself has the ability to do things like create projects and associated planning boards (Kanban). There are also third party tools
for this, but as noted this keeps all tracking in one place.

Below is an example of the above issues shown in various states. For convenenience
using tool which allows you to associate commits (pull requiests or PRs) with issues along with automated state tracking should make things very simple.

![image](https://user-images.githubusercontent.com/49369885/149637182-f8a8b485-c562-4032-9a3d-8ce93d9528f1.png)

Of course you'll need to associate your commit with an issue, which is simple
to do by adding the appropriate [Markdown references or manually linking](https://docs.github.com/en/issues/tracking-your-work-with-issues/linking-a-pull-request-to-an-issue). 

Note that you can connect to issues across repos if for example your issue is kept in your own fork.

# Summary
To summarize, find the tooling that the repo owner suggests and use it. If inflexible, then you can fork to keep track of additional information.
Keep stuff human readable and local -- which means learing some MarkDown or html.

