## Element/Ca ratios reveal Phylogenetic Relationships in Modern Cnidarians 

  Element-to-calcium (X/Ca) ratios, measured in marine organisms such as foraminifera, coral, and mollusks, are frequently used as geochemical proxies for paleoclimate reconstructions. Whereas X/Ca ratios in abiotic calcium carbonate reflect the abundance of those elements in ambient seawater (as well as water temperature), X/Ca ratios in biominerals are often distinct from the surrounding seawater. These so-called “vital effects” describe the biological control that calcifying organisms exhibit over their internal environment during the calcification process (Blamart et al., 2007; Cohen and Gaetani, 2011). While vital effects can elucidate interesting properties of the biomineralization process, they often obstruct the use of X/Ca ratios as paleoclimate proxies. Some studies have attempted to circumvent this issue by quantifying species-specific calibrations between X/Ca ratios and the environmental variable in question, however this can only be accomplished if the species in question is extant  (Trotter et al., 2011). The fact that these calibrations are species-specific implies that phylogeny impacts X/Ca ratios and, by extension, suggests that the trace elements incorporated into biominerals can be correlated with an organism’s taxonomy and evolutionary history (Edgar et al., 2017). The present study aims to examine a suite of X/Ca ratios in extant cnidaria in order to test the hypothesis that X/Ca ratios in biomineralizers are linked to an organism’s evolutionary history.


***

## Introduction 

  Marine biomineralizers utilize a variety of minerals to build their skeletons. For example, many foraminifera and radiolarians have silica-based skeletons, whereas corals more commonly build their skeletons using the polymorphs of calcium carbonate: aragonite and calcite. There is ample evidence suggesting that the evolution of skeletal mineralogy was heavily influenced by shifting global seawater composition, specifically the shifting between calcite and aragonite seas in the Ediacaran-Cambrian periods (Figure 1, Porter, 2007; Gilbert et al., 2022). But even as bulk ocean composition transformed over time, skeletal mineralogy of various phyla did not evolve to reflect the new thermodynamically preferential polymorph, demonstrating what some have called ‘deep resilience’ (Gold and Vermeij, 2023). 
Deep resilience is thought to be influenced by an organism’s energy budget, or how much energy that organism must expend in order to perform various functions required for survival (Vermeij, 2020). Changing ocean conditions impact the energy budget required for survival, and it has been suggested that species with enhanced resilience may be able to more easily offset energetic costs associated with changing conditions such as acidification (Gold and Vermeij, 2023). It stands to reason, then, that different groupings of organisms could have evolved calcification mechanisms that compliment the unique ocean conditions at the time of their evolution. This concept was examined by Edgar et al. (2017), who analyzed planktonic foraminiferal 𝛿13C and 𝛿18O values spanning 107 million years. These authors demonstrated that the species-specific vital effects of  𝛿13C are impacted by evolutionary history of the macroperforate foraminiferal species of the Cenozoic. It seems probable, then, that vital effects of trace element ratios could be a result of residual evolutionary pressures that impacted an organism’s biomineralization mechanisms at the time of evolution (Edgar et al., 2017). In order to robustly test this hypothesis, we must determine the degree to which we can link skeletal trace element composition to taxonomy in modern taxa.
  It has been demonstrated that X/Ca ratios can be linked to taxa at the phylum level (Ulrich et al., 2021), but it is unknown if finer scale taxonomic resolution can be achieved. The present study has chosen to use a suite of modern cnidarians on which to conduct geochemical analyses that may enable rigorous classification of taxa at lower taxonomic levels. 


There is some dataset that we can use to help solve this problem. This allows a machine learning approach. This is how I will solve the problem using supervised/unsupervised/reinforcement/etc. machine learning.

We did this to solve the problem. We concluded that...

## Data

Here is an overview of the dataset, how it was obtained and the preprocessing steps taken, with some plots!

![](assets/IMG/datapenguin.png){: width="500" }

*Figure 1: Here is a caption for my diagram. This one shows a pengiun [1].*

## Modelling

Here are some more details about the machine learning approach, and why this was deemed appropriate for the dataset. 

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

