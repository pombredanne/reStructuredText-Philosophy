Guide to reST
=============

reST is white space sensitive.
------------------------------

    * Like python, a lot of the structure of the text comes from indention.
    * A lot of things (code blocks) require whitespace before and after.

reST groups strings together with `````'s.
------------------------------------------

reST uses ``..`` as the means to call a function
-------------------------------------------------

    * So most of the time you want to get data into reST, 
      or make something happen, you use ``..``

reST uses ``::`` in the main text to to break function names from arguments.
----------------------------------------------------------------------------
    * This is done because comments are likely to have a : in them.
    * For example::

        .. note:: This is a sweet note.
                  The whitespace here matters.

reST uses ``:<ref>:```` to reference things
----------------------------------------------------------------------------
    * This allows you to link to other parts of your document, and even other sphinx projects with :ref:`.
    * For example::
        
        You might look at the :doc:`getting-started` document for more information.
        You can call :func:`get_all_objects` to get all of the objects.


.. _rest-link-underscores:

reST links to things with ``_``
-------------------------------

    * This means hyperlinks in the main body of text end in _
    * Single word hyperlinks can just be that::
        
        Look at the Python_ source.

    * Multiple word hyperlinks must be joined with `````'s::

        Look in the `Django Documentation`_.
    
    * At the bottom of the page or paragraph, use the `..` syntax to match the links together::

        .. _Django Documentation: http://docs.djangoproject.com

.. note:: The hyperlink section with the actual URL only has one :, because it is seperate
          from the main body of the text, as noted above


