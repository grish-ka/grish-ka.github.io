sphinxBetterBlocks
##################

This is a Sphinx plugin that provides better blocks for your documentation. It includes:
- github blocks for linking to repositories and files. As shown here:

.. github::
    You can find the source code for this project here:

    .. button-link:: https://github.com/grish-ka/sphinxBetterBlocks
        :color: primary
        :outline:

        :octicon:`plug`


.. _documentation-for-sphinxBetterBlocks:

Documentation
*************

.. rst:directive:: github

   This is a GitHub link block. You can use it to link to your project's
   repository or specific files within it. 
   
   Example usage:
   
   .. code-block:: rst
        :linenos:

        .. github::

            Check out the code here!

            .. button-link:: example.com
                :color: primary
                :outline:

                :octicon:`mark-github`

That is it for now! More block types and features will be added in the future.