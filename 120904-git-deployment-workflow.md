# Git Deployment Workflow

I'm going to describe a Git workflow.

## Background

## Assumptions

## The Workflow

1. Claim and start the story.
2. Pull the latest changes to the master branch.
  * I recommend rebasing everytime you pull. For more info, see [http://stackoverflow.com/questions/2472254/when-should-i-use-git-pull-rebase](http://stackoverflow.com/questions/2472254/when-should-i-use-git-pull-rebase)
3. Create a branch from master.
  * I recommend naming your brach &lt;bug|feature&gt;-&lt;story ID&gt;-&lt;short description&gt;. For example, `feature-238476-article-pagination`.
4. Develop, commit, repeat.
  * Commit often! You'll have a chance to clean up and combine your commits later.
  * Rebase with master as needed.
6. After completing the story, merge your branch into the review branch and push both. Mark the story finished.
7. The review branch can be deployed to the review server at any time. After a deploy, mark all finished stories delivered. For each story delivered, issue a pull request to master from the story's branch.
8. When a story is confirmed in review, mark it accepted and merge the pull request.

### Notes

* It's important not to merge the review branch into a story branch.