Rst Examples
===============================
Add your content using ``reStructuredText`` syntax. See the
`reStructuredText <https://www.sphinx-doc.org/en/master/usage/restructuredtext/index.html>`_
documentation for details.

.. note::
   This is the content of your note. It should be indented
   to be part of the note block.

.. warning::
   This is the content of your warning. It should be indented
   to be part of the warning block.

.. tip::
   This is the content of your tip. It should be indented
   to be part of the tip block.

.. seealso::
   
   This is the content of the "See also" block.
   
   You would typically put links to other parts of
   your documentation or external resources here.

   :doc:`noteBlocks`

+-------+-------+-------------+
| item  | path  | test result |
+=======+=======+=============+
| test  | test  | passed      |
+-------+-------+-------------+
| test2 | test2 | failed      |
+-------+-------+-------------+

.. py:function:: enumerate(sequence[, start=0])

   Return an iterator that yields tuples of an index and an item of the
   *sequence*. (And so on.)

.. code-block:: python
   
   def my_function():
       """This is a Python code snippet."""
       print("Hello, world!")

Here is some example code::
   
   # This will be rendered as a code block,
   # but it might not have highlighting.
   x = 1
   y = 2

.. highlight:: rst

Now I'll show some reST code::
   
   .. note::
      This will be highlighted as reST.

.. highlight:: bash

And now some shell commands::

   # This will be highlighted as bash
   ls -l
   rm -rf /

.. button-link:: https://example.com
    :color: primary
    :outline:

    :octicon:`container`

.. dropdown:: Github repo
    :icon: mark-github
    :color: dark

    test

or

.. github::

    This is a GitHub link block.
    this is useful for linking to your project's
    repository or specific files within it.
    you can not customize the block here.

    .. button-link:: https://example.com
        :color: primary
        :outline:

        :octicon:`mark-github`

.. github::

    you can find the plugin source code here:
    
    .. button-link:: https://github.com/grish-ka/sphinxBetterBlocks
        :color: primary
        :outline:

        :octicon:`plug`