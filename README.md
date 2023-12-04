**Kira's ML Project Website** <img align="right" width="220" height="220" src="/assets/IMG/template_logo.png">

## TITLE 

  Element-to-calcium (X/Ca) ratios, measured in marine organisms such as foraminifera, coral, and mollusks, are frequently used as geochemical proxies for paleoclimate reconstructions. Whereas X/Ca ratios in abiotic calcium carbonate reflect the abundance of those elements in ambient seawater (as well as water temperature), X/Ca ratios in biominerals are often distinct from the surrounding seawater. These so-called “vital effects” describe the biological control that calcifying organisms exhibit over their internal environment during the calcification process (Blamart et al., 2007; Cohen and Gaetani, 2011). While vital effects can elucidate interesting properties of the biomineralization process, they often obstruct the use of X/Ca ratios as paleoclimate proxies. Some studies have attempted to circumvent this issue by quantifying species-specific calibrations between X/Ca ratios and the environmental variable in question, however this can only be accomplished if the species in question is extant  (Trotter et al., 2011). The fact that these calibrations are species-specific implies that phylogeny impacts X/Ca ratios and, by extension, suggests that the trace elements incorporated into biominerals can be correlated with an organism’s taxonomy and evolutionary history (Edgar et al., 2017). The present study aims to examine a suite of X/Ca ratios in extant cnidaria in order to test the hypothesis that X/Ca ratios in biomineralizers are linked to an organism’s evolutionary history.

***

## Introduction 

  Marine biomineralizers utilize a variety of minerals to build their skeletons. For example, many foraminifera and radiolarians have silica-based skeletons, whereas corals more commonly build their skeletons using the polymorphs of calcium carbonate: aragonite and calcite. There is ample evidence suggesting that the evolution of skeletal mineralogy was heavily influenced by shifting global seawater composition, specifically the shifting between calcite and aragonite seas in the Ediacaran-Cambrian periods (Figure 1, Porter, 2007; Gilbert et al., 2022). But even as bulk ocean composition transformed over time, skeletal mineralogy of various phyla did not evolve to reflect the new thermodynamically preferential polymorph, demonstrating what some have called ‘deep resilience’ (Gold and Vermeij, 2023). 
Deep resilience is thought to be influenced by an organism’s energy budget, or how much energy that organism must expend in order to perform various functions required for survival (Vermeij, 2020). Changing ocean conditions impact the energy budget required for survival, and it has been suggested that species with enhanced resilience may be able to more easily offset energetic costs associated with changing conditions such as acidification (Gold and Vermeij, 2023). It stands to reason, then, that different groupings of organisms could have evolved calcification mechanisms that compliment the unique ocean conditions at the time of their evolution. This concept was examined by Edgar et al. (2017), who analyzed planktonic foraminiferal 𝛿13C and 𝛿18O values spanning 107 million years. These authors demonstrated that the species-specific vital effects of  𝛿13C are impacted by evolutionary history of the macroperforate foraminiferal species of the Cenozoic. It seems probable, then, that vital effects of trace element ratios could be a result of residual evolutionary pressures that impacted an organism’s biomineralization mechanisms at the time of evolution (Edgar et al., 2017). In order to robustly test this hypothesis, we must determine the degree to which we can link skeletal trace element composition to taxonomy in modern taxa.
  It has been demonstrated that X/Ca ratios can be linked to taxa at the phylum level (Ulrich et al., 2021), but it is unknown if finer scale taxonomic resolution can be achieved. Ultimately, we aim to utilize a large geochemical dataset with 8-10 X/Ca ratios measured in 12 species of modern cnidarians spanning 3 coral types - scleractinians, octocorals, and hydrocorals. While the preparation of that full dataset is underway, we can utilize an unsupervised machine learning approach (KMeans) on a smaller set of coralline geochemical data to explore if the data are clustering according to phylogeny within one coral type – scleractinians. This course project serves as a small part of what will later be developed into a supervised learning classification problem. 
	The data used here was collected several years ago by some members of the Eagle-Tripati lab, namely Ilian DeCorte and Maxence Guillermic, measured using inductively coupled plasma optical emission spectroscopy (ICP-OES). The dataset includes six coral species that can be divided into in five separate families representing 2 evolutionary “clades” (with Siderastreidae having species representation in both clades). Ten X/Ca ratios are represented (Li/Ca, B/Ca, Mg/Ca, Sr/Ca, U/Ca, Cd/Ca, Ba/Ca, Na/Ca, Mn/Ca, and Al/Ca). 

Table 1: Summary of dataset taxa
| Coral Type   | Clade    | Family          | Species                      |
|--------------|----------|-----------------|------------------------------|
| Scleractinian| Robust   | Pocilloporidae  | P. damicornis, S. pistillata |
|              |          | Mussidae        | Ps. strigosa                 |
|              | Complex  | Poritidae       |Po. astreoides                |
|              |          | Agariciidae     | U. tenuifolia                |
|              |  Split   | Siderastreidae | S. siderea                    |

## Modelling
_Dataset Preprocessing_
The dataset had a total of 279 NaN values, 256 of which came from the Al/Ca, Mn/Ca, and Na/Ca features. The large swaths of missing values for these features was likely due to machine error, which is common in geochemical analyses. For this reason, the ratios Al/Ca, Mn/Ca, and Na/Ca were dropped from the analysis. That left a total of 23 NaN values. In order to avoid losing any more statistical power, I chose to estimate the missing values using the K-Nearest Neighbors Imputation from sklearn.impute with n = 3. 

I first ran through the entire experiment without removing any outliers, but it quickly became clear that outliers were severely impacting the clustering algorithm. I then identified outliers using z-scores. When removed from the dataset, the number of samples was reduced from 236 to 215, leaving us with 1,505 total data points. 



The model might involve optimizing some quantity. You can include snippets of code if it is helpful to explain things.

```python
from sklearn.ensemble import ExtraTreesClassifier
from sklearn.datasets import make_classification
X, y = make_classification(n_features=4, random_state=0)
clf = ExtraTreesClassifier(n_estimators=100, random_state=0)
clf.fit(X, y)
clf.predict([[0, 0, 0, 0]])
```

This is how the method was developed.

## Results

Figure X shows... [description of Figure X].

## Discussion

From Figure X, one can see that... [interpretation of Figure X].

## Conclusion

Here is a brief summary. From this work, the following conclusions can be made:
* first conclusion
* second conclusion

Here is how this work could be developed further in a future project.

## References
[1] DALL-E 3

[back](./)
