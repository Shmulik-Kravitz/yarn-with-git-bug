# Bug in "yarn workspaces" does not play nice with `git clean -xdf`

When running  `git clean -xdf` in a repo with yarn workspaces the contents of the workspaces are deleted.

## How to reproduce

 1. Clone the repo.
 2. Run `yarn`  in the root folder or in one of the workspaces.
 3. Run `git clean -xdf` 

