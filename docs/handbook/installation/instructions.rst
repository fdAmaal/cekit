Installation instructions
=========================

.. contents::
    :backlinks: none

We provide RPM packages for Fedora, CentOS/RHEL distribution.
CEKit installation on other platforms is still possible via ``pip``.

RPM packages are distributed via regular repositories in case of Fedora
and the EPEL repository for CentOS/RHEL.

.. warning::
    Currently packaged version is a snapshot release of the upcoming CEKit 3.0.

.. tip::
    You can see latest submitted package updates `submitted in Bodhi <https://bodhi.fedoraproject.org/updates/?packages=cekit>`_.

.. warning::

   Make sure you read the :doc:`dependencies </handbook/installation/dependencies>` chapter which contains important
   information about how CEKit dependencies are handled!

Fedora
-------------------

.. note::
    Supported versions: 29+.

CEKit is available from regular Fedora repositories.

.. code-block:: bash

    dnf install cekit

CentOS / RHEL
-------------------

.. note::
    Supported versions: 7.x

CEKit is available from the `EPEL repository <https://fedoraproject.org/wiki/EPEL>`_.

.. code-block:: bash

    yum install epel-release
    yum install cekit

Other systems
-------------------

We strongly advise to use `Virtualenv <https://virtualenv.pypa.io/en/stable/>`_ to install CEKit.
Please consult your package manager for the correct package name.

To create custom Python virtual environment please run following commands on your system:

.. code-block:: bash

    # Prepare virtual environment
    virtualenv ~/cekit
    source ~/cekit/bin/activate

    # Install CEKit
    # Execute the same command to upgrade to latest version
    pip install -U cekit

    # Now you are able to run CEKit
    cekit --help

.. note::

   Every time you want to use CEKit you must activate CEKit Python virtual environment by
   executing ``source ~/cekit/bin/activate``

If you don't want to (or cannot) use Virtualenv, the best idea is to install CEKit in the user's home with the
``--user`` prefix:

.. code-block:: bash

    pip install -U cekit --user

.. note::
    In this case you may need to add ``~/.local/bin/`` directory to your ``$PATH`` environment variable to
    be able to run the ``cekit`` command.