# Tracked file are being deleted when running "git clean -xdf" in "yarn workspaces"

When running `git clean -xdf` in a repo with yarn workspaces, the contents of the workspaces are deleted.

Consider this folder structure:

 - workspace1
   - **index.js**
   - **package.json**
 - workspace2
   - **index.js**
   - **package.json**
 - .gitignore
 - README.md
 - package.json
 - yarn.lock

After running git clean -xfd the files in bold (tracked source controlled files) are deleted! Even though clean shouldn't have impacted tracked files at all.

I believe yarn workspaces bug. I've opened an issue @yarn:
https://github.com/yarnpkg/yarn/issues/7536

## How to reproduce

 1. Clone the repo.
 2. Run `yarn`  in the root folder or in one of the workspaces.
 3. Run `git clean -xdf` 
 
 The contents of the workspaces are deleted.
