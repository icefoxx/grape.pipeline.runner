Welcome to grape.pipeline.runner's documentation!
=================================================

Grape (Grape RNA-Seq Analysis Pipeline Environment) is a pipeline for processing
and analyzing RNA-Seq data developed at the Bioinformatics and Genomics unit of
the Centre for Genomic Regulation (CRG) in Barcelona. 

The grape.buildout packages installs the command line tools of the grape.pipeline.runner
package for automatically running your configured pipelines.

To learn more about Grape, and to download and install it, go to the Bioinformatics 
and Genomics website at:

`Grape Homepage <http://big.crg.cat/services/grape>`_ 

.. note::

    The grape.pipeline.runner package is a Buildout recipe used by grape.buildout, 
    and is not a standalone Python package. It is only going to be useful as installed 
    by the grape.buildout package.


Motivation
----------

Here at the CRG, we configure all our RNASeq pipeline runs in a central place
before running the Grape pipelines. Once all the accessions and pipeline
profiles have been defined and the buildout parts have been created, we start
and execute them.

When we receive Fastq or bam files for a project, we typically have to:

1. Define the accessions and profiles in::

    grape.buildout/accessions/MyProject/db.cfg
    grape.buildout/profiles/MyProject/db.cfg

2. Create a pipeline project folder in::

    grape.buildout/pipelines/MyProject

3. Configure the buildout in::

    grape.buildout/pipelines/MyProject/buildout.cfg

4. Run the buildout in::

    grape.buildout/pipelines/MyProject

5. Run the pipeline with the console script::

    cd grape.buildout/pipelines/MyProject
    ./bin/grape-runner

The grape.pipeline.runner package install the grape-runner console script that is used
in step number 5. 
The buildout uses the recipe to produce the individual pipelines and 
preconfigure the start and execute scripts with all the necessary command 
line options, used by the grape-runner console script.


Contents:

.. toctree::
   :maxdepth: 2

Indices and tables
==================

* :ref:`genindex`
* :ref:`modindex`
* :ref:`search`

