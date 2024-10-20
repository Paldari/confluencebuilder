Roles
=====

The following outlines additional `roles`_ supported by this extension.

.. index:: Macros; Emoticon Macro (role)
.. index:: Emoticon Macro

Emoticon Macro
--------------

The following role can be used to help include Confluence emoticon macros into
generated Confluence documents.

.. rst:role:: confluence_emoticon

    The ``confluence_emoticon`` role allows a user to build inlined emoticon
    macros. For example:

    .. code-block:: rst

        :confluence_emoticon:`tick`: This is done.

        :confluence_emoticon:`cross`: This is incomplete.

    .. versionadded:: 1.9

.. index:: Macros; Jira Macro (role)
.. _jira-roles:

Jira
----

The following role can be used to help include Jira macros into generated
Confluence documents.

.. index:: Jira; Adding a single Jira link (role)

.. rst:role:: jira

    The ``jira`` role allows a user to build an inlined Jira macro to be
    configured with a provided Jira key. For example:

    .. code-block:: rst

        See :jira:`TEST-123` for more details.

    .. versionadded:: 1.7

See also :ref:`Jira directives <jira-directives>`.

.. index:: Macros; LaTeX Macro (role)
.. index:: LaTeX Macro; Adding inlined LaTeX (role)
.. _latex-roles:

LaTeX
-----

.. note::

    LaTeX support requires dvipng/dvisvgm to be installed on system; however,
    if a Confluence instance supports a LaTeX macro, the
    :lref:`confluence_latex_macro` option can be used instead. For more
    information, please read :doc:`guide-math`.

The following role can be used to help include LaTeX content into generated
Confluence documents.

.. rst:role:: confluence_latex

    The ``confluence_latex`` role allows a user to build inlined LaTeX
    content. For example:

    .. code-block:: rst

        This is a :confluence_latex:`$\\mathfrak{t}$est`.

    .. versionadded:: 1.8

See also :ref:`LaTeX directives <latex-directives>`.

.. index:: Macros; Mentions Macro (role)
.. index:: Mentions; Macro (role)
.. _mention-roles:

Mentions
--------

The following role can be used to help include `Confluence mentions`_ into
generated Confluence documents.

.. rst:role:: confluence_mention

    .. warning::

        Confluence Cloud mentions should always use account identifiers; where
        Confluence Data Center mentions should use either usernames or user
        keys. Attempting to use Confluence Cloud account identifiers when
        publishing to a Confluence Data Center will most likely result in an
        "Unsupported Confluence API call" error (500).

    The ``confluence_mention`` role allows a user to build inlined mentions.
    For Confluence Cloud instances, a mention to a specific user's account
    identifier would be defined as follows:

    .. code-block:: rst

        See :confluence_mention:`3c5369:fa8b5c24-17f8-4340-b73e-50d383307c59`.

    For Confluence Data Center, a mention to a specific user can either
    be set to the username value or a user's key value:

    .. code-block:: rst

        For more information, contact :confluence_mention:`myuser`.
         (or)
        Contact :confluence_mention:`b9aaf35e80441f415c3a3d3c53695d0e` for help.

    A user mapping table can also be configured using the
    :lref:`confluence_mentions` option.

    .. versionadded:: 1.9

.. index:: Smart links; Roles
.. _smart-link-roles:

Smart links
-----------

.. note::

    Smart links will only render when using the v2 editor
    (see :lref:`confluence_editor`).

Support for inlined smart links can be created using the following roles.

.. rst:role:: confluence_doc

    The ``confluence_doc`` role allows a user to define an inlined link to a
    document that is styled with a card appearance. The role accepts the
    name of a document in an absolute or relative fashion (in the same manner
    as Sphinx's `:doc: <role-doc_>`_ role). For example:

    .. code-block:: rst

        See :confluence_doc:`my-other-page`.

    .. versionadded:: 2.1

.. rst:role:: confluence_link

    The ``confluence_link`` role allows a user to define an inlined link to a
    page that is styled with a card appearance. The role accepts a URL.
    How Confluence renders the context of a link card will vary based on
    which link targets Confluence supports. For example:

    .. code-block:: rst

        See :confluence_link:`https://example.com`.

    .. versionadded:: 2.1

See also :ref:`smart link directives <smart-link-directives>`.

.. index:: Macros; Status Macro (role)
.. index:: Status Macro

Status Macro
------------

The following role can be used to help include `Confluence status macro`_ into
generated Confluence documents.

.. rst:role:: confluence_status

    The ``confluence_status`` role allows a user to build inlined status
    macros. For example:

    .. code-block:: rst

        :confluence_status:`My Status`

    The color of a status macro can be configured to a value supported by
    Confluence's status macro. For example, to adjust the status value to
    a yellow color, the following can be used:

    .. code-block:: rst

        :confluence_status:`WARNING <yellow>`

    To tweak the style of a status macro to an outlined variant (if supported
    by the configured Confluence editor), adjust the color enclosure to
    square brackets:

    .. code-block:: rst

        :confluence_status:`PASSED [green]`

    .. versionadded:: 1.9

.. index:: Strikethrough (role)
.. _confluence_strike-role:

Strikethrough
-------------

The following role can be used to explicitly define strikethrough text into
generated Confluence documents.

.. rst:role:: confluence_strike

    The ``confluence_strike`` role allows a user to build inlined text that has
    been styled with a strikethrough. For example:

    .. code-block:: rst

        :confluence_strike:`My text`

    .. versionadded:: 2.1

See also :doc:`guide-strike`.

.. references ------------------------------------------------------------------

.. _Confluence mentions: https://support.atlassian.com/confluence-cloud/docs/mention-a-person-or-team/
.. _Confluence status macro: https://support.atlassian.com/confluence-cloud/docs/insert-the-status-macro/
.. _role-doc: https://www.sphinx-doc.org/en/master/usage/restructuredtext/roles.html#role-doc
.. _roles: https://www.sphinx-doc.org/en/master/usage/restructuredtext/roles.html
