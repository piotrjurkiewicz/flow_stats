.. flow-models documentation master file, created by
   sphinx-quickstart on Thu Dec 24 01:48:45 2020.
   You can adapt this file completely to your liking, but it should at least
   contain the root `toctree` directive.

Welcome to flow-models's documentation!
***************************************

`flow-models`_ is a software framework for creating precise and reproducible statistical flow models from
NetFlow/IPFIX flow records. It can be used to merge split records, calculate histograms of flow features and create
General Mixture Models fitting them. Created models can be used both as an input in analytical calculations and to
generate realistic traffic in simulations.

Provided tools
==============

The framework currently includes the following tools:

- `tools/merge` -- merges flows which were split across multiple records due to *active timeout*
- `tools/sort` -- sorts flow records according to specified fields (requires `numpy`)
- `tools/hist` -- calculates histograms of flows length, size, duration or rate
- `tools/hist_np` -- calculates histograms using multiple threads (requires `numpy`, much faster, but uses more memory)
- `tools/fit` -- creates General Mixture Models (GMM) fitted to flow records (requires `scipy`)
- `tools/plot` -- generates plots from flow records and fitted models (requires `pandas` and `scipy`)
- `tools/generate` -- generates flow records from histograms or mixture models
- `tools/summary` -- produces TeX tables containing summary statistics of flow dataset (requires `scipy`)
- `tools/convert` -- converts flow records between supported formats

Following the Unix philosophy, each tool is a separate Python program aimed at a single purpose. Features provided
by the tools are orthogonal and they are tailored to be used sequentially in data-processing pipelines.

Contents
========

.. toctree::
   :hidden:

   self

.. toctree::
   :maxdepth: 2

   tutorial
   workflow
   formats
   tools
   flow_models

Indices and tables
==================

* :ref:`genindex`
* :ref:`modindex`
* :ref:`search`
