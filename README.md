Atom Settings
=============

Contains all my personal settings for the [Atom](http://atom.io) editor.

Installation
------------

```
$ cd ~
$ git clone git@github.com:<account>/atom-settings.git .atom
```

Since these are my setting, I recommend that you fork the repo into your own account and `git clone` from your version instead of mine.

Packages
--------

Instead of checking in packages which are maintained elsewhere, here is the list of installed packages:

1. atom-monokai-dark
1. atom-ungit
1. color-picker
1. extract-method
1. git-plus
1. go-plus
1. highlight-selected
1. language-ini
1. language-rabl
1. minimap
1. minimap-git-diff
1. minimap-highlight-selected
1. monokai
1. monokai-dark
1. monokai-extended
1. Quippet
1. rspec
1. Sublime-Style-Column-Selection
1. symbol-gen
1. symbols-view
1. tabularize
1. Zen

On mac `shift + cmd + p` and type `install packages`.  Then type the package name.  Click install next to the package name when it comes up.  You can install all packages before you restart atom.

CTags
-----

The `symbol-gen` and `symbols-view` packages are great for jumping specifically to functions, but they don't work for every language.  The following are the CTAG finders that I added.

```
--langdef=Go
--langmap=Go:.go
--regex-Go=/func([ \t]+\([^)]+\))?[ \t]+([a-zA-Z0-9_]+)/\2/d,func/
--regex-Go=/var[ \t]+([a-zA-Z_][a-zA-Z0-9_]+)/\1/d,var/
--regex-Go=/type[ \t]+([a-zA-Z_][a-zA-Z0-9_]+)/\1/d,type/
```

Add the above to `~/.ctags` then regenerate the symbols and the new patterns will be indexed.

Ungit
-----

[Ungit](https://github.com/FredrikNoren/ungit) is Git GUI written in node.  It will show up directly in atom if it is installed and you have the `atom-ungit` plugin.
