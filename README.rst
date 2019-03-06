Python interface to the JWST DMS Engineering Database
-----------------------------------------------------

.. image:: https://travis-ci.org/spacetelescope/jwst-dms-edb.svg?branch=master
    :target: https://travis-ci.org/spacetelescope/jwst-dms-edb

.. image:: https://badge.fury.io/py/jwedb.svg
    :target: https://badge.fury.io/py/jwedb

.. image:: http://img.shields.io/badge/powered%20by-AstroPy-orange.svg?style=flat
    :target: http://www.astropy.org
    :alt: Powered by Astropy Badge

Python interface to the JWST DMS Engineering Database


Installation
------------
From PyPi::

    pip install jwedb


Example usage
-------------

For complete functionality and in particular to retrieve mnemonic values, a valid MAST token has
to be provided. Please visit https://auth.mast.stsci.edu/info to generate a token.

One way to store it locally is using .netrc file in the local home directory.
If the MAST token is stored in the following format within .netrc, the code below will work::

    machine mast
        login <username>
        password <token>

Code::

    import netrc
    from astropy.time import Time
    from jwedb.edb_interface import query_single_mnemonic

    # get MAST token from the .netrc file in the home directory
    host = 'mast'
    secrets = netrc.netrc()
    mast_token = secrets.authenticators(host)[2]

    mnemonic_identifier = 'SA_ZFGOUTFOV'
    start_time = Time(2018.0, format='decimalyear')
    end_time = Time(2018.1, format='decimalyear')

    data, meta, info = query_single_mnemonic(mnemonic_identifier, start_time, end_time,
                                             token=mast_token)

    data.pprint()

Contributing
------------

jwedb is open source

Please see the `jwql` contribution guide for how to contribute to jwedb:
https://github.com/spacetelescope/jwql#software-contributions



License
-------

This project is Copyright (c) Space Telescope Science Institute and licensed under
the terms of the Aura license. This package is based upon
the `Astropy package template <https://github.com/astropy/package-template>`_
which is licensed under the BSD 3-clause licence. See the licenses folder for
more information.


