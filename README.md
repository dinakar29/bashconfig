# Bash-it personalization

## Installation

1. Check out a clone of this repo to a location of your choice, such as
   `git clone --depth=1 https://github.com/dinakar29/bashconfig.git ~/.bash_it`
2. Run `~/.bash_it/install.sh` (it automatically backs up your `~/.bash_profile` or `~/.bashrc`, depending on your OS)
3. Edit your modified config (`~/.bash_profile` or `~/.bashrc`) file in order to customize Bash-it.
4. Check out available aliases, completions, and plugins and enable the ones you want to use (see the next section for more details).

### Install Options

The install script can take the following options:

* `--interactive`: Asks the user which aliases, completions and plugins to enable.
* `--silent`: Ask nothing and install using default settings.
* `--no-modify-config`: Do not modify the existing config file (`~/.bash_profile` or `~/.bashrc`).

When run without the `--interactive` switch, Bash-it only enables a sane default set of functionality to keep your shell clean and to avoid issues with missing dependencies.
Feel free to enable the tools you want to use after the installation.

When you run without the `--no-modify-config` switch, the Bash-it installer automatically modifies/replaces your existing config file.
Use the `--no-modify-config` switch to avoid unwanted modifications, e.g. if your Bash config file already contains the code that loads Bash-it.

**NOTE**: Keep in mind how Bash load its configuration files,
`.bash_profile` for login shells (and in macOS in terminal emulators like [Terminal.app](http://www.apple.com/osx/apps/) or
[iTerm2](https://www.iterm2.com/)) and `.bashrc` for interactive shells (default mode in most of the GNU/Linux terminal emulators),
to ensure that Bash-it is loaded correctly.
A good "practice" is sourcing `.bashrc` into `.bash_profile` to keep things working in all the scenarios.
To achieve this, you can add this snippet in your `.bash_profile`:

```
if [ -f ~/.bashrc ]; then
  . ~/.bashrc
fi
```
