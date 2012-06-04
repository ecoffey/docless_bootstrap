Why?
=================

Testing to see if it's feasible to trim down a repo with the goal of submoduling.

How?
=================

`git clone https://github.com/twitter/bootstrap.git`
`rm -rf <directories and files you don't care about>`
`git commit -am 'Trimming things out'`

On github: create an empty repo, say docless_bootstrap

`git remote add docless <r+w url>`
`git push docless master`

Now the docless repo can be submoduled into another project:

`git submodule add <docless_url> <local_path`

(Further reading: [http://git-scm.com/book/en/Git-Tools-Submodules](http://git-scm.com/book/en/Git-Tools-Submodules))
