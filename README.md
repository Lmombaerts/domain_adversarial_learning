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

Another approach is called **unsupervised domain adversarial training** relies on domain invariant features to achieve good domain adaptation. There are several methods:

- Discriminator framework
- Partial transfer learning (assuming that the target domain is a subset of the source domain)
- Using associations between the source and target domains (e.g. increasing correlation / coveriance, subspace alignment)

Of the commonly used adversarial training approaches, domain adversarial training of neural network (DANN) has been applied to several baseline architectures and is explored on multiple datasets, and has been shown to be succesful on task-specific domain adaptation.


## What is the DANN model?

The DANN model consists of a feature extractor network with a domain predictor and a label predictor. The adversarial training of the domain predictor is achieved using a gradient-reserval layer, placed between the feature extractor and the domain prediction, optimising the features and shared weights.

(Alternatively, a domain unlearning (DU) approach was proposed, which involves learning the domain prediction for a fixed feature representation, and then minimizing the domain shift between features, resulting in a maximal domain confusion that is equally uninformative across domains)