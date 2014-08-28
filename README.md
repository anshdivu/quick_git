Quick Git
=======================

### Install the script (link it to local bin folder):
```bash
$ git clone https://github.com/anshdivu/quick_git.git
$ cd quick_git
$ ln -s $PWD/git_commit_jira /usr/local/bin/qg
```

### Usage Example:
* Assuming you are working in branch "ISSUE-NUM-my-branch"

  ```bash
  $ qg "Easy Commit"
  ```

  This command would internally execute:
  ```bash
  $ git commit -v -m "ISSUE-NUM Easy Commit"
  ```

* Assuming you are working in branch "123-my-branch" and the repo url is "https://github.com/MyOrg/MyRepo"

  ```bash
  $ qg "Easy Commit"
  ```

  This command would internally execute:
  ```bash
  $ git commit -v -m "MyOrg-123 Easy Commit"
  ```


* My Favorite combination:

  ```bash
  $ qg -apo "Awesome Commit"
  ```

  This command would internally execute:
  ```bash
  $ git add -A .
  $ git commit -v -m "ISSUE-NUM Easy Commit"
  $ git push origin CURRENT_BRANCH
  $ echo "commit_url" | pbcopy     # OS X only - copies to clipboard
  $ open "commit_url"              # OS X only - opens in web browser
  ```

* Use '-h' or '--help' to get help manual

  ```bash
  $ qg -h
  #### or ####
  $ qg --help
  Usage: qg "commit message"
      -a, --all                        automatically stage files that have been modified, added or deleted
      -h, --help                       Prints help message
      -m, --message=<msg>              Uses the given <msg> as the commit message. Uses '<prefix>-<number> <msg>' as the commit message format
      -n, --number=<number>            Uses the given <number> as part of the commit message. The commit message format will be '<prefix>-<number> <msg>'
      -o, --open                       (OS X only) Opens commit url in browser and copies the url to clipboard
      -p, --push                       Push commits to remote
      -r, --prefix=<prefix>            Uses the given <prefix> as part of the commit message. The commit message format will be '<prefix>-<NUMBER> <msg>'
  ```
  
