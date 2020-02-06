OPETH
=====

.. rtd-inclusion-marker-do-not-remove

Online Peri-Event Time Histogram for `Open Ephys <http://www.open-ephys.org/gui>`_.

Performs spike detection based on raw Open Ephys data exported via `ZeroMQ <https://zeromq.org>`_. 
Requires triggers from Open Ephys for histogram display as spikes are detected around them.

Usage
-----

- Needs `ZMQInterface plugin <https://github.com/bandita137/ZMQInterface>`_ (e.g. in the Open Ephys plugin folder). 
  For Windows a `precompiled dll <https://github.com/bandita137/ZMQInterface/releases/download/v0.2-pre/ZMQInterface.dll>`_ is present. 
- Set up Open Ephys with ZMQInterface plugin. Plugin is recommended to be put after bandpass 
  filter and/or common average reference filter, but spike detector is not required.
- Start ``opeth/gui.py``.

Installation
------------

Setting up python environment (auto)
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Using conda/miniconda, create a new environment issuing the command

::

    conda create --name opeth --file requirements.txt python=3.7

in the root dir of opeth, which will install all necessary prerequisites. 

Activate the new environment with the command

::

    conda activate opeth

and once activated you may start OPETH with

::

    python opeth/gui.py

Python 3.8
^^^^^^^^^^

As of Jan 2020, Python 3.8 is not installed by default for conda, neither was it actively tested.

One may use the command::

    conda env create --file environment.yml

to set up an ``opeth`` environment for Python 3.8 using the conda-forge version of pyqtgraph, but be prepared for issues in pyqtgraph.

Setting up python environment (manually)
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Required non-default packages: pyzmq, pyqtgraph (and one of the qt versions for pyqtgraph).

Contributors
------------

Developed by Andras Szell (szell.andris@gmail.com) and other Hangyalab members (http://hangyalab.koki.hu/).

Open Ephys ZMQ plugin connection is based on 
`sample python scripts <https://github.com/MemDynLab/ZMQInterface/tree/master/python_clients>`_ by Francesco Battaglia.

License
-------

GNU General Public License v3.0 or later.

See `LICENSE <https://github.com/hangyabalazs/opeth/blob/master/LICENSE>`_ for the full text.