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


Sessions
--------


### List alive sessions

A session is quite like a new tab in your teminal but the advantage of tmux is 
that it lets you switch between session without much effort.

To list your available sessions:
`$ tmux list-sessions` or simply `$ tmux ls`

If no session is already present you will see a message signaling that no alive session is available to attach.


### Create a new session

You can create a new session by typing:

`$ tmux new -s <my-new-session-name>` 

if you want to create it without entering it:

`$ tmux new -s <my-new-session-name> -d` ( -d i.e in detached mode )


### Attach to session

By typing `$ tmux attach` you will attach to the last session created ( see tmux ls ).

You can specify the session you want to attach to with a target option:

`$ tmux attach -t <target-session-name>`


### Detach from session

Hit `Ctrl + d`


### Killing session

Killing session follow the same basic principle that creating it.
If you have just one session as you will be killing it else you may target the session you want to kill.

`$ tmux kill-session [-t <target-session>]`


Windows
-------

### The basic

Windows are kind of tab that help you organise your work in the same session.

To open a new window: `Ctrl + b` and `c`

To close a window your on: `Ctrl + b` and `&` or simply type `exit` in the window.

To navigate between your windows: `Ctrl + b` and `n` (next) `p` (previous).

Find window: `Ctrl + b` and `f` and then type text you are searching for.

To display a menu with available windows: `Ctrl + b` and `w`

To rename a window: `Ctrl + b` and then `,`
























