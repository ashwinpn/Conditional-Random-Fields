# Conditional-Random-Fields
An analysis and implementation of Conditional Random Fields (CRF's) (https://en.wikipedia.org/wiki/Conditional_random_field) - with applications to Natural Language Processing.


<ins>Why the discussion on Conditional Random Fields?</ins>

Models such as HMM do not really work that well on complex POS tagging (Part of speech tagging) tasks, since they do not deal with context all that well. Superior models for POS tagging, such as structured correspondence learning, are based on either Markov Random Fields or Conditional Random Fields.

MRF and CRF bring to the forefront a probabilistic graphical model, and showcases the dependencies between input parameters, something which HMM and Naive Bayes Classifier fail to consider (or rather, lack the capacity to consider). Essentially, CRF's are discriminative graphical models that are useful for performing inference when output variables are known to obey a structure.

<ins>Uses</ins>

Conditional Random Fields are used for entity recognition, genome analysis, and other tasks which have a sequence based structure associated with them.

## Sparse Gaussian Conditional Random Fields

```crf_math_1.py``` consists of an implementation of Sparse Gaussian Conditional Random Fields. 

Sparse Gaussian CRF's are a particular variant of Gaussian CRF's where the loss function incorporates an ```L1``` penalty in order to promote sparsity among the estimated parameters. Setting ```lamda[L] >> lambda[T]``` results in Lasso regression, while setting ```lamda[T] >> lamda[L]``` results in a Graphical Lasso.

## Hidden State Conditional Random Field
The model classifies sequences according to a latent state sequence. This package consists of methods to enable the learning of parameters from example sequences and to score new sequences.

### States
Each state is numbered ```0, 1, ..., num_states - 1```. The state machine starts in ```state 0``` and ends in ```num_states - 1```. Currently the state transitions are constrained so that, on each element in the input sequence, the state machine either stays in the current state or advances to a state represented by the next number. This default can be changed by setting the ```transitions``` and corresponding ```transition_parameters``` properties.
