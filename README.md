# Project Donut

:doughnut:

Bringing the Windows ecosystem to Pivotal's Cloud Foundry, one feature at a time.

### To use:

1. [Install `repo`](https://source.android.com/source/downloading)
1. Make a workspace: `WORKSPACE=/some/path/you/like mkdir $WORKSPACE && pushd $WORKSPACE && repo init -u <raw_master.xml_link>`
1. Become current: `repo sync`
1. Make a branch: `repo start NEW_AWESOME_WINDOWS_INTEGRATION PROJECT_NAME` <- `PROJECT_NAME` is the repo you want to make changes to.
1. Start working in whichever project you need.
1. Finalise your changes: `git commit && git push origin`

### Note

`repo` is designed to use Gerrit, and thus it uses cherry-picking commits back into `master`. When you run `repo sync` on an existing workspace, it will overwrite (or fail, depending) your local changes not in the master branch. If you aren't interested in Gerrit (which is fair, I like it), then just run `repo sync -n`, which just fetches changes; merging is then on you as a user.
