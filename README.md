delsel-mode for zsh
===================

Synopsis
--------

* delsel-mode - zle tweak to delete an active region just by hitting a key

Description
-----------

This mode makes an active region work much like a text selection in
typical GUI.  You can delete the selected text just by hitting a
delete key, or overwrite it by typing text or yanking.

How to set up
-------------

Put the file `delsel-mode` somewhere in your `$fpath` and add these
lines to your `.zshrc`:

```shell
autoload -Uz delsel-mode
delsel-mode
```

If you are enabling `url-quote-magic`, make sure to load it first and
then load `delsel-mode`.

Configuration
-------------

By default, an active region is deleted or replaced by invoking the
following commands:

- `self-insert`
- `delete-char`
- `backward-delete-char`
- `yank`

To add more commands, call `delsel-mode.wrap-command` like so:

```shell
delsel-mode.wrap-command your-insert-command
delsel-mode.wrap-command your-delete-command
```

License
-------

Copyright (c) 2019 Akinori MUSHA

Licensed under the 2-clause BSD license.
See `LICENSE` for details.
