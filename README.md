Git-Commit-with-Jira-ID
=======================

### Install the script (link it to local bin folder):
```bash
$ git clone http://github.cerner.com/DB020377/Git-Commit-with-Jira-ID.git
$ cd Git-Commit-with-Jira-ID
$ ln -s $PWD/git_commit_jira /usr/local/bin/gcj
```

### Usage Example:
* Assuming you are working in branch "PHAPPDEV-123-my-branch"

  ```bash
  $ gcj "Easy Commit"
  ```

  This command would internally execute:
  ```bash
  $ git commit -v -m "PHAPPDEV-123 Easy Commit"

* Assuming you are working in branch "123-my-branch" and the repo url is "http://github.cerner.com/PhAppInfra/MyProject"

  ```bash
  $ gcj "Easy Commit"
  ```

  This command would internally execute:
  ```bash
  $ git commit -v -m "PHAPPINFRA-123 Easy Commit"

* Use '-h' or '--help' to get help manual

  ```bash
  $ gcj -h
  #### or ####
  $ gcj --help
  ```
