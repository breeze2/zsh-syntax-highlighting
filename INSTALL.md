How to install
--------------

### Using packages

* Arch Linux: [community/zsh-syntax-highlighting][arch-package] / [AUR/zsh-syntax-highlighting-git][AUR-package]
* Debian: `zsh-syntax-highlighting` package [in `stretch`][debian-package]
* Fedora: [zsh-syntax-highlighting package][fedora-package] in Fedora 24+
* FreeBSD: `pkg install zsh-syntax-highlighting` (port name: [`textproc/zsh-syntax-highlighting`][freebsd-port])
* Gentoo: [mv overlay][gentoo-overlay]
* Mac OS X / Homebrew: [brew install zsh-syntax-highlighting][brew-package]
* Ubuntu: `zsh-syntax-highlighting` package [in Xenial][ubuntu-package]

[arch-package]: https://www.archlinux.org/packages/zsh-syntax-highlighting
[AUR-package]: https://aur.archlinux.org/packages/zsh-syntax-highlighting-git
[debian-package]: https://packages.debian.org/zsh-syntax-highlighting
[freebsd-port]: http://www.freshports.org/textproc/zsh-syntax-highlighting/
[gentoo-overlay]: http://gpo.zugaina.org/app-shells/zsh-syntax-highlighting
[brew-package]: https://github.com/Homebrew/homebrew-core/blob/master/Formula/zsh-syntax-highlighting.rb
[ubuntu-package]: https://launchpad.net/ubuntu/+source/zsh-syntax-highlighting
[fedora-package]: https://apps.fedoraproject.org/packages/zsh-syntax-highlighting


### In your ~/.zshrc

Simply clone this repository and source the script:

        git clone https://github.com/zsh-users/zsh-syntax-highlighting.git
        echo "source ${(q-)PWD}/zsh-syntax-highlighting/zsh-syntax-highlighting.zsh" >> ${ZDOTDIR:-$HOME}/.zshrc

  Then, enable syntax highlighting in the current interactive shell:

        source ./zsh-syntax-highlighting/zsh-syntax-highlighting.zsh

  If `git` is not installed, download and extract a snapshot of the latest
  development tree from:

        https://github.com/zsh-users/zsh-syntax-highlighting/archive/master.tar.gz

  Note the `source` command must be **at the end** of `~/.zshrc`.


### With a plugin manager

Note that `zsh-syntax-highlighting` must be the last plugin sourced.

The zsh-syntax-highlighting authors recommend manual installation over the use
of a framework or plugin manager.

This list is incomplete as there are too many [frameworks / plugin managers]
(https://github.com/unixorn/awesome-zsh-plugins#frameworks) to list them all
here.

#### [Antigen](https://github.com/zsh-users/antigen)

Add `antigen bundle zsh-users/zsh-syntax-highlighting` as the last bundle in
your `.zshrc`.

#### [Oh-my-zsh](https://github.com/robbyrussell/oh-my-zsh)

1. Clone this repository in oh-my-zsh's plugins directory:

        git clone https://github.com/zsh-users/zsh-syntax-highlighting.git ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-syntax-highlighting

2. Activate the plugin in `~/.zshrc`:

        plugins=( [plugins...] zsh-syntax-highlighting)

3. Source `~/.zshrc`  to take changes into account:

        source ~/.zshrc

#### [Prezto](https://github.com/sorin-ionescu/prezto)

Zsh-syntax-highlighting is included with Prezto. See the [Prezto documentation]
(https://github.com/sorin-ionescu/prezto/tree/master/modules/syntax-highlighting)
to enable and configure highlighters.

#### [zgen](https://github.com/tarjoilija/zgen)

Add `zgen load zsh-users/zsh-syntax-highlighting` to the end of your `.zshrc`.

#### [zplug](https://github.com/zplug/zplug)

Add `zplug "zsh-users/zsh-syntax-highlighting", nice:10` to your `.zshrc`.

#### [zplugin](https://github.com/psprint/zplugin)

Add `zplugin load zsh-users/zsh-syntax-highlighting` to the end of your
`.zshrc`.


### System-wide installation

Any of the above methods is suitable for a single-user installation,
which requires no special privileges.  If, however, you desire to install
zsh-syntax-highlighting system-wide, you may do so by running

    make install

and directing your users to add

    source /usr/local/share/zsh-syntax-highlighting/zsh-syntax-highlighting.zsh

to their `.zshrc`s.
