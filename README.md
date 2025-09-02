# Command Line Tips & Tricks

This is a collection of tools and settings I've found helpful for making the
command line more comfortable and convenient.

⭐ is what I use.


## Shell

Get a modern shell. Compared to sh and Bash, they usually have a syntax that's
simpler, more consistent, and more predictable. Many also have convenience
features like fuzzy tab completion and shared history.

You might occasionally hear people say it's important to use sh (or Bash) for
compatibility across a computers. That's sometimes true for scripts you plan to
distribute widely. But you can write and run sh (and Bash) scripts as needed
with the `sh` and `bash` commands even if your day-to-day shell is something
else.

Two modern shells are especially popular because they're easy to learn if you
already know Bash:

* ⭐[fish][] is a shell designed to be more user-friendly than Bash. The syntax
  is more like a modern programming language and removes many of the pitfalls
  of Bash while still feeling familiar. It comes with helpful defaults.
* [zsh][] is the default shell on macOS. The syntax is nearly the same as Bash,
  so there are only minor improvements there, but it has many other features
  and is highly customizable. The default configuration is not especially
  helpful and configuring zsh has a reputation for being time-consuming. You
  can spend time learning to configure it, or use [oh-my-zsh][omz] as a
  starting point.

[fish]: https://fishshell.com/
[zsh]: https://www.zsh.org/
[omz]: https://ohmyz.sh/

There are also several shells that are substantially different from Bash. These
might take longer to get used to if you decide to switch. Here are a few:

* [xonsh][] is a Python shell. The syntax is Python with a few additions to
  make interactive use as a shell more convenient.
* [nushell][] is a shell designed around safely passing data between commands.

[xonsh]: https://xon.sh/
[nushell]: https://www.nushell.sh/


## Text Editor

Get a command line text editor you like. Even if you do most editing in a
graphical text editor or integrated development environment, it's good to have
a familiar tool for when you can't work graphically and as a backup.

Here are a few editors (but there are many more):

* ⭐[NeoVim][] or [Vim][] are modernized versions of `vi` (although Vim is also
  quite old). Both use a modal editing model that takes some time to learn.
  NeoVim improves on Vim by providing helpful defaults, providing built-in
  support for the language server protocol, using the [Lua][] language for
  configuration and plugins, and more.
* [Emacs][] is quite old but extremely popular. Its main feature is that it
  uses the [Lisp][] language for configuration and plugins, and there are many
  mature, stable plugins available.
* [helix][] is inspired by NeoVim (and Kakoune), but has many distinct design
  choices. It's intended as a "batteries included" editor that has many
  features and requires minimal configuration.
* [micro][] is a modernized `nano`. It's easy to install and start using, has
  built-in syntax highlighting, and can be customized.

[NeoVim]: https://neovim.io/
[Vim]: https://www.vim.org/
[Lua]: https://lua.org/
[Emacs]: https://www.gnu.org/software/emacs/
[Lisp]: https://en.wikipedia.org/wiki/Lisp_(programming_language)
[helix]: https://helix-editor.com/
[micro]: https://micro-editor.github.io/


## Terminal Multiplexer

Get a terminal multiplexer, a kind of session manager for the terminal. With a
terminal multiplexer, you can run multiple programs simultaneously and
side-by-side in one terminal, detach to run things in the background, and won't
lose anything if you accidentally close the terminal.

There are two popular options:

