NOTES ON TMUX LEARNING
======================

These note are taken from the reading of the book: *Tmux 2 Productive Mouse Free Development* which is edited by Pragmatic Bookshelf

Installation (Linux)
--------------------

Install the dependencies (Debian/Ubuntu like):

`$ sudo apt install build-essential libevent-dev libncurses-dev`

If you want the version from your package manager:

`$ sudo apt install tmux`

If you want the latest stable version (from the directory of your choice):

Download (`$ sudo apt install wget` if not on your system):

`$ wget https://github.com/tmux/tmux/releases/download/{STABLE-VERSION-NUMBER}/tmux-{STABLE-VERSION-NUMBER}.tar.gz`

Configure and compile:

```
$ cd tmux-{STABLE-VERSION-NUMBER}
$ ./configure && make
$ sudo make install
```

Starting / Stopping Tmux
------------------------

To start tmux: `$ tmux`

To exit tmux, you can type `$ exit` just like a normal terminal.

Inside a tmux terminal all the command are prefixed by `Ctrl + b`

Example: `Ctrl + b` and `t` display a clock.
