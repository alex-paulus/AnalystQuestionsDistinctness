# InformationRevelation

***Julia Haag, Christian Hofmann, Alexander Paulus, Nina Schwaiger, Thorsten Sellhorn<br>***
*LMU Munich School of Management*

Code and illustrative example complementing our paper "Analysts’ Questions When Peers Are Listening"
---

This repository contains the code and an illustrative example for the calculation of an analyst question's thematic distinctness in earnings conference calls used in [Haag et al. [2022]](https://papers.ssrn.com/sol3/papers.cfm?abstract_id=3853869).

***Measurement of an analyst question's thematic distinctness:***

As described in the paper, we conceptually follow [Lee [2016]](https://doi.org/10.2308/accr-51135) as well as [Cicon [2017]](https://doi.org/10.1007/s11156-015-0542-0) by arguing that analysts’ questions act as the natural triggers of managers’ answers. We measure the thematic distinctness by the extent to which the question’s topics are not covered in the management presentation. Thus, higher levels of thematic distinctness reflect a more-distinct question whereas lower levels of thematic distinctness are indicative of questions that follow up on topics addressed in the management presentation. Following [Cicon [2017]](https://doi.org/10.1007/s11156-015-0542-0), we apply the concept of cosine modification to approximate the degree of thematic distinctness across texts [(Brown and Tucker [2011])](https://doi.org/10.1111/j.1475-679X.2010.00396.x). Appendix B describes the calculation of cosine modification in detail.

In our code, we use the prespecified [cosine similarity](https://scikit-learn.org/stable/modules/generated/sklearn.metrics.pairwise.cosine_similarity.html) module from scikit learn. For a brief introduction of the syntax of scikit learn please refer to the scikit learn. This module requires the [CountVectorizer](https://scikit-learn.org/stable/modules/generated/sklearn.feature_extraction.text.CountVectorizer.html) module from scikit learn to transform the management presentation and the analysts’ questions to a term-document matrix.

**Modules (Python packages)** - Please make sure to install the latest version of the following Python modules:
- [Numpy](https://numpy.org/)
- [Pandas](https://pandas.pydata.org/)
- [nltk]( https://www.nltk.org/)
- [spacy]( https://spacy.io/)
- [sklearn]( https://scikit-learn.org/); download “en_core_web_sm” dictionary
