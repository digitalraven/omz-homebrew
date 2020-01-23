OMZ Homebrew
============

Description
-----------

An alternative polugin for [Oh My Zsh][0] offering several aliases for common [brew][1] commands. While there is an existing `brew` plugin, its provided aliases don't match my needs. This plugin does not conflict with the official one, and both can be used side-by-side.

Aliases
-------

| Alias | Command                                                                                                       | Description                                                                                                        |
|-------|---------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------|
| bl    | `echo "Forumulae\n========" && brew list -1 && echo "\nCasks\n=====" && brew cask list -1`                    | List installed forumulae and casks                                                                                 |
| bi    | `brew install`                                                                                                | Install a forumula                                                                                                 |
| bci   | `brew cask install`                                                                                           | Install a cask                                                                                                     |
| bup   | `brew update && echo "\nForumulae\n========" && brew outdated && echo "\nCasks\n=====" && brew cask outdated` | Fetch the latest version of Homebrew, then list outdated formulae and casks                                        |
| bug   | `brew upgrade && brew cask upgrade && brew cleanup`                                                           | Upgrade outdated (and unpinned) forumlae and casks, then removes stale lockfiles, outdated downloads, and versions |
| buddy | `brew upgrade --dry-run && brew cask upgrade --dry-run`                                                       | List the packages that would be updated by `bug`                                                                   |


[0]: https://ohmyz.sh
[1]: https://brew.sh
