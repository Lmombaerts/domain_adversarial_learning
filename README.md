# Domain Adversarial Learning
Implementations of Domain Adversarial Learning algorithms

## What is Domain adaptation (DA) ?

Domain adaptation methods address the issue of discrepancies in the data distributions obtained from various domains, which then affects model performances.

Withian DA frameworks, the restriction posed by limited availability of manually labelled data for training has been addressed by various methods:

- Semi-supervised
- Self-labelling
- Pseudo-labelling

Self and pseudo labelling methods use small amount of labelled data, together with large amount of unlabeled data to improve model performance. 

**Transfer learning** can be considered a form of domain adaptation. However, transfer learning has an inherent limitation by the fact that the training occurs on different domains separately, so that the features of the domains are not combined while training. In addition, fine-tuning is not trivial in the sense that the number of target training subjects required is unknown, but the performances of the final model are dependent to a small extend from this.

Another approach is called **unsupervised domain adversarial training**

