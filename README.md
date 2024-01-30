## Instalattion

- copy `featureup` file from this repository to any location in your `$PATH` (eg `/usr/bin/local/featureup`)
- make it executable `chmod +x /usr/bin/local/featureup`

## Requirements
- `git` and `gh` (GitHub CLI) must be installed

## Usage

Suppose from `develop` branch you created feature branch called `our-new-feature`.
Then from `our-new-feature` developers created their sub-branches and created PR for them (they can be drafts)

Then:
- navigate to your repository directory
- run `featureup our-new-feature`

This will:
- update your local `develop` to be in sync with `develop` in remote repository
- update your local `our-new-feature` branch to be in sync with remote
- merge `develop` in `our-new-feature` and push
- get the list of all sub-branches
- for each sub-branch, it will merge `our-new-feature` into them and push

If any error happen (command execution fails, merge impossible due to conflicts) script will terminate with code `1` and print the info about the termination reason.
