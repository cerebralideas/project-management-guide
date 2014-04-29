# “Scrum” Style Project Management

Since we have multiple developers from multiple timezones, communication will be hard. We will need to adapt certain will known communication techniques to fulfill our needs. Here they are:

## Asynchronous Communication Channels

We have four separate mediums with which we can communication: email, Basecamp, Slack and Github.

### Email

This is a well know channel for communication, but should be avoided as much as possible. Email threads can spin out of control and be hard to find, search or archive. Use this sparingly if you need to make something more official.

### Basecamp

This will be our topic specific discussion forum and todo manager. We share files, images, documents and such within Basecamp to centralize our efforts. Make sure to include only the persons relevant to the discussion if a post is initiated. Be sure to include Me, Justin, in all threads; this is a requirement.

I will post everyone’s todos using Basecamp and will ensure prioritization is clear. If you have a question, ask it. Make sure threads are specific and kept on the original subject. Don’t spawn hundreds of threads and don’t hijack existing threads.

### Slack

Slack will be our logged chat and direct messaging. Specific rooms will be labeled and used to keep our chats organized and searchable. Use Slack for quick questions, general comments and informal chatting.

Slack has the feature of specifically naming those you want notified of your question or comment. It’s done similarly to Twitter. This naming will send the user an email notification that you want to chat.

## TODO Management

There are four todo lists:

1. Backlog
2. Todo
3. Doing
4. Completed
5. Accepted

The methodology tracks the stages of a todo, rather than the binary state of done or not.

What this means is that if a task is in the Todo list and assigned to you it's ready and you accept the task as is (you plan on doing it this sprint). Once you actually start the task, you move it to Doing. When you finish the task, you move it to Completed.

Then, I'll move it to accepted after I've reviewed it, merged it …

When the sprint is over, that's when I'll check the all off, so they are removed from the list.

### Github

Use Github sparingly as their issue management is not very well designed, IMO, and it’s hard to manage multiple threads. *Only* use Github for **code** specific communications, and PR comments.

## Our Communication Practices

### “Daily Standup”

We will have a Slack channel (or chat room) dedicated to the idea of daily standup. Each team member, at the beginning of their day will read what’s been posted before them by other team members and then post what they did the prior work day and what they are going to do that day. **This is mandatory!**

Keep what you write concise and to the point, but cover all important topics. If you read that someone is doing something that you were planning on doing, or that what they did may overlap with what you are doing, then make sure to reach out to that developer. This can be done in a topic specific room, but intentionally naming them in the thread, or by DMing them personally.

If either are not possible due to timezone conflicts, then contact me, Just, your project manager.

## “Sprints”

At first, we will use a one week sprint methodology. At the end of each sprint, we discuss how we think it went, and then we plan for next sprint. The discussion will happen in Slack under Sprint Planning, but task management and specific task discussion will happen in Basecamp.

## Coding Practices

We use feature branching to develop our code base, and when your code changes are ready to be reviewed, commit a PR into master. I will then review that PR and provide feedback or merge it into master.

Once you have committed a PR, that feature should be considered done, and you start on a new task that correlates with a new git branch. Name your branches according to the feature or bug you are working on.

If you are pair programming, there will need to be a shared branch that both of you will be branching off and merging into that is NOT the master branch. Make sure that one of you is responsible for keeping that up to date with master.

**Before you commit your PR, make sure you pull from master, this will eliminate any code conflicts from your modification and makes reviewing PRs much easier.**

### Git Rules

Only use these commands in Git:

- `git clone <repo_location>`
- `git pull <repo> <branch>`
- `git push <repo> <branch>`
- `git checkout [-b] <branch>`
- `git log`
- `git reset —`
- `git clean -i`
- `git branch [-d, -D]`

If you need to use another git command other than the ones above, **please** be sure you know what you’re doing. Some commands can be very destructive if not done right. If something bad happens, whatever you do, **don’t push the darn code!**. Just `git reset` and `git clean` to get out of the branch and then delete it.

### Only I, Justin, can merge or modify master , no exceptions!

## Coding Style

We all follow the code style and conventions according to this style and conventions guide: [Cerebral Coding Guide](https://github.com/cerebralix/cerebral-coding-guide). All PRs must follow these guidelines. If not, I will ask for modification. The integrated JSHint Grunt plugin will also enforce these guideline.

We are engineers, not brogrammers, so we appreciate clean, well written verbose code that other people can read and understand quickly. **Don’t write clever code.** 

Write in a “self-commenting” style and leave additional comments if there is still a chance of confusion. *Over-communication is better than under-communication.*

Follow established convention in the existing codebase, even if you don’t agree with it. If you would like something changed, request a PR and validate your stance. We do not use a classic inheritance pattern. We don’t write “classes” in JavaScript and don’t use Constructor/Prototype patterns.

What we use is behavior delegation with the Object.create() method. You can read more about that here: [JavaScript Objects by Kyle Simpson](http://davidwalsh.name/javascript-objects). We also follow Doug Crockford’s book *JavaScript: The Good Parts* methodology, and we use patterns from *Effective JavaScript* by David Herman
