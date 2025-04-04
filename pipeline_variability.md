---
layout: default
title: Pipeline Variability
nav_order: 80
---

# Diffusion MRI Pipeline Variability
*A project looking at the consistency of hub locations across different diffusion MRI processing pipelines*
- [Paper (OA)](https://direct.mit.edu/netn/article/7/4/1326/116174/Can-hubs-of-the-human-connectome-be-identified)
- [Data](https://bridges.monash.edu/collections/Degree_Variability/6352886/1)
- [Code](https://github.com/NSBLab/DegreeVariability)


## Aims
In this project, we sought to compare the effects of different choices at key steps in the dMRI pipeline on properties of hub connectivity in a normative cohort of 294 healthy young adults. We evaluated the effects of each of these choices on measures of binary and weighted node degree, given that these measures are fundamental to many other network measures and to the definition of network hubs (Oldham et al., 2019). In particular, we focussed on both the distribution of degree measures across nodes and their spatial topography, evaluating the consistency with which hubs are localized to the same anatomical positions.

## Materials and Methods
We evaluated effects of four factors in individual connectome reconstruction (paper Figure 1). Three pertain to the tractography workflow (probabilistic versus deterministic algorithm, propagation constraints, streamline seeding; a total of 10 options for comparison) and the last pertains to parcellation (4 options). Then, as group-representative connectomes are commonly used in the literature, we also considered how the aforementioned factors interact with different group-aggregation methods (4 options) and thresholds (11 options). The different options examined at each step resulted in 1760 different group-representative connectomes. 

## Results
### Statistical properties of node degree distributions
Paper Figure 2 shows how properties of the node strength distributions vary as a function of parcellation and tractography parameters. All pipeline variations qualitatively show some evidence of skewness and a heavy tail. The DK68 and HCP360 parcellations show the largest positive skews, whereas the S200 and S500 parcellations show much smaller tails, consistent with a lower likelihood of finding very highly connected hubs. The exception is the use of Pipeline 3 (ACT/WM seeding/FACT), which shows an extended tail across all parcellations. 

### Topographical properties of node degree
Paper Figure 3 shows correlation matrices representing the similarity in spatial location of hubness between tractography workflows. Hierarchical agglomerative clustering of these matrices was used to group similar pipelines together. With the S200 parcellation as an example, there are substantial differences in the node strength correlation between pairs of pipelines, spanning the range $-0.11 < \rho < 1.00$, with an average of 0.47.
 
Paper Figure 4 shows how the spatial distribution of node strengths varies across pipelines and parcellations. First, for a fixed parcellation (e.g., the S200 parcellation), the location of putative hubs varies considerably across maps under different processing variations. When using deterministic tractography (FACT), the highest strength nodes are located in the vicinity of the paracentral lobule and supplementary motor area, in comparison to the hubs located in primary visual areas when using probabilistic tractography (iFOD2).

### The effect of variations in regional surface area
The effects of parcellation on node strength seem, in some cases at least, related to the node surface area (here, node surface area is defined as the average surface area of the given node across all participants). For instance, the most skewed strength distributions were observed for the DK68 and HCP360 parcellations, which have a much wider variance in regional surface areas than the S200 and S500 parcellations. Moreover, the medial PFC in the DK68 parcellation falls under the superior_frontal_gyrus anatomical label, which is largest region in this parcellation.

Paper Figure 5A shows spatial maps of node strengths obtained for two example parcellation and pipeline combinations (S200 + GWM/dynamic seeding/iFOD2 and HCP360 + ACT/GMWMI/FACT) and Figure 5B shows the scatterplot of the association between node surface area and strength for each. Across all processing and parcellation combinations, the correlations between node strength and node surface area spanned the range $0.10 < r < 0.96$, with a median of 0.82. Correlations for pipelines using probabilistic tractography (iFOD2) were all above $r = 0.78$ with a median correlation coefficient of 0.88. This high correlation persists regardless of thresholding algorithm or connection density.


## Conclusions
We found that, across all the investigated pipelines, evidence of concentrated connectivity in hubs (i.e., degree distribution properties that differ from the exponential case) was apparent in only a minor fraction of pipeline variations. When relying on node strength to define hubs, variations in tractography algorithm and parcellation had a much greater effect than changes in group reconstruction method and connection density. The use of binary degree yielded a less pronounced concentration of connectivity in network hubs and the resulting connectomes are more sensitive to connection density. When considering the spatial topography of hubs, the choice between probabilistic and deterministic tractography resulted in the largest difference and, in some circumstances, led to anti-correlated weighted degree sequences. Finally, although hubs were often the regions with the largest surface area, particularly in weighted connectomes, removal of this dependence of degree on region size generally retained a similar hub topography. Together, these findings raise concerns about the consistency with which hubs can be identified in the literature and suggest that careful consideration must be paid to preprocessing choices when mapping connectomes with diffusion MRI. 

