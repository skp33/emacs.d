## Installation

**General**
`git clone git@github.com:munen/emacs.d.git ~/.emacs.d`

**Dependencies**
Emacs dependencies/libraries are managed via the internal
[package management system](https://www.gnu.org/software/emacs/manual/html_node/emacs/Packages.html#Packages). To
initially install packages, open `~/.emacs.d/init.el`, refresh your
package list with `M-x package-refresh-contents` and install
everything using `M-x eval-buffer`.

## orgmode
### Pomodoro
A leightweight implementation of the Pomodoro Technique is
implemented in customizing orgmode in `init.el`. For every Clock that
is started (`C-c C-x C-i`) an automatic Timer is scheduled to
25min. After these 25min are up, a "Time to take a break!" message is
played and a pop-up notification is shown.

The timer is not automatically stopped on clocking out, because
clocking in should still work on new tasks without resetting the
Pomodoro.

The timer can manyally be stopped with `M-x org-timer-stop`.

A break can be started with `M-x pomodoro-break`. A pomodoro can also
manually be started without clocking in via `M-x pomodoro-start`.

## Clojure

### Cider
https://github.com/clojure-emacs/cider

* `M-x cider-jack-in` To start REPL
* `C-c C-k` Evaluate current buffer
* `C-c M-n` Change ns in cider-nrepl to current ns
* `C-c C-d C-d` Display documentation for the symbol under point
* `C-c C-d C-a` Apropos search for arbitrary text across function names and documentation

** CIDER REPL Key Bindings **

* `C-↑, C-↓` Cycle through REPL history.

More Cider shortcuts [here](https://github.com/clojure-emacs/cider#cider-mode).

### Impatient Mode - Live Coding Emacs/Browser

https://github.com/netguy204/imp.el

Enable the web server provided by simple-httpd:

    M-x httpd-start

Publish buffers by enabling the minor mode impatient-mode.

    M-x impatient-mode

And then point your browser to http://localhost:8080/imp/, select a buffer, and watch your changes appear as you type!