* ⭐[tmux][] is newer than Screen. It provides a user interface to help you
  understand its status and what programs are running. It also provides shell
  commands so that you can control it from any terminal (not just ones where
  it's open).
* [Screen][]

[tmux]: https://github.com/tmux/tmux/wiki
[Screen]: https://www.gnu.org/software/screen/

Some terminals provide a built-in terminal multiplexer, in which case a
separate terminal multiplexer is not necessary.


## Other Stuff

I use all of these so imagine a ⭐ next to all of them.

### Essential Shell Tools

* [zoxide][]: replaces `cd`. You can "jump" to directories you use frequently
  without typing the entire path.
* [atuin][]: stores your shell command history in a database, with optional
  support for syncing across multiple machines.
* [starship][]: replaces the shell prompt. Provides customizable status
  information for many different kinds of projects (such as Git repos and
  specific programming languages).

[zoxide]: https://github.com/ajeetdsouza/zoxide
[atuin]: https://github.com/atuinsh/atuin
[starship]: https://starship.rs/


### Helpful Shell Tools

* [bat][]: replaces `cat`. Provides syntax highlighting and is Git-aware. Can
  do neat things like provide syntax highlighting for `man` pages.
* [eza][]: replaces `ls`. Helpful defaults, better color support, icon support
  (with appropriate fonts installed), Git support, and more.
* [fd][]: replaces `find` (find files by name). Sensible interface and
  defaults.
* [fzf][]: a fuzzy finder, meaning it displays an interface for selecting items
  from a list and supports fuzzy text matching to select them. On its own, you
  can use it to select files in a directory tree, but it's especially useful in
  conjunction with other tools that produce or ask you to select from lists.
* [ouch][]: replaces `tar`, `zip`/`unzip`, and more.
* [ripgrep][] replaces `grep` (search for patterns within files). Faster, has
  sensible defaults, and has more features.
* [sd][]: replaces `sed` (replace patterns within files). Uses regular
  expressions rather than yet another language to learn.

[bat]: https://github.com/sharkdp/bat
[eza]: https://github.com/eza-community/eza
[fd]: https://github.com/sharkdp/fd
[fzf]: https://junegunn.github.io/fzf/
[ouch]: https://github.com/ouch-org/ouch
[ripgrep]: https://github.com/BurntSushi/ripgrep
[sd]: https://github.com/chmln/sd


### Terminals

Choosing a different terminal is not critical, but can be nice for customizing
keyboard shortcuts and aesthetics (like font size and colors). I'm a fan of
[WezTerm][], which is cross-platform and uses Lua for customization.

[WezTerm]: https://wezterm.org/


### Aesthetics

* Find a monospace font you like. You can try out more than 150 fonts at
  [Programming Fonts][pfonts]. If it's hard to choose, you can select a
  favorite font tournament-style at [Coding Font][cfont].

  The [Nerd Fonts][] project patches fonts to include many useful symbols, so
  the supported fonts are a good choice. If you frequently use non-Latin
  characters, the [Noto font family][noto] may cover more languages than any
  other family, and includes a monospace font.

* [tinted-theming][] is a huge collection of color schemes for shells, text
  editors, and more. They also provide a tool, Tinty, to switch the color
  schemes for all of your shell tools with a single command.

[pfonts]: https://www.programmingfonts.org/
[cfont]: https://www.codingfont.com/
[Nerd Fonts]: https://www.nerdfonts.com/
[noto]: https://en.wikipedia.org/wiki/Noto_fonts
[tinted-theming]: https://github.com/tinted-theming


## Installation

Always check each tool's individual installation instructions. You can install
many of these tools with [Pixi][] (all platforms), even on computers where you
aren't an administrator. For Linux, tools that aren't on conda-forge (such as
NeoVim) are sometimes available as a portable AppImage that you can simply
download and run.

[Pixi]: https://pixi.sh/

On computers where you are an administrator, it might be preferable to use the
built-in package manager. On macOS, [Homebrew][] is a good option. On Windows,
the situation is more difficult and the best solution is probably to use the
[Windows Subsystem for Linux][wsl]. That said, [MSYS2][] and [Scoop][] are
potentially helpful package managers for Windows.

[wsl]: https://learn.microsoft.com/en-us/windows/wsl/install
[Homebrew]: https://brew.sh/
[MSYS2]: https://www.msys2.org/
[Scoop]: https://scoop.sh/


## To Learn More

I also have many helpful aliases in [my dotfiles][dotfiles] (specifically, take
a look at `.bashrc`).

[dotfiles]: https://github.com/nick-ulle/dotfiles/
