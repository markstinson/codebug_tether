CodeBug Loader
==============
Can control a tethered CodeBug by sending GET/SET/BULK messages.

Also used to program a CodeBug with a user program generated by the website.

Depends on `python3-serial` (or `python-serial`).


CodeBug Loader RX (cblrx)
=========================
This is a test receiver for the CodeBug loader.

In terminal 1:

    $ cd cblrx
    $ make
    $ ./cblrx
    Fake CodeBug serial port is: /dev/pts/4

In terminal 2:

    $ python3
    >>> import serial
    >>> from codebug_loader.core import CodeBug
    >>>
    >>> cb = CodeBug(serial.Serial('/dev/pts/4'))
    >>>
    >>> cb.set(0, 0b10101)

Watch terminal 1 change.
