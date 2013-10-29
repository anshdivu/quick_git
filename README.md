Git-Commit-with-Jira-ID
=======================

Link the script to local bin folder:

    ln -s $PWD/git_commit_jira /usr/local/bin/gcj

Usage Example:

    $ gcj -j 100 -m "Easy Commit"
    ### or ###
    $ gcj 100 "Easy Commit"

This command would internally execute:

    $ git commit -v -m "PHAPPDEV-100 Easy Commit"
