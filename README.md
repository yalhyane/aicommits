# AI Commit

Have AI Commit write your git commit messages for you so you never have to write a commit message again.

[![AI Commit Screenshot](./screenshot.png)](https://twitter.com/nutlope/status/1624646872890589184)

## How to install

`npm install -g autocommit`

**Note:** The process to install this will get vastly simplified when I rewrite this CLI and publish it as an npm package to be run with `npx`.

## How it works

This project uses a command line interface tool called zx that's developed by google. In the script, it runs a `git diff` command to grab all the latest changes, sends this to OpenAI's GPT-3, then returns the AI generated commit message. Video coming soon where I rebuild it from scratch to show you how to easily build your own CLI tools powered by AI. Fully privacy friendly as commands only run on your local machine using your OpenAI account.

This CLI also supports conventional commits. If you want conventional commits, simply set the `conventionalCommit` variable at the top of the script to `true`.

## Remaining tasks

Now:

- [ ] Rewrite this in node to publish as an npm package
  - [ ] Figure out how to fail gracefully instead of exit 1
  - [ ] Try openai curie And/OR codex

After:

- [ ] Rewrite in TypeScript
- [ ] Look into better conventional commit support, look at other CLIs
- [ ] Try supporting more than 200 lines by grabbing the diff per file
- [ ] Build landing page

# How to run new version