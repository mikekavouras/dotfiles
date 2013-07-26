# mikekavouras does dotfiles

## dotfiles

Your dotfiles are how you personalize your system. These are mine.

This repository was forked from [Zach Holman's](http://github.com/holman) excellent
[dotfiles](http://github.com/holman/dotfiles) but I tailored it to my system
and to bash over zsh.

## install

Run this:

```sh
git clone https://github.com/mikekavouras/dotfiles.git ~/.dotfiles
cd ~/.dotfiles
script/bootstrap
```

If you don't have git installed, run this:

```sh
curl -fsSL https://raw.github.com/mikekavouras/dotfiles/master/script/bootstrap | sh
```

This will symlink the appropriate files in `.dotfiles` to your home directory.
Everything is configured and tweaked within `~/.dotfiles`.

`dot` is a simple script that installs some dependencies, sets sane OS X
defaults, and so on. Tweak this script, and occasionally run `dot` from
time to time to keep your environment fresh and up-to-date. You can find
this script in `bin/`.

## topical

Everything's built around topic areas. If you're adding a new area to your
forked dotfiles — say, "Java" — you can simply add a `java` directory and put
files in there. Anything with an extension of `.zsh` will get automatically
included into your shell. Anything with an extension of `.symlink` will get
symlinked without extension into `$HOME` when you run `script/bootstrap`.

## what's inside

A lot of stuff. Seriously, a lot of stuff. Check them out in the file browser
above and see what components may mesh up with you. Fork it, remove what you
don't use, and build on what you do use.

## components

There's a few special files in the hierarchy.

- **bin/**: Anything in `bin/` will get added to your `$PATH` and be made
  available everywhere.
- **topic/\*.symlink**: Any files ending in `*.symlink` get symlinked into
  your `$HOME`. This is so you can keep all of those versioned in your dotfiles
  but still keep those autoloaded files in your home directory. These get
  symlinked in when you run `script/bootstrap`.

* Unlike Zach's original, *.zsh is not added to your environment.

## bugs

I want this to work for everyone; that means when you clone it down it should
work for you even though you may not have `rbenv` installed, for example. That
said, I do use this as *my* dotfiles, so there's a good chance I may break
something if I forget to make a check for a dependency.

If you're brand-new to the project and run into any blockers, please
[open an issue](https://github.com/mikekavouras/dotfiles/issues) on this repository
and I'd love to get it fixed for you!

## thanks

This repository comes from:

- [Zach Holman's](http://github.com/holman) excellent[dotfiles](http://github.com/holman/dotfiles)
- [Ryan Bates](http://github.com/ryanb)' excellent [dotfiles](http://github.com/ryanb/dotfiles)

A decent amount of the code in these dotfiles stem or are inspired from Zach's or Ryan's original projects.
