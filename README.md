# Template Config for git

The data in 'template' will be placed inside '.git' when running `git init`.
NOTE: the actual hook scripts are in the folder 'scripts', while the template directory only contains symlinks.
This is done so that repositories always use the latest version of the scripts.

Note: templates work because ~/.gitconfig has the following:

```
[init]
    templateDir = ~/git/template


```

## How to install

1. Clone this repostory
2. Tell git where to look for git hooks: `git config --global core.hooksPath /path/to/this/repo/scripts`
3. Git will now automatically run this hook and then look for `.git-pre-commit` files in a project for project specific hooks.

