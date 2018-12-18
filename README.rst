========
BASED ON
========

- https://github.com/ionelmc/cookiecutter-pylibrary

build
========
rm -rf build
rm -rf src/*.egg-info

tox -e check

python setup.py clean --all sdist bdist_wheel

install 
=========
locally (when you are in main folder, e means you do not have to rebuild)
´pip install -e .´

from github 
´pip install git+https://github.com/EmilMachine/ultimateml.git´



pip install git+https://github.com/tangentlabs/django-oscar-paypal.git@issue/34/oscar-0.6
And specify the branch name without the leading /.

========
Overview
========

.. start-badges

.. list-table::
    :stub-columns: 1

    * - docs
      - |docs|
    * - tests
      - | |travis| |appveyor| |requires|
        | |codecov|
    * - package
      - | |version| |wheel| |supported-versions| |supported-implementations|
        | |commits-since|

.. |docs| image:: https://readthedocs.org/projects/python-ultimateml/badge/?style=flat
    :target: https://readthedocs.org/projects/python-ultimateml
    :alt: Documentation Status


.. |travis| image:: https://travis-ci.org/emilmachine/python-ultimateml.svg?branch=master
    :alt: Travis-CI Build Status
    :target: https://travis-ci.org/emilmachine/python-ultimateml

.. |appveyor| image:: https://ci.appveyor.com/api/projects/status/github/emilmachine/python-ultimateml?branch=master&svg=true
    :alt: AppVeyor Build Status
    :target: https://ci.appveyor.com/project/emilmachine/python-ultimateml

.. |requires| image:: https://requires.io/github/emilmachine/python-ultimateml/requirements.svg?branch=master
    :alt: Requirements Status
    :target: https://requires.io/github/emilmachine/python-ultimateml/requirements/?branch=master

.. |codecov| image:: https://codecov.io/github/emilmachine/python-ultimateml/coverage.svg?branch=master
    :alt: Coverage Status
    :target: https://codecov.io/github/emilmachine/python-ultimateml

.. |version| image:: https://img.shields.io/pypi/v/ultimateml.svg
    :alt: PyPI Package latest release
    :target: https://pypi.org/project/ultimateml

.. |commits-since| image:: https://img.shields.io/github/commits-since/emilmachine/python-ultimateml/v0.1.0.svg
    :alt: Commits since latest release
    :target: https://github.com/emilmachine/python-ultimateml/compare/v0.1.0...master

.. |wheel| image:: https://img.shields.io/pypi/wheel/ultimateml.svg
    :alt: PyPI Wheel
    :target: https://pypi.org/project/ultimateml

.. |supported-versions| image:: https://img.shields.io/pypi/pyversions/ultimateml.svg
    :alt: Supported versions
    :target: https://pypi.org/project/ultimateml

.. |supported-implementations| image:: https://img.shields.io/pypi/implementation/ultimateml.svg
    :alt: Supported implementations
    :target: https://pypi.org/project/ultimateml


.. end-badges

An example package. Generated with cookiecutter-pylibrary.

* Free software: MIT license

Installation
============

::

    pip install ultimateml

Documentation
=============


https://python-ultimateml.readthedocs.io/


Development
===========

To run the all tests run::

    tox

Note, to combine the coverage data from all the tox environments run:

.. list-table::
    :widths: 10 90
    :stub-columns: 1

    - - Windows
      - ::

            set PYTEST_ADDOPTS=--cov-append
            tox

    - - Other
      - ::

            PYTEST_ADDOPTS=--cov-append tox
