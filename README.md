# Submodules (https://git-scm.com/book/en/v2/Git-Tools-Submodules)

## Creating

`git submodule add <git_url>`

## Cloning

`git clone …`

`git submodule init`
To initialize your local configuration file

`git submodule update`
To fetch all the data from that project and check out the appropriate commit listed in your super-project

OR

`git clone --recurse-submodules …`
This command will automatically initialize and update each submodule in the repository, including nested submodules if any of the submodules in the repository have submodules themselves.

OR (preferred)

`git submodule update --init --recursive`
To also initialize, fetch and checkout any nested submodules, you can use the foolproof command above.

## Pulling in Upstream Changes from the Submodule Remote

`git submodule update --remote`
Git will go into your submodules and fetch and update for you.

## Pulling Upstream Changes from the Project Remote

`git pull`
`git submodule update --init --recursive`

## Working with submodules

When work on sub is complete, from sub:
`git submodule update --remote --merge`

When all work is complete, from project root:
`git push --recurse-submodules=check`
