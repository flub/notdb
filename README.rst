============================
Pythonic libnotmuch bindings
============================

This package contains Python bindings for the notmuch_ library.  These
bindings are built with CFFI_ so that they are performant on both
CPython_ and PyPy_.  But most importantly these bindings are doing
**correct memory management** of libnotmuch and using the high-level
API it should not be possible to crash the Python interpreter.  In
contrast the currently bundled Python bindings accompanying libnotmuch
is both slow on PyPy_ and can fairly easily result in SIGSEGV for the
Python interpreter, unless the notmuch memory model is carefully
understood and catered for.

.. _notmuch: https://notmuchmail.org
.. _CFFI: https://cffi.readthedocs.io
.. _CPython: https://www.python.org
.. _PyPy: http://pypy.org
