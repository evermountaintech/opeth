OPETH
=====

More detailed documentation: https://opeth.readthedocs.io/

.. rtd-inclusion-marker-do-not-remove

Online Peri-Event Time Histogram for `Open Ephys <http://www.open-ephys.org/gui>`_.

OPETH visualizes Peri-Event Time Histograms (PETH) of spikes detected in raw Open Ephys data, 
broadcasted via `ZeroMQ <https://zeromq.org>`_. PETH is aligned to triggers from Open Ephys.

Quickstart
----------

- OPETH requires `ZMQInterface plugin <https://github.com/open-ephys-plugins/ZMQPlugins/tree/master/ZMQInterface>`_. 
  It is part of Open Ephys from version 0.4.6 up.
- Set up Open Ephys with ZMQInterface plugin. The ZMQ plugin is recommended to be put after bandpass 
  filter and/or common average reference filter in the Open Ephys signal chain, while spike detector filter is not required.
- Start with the ``opeth`` command when using the pip package or start with ``python opeth/gui.py`` when running from sources (see below).

Installation
------------

Simplest way is to install the opeth package for Python 2.7 or Python <=3.7 with pip::

    pip install opeth

Then start with::

    opeth

(Python 3.8 support is partially broken until the release of pyqtgraph 0.11.)

Dependencies
^^^^^^^^^^^^

Required non-default packages: ``pyzmq``, ``pyqtgraph`` plus one of the qt versions for pyqtgraph, preferably ``PyQt5``,
and also their dependencies (e.g. ``numpy``).

Running from sources
--------------------

After cloning the git repository or extracting a source zip file, multiple methods could work.

Setting up python environment with conda
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Conda builds are not available yet.

Using conda/miniconda, create an ``opeth`` environment issuing the following command in the root dir of opeth::

    conda env create --file environment.yml 
     
which will install all necessary prerequisites for Python 3.7.

Activate the new environment with the command

::

    conda activate opeth

and once activated, you may start OPETH with

::

    python opeth/gui.py

Using python 3.8 is not recommended (Feb 2020) as some bugs are to be addressed (most probably residing in pyqtgraph),
but it is possible with the conda-forge version of pyqtgraph (default environment name will be ``opeth_python38``)::

    conda env create --file env38.yml

Setting up python environment with pip
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Python 3.7 dependencies can be installed with the command

::

    pip install -r requirements.txt


