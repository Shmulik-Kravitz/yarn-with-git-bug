# Bug in "yarn workspaces" does not work nice with `git clean -xdf`

When runnig  `git clean -xdf` in a repo with yarn workspaces the contens of the workspaces are deleted.

## How to reproduce

 1. Clone the repo.
 2. Run `yarn`  in root folder or in one of the workspaces.
 3. Run `git clean -xdf` 

