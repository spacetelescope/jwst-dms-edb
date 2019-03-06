************
jwedb Documentation
************
Python interface to the JWST DMS Engineering Database (EDB).

Functionalities
==========================
* Retrieve the EDB mnemonic inventory.
* Retrieve descriptive information for a specific mnemonic.
* Retrieve the timestamp-value pairs for a specific mnemonic in a given timerange. By default, the data is returned as an ``astropy.table.Table``

Where to Find jwedb
==========================
jwedb is hosted and developed at https://github.com/spacetelescope/jwst-dms-edb


Installation
==================
This package is being developed in a python 3.5 environment.

How to install
**************
jwedb is available on `PyPI <https://pypi.org/project/jwedb/>`_ .


`pip install jwedb`

Clone the repository:
`git clone https://github.com/spacetelescope/jwst-dms-edb`
Install jwedb:
`cd jwedb`
`python setup.py install` or
`pip install .`



User Documentation
==================
Example usage:

Reporting Issues / Contributing
===============================
Do you have feedback and feature requests? Is there something missing you would like to see? Please open a new issue or new pull request at https://github.com/spacetelescope/jwst-dms-edb for bugs, feedback, or new features you would like to see. If there is an issue you would like to work on, please leave a comment and we will be happy to assist. New contributions and contributors are very welcome! This package follows the STScI `Code of Conduct <https://github.com/spacetelescope/jwedb/blob/master/CODE_OF_CONDUCT.md>`_ strives to provide a welcoming community to all of our users and contributors.

Coding and other guidelines
###########################
We strive to adhere to the `STScI Style Guides <https://github.com/spacetelescope/style-guides>`_.

How to make a code contribution
###############################
Please see the guidelines for ``jwql``: `<https://github.com/spacetelescope/jwql>`_


Reference API
=============
.. toctree::
   :maxdepth: 1

   edb_interface.rst
