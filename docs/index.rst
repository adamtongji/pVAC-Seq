.. pVAC-Seq documentation master file, created by
   sphinx-quickstart on Wed Aug 31 08:31:01 2016.
   You can adapt this file completely to your liking, but it should at least
   contain the root `toctree` directive.

pVAC-Seq
====================================

.. warning::
    pVAC-Seq has been renamed to pVACseq and is now part of the pVACtools
    immunotherapy tools suite. The ``pvacseq`` package will no longer be
    updated or maintained. Please update your local installation to the ``pvactools``
    package. Please see the `pVACtools documentation <http://pvactools.readthedocs.io/>`_ for more information.

pVAC-Seq is a cancer immunotherapy pipeline for the identification of **p**\ ersonalized **V**\ ariant **A**\ ntigens by **C**\ ancer **Seq**\ uencing (pVAC-Seq) that integrates tumor mutation and expression data (DNA- and RNA-Seq). It enables cancer immunotherapy research by using massively parallel sequence data to predicting tumor-specific mutant peptides (neoantigens) that can elicit anti-tumor T cell immunity. It is being used in studies of checkpoint therapy response and to identify targets for cancer vaccines and adoptive T cell therapies. For more general information, see the `manuscript published in Genome Medicine <http://www.genomemedicine.com/content/8/1/11>`_.

.. toctree::
   :maxdepth: 2

   features
   install
   prerequisites
   run
   filter_commands
   additional_commands
   optional_downstream_analysis_tools
   frequently_asked_questions
   contact

New in version |version|
------------------------

This is a hotfix release to fix a bug with how certain types of frameshift
mutations were handled. Previously, we were not creating the correct mutant
peptide sequence for these variants. See `this GitHub issue
<https://github.com/griffithlab/pVAC-Seq/issues/323>`_ for more information.

This version also includes a sanity check to error out if the wildtype
amino acid in the wildtype protein sequence differs from the expected wildtype
amino acid as listed in the protein change. This situation might occur if the
VCF was annotated with a different reference build than the one used for
alignment and variant calling.

Citation
--------

Jasreet Hundal, Beatriz M. Carreno, Allegra A. Petti, Gerald P. Linette, Obi L. Griffith, Elaine R. Mardis, and Malachi Griffith. `pVAC-Seq: A genome-guided in silico approach to identifying tumor neoantigens <http://www.genomemedicine.com/content/8/1/11>`_. Genome Medicine. 2016, 8:11, DOI: 10.1186/s13073-016-0264-5. PMID: `26825632 <http://www.ncbi.nlm.nih.gov/pubmed/26825632>`_.

License
-------
This project is licensed under `NPOSL-3.0 <http://opensource.org/licenses/NPOSL-3.0>`_.
