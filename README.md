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

## Changes needed in KiCad

The way that the footprints work today is that they reference their 3D model's
path via the KISYS3DMOD variable which is a "global" variable (technically it's
stored in the user's `~/.config/` directory).  Unfortunately this means that
there can only be one location which KiCad will look for 3D models regardless of
which project you're working in (this is in contrast to how symbols and
footprints have both a global and local per-project list of libraries).

To deal with this, be sure to set your KiCad KISYS3DMOD variable to point to the
`./kicad-packages3D/` directory after you clone this top level repo and use myrepos
to checkout the sub-repos.
