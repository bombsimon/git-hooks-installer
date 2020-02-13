# Git Hooks Installer

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

Make it easy to install git hooks to your project. After the initial setup is
ran by you, others contributing to the project can install the same hooks
locally by executing `install-hooks`.

## What are Git hooks?

Git hooks are scripts that Git executes before or after events such as: commit,
push, and receive. Git hooks are a built-in feature - no need to download
anything. Git hooks are run locally.

You can read more about git hooks at [githooks.com](https://githooks.com).

## Usage

Ensure that this directory is in your path (and that the script dir is in the
same directory as `git-hooks-installer`. Or just reference the full path:

```sh
$ git clone git@github.com:bombsimon/git-hooks-installer.git ~/git/`

$ ~/git/git-hooks-installer/git-hooks-installer --help
git-hooks-installer - Install git hooks wrapper in your project!

Usage: git-hooks-installer [-f|--force] [-i|--install-path <project>] [project]

  -h|--help         : Print this help text
  -f|--force        : Don't prompt for yes/no questions, assume yes
  -i|--install-path : The path to install in (defaults to pwd)
  -s|--script-dir   : The name of the directory to use for scripts

$ ~/git/git-hooks-installer/git-hooks-installer /path/to/my/git-project
```

### With Git

Since `git` will call executables prefixed with `git-` in your path you can use
this as a git command if you're located in the root of a git repository.

```sh
$ export="$PATH:/path/to/git-hooks-installer"
$ cd /path/to/my/git-project
$ git hooks-installer
```

## Examples

There's an [example](example-hooks/) folder with example hooks. Feel free to use
and/or add new hooks which might be useful.

An example hook will be be added to your project which you may remove. To
install all the hooks, execute the install script with `script/install-hooks`
(or the relevant path if you set a custom script directory).
