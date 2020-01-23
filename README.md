OMZ Homebrew
============

Description
-----------

An alternative polugin for [Oh My Zsh][0] offering several aliases for common [brew][1] commands. While there is an existing `brew` plugin, its provided aliases don't match my needs. This plugin does not conflict with the official one, and both can be used side-by-side.

Aliases
-------

| Alias | Command                                                                                                       | Description                                                                                                        |
|-------|---------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------|
| bl    | `echo "Formulae\n========" && brew list -1 && echo "\nCasks\n=====" && brew cask list -1`                    | List installed forumulae and casks                                                                                 |
| bi    | `brew install`                                                                                                | Install a forumula                                                                                                 |
| bci   | `brew cask install`                                                                                           | Install a cask                                                                                                     |
| bup   | `brew update && echo "\nFormulae\n========" && brew outdated && echo "\nCasks\n=====" && brew cask outdated` | Fetch the latest version of Homebrew, then list outdated formulae and casks                                        |
| bug   | `brew upgrade && brew cask upgrade && brew cleanup`                                                           | Upgrade outdated (and unpinned) forumlae and casks, then removes stale lockfiles, outdated downloads, and versions |
| buddy | `brew upgrade --dry-run && brew cask upgrade --dry-run`                                                       | List the packages that would be updated by `bug`                                                                   |

Installation
------------

1. Clone this repository into `$ZSH_CUSTOM/plugins` (by default `~/.oh-my-zsh/custom/plugins`)

    ```sh
    git clone https://github.com/digitalraven/omz-homebrew ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/omz-homebrew
    ```

2. Add the plugin to the list of plugins for Oh My Zsh to load (inside `~/.zshrc`):

    ```sh
    plugins=(... omz-homebrew)
    ```

3. Re-source your `~/.zshrc`

    ```sh
    source ~/.zshrc
    ```

4. There is no step 4.

[0]: https://ohmyz.sh
[1]: https://brew.sh
