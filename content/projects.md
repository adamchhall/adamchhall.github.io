+++
date = '2026-02-20T14:22:52-05:00'
draft = true
title = 'Projects'
+++


Below is a list of some of the projects I have contributed to.

# Language Support for US Elections
Section 203(b) of the Voting Rights Act (VRA) requires some places to make voting materials 
available in languages other than English. The US Census Bureau determines whether a jurisdiction, 
e.g., county, is subject to such requirements based on the rates of limited English language proficiency
and illiteracy within language minority groups (LMGs), in that jurisdiction. Since 2011, 
Section 203 determinations have been based on estimates from small-area models to compensate 
for low sample sizes in some areas. I have made several contributions to research that 
aims to improve these models. Examples include:
* [Statistical Methodology (2021) for Voting Rights Act, Section 203 Determinations](https://www.census.gov/library/working-papers/2022/adrm/RRS2022-06.html)
* [Small area estimates for Voting Rights Act Section 203(b) coverage determinations](https://journals.sagepub.com/doi/10.1177/00080683231215985)
* [Inference with Polya-Gamma Augmentation for US Election Law](https://www.mdpi.com/2227-7390/13/6/945)
* [A Machine Learning Approach for Counting Language Minority Groups in the United States](https://www.census.gov/library/working-papers/2025/adrm/RRS2025-03.html)
* [A Random Forest Approach for Counting Language Minority Groups in the United States]()

# The Ranking Project
It is common to see listicles ranking cities, states, or countries on some criteria or another. 
Typically, these rankings are derived from survey data, and do not take into account uncertainty 
in the ranking of the estimates due to sampling error. [The Ranking Project](https://www.census.gov/topics/research/stat-research/ranking.html) 
aims to find more effective ways to understand and communicate the uncertainty around such rankings to the public.
As a member of the ranking project team, I've made contributions to writing backend code for the 
following research visualizations of the uncertainty in the rankings of US states based on survey data 
from the American Community Survey (or ACS):
* [Estimated Rankings of All States](https://www.census.gov/csrm/rankings/)
* [Comparisons of A State with Each Other State](https://www.census.gov/csrm/comparisons/)

# Generalizing Tsao \& Wright's Maximum Ratio
Researchers often have multiple estimates of the same unknown quantity, but don't know
whether all of them are good. In response to this concern, 
[Tsao and Wright (1983)](https://www.tandfonline.com/doi/abs/10.1080/00031305.1983.10483139) 
proposed a method called the “maximum ratio test” that flags groups of estimates when one is 
“too far” from the truth. This method requires very few assumptions, but can be diﬀicult to interpret. 
This project aims to address this problem by generalizing the maximum ratio test to higher dimensional 
versions that can be used when a parameter and its estimates are vectors, and by proposing useful heuristics
that can be used to help interpret the results in practical contexts.
* [Interpreting and Extending the Maximum Ratio Test of Unacceptability](https://www.census.gov/library/working-papers/2024/adrm/RRS2024-07.html)
* [Maximum Norm Ratio Test](https://www.census.gov/library/working-papers/2025/adrm/RRS2025-01.html)

# Disclosure Avoidance and Privacy Protection
Drawing valid statistical inference based on privacy protected data has been the topic of
rigorous research at the US Census Bureau and other statistical agencies. The need to
develop appropriate statistical methods based on perturbed or synthetic data rather than
the original data stems from the fact that sometimes the original microdata are sensitive and
cannot be released due to privacy considerations. What the statistical agencies will release
instead is a synthetic version of the original data, hiding any confidential or sensitive parts.
* [Inference about a Binomial Proportion under Privacy Protection](https://www.census.gov/library/working-papers/2026/adrm/RRS2026-01.html)
* [Inference about a Binomial Proportion under Privacy Protection (IJSS)](https://doi.org/10.3329/ijss.v26il.*****)

# Price Index Research
I have contributed to research studying novel price indices and other methods to measure
differences in purchasing power by using computer-generated retail scanner data sets 
to compensate for the absence of sufficiently detailed pricing data in the national 
accounts. 
* [Unified Price Indices for Spatial Comparisons (My Dissertation)](/documents/FullDissertationThesis.pdf)
