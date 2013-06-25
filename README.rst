Welcome to python-rex
=====================

Python REX is regular expressions for humans.

It is for the `re standard module<http://docs.python.org/2/library/index.html>`_ like
`requests<http://docs.python-requests.org/en/latest/>`_ is for `urllib module<http://docs.python.org/2/library/urllib.html>`_.

REX means also the King, and the King of regular expressions is Perl. So REX API tries to mimic at least some Perl's
idioms.

Quickstart
==========

Simply match any text::

    if 'This is a dog' == rex('/dog/'):
        print 'Oh yeah'


or::

    if 'My lucky 777 number' == rex('/[0-9]+/'):
        print 'Number found'


You can use Perl notation and prepend ``m`` character to your search::


    if 'My lucky 777 number' == rex('m/[0-9]+/'):
        print 'Number found'


And some substitutions::

    >>> print "This is a cat" == rex('s/CAT/dog/i')
    This is a dog
