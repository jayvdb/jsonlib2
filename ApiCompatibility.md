# Introduction #

jsonlib2 is almost a drop-in replacement for simplejson - at least that's how we use it at [Freebase](http://www.freebase.com/). We use the more common features, and this library does its best to support a few more.

# Supported API #

## dump/dumps ##

  * ensure\_ascii
  * allow\_nan
  * indent
  * separators
  * default

## load/loads ##

  * parse\_float
  * parse\_int
  * parse\_constant

# API differences #

a few keywords are not supported, but more importantly, jsonlib2 tends to output 8-bit strings so that they can be dumped directly through HTTP rather than make a 2nd conversion back

## dump/dumps ##
  * skipkeys - probably quite easy to implement
  * check\_circular - probably quite easy to implement
  * cls - really might not be possible, due to C implementation
  * encoding - may be a big pain in the neck, because much of the code makes a lot of UTF8 assumptions.

## load/loads ##

  * encoding - again, might be a pain in the neck
  * cls - again, might not be possible due to C implementation
  * object\_hook - probably quite easy to implement