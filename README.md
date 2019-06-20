
## Topic Modeling Using Latent Dirichlet Allocation (LDA) in Scikit Learn and pyLDAviz

Here the attempt is to discover topics present in the 20 Newsgroup data set. The implementation uses following libraries.
1. [Spacy](https://spacy.io/) is used for text processing.
2. Scikit is used for topic modeling ([LDA](https://scikit-learn.org/stable/modules/generated/sklearn.decomposition.LatentDirichletAllocation.html)).
3. [pyLDAvis](https://github.com/bmabey/pyLDAvis/blob/master/notebooks/sklearn.ipynb) is used for visualizing topics.

The implementation is self explanatory is available in the jupyter notebook `topic-model.ipynb`.
* 20 Newsgroup data set is sourced from a CSV file available as `20newsgroup.csv`.

### Notes:
1. Modeling time can be reduced (at cost of optimal result) by providing small vocabulary size and/or reducing the iterations for the LDA. This is available at `max_features` of `CountVectorizer` and `max_iter` of `LatentDirichletAllocation` respectively.
2. Other methods to speed up the process is to tweak `batch_size` and `n_jobs` parameters of `LatentDirichletAllocation`