Advertising & Discovering Network Services
==========================================

..  automodule:: networkzero.discovery
    :synopsis: Network discovery
    :show-inheritance:
..  moduleauthor:: Tim Golden <mail@timgolden.me.uk>


Introduction
------------

The discovery module implements a UDP beacon in a daemon thread to advertise 
a directory of name-to-address mappings. The names are added to the directory via the
:func:`advertise` function, and discovered via :func:`discover`. A list of all
currently-advertised names can be obtained by calling :func:`discover_all`.

To simplify things: when a name is advertised, if no address is supplied, one
is generated by combining the first of the host's IP addresses with a port
randomly selected from the list of valid dynamic ports [0xC000 - 0xFFFF].
While the selected port is removed from the list for the purposes of the
networkzero package, there's a slim chance that it might be in use by some 
other process.

Functions
---------

..  autofunction:: advertise
..  autofunction:: discover
..  autofunction:: discover_all
