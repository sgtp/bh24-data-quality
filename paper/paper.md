---
title: 'On the value of data (#BioHackJP version)'
title_short: 'a collaborative experiment on data evaluation'
tags:
  - data strategy
  - data quality
  - data economics
authors:
  - name: Andrea Splendiani
    orcid: 0000-0000-0000-0000
    affiliation: IQVIA
  - name: Erick Antezana
    orcid: 0000-0000-0000-0000
    affiliation: United Nations
  - name: Achille Zappa
    orcid: 0000-0000-0000-0000
    affiliation: TBD
  - name: Yasunori Yamamoto
    orcid: 0000-0000-0000-0000
    affiliation: DBCLS

date: 30 August 2022
cito-bibliography: paper.bib
event: BioHack24JP
biohackathon_name: "BioHackathon Japan 2024"
biohackathon_url:   "https://biohackathon-europe.org/"
biohackathon_location: "Fukushima, Japan, 2024"
group: Project 26
# URL to project git repo --- should contain the actual paper.md:
git_url: https://github.com/biohackrxiv/publication-template
# This is the short authors description that is used at the
# bottom of the generated paper (typically the first two authors):
authors_short: Andrea Splendiani \emph{et al.}
---


# Preface

This the version a collaborative paper "on the value of data", that has been iterated at the BioHackathon in Fukushima, 2024.

# Introduction
What is the value of a data asset?
It’s a simple question, somehow abstract and hard to answer, as the value of a data depends on its use, and can be somehow subjective. 
However, this is not unique to data, and it’s a question that we are called to answer quite frequently, if implicitly, as we routinely need to make decisions about data (what to acquire, qhat to discard, what to curate,...)
If we think in terms of FAIR data, the question is how much FAIR is fair enough (and when), and you can’t answer this question without a notion of value.
This document attempts to sketch a framework to conduct data evaluation, in the view of driving data related decisions.
To focus and simplify the thinking, we consider that the value of a dataset resides in its use to answer a question (one or more business or research questions). 

## What is data ?
We consider here data as an information asset in its broader sense (not only the representation of such information), extending its meaning to all additional information and context that can be itself represented in a data artifact (in principle we would include all layers of the DKW [DKW] mode here, insofar they can be represented as an artifact of service that we need to evaluate).
To this respect, and as noted in [EMA], we don’t make a distinction between data and metadata as, from the point of view of delivering value, both are needed and integrated: “42” won’t have any value unless it’s known what it represents. Furthermore, from a technical perspective, the boundary between data and metadata is quite fluid, e.g.L in self describing standards.

Arguably how much metadata is needed is not a fundamentally different question from: how much data or how much precision is needed.

## What is value ?
In its abstract meaning, value is a potential of something to deliver some utility of any sort (material, or even subjective). In practical terms, often value is associated with an “evaluation” resulting in a number, so that different items can be in some way compared vs their respective utility.
In simple terms, we can think that a dataset A is more valuable than B if, for a given use and all conditions being equal, A would be preferred to B.
In this document we consider value as the result of an evaluation that takes place to drive data management decisions (e.g.: data acquisition, retention, curation…)
To avoid confusion, we call distinct but related concepts to value:
Price is an evaluation done in financial terms with the focus on balancing the utility of producers and buyers of a given good.
Cost is the evaluation of the resources needed to generate (or acquire) a given asset.
It is also worth noting that value is dynamic, as it changes both in relation to the assets evolution, and its contex

## General approaches to data evaluation
A review of current approaches for data evaluation can be found in [R1]. This distinguish between three main models to evaluate data:
- **Market driven**: related to the cost of making a dataset, the sale price of an overall data asset, or the evaluation of oa company whose primary focus is data generation.
- **Economic impact based**: related to the estimated impact of the availability of such data for an overall economy.
- **Dimensional based**: estimating the impact of a given dataset to a business, via metrics defined based on datasets dimensions.
Of these, we consider the third category more adequate to take data investment decisions by part of an organization. Market driven models can provide a lower and upper floor for viability, but they really make sense only if data is effectively purchased or sold.
Economic impact models are more suited to policy decisions, as they don’t easily capture the economic impact for a given organization investing in data.

## Data evaluation strategy
In devising an approach for data evaluation, we consider the following steps:
- A qualification of the context in which a dataset is used
- Dimensions that contribute to the value of data
- What is measurable about such dimensions
- How these can be combined into metrics
The intention of this document is not to define finalized and applicable metrics, but to provide an approach to devise some, and to provide a “thought experiment” validation that the approach makes sense.




This document use Markdown and you can look at [this tutorial](https://www.markdowntutorial.com/).

## Subsection level 2

Please keep sections to a maximum of only two levels.

## Tables and figures

Tables can be added in the following way, though alternatives are possible:

Table: Note that table caption is automatically numbered and should be
given before the table itself.

| Header 1 | Header 2 |
| -------- | -------- |
| item 1 | item 2 |
| item 3 | item 4 |

A figure is added with:

![Caption for BioHackrXiv logo figure](./biohackrxiv.png)

# Other main section on your manuscript level 1

Lists can be added with:

1. Item 1
2. Item 2

# Citation Typing Ontology annotation

You can use [CiTO](http://purl.org/spar/cito/2018-02-12) annotations, as explained in [this BioHackathon Europe 2021 write up](https://raw.githubusercontent.com/biohackrxiv/bhxiv-metadata/main/doc/elixir_biohackathon2021/paper.md) and [this CiTO Pilot](https://www.biomedcentral.com/collections/cito).
Using this template, you can cite an article and indicate _why_ you cite that article, for instance DisGeNET-RDF [@citesAsAuthority:Queralt2016].

The syntax in Markdown is as follows: a single intention annotation looks like
`[@usesMethodIn:Krewinkel2017]`; two or more intentions are separated
with colons, like `[@extends:discusses:Nielsen2017Scholia]`. When you cite two
different articles, you use this syntax: `[@citesAsDataSource:Ammar2022ETL; @citesAsDataSource:Arend2022BioHackEU22]`.

Possible CiTO typing annotation include:

* citesAsDataSource: when you point the reader to a source of data which may explain a claim
* usesDataFrom: when you reuse somehow (and elaborate on) the data in the cited entity
* usesMethodIn
* citesAsAuthority
* citesAsEvidence
* citesAsPotentialSolution
* citesAsRecommendedReading
* citesAsRelated
* citesAsSourceDocument
* citesForInformation
* confirms
* documents
* providesDataFor
* obtainsSupportFrom
* discusses
* extends
* agreesWith
* disagreesWith
* updates
* citation: generic citation


# Results


# Discussion

...

## Acknowledgements

...

## References
