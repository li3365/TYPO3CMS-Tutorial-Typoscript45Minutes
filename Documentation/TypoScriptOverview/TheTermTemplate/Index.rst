.. include:: ../../Includes.txt


.. _template:
.. _the-term-template:

The term template
^^^^^^^^^^^^^^^^^

The term template has a double meaning in TYPO3 CMS. On the one hand,
there is the *HTML template file*, which serves as the skeletal
structure in which the content, provided by the CMS,
will be rendered. On the other hand, there is the *TypoScript template*,
which is created in the template module in the TYPO3 CMS
Backend and can exist on any page.

The :ref:`Templating Tutorial <t3templating:start>` shows how the two are related
together. This manual is purely about TypoScript templates.

Common mistakes made with TypoScript templates can cause a message like this:

.. figure:: ../../Images/NoTypoScriptTemplateFound.png
   :alt: Error message "No TypoScript template found!"


"No TypoScript template found": This warning appears if no template,
with the root level flag enabled, is found in the page tree.

.. figure:: ../../Images/ThePageIsNotConfigured.png
   :alt: Error message "The page is not configured!"


"The page is not configured": This warning appears if the rootlevel
flag of a template in the page tree is enabled (i.e. this template
is used), but no :ref:`PAGE <t3tsref:page>` Object can be found.

The following code is enough to remove this warning::

   page = PAGE
   page.10 = TEXT
   page.10.value = Hello World

Do not worry about this code for now, it will be explained later.
