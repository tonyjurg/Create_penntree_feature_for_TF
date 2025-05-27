[![Project Status: WIP – Initial development is in progress, but there has not yet been a stable, usable release suitable for the public.](https://www.repostatus.org/badges/latest/wip.svg)](https://www.repostatus.org/#wip) [![License: CC BY 4.0](https://img.shields.io/badge/License-CC_BY%204.0-lightgrey.svg)](https://creativecommons.org/licenses/by/4.0/)

# Create penntree feature for Text-Fabric

This repository contains the Jupyter Notebook used to create three new Text-Fabric feature:

   - [pentree](https://tonyjurg.github.io/N1904addons/features/pentree.html): Penn tree like syntax tree.

The final feature files will be added to the package available at the [tonyjurg/N1904addons](https://tonyjurg.github.io/N1904addons/) repository.

## Example 

The following example shows the penn tree generated whenn passing the feature data to [nltk](https://www.nltk.org/): 

```text
from nltk import Tree
ptbString=F.penntree.v(sentenceNode)
tree = Tree.fromstring(ptbString)
tree.pretty_print()  # console-style print   
                                               S                                 
                                               |                                  
                                               WG                                
            ___________________________________|_________________                 
           CL                                                    |               
    _______|________________                                     |                
   |                      NP-SBJ                                 |               
   |        ________________|_____________                       |                
   |       |       |                      CL                     |               
   |       |       |         _____________|____                  |                
  VP-V     |       |       VP-V              PP-ADV              CL              
   |       |       |        |         _________|______       ____|____________    
  VERB    NOUN   PUNCT     VERB     PREP      NOUN  PUNCT  NOUN PRON  NOUN  PUNCT
   |       |       |        |        |         |      |     |    |     |      |   
ἐγένετο ἄνθρωπος   ,   ἀπεσταλμένος παρὰ      θεοῦ    ,   ὄνομα αὐτῷ ἰωάνης   ·  
```

## Production notebook

You can view the production notebook on [nbviewer.org](https://nbviewer.org/github/tonyjurg/Create_penntree_feature_for_TF/blob/main/create_penn_tree.ipynb).

Alternative, you can also download it from the [GitHub repository](https://github.com/tonyjurg/Create_penntree_feature_for_TF/blob/main/create_penn_tree.ipynb).

## Attribution and footnotes

The following resources were consulted for creating the notebook:

- [Penn Treebank Tag Guidelines PDF](https://catalog.ldc.upenn.edu/docs/LDC99T42/tagguid1.pdf)
- [NLP @ Univ. of Pennsylvania](https://alliance.seas.upenn.edu/~nlp) (note: the original homepage of the Penntree bank project is gone.)
- [Building a Large Annotated Corpus of English: The Penn Treebank ](https://alliance.seas.upenn.edu/~nlp/publications/pdf/marcus1993.pdf)
- [The Penn treebank: an overview](https://www.researchgate.net/publication/2873803_The_Penn_Treebank_An_overview)

The Greek base text is from Nestle1904 Greek New Testament, edited by Eberhard Nestle, published in 1904 by the British and Foreign Bible Society:
> Nestle, Eberhard. Η Καινή Διαθήκη Novum Testamentum Graece (New York: Fleming H. Revell Company, 1904).
The 1913 reprint is available [here](https://archive.org/details/hkainediathekete00lond/), which was transcribed by [Diego Santos](https://sites.google.com/site/nestle1904/home). All this material is in Public domain.


The [N1904-TF dataset](https://centerblc.github.io/N1904/) available under [MIT license](https://github.com/CenterBLC/N1904/blob/main/LICENSE.md). Formal reference: 
> Tony Jurg, Saulo de Oliveira Cantanhêde, & Oliver Glanz. (2024). *CenterBLC/N1904: Nestle 1904 Text-Fabric data*. Zenodo. DOI: [10.5281/zenodo.13117911](https://doi.org/10.5281/zenodo.13117910).

## License

This notebook is released under the [Creative Commons Attribution 4.0 International (CC BY 4.0)](https://github.com/tonyjurg/Create_penntree_feature_for_TF/blob/main/LICENSE.md)

## Citation

If you use this repository in your academic work, please [cite it](CITATION.cff).
