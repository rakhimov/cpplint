cpplint - static code checker for C++
=====================================

This project continues the work of cpplint, a C++ style checker following `Google's C++ style guide <http://google.github.io/styleguide/cppguide.html>`_. It provides cpplint as a PyPI package and adds a few features and fixes. It is maintained as a fork of `google/styleguide <https://github.com/google/styleguide>`_ in hopes that it can be merged in the future.

To install cpplint from PyPI, run:

.. code-block:: bash

    $ pip install cpplint

Then run it with:

.. code-block:: bash

    $ cpplint [OPTIONS] files

For full usage instructions, run:

.. code-block:: bash

    $ cpplint --help

Changes
-------

The modifications in this branch are minor fixes and cosmetic changes:

* more default extensions
* python 3k compatibility
* minor fixes around default file extensions
* continuous integration on travis
* support for recursive file discovery via the --recursive argument
* support for excluding files via --exclude
* JUnit XML output format
* Overriding repository root auto-detection via --repository
* Support ``#pragma once`` as an alternative to header include guards

Maintaining
-----------

To release a new version:

.. code-block:: bash

    vi setup.py # increment the version
    vi changelog.rst # log changes
    git add setup.py changelog.rst
    git commit -m "Releasing 0.0.6"
    git tag 0.0.6
    git push
    git push --tags
    python setup.py sdist register -r pypi
    python setup.py sdist upload -r pypi

Thanks to `tkruse <https://github.com/tkruse>`_ for putting cpplint on PyPI and maintaining the PyPI version for many years!

.. image:: https://travis-ci.org/theandrewdavis/cpplint.svg
    :target: https://travis-ci.org/theandrewdavis/cpplint
