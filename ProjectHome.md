jsonlib2 is a JSON encoder and decoder for python, written in C. It is between 5x and 20x faster than [simplejson](http://pypi.python.org/pypi/simplejson/) for both encoding and decoding.

It is (as of version 1.5) almost completely API-compatible with [simplejson](http://pypi.python.org/pypi/simplejson/), which is included as the [json](http://docs.python.org/library/json.html) module in Python 2.6.

This is a fork of https://launchpad.net/jsonlib - jsonlib was forked because freebase.com was interested in the lenient-parsing of simplejson, with the performance of C.

Happily accepting packages from folks who know the C-Python API better than me... this code needs lots of cleanup!

Version 1.5.2 was released in December, 2009, and fixes a reference-counting error that cause jsonlib2 to crash when using the separators= parameter.

For details about API compatibility with simplejson/json, see [ApiCompatibility](ApiCompatibility.md)