========
Overview
========

.. start-badges

.. list-table::
    :stub-columns: 1

    * - tests
      - | |githubactions|
        

.. |githubactions| image:: https://github.com/ehthiede/packaging_demo/actions/workflows/testing.yml/badge.svg?branch=main
    :alt: Testing Status
    :target: https://github.com/ehthiede/packaging_demo/actions

Sandbox code for exploring algorithms for reconstructing tomographs.
Currently, the only implemented algorithm is weighted backprojection

Installation
============
To install, run 

::

    pip install -e .

in this directory.

Running the Code
================

The weighted backprojection can be imported in your python files as 

::

    import tomo_sandbox.weighted_backprojection_1d
    volume = weighted_backprojection_1d(images, angles)

If images are equispaced, then the command line interface can also be used,

::

    python -m tomo_sandbox.perform_reconstruction image_file.ny 0 172 --degrees

Running the Tests
=================
Tests can be run in your current environment using pytest,

::

    pytest tests/
