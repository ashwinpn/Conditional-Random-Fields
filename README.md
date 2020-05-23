# Conditional-Random-Fields
An analysis and implementation of Conditional Random Fields, which are used when the input data is dependent on each other.


## Why the discussion on CRF?

Models such as HMM do not really work that well on complex POS tagging (Part of speech tagging) tasks, since they do not deal with context all that well. Superior models for POS tagging, such as structured correspondence learning, are based on either Markov Random Fields or Conditional Random Fields.

MRF and CRF bring to the forefront a probabilistic graphical model, and showcases the dependencies between input parameters, something which HMM and Naive Bayes Classifier fail to consider (or rather, lack the capacity to consider).


## Uses

Conditional Random Fields are used for entity recognition, genome analysis, and other tasks which have a sequence based structure associated with them.
