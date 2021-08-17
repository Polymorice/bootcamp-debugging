**_TL,DR: DO NOT pull origin in a new empty repo. Add and commit before you do so._**

Last year GitHub implemented the change that the base branch is rename from master to main.

Normally when you follow the instructions on Compass, and you are not aware of the change. You might just ended up with two branches in the repo, both master and main. You could easily Google and follow the instruction to do a merge. If you pay attention. GitHub will remind you about it, and provide instruction on the repo page.

However I have encountered something really annoying which drives me crazy. That is sometimes there is a master branch created, but I cannot pull or clone the newly created main from GitHub, and it will not let me merge. I would get error messages like following when I try to do the renaming or merge.
![image](https://media.giphy.com/media/WH85q8e201wlO/giphy.gif)

> `fatal: The current branch master has no upstream branch.`

> `fatal: Not a git repository (or any parent up to mount point /vagrant)`

> `error: src refspec main does not match any.`

I have only encouter it a couple times, but I began to see the pattern. It is when a new repo is created locally, and new remote origin is pulled to the local repo. There is no items to add and commit. I suspect it will generate a 'ghost' master branch. Since it is empty, it cannot be deleted or merged.

The work-around is to add and commit a file, like an empty README, before pulling the remote origin. When you created the GitHub repo and about to copy SSH link, scroll down a bit. GitHub provided ready to use command lines for easy application.
