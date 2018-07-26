mr-kibrarian repo
=================

This is a top-level [myrepos](https://myrepos.branchable.com/) git repository
which organizes other git repos used by Kibrarian Group for KiCad parts library
work.

To quickly get setup with all the needed git repos for KiCad library work, you
can follow these exact steps:

1. Clone this repo: `git clone https://github.com/kibrarian-group/mr-kibrarian.git`
2. Enter the mr-kibrarian directory: `cd mr-kibrarian`
3. Tell myrepos to trust this directory: `echo $(pwd)/.mrconfig >> ~/.mrtrust`
4. Checkout all the git repos with myrepos: `mr checkout`

By default, you'll get the master branch of each git repo checked out
automatically and there will be 2 remotes setup:

1. The "upstream" remote
2. The Kibrarian Group remote
