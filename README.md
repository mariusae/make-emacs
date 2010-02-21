make-emacs
==========

`make-emacs` is a simple utility to create a self-contained,
relocatable script to invoke emacs with your own configuration and
intialization code. This is convenient for using emacs with your own
configuration on remote machines.

It works by creating a [shar archive][shar] of all of your
configuration, wrapped in some simple invocation code. `make-emacs`
also caches extracted configuration files.

        $ make-emacs ~/.emacs.d /tmp/e
        $ scp /tmp/e remoteserver:
        $ ssh remoteserver
        $ ./e
        extracting emacs.d..
        <bliss>

[shar]: http://en.wikipedia.org/wiki/Shar
