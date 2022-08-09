# GH CLI DEMO

This is designed to be a 20-minute Fast Focus talk

## Links

- https://cli.github.com
- https://cli.github.com/manual/

## Before The Demo

- Make sure to set terminal background to white with black letters (easier on projectors)

## Demo Outline

- Start with screensaver running on command prompt
  - `gh screensaver --saver starfield`
  - extensions
- Slides
- Create a new repo
- Open an issue
- Make a code change
- Submit/merge a pull request
- Run a GitHub Actions workflow
- Misc (if time)
  - Alias
  - Codespaces
  - API

# Details

- Start with screensaver
  - `gh screensaver --saver starfield`
  - "Welcome to the GH CLI talk. For the next 20 minutes, our goal is to navigate ourselves around GitHub purely from the command line. Let's get to it"
  - Not going to show how to install, read directions for that
  - Screensaver is an extension
  - `gh extensions list`
  - `gh screensaver --help`
- Slides
  - `gh reset-slide`
  - `gh next-slide`
- Create a repo
  - Going to create a repo using a repository template
  - Start in repos folder
  - `gh --help`
  - `gh repo --help`
  - `gh repo create mickeygoussetorg/gh-cli-demo1 --template mickeygoussetorg/gh-cli-template-repo --clone --public`
  - cd gh-clit-demo1
  - `gh repo view`
  - `gh repo view --web`
- Open an issue
  - We need an issue to track our work
  - `gh issue --help`
  - `gh issue create --title "Fix the bug in the workflow file" --body "There is a bug in the workflow file. Fix it" --label "bug" --assignee "@me"`
  - `gh issue list`
  - `gh issue view 1`
  - `gh issue comment 1 --body "ok, I will fix it"`
  - `gh issue view 1`
- Make a code change (consider doing this with codespaces instead)
  - `git checkout -B mickeygousset/code-change`
  - `vi .github/workflows/Manual\ workflow.yml`
  - Add a blank line, save, commit
  - `git push --set-upstream origin mickeygousset/code-change`
- Submit/Merge PR
  - `gh pr --help`
  - `gh pr create --help`
  - `gh pr create --title "Fixed the bug" --body "Fixed the bug related to issue #1"`
  - `gh pr view 2`
  - `gh pr diff 2`
  - `gh pr merge --help`
  - `gh pr merge 2 --subject "time to merge!" --body "Merge baby merge!" --delete-branch --merge`
  - `gh pr list --state all`
- GitHub Actions
  - `gh workflow --help`
  - `gh workflow list --help`
  - `gh workflow view ID`
  - `gh workflow view ID --yaml`
  - `gh workflow run --help`
  - `gh workflow run ID`
  - `gh run list`
  - `gh run watch ID`
  - `gh run list`
  - `gh run view ID`
  - `gh run view --job=ID`
- API
  - GH CLI is a create way to interact with the API and script the API, instead of using curl commands
  - `gh api users/mickeygousset`
  - `gh api /orgs/mickeygoussetorg/repos`
- Now I promised to stay in the CLI for most of this demo, but just so you know:
  - `gh --help`
  - Codespaces, gists, releases, ssh keys, secrets, and more


