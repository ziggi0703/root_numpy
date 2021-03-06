.. _reference:

####################
root_numpy Reference
####################

:Release: |version|
:Date: |today|

This reference manual details the functions included in root_numpy, describing
what they are and what they do.

root_numpy
----------

.. module:: root_numpy

.. autosummary::
   :toctree: generated

   array
   matrix
   root2array
   root2rec
   tree2array
   tree2rec
   array2tree
   array2root
   hist2array
   array2hist
   fill_hist
   fill_profile
   fill_graph
   random_sample
   evaluate
   list_trees
   list_branches
   list_structures
   rec2array
   stack
   stretch
   dup_idx
   blockwise_inner_join

root_numpy.tmva
---------------

.. module:: root_numpy.tmva

.. autosummary::
   :toctree: generated

   add_classification_events
   add_regression_events
   evaluate_reader
   evaluate_method

.. _conversion_table:

Type Conversion Table
---------------------

Types are converted according to this table:

==================  =========================
ROOT                NumPy
==================  =========================
Bool_t              np.bool
Char_t              np.int8
UChar_t             np.uint8
Short_t             np.int16
UShort_t            np.uint16
Int_t               np.int32
UInt_t              np.uint32
Float_t             np.float32
Double_t            np.float64
Long64_t            np.int64
ULong64_t           np.uint64
x[10]               (np.primitivetype, (10,))
x[nx]               np.object
string              np.object
vector<t>           np.object
vector<vector<t> >  np.object
==================  =========================

Variable length arrays (such as ``particletype[nparticle]``) and vectors
(such as ``vector<int>``) are converted to NumPy arrays of the corresponding
types. Fixed length arrays are converted to fixed length NumPy array fields.
