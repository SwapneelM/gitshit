# Gitshit: A Lazy Approach to 'Git' Shit Done

* Gitshit is a library designed to make life easier when using basic git commands repetitively:

```
        git add <filename>
        git commit -m "Commit Message"
        git status
        git push origin <branch-name>
```

**can now be replaced by**

```
        gitshit done
```

_There are, of course, caveats to this oversimplification._

* Gitshit offers the option to combine all of this into a single command but additionally allows users to add the correspending command-line options for each of the parameters i.e. `<filename>`, `"Commit Message"`, and `<branch-name>`

## The complete set of use-cases for Gitshit are illustrated below

1. `gitshit done` : Uses default settings committing all files to the master branch with a pre-defined commit message `"Adding changes to file"`

_This was the primary reason behind the development of `gitshit`._

## Command-line Options

* `-f` or `--filename` is used to provide absolute or relative filepaths for committing individual files. The default setting for this option is to place all modified files in a single commit using `--all`.


* `-m` or `--commit-message` is used to add a custom message to the current commit. The default message is `"Adding changes to file"`.

* `-b` or `--branch-name` is used to commit to a custom branch. The default value for this option is `master`.

## Rolling back

* While laying out a design for gitshit, I realized that shit can go wrong when chaining together these commands so I plan to add a soft and hard rollback option using a wrapper for the `git reset` command.

_To be fair, I was originally going to make a new script called `shitgit` but I realized it was (probably) overkill (albeit funny). Maybe I'll do it anyway._

**Further development will mainly be motivated by the need to induce automation into my daily routine but I will most certainly attempt to publish scripts that help someone other than myself.**