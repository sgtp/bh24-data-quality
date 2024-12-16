---
title: 'On the value of data (#BioHackJP version)'
title_short: 'a collaborative experiment on data evaluation'
tags:
  - data strategy
  - data quality
  - data economics
authors:
  - name: Andrea Splendiani
    orcid: 0000-0002-3201-9617
    affiliation: 1
  - name: Erick Antezana
    orcid: 0000-0002-2497-8236
    affiliation: 2
  - name: Achille Zappa
    orcid: 0000-0003-4040-9620
    affiliation: 3
  - name: Yasunori Yamamoto
    orcid: 0000-0002-6943-6887
    affiliation: 4
affiliations:
  - name: IQVIA, CH
    index: 1
  - name: United Nations, ES 
    index: 2
  - name: Soka University, JP
    index: 3
  - name: DBCLS, JP
    index: 4 

date: 30 August 2022
cito-bibliography: paper.bib
event: BioHack24JP
biohackathon_name: 'BioHackathon Japan 2024'
biohackathon_url:   'https://biohackathon.org'
biohackathon_location: 'Fukushima, Japan, 2024'
group: Project 26
git_url: 'https://github.com/sgtp/bh24-data-quality/edit/main/paper/paper.md'
authors_short: 'Andrea Splendiani \emph{et al.}, on the value of data (#BioHackJP version)'

---


# Preface

This the version a collaborative paper "on the value of data", that resulted from the discussions at the BioHackathon in Fukushima, 2024.
The live version of this document can be found at [@citation:valueOfData].

# Introduction
What is the value of a data asset?

This is a simple question, quite intuitive to formulate, but that is somehow abstract and hard to answer, as the value of a data depends on its use, or it is even subjective. 
It is however a question that we are called to answer quite frequently, if implicitly, as we routinely need to make decisions about data (what to acquire, qhat to discard, what to curate,...). And the difficulty of putting a value on something is not unique to data.
If we think in terms of FAIR data, it is important to determine how much FAIR is fair enough, and it is impossible to answer this question without a notion of value.
This document attempts to sketch a framework to conduct data evaluation, in the view of driving data related decisions.
To simplify the task, we focus on a value of a dataset as its utility to answer a question (one or more business or research questions). 

## What is data ?
We consider here data as an information asset in its broader sense (not only the representation of such information), extending its meaning to all additional information and context that can be itself represented in a data artifact (in principle we would include all layers of the DKW [@citation:DKW] mode here, insofar they can be represented as an artifact of service that we need to evaluate).
To this respect, and as noted in [@citation:EMADQF], we don’t make a distinction between data and metadata as, from the point of view of delivering value, both are needed and integrated: “42” won’t have any value unless it’s known what it represents. Furthermore, from a technical perspective, the boundary between data and metadata is quite fluid, as for instance self describing standards naturally combine both aspects.

Arguably how much metadata is needed is not a fundamentally different question from: how much data or how much precision is needed.

## What is value ?
In its abstract meaning, value is a potential of something to deliver some utility of any sort (material, or even subjective). In practical terms, often value is associated with an “evaluation” resulting in a number, so that different items can be in some way compared vs their respective utility.
In simple terms, we can think that a dataset A is more valuable than B if, for a given use and all conditions being equal, A would be preferred to B.
In this document we consider value as the result of an evaluation that takes place to drive data management decisions (e.g.: data acquisition, retention, curation…)
To avoid confusion, we recall distinct but related concepts to value:
Price is an evaluation done in financial terms with the focus on balancing the utility of producers and buyers of a given good.
Cost is the evaluation of the resources needed to generate (or acquire) a given asset.
It is also worth noting that value is dynamic, as it changes both in relation to the assets evolution, and its contex.

## General approaches to data evaluation
A review of current approaches for data evaluation can be found in [@citation:Fleckenstein2023]. This distinguishes between three main models to evaluate data:

  - **Market driven**: related to the cost of making a dataset, the sale price of an overall data asset, or the evaluation of a company whose primary focus is data generation.
  - **Economic impact based**: related to the estimated impact of the availability of such data for an overall economy.
  - **Dimensional based**: estimating the impact of a given dataset to a business, via metrics defined based on datasets dimensions.
    
Of these, we consider the third approach as more adequate to take data investment decisions by an organization. Market driven models can provide a lower and upper floor for viability, but they really make sense only if data is effectively purchased or sold.
Economic impact models are more suited to policy decisions, as they don’t easily capture the economic impact for a given organization investing in data.

## Data evaluation strategy
In devising an approach for data evaluation, we consider the following steps:
- A qualification of the context in which a dataset is used
- Dimensions that contribute to the value of data
- What is measurable about such dimensions
- How these can be combined into metrics
The intention of this document is not to define finalized and applicable metrics, but to provide an approach to devise some, and to provide a “thought experiment” validation that the approach makes sense.

# The context (purpose) of data use
Obviously, data is valuable insofar it has a (possibly potential) purpose, e.g.: to generate new insights, or for instance to validate an hypothesis. Therefore in order to assess the value of data we need to characterize how data relates to its usage to address a given purpose. 
We can, in a first approximation, consider a “question” (e.g.: a research question, or a business question) as the “purpose” of a dataset.
We can then break down how we characterize such a question, and how we characterize the relation of a dataset to such a question, as well as the life cycle of such question.
Can we then identify some “typical and relative” patterns for such questions, corresponding to different classes, or contexts, of use?

## Aspects characterizing the business need
One way to characterise a "data question" is based on its relation to its intended usage in a business, by considering:
### Breadth
Whether the use of data is specific to a given question, or just explorative.
  - **Specific**. Data is intended to be used to answer one specific question.
  - **Thematic**. Data is intended to be used to answer a range of related questions.
  - **Explorative**. Data is not intended to answer a specific question, but rather availble for exploration.
### Question life cycle
Where a question is in its life cycle:
  - **Initiating**. The question the data is called to answer is in the its initial phases, vs delivering value.
  - **Mature**. The question the data is called to answer is routinely delivering value.
  - **Phase-out**. The question the data is called to answer is being phased out.

## Aspects characterizing the usage of data to address a business need
Another way to characterise data is how it relates to the business question.
### Competitiveness
Whether the data is providing a competitive advantage in answering a qustion (with the implication that there is value in data that others don’t have access to).
  - **Competitive**: Data is contributing value by providing information that others don’t have (sub-case: having it earlier than others). Example: latest news.
  - **Non-competitive**: There is no particualar value in data being exclusive to a user. 
  - **Synergistic**:  Data is providing value by being shared with others. Example: reference data, where the more this is shared, the more data integration costs are minimized.
### Recurrence
The relation between purpose and time.
Another possible category is the “life-span”. Is the task a once-only task, or a repeated task?
- **One-off**. The utility of the data is for a specific question, after which data need would need to be re-evaluated
- **Repeated**. The question this data is called to answer is recurrent. We could further distinguish whether in this case information is time-sensitive or not (e.g.: whether queries are about information in real time or not).
### Restrictivness
Whether data usage is in a confidential context and is restricted in the way it can be applied to answer questions, or not (e.g.: some data may be tied to a question due to consent restriction, some data may not be linked to other data due to privacy restrictions)..
- **Restricted**
- **Public**

## Relations of a dataset to a purpose
Another category is in what ways a dataset contributes to answer a business question.
### Relatedness
How the dataset relates to a specific investigation. One way to think about this is to have a set of levels by which data assets can be ordered:
Necessary and sufficient. This data asset is all that is needed to clearly address a purpose (e.g.: needs a list of addresses per postcodes in a country, this could be in a single data asset from the government)
- **Necessary**. Without this asset a purpose could not be addressed, but the dataset may not be sufficient (e.g.: weather forecast is necessary for airplane traffic planning).
- **Relevant**. There is some established potential for a dataset to address a purpose, but this is still only a conjecture.
- **On topic**. There is no clear link between this dataset and a given task, except that the dataset is “on topic”. E.g.: for the objective of computing food calories, the dataset is about regional food recipes.
**Unrelated**. The dataset is in principle unrelated to the task at hand (e.g.: a food recipe dataset for weather forecast)
### Generation
Whether the dataset is generated for a specific task, or if it is “re-used”.
- **Primary whether**. the dataset is generated on purpose for a given topic
- **Secondary**. whether a dataset, generated for another use case, can be repurposed
- **A-priori**. whether a dataset is provided independently from use cases.
### Role
- **Generic input**. The dataset is intended to provide information that directly or indirectly answer the question.
- **Training**. The dataset is intended to be used for training.
- **Test**. The dataset is intended to be used for testing.
- **Validation**. The dataset is intended to be used for validation.
## Data Life cycle
Where data stands its generation life cycle. Any assessment or qualification of a data in its value needs to be related to the project stage when it has been produced and its generation and role.
Usually any project as three stages:  
- **Initiation**
- **Maturity**
- **Phase-out / legacy support**


## Definition of characteristic contexts
We have defined several aspects to characterize a data usage context, or question, here reported for readability:
- The breadth of the question (Specific, Thematic, Explorative)
- The relation of the dataset to a given question:
-- The competitive advantage of a dataset (Competitive, non-competitive, Synergistic)
-- The recurrence of a data use (One-off, repeated))
-- The restrictions on the use of a dataset (restricted, public)
-- The relatedness to the question (Necessary and sufficient, necessary, relevant, on topic, unrelated)
-- The generation of the dataset in relation to a question (primary, secondary, a-priori)
-- The role of a dataset in answering the question (Generic input, training, test, validation)
- The life cycle of a question (initiation, maturity, phase out)

Different combinations of the above define different scenarios under which data can be valued differently: the value of data being standardized, for instance, is intuitively more valuable if this is used for exploration in the context of other data, than in a one-off data analysis. 

We proceed now to identify some archetypical scenarios or contexts.

There could be different criteria for defining such contexts. We could think in terms of type of information (e.g.: laboratory data vs reports), or in terms of communities (cfr. FAIRmetrics).
As a first tentative, we consider some combination of the above aspects.

First we could for instance assess how relatedness supports different breadth of queries. E.g.: answering the question: would a dataset that ”necessary and sufficient”, “necessary”, “related” address the need of a query that is “specific”, “broad”, “explorative”?
An assessment is reported in the following table.


| |Specific|Thematic|Explorative|
| ------ | ----- | ----- | ----- |
| Necessary and sufficient | Yes | N/A |N/A |
| Necessary | Yes | N/A | N/A |
| Relevant | Little | Yes | Yes |
| On topic |Very little | Little | Yes |
| Unrelated | No| No| Little |


From this can we identify, with some simplification, four contexts reported below:


**1) specific-necessary**

| |Specific|
|-----|-----|
|Necessary and sufficient|Yes|
|Necessary| Yes|

Well defined task, essential relation of the data to the task. In brief, we call this: specific-necessary

**2) specific-additional**

||Specific|
|-----|-----|
|Relevant|Little|
|On topic|Very little|


Well defined task, additional data. In brief, we call this: specific-additional (this context capture scenario where some information may hold some value, for validation, cross-referencing or perhaps in unexpected ways).

### 3) thematic

||Thematic|
|-----|-----|
|Relevant|Yes|
|On topic|Little|

Non defined task, but clear range of questions asked. We can this simply thematic 

### 4) explorative

||Explorative|
|-----|-----|
| Relevant|Yes|
|On topic|Yes|
|Unrelated|Little|

Non defined questions. Typical purpose is data mining. We call this simply explorative.

We can now try to assess in which ways these context relate to the data life-span, or more in general their relation to sustainability:


||one-off|repeated|repeated/time critical|
|-----|-----|-----|-----|
|specific-necessary|Yes|redundant?|Yes|
|specific-additional|Yes|redundant?|unlikely|
|thematic|No|Yes|In some cases|
|explorative|unlikely|Yes|Low interest|

And from combining these two tables we can derive a set of contexts:

- **Specific-necessary-non-tc**: There is a specific question for which the data under discussion is necessary (perhaps even sufficient). This may be one-off or repeated over time. Time is not critical, meaning that the question itself is not about the most up to date information.
- **Specific-necessary-tc**: There is a specific question for which the data under discussion is necessary (perhaps even sufficient). This may be one-off or repeated over time. Time is critical: the question itself is about the most up to date information (e.g.: what are the latest information on a topic?)
- **Specific-additional-non-tc**: There is one specific question to be answered, and this data is not necessary but maybe useful. Non time sensitive (as for the above definition)
- **Thematic-repeated**: There is a range of related questions on a coherent topic. In general, these don’t focus on “real time data”/
- **Thematic-repeated-tc**: There is a range of related questions on a coherent topic, which is intrinsically related to real time data.
- **Explorative-repeated**: No specific question, data is used for exploration (cfr. Fishing expedition).


# Dimensions that contribute to the value of data

## Novelty/delta respect to other sources 
Not an absolute measure, but any additional piece of knowledge will be more valuable as it adds new information to what is already known. Note that in some cases extra data may only be noise.
### “real-time”-ness
Whether the information (time dependent) is relative to the “current” time. For instance, data feeds monitoring real-world entities (e.g.: weather, traffic, stock-market) have an intrinsic value the more this information is real-time and not delayed. This can be seen as a delta respect to knowledge that becomes more widely available in time.
### uniqueness
Is this the only source for this information? Or are multiple sources available? This can be seen as a delta respect to other agents.

## Quality  
The value of data is clearly related to its quality, as in:
### truth  
Where data is true or accurate. Traceability may be part of this. “Truth” is in principle hard to establish, as what we can measure is really consistency (e.g.: respect to experimental evidence).
### “completeness”
Whether data lacks missing values. Is there a reference?

Note: several aspects of quality could probably be quantified numerically (e.g.: by sampling a dataset).

## Usability
Data will be more valuable the more “usable” it is. Usability can have different sub-aspects.
### Standardization
The more the data is represented following standards, the more it is easier (or at all possible) to integrate.
### Interrelation
The more data has link to other data, the more it is easier (or at all possible) to integrate and contextualise it.

## Amount
The value of a data asset may be in some way proportional to how much information is there:
## extensiveness
In terms of coverage of a domain. If we are considering for instance a dataset about publications relevant for a specific domain, extensiveness could be captured by the amount of publications in the dataset, respect to the estimate of the total amount of publications available on the subject. 
It should be feasible to have a normalised value (e.g.: in [0,1]) for this measure.
## detail
In terms of depth of detail. We can capture, for a dataset, the average of how many distinct structured data items this presents. But it’s a discretionary value as the granularity of a data element is undefined. Plus it cannot be easily normalised (as detail itself is a recursive concept).

## information content
Could we have an “entropy like” measure of the information content of a data asset, perhaps respect to some prediction potential?

## Interpretability
Do we need to acknowledge DIKW model here?
Sometimes people think data themselves are a set of inorganic things aligned with a given structure. Information would be something semantic.
Cf. https://www.ontotext.com/knowledgehub/fundamentals/dikw-pyramid/

## Sustainability
Whether we know that a dataset is going to be kept up to date or not.
### Curation model
Who is in charge of the data cleansing? Is it the provider (source), the consumer or a third party? Is there a model where curation is shared among users in a pre-competitive space? (possibly maximizing value).

### Freshness
Independently of curation, not all types of data hold value through time in the same way. For instance weather forecasts are continuously updated. An superseded forecast has no value (to the point that it’s not even meaningful to retain it as a reference). On the other hand reference data or historical data maye holds its value forever (e.g.: data about the world population over the years is not affected by time).



# What can be measured?
For each of the factors that influence data value, what can we measure? We can distinguish what we could measure “in principle” from what we could measure “in practice”. We can also provide an indication on what type this measure could be (e.g.: normalised? qualitative?). Note that measures should be relative to the data itself, not to usage contexts. In general, measures relate to a point in time (as the state of global knowledge changes in time, so some of these measures will).
Novelty


## Novelty
| | Theoretical measures | Practical measures | Measure type | Notes |
|----------------------|----------------------|--------------------|--------------|-------|
| “Real-time”-ness | % of new information respect the whole body | - For each dataset, delta vs previous versions - Same domain? Same originator? |Numeric normalised.|
| Uniqueness | Inverse of the number of sources that present the same information. Maybe this is non-linear (the difference between an information being shared between 2 or 3 resources is more than between 10 or 11) | Yes/No? | ?| Can we really assess this? It would imply that all information is reconciled. |

## Quality
| | Theoretical measures | Practical measures | Measure type | Notes |
|----------------------|----------------------|--------------------|--------------|-------|
| Truth | Almost impossible! | - Sampling/error rate - % of information with provenance -Amount of citations/derivations | % of information with provenance ||
| Completeness | % of filled fields, respect to a global consensus of required fields | % of filled fields respect to the dataset definition | Numeric, normalised. ||


## Usability
| |Theoretical measures | Practical measures | Measure type | Notes |
|----------------------|----------------------|--------------------|--------------|-------|
| Standardization | ? | Percentage of values from ontologies shared by one or more of other independent resources | Could be a normalised numeric, although perfection would not be 1 (you cannot be standard for information for which standards have yet to be defined) |
| Interrelation | ? | Percentage of identifiers linked to one of more independent resources | Could be a normalised numeric, although perfection would not be 1(not everything can be linked) |

## Extensiveness
| |Theoretical measures | Practical measures | Measure type | Notes |
|----------------------|----------------------|--------------------|--------------|-------|
| Amount | This could be an absolute measure, or relative (e.g.: respect to a number of entities in the world) | - Number of statements - Percentage of entities covered - Total amount of entities covered | Absolute, or normalised. | Nonlinear correction needed: arguably not all facts have the same weight and there is tradeoff between quantity and complexity of obtaining information |
| Detail | ? | Average number of statement per entity | Absolute? |Nonlinear correction needed|

## Maintenance
|| Theoretical measures | Practical measures | Measure type | Notes |
|----------------------|----------------------|--------------------|--------------|-------|
| We can define some curation categories: curation once, continuous curation. Maybe for these the amount of “coverage” in terms of entities. An alternative approach would be to think in terms of MM/data. Maybe each curation-model has its own metrics. |-  Presence of evidence codes? - N. of tickets opened/closed - N. of messages on mailing lists? | ? ||
| Freshness | Yes/No, maybe with a fuzzy assessment | ? | ? ||




# Toward a development of metrics
What contributes to data value in each context?
One first step is to assess which dimensions are more relevant to data value for each of the identified contexts
One way to address this is to ask the question: in a context, would I “sacrifice” one factor for another? (it is still be a bit subjective, at least at this stage, but the process helps in being more consistent).
Basically, for each context, we can fill a trade-off matrix as below:

Trade-off matrix example:


| |Novelty/time| Quality/truth| Quality/completeness| Usability/standardization| Usability/interrelation| Amount/extensivity| Amount/detail|Maintenance/curation model| Maintenance/freshness| Novelty/time|
|------|------|------| ------| ------| ------| ------|------| ------| ------|-----|
|Novelty/uniq|No question||||||||||
|Quality/truth|trade?|No question||||||||||
|Quality/completeness|trade?|trade?|No question||||||||
|Usability/standardization|trade?|trade?|trade?|No question|||||||
|Usability/interrelation|trade?|trade?|trade?|trade?|No question||||||
|Amount/extensivity|trade?|trade?|trade?|trade?|trade?|No question|||||
|Amount/detail|trade?|trade?|trade?|trade?|trade?|trade?|No question||||
|Maintenance/curation model|trade?|trade?|trade?|trade?|trade?|trade?|trade?|No question|||
|Maintenance/freshness|trade?|trade?|trade?|trade?|trade?|trade?|trade?|trade?|No question||
|Novelty/time|trade?|trade?|trade?|trade?|trade?|trade?|trade?|trade?|trade?|trade?|No question|

Elements on the diagonal are excluded from a trade-off questions, and we indicate a trade question only for part of the matrix as answers are symmetric.

For the sake of simplicity, we can aggregate dimensions at the higher level, as follow:

Would I trade x for y?
||Novelty|Quality|Usability|Amount|Maintenance|Score|
|-----|-----|-----|-----|-----|-----|-----|
|Novelty||No|||||
|Quality|Yes||No|?|Yes|-1|
|Usability|||||||
|Amount|||||||
|Maintenance|||||||

Here we also introduce a simple score for each dimension, defined as follows: for each row, we add 1 each time we find a “No” (would not trade for another factor), -1 if ‘Yes” and we keep the value unvaried in case of dubious or undefined cases.
We can then use the resulting value to sort the factors in order of relevance, for a given context.

We can follow this approach to prioritize aspects for each contexts.

## Context: Specific-necessary-non-tc

|Would I trade x for y?|Novelty|Quality|Usability|Amount|Maintenance|Score|
|-----|-----|-----|-----|-----|-----|-----|
|Novelty||Yes|No|?|Yes|-1|
|Quality|No||No|?|!|2|
|Usability|Yes|Yes||Yes|Yes|-4|
|Amount|?|?|No||?|1|
|Maintenance|No|!|No|?||2|


#### Ranking
1. Quality/Maintenance
2. Amount
3. Novelty
4. Usability

## Specific-necessary-tc

|Would I trade x for y?|Novelty|Quality|Usability|Amount|Maintenance|Score|
|-----|-----|-----|-----|-----|-----|-----|
|Novelty||No|No|No|No|4|
|Quality|Yes||Yes|?|!|-2|
|Usability|Yes|No||Yes|Yes|-2|
|Amount|Yes|?|No||?|0|
|Maintenance|Yes|!|No|?||0|

### Ranking
1. Novelty
2. Amount/Maintenance
3. Quality/Usability


## Specific-additional-non-tc

|Would I trade x for y?|Novelty|Quality|Usability|Amount|Maintenance|Score|
|-----|-----|-----|-----|-----|-----|-----|
|Novelty||Yes|Yes|Yes|Yes|-4|
|Quality|No||No|?|!|2|
|Usability|No|Yes||?|No|1|
|Amount|No|?|?||?|1|
|Maintenance|No|!|Yes|?||0|

### Ranking
1. Quality
2. Usability/Amount
3. Maintenance
4. Novelty

## Thematic-repeated

|Would I trade x for y?|Novelty|Quality|Usability|Amount|Maintenance|Score|
|-----|-----|-----|-----|-----|-----|-----|
|Novelty||?|Yes|Yes|No|-1|
|Quality|?||No|?|!|1|
|Usability|No|Yes||?|No|1|
|Amount|No|?|?||Yes|0|
|Maintenance|Yes|!|Yes|No||-1|

### Ranking
1. Quality, Usability
2. Amount
3. Novelty, maintenance

## Thematic-repeated-tc

|Would I trade x for y?|Novelty|Quality|Usability|Amount|Maintenance|Score|
|-----|-----|-----|-----|-----|-----|-----|
|Novelty||No|No|No|No|4|
|Quality|Yes||Yes|?|!|-2|
|Usability|Yes|No||?|No|1|
|Amount|Yes|?|?||Yes|1|
|Maintenance|Yes|!|Yes|No||-1|


### Ranking
1. Novelty
2. Usability
3. Amount, Maintenance
4. Quality

## Explorative-repeated

|Would I trade x for y?|Novelty|Quality|Usability|Amount|Maintenance|Score|
|-----|-----|-----|-----|-----|-----|-----|
|Novelty||Yes|Yes|Yes|Yes|-4|
|Quality|No||?|Yes|!|0|
|Usability|No|?||No|?|2|
|Amount|No|No|Yes||?|1|
|Maintenance|No|!|?|?||1|

### Ranking
1. Usability
2. Amount, maintenance
3. Quality
4. Novelty

# Reality check: a thought experiment 
As a (rather extreme) thought experiment, we can consider a data evaluation problem, sketch some metrics, and apply the above thinging, to see if the resulting data evaluation is at least consistent, in that it doesn’t lead to nonsensical conclusions.

The problem that we are considering is the evaluation of data curation strategies: given three different scenarios, what curation strategy leads to the highest value of data per moeny invested? We focus on the relative value of curation strategies in these scenarios as this provides a "measure" abstract enough that can compensate the noise deriving from all assumption we made, and still provide for some intuitive evaluation of results.

## Conditions
- A dataset consists of annotations of 10k genes (out of a total of 30k), in free text.
- We consider an investment of a nominal value of 100.
- An automatic process to standardize data to ontologies costs 0.01 x gene, with an error rate of 10%.
- A manual curation costs 0.1 x gene, with an error rate of 1%.
- Annotation of an extra gene costs 10 x gene.

We want to evaluate the gain in value of different strategies in different scenarios:

## Strategies
- Automatic curation
- Manual curation
- Extra annotation

## Scenarios
- Specific-annotation-tc
- Specific-annotation-non-tc
- Explorative-repeated


## Metrics and values
### Novelty
In this case we can consider a delta respect to the whole body of knowledge. We only compute the additional absolute value for this feature. For the three strategies, we have:

|Strategy||
|-----|-----|
|Automatic curation|0|
|Manual curation|0|
|Extra annotation|10/30000=0.0003|

In the above, we considered that an investment of 100 can result in the annotation of 10 extra genes, that correspond to an increase of 0.0003% in the overall body of knowledge (metric for novelty).

Starting state: 0.

### Quality
The percentage of correct information. We consider all initial statements true and only the post-curation state.

|Strategy||
|-----|-----|
|Automatic curation|39000/40000=0.975|
|Manual curation|30990/31000=0.999|
|Extra annotation|30010/30010=1|

e.g.: automatic curation is delivering 9k new correct data points.

Starting state: 1

### Usability
We consider the number of ontology annotations respect to the whole.

|Strategy||
|-----|-----|
|Automatic curation|10000/30000=0.33|
|Manual curation|1000/30000=0.033|
|Extra annotation|10/3000=0.0033|

Starting state: 0

#### Amount
We consider the coverage of the domain.

|Strategy||
|-----|-----|
|Automatic curation|10000/30000=0.33|
|Manual curation|10000/30000=0.33|
|Extra annotation|10010/30000=0.33|

### Maintenance
We don’t consider this.

## Combining single metrics
We consider the order of relevance for each scenario:

|scenario|1st factor|2nd factor|3rd factor|4th factor|
|-----|-----|-----|-----|-----|
|Specific-necessary-tc|Novelty|Amount|Quality / Usability |
|Specific-necessary-non-tc|Quality|Amount|Novelty|Usability|
|Explorative-repeated|Usability|Amount|Quality|Novelty|
|factor weight|8|4|2|1|


We start with an extremely crude approach, we sum all values, modifying them via a constant that is based on the ranking. We map the order of relevance to a power of two, so that a metric will weight double the following metrics in order of least relevance (totally arbitrary). Addition will not result in anything sensibly normalized. Overall, we want to see only if this leads us to counterintuitive results or not.


## Results

||Automatic curation|Manual curation|Extra annotation|
|-----|-----|-----|-----|
||Nov.:0 Qual:0.975 Us:0.33 Am: 0.33|Nov.:0 Qual:0.999 Us:0.033 Am:0.33|Nov.:0.0003 Qual:1 Us:0.0033 Am:0.33|
|Specific-necessary-tc (1000*Nov+100*Am+10*Qual+10*Us)|3.6|3.351|3.3257|
|Specific-necessary-non-tc (1000*Qual+100*Am+`10*Nov+1*Us)|9.45|9.345|9.3233|
|Explorative-repeated (1000*Us+100*Am+10*Qual+1*Nov.)|5.91|3.582|3.3467|



Does this make any sense?

We see as in all cases the automatic curation results as the best strategy, albeit by a higher margin in the explorative scenario. Intuitively, we should expect that in an exploratory scenario, extensiveness somehow trumps quality, as not all data will be relative to a question, and at least some curation will help finding relevant, maybe imperfect, information (which is better than no information at all).
However we would imagine the reverse to hold in scenarios where data is directly relevant to answer a question, even more so when additional (novel) information provides a competitive advantage.
On a close look though, it is true that under our assumptions about costs, manual curation or extra annotation simply don’t add enough data, respect to the whole (note that we reason a-priori respect to the relevance of some specific information).
At the very least this experiment gave us a way to reflect on the price point at each some strategy (thought to be advantageous) actually provides value.

This is clearly very preliminary work, but at least it provides the outline of an approach to develop value metrics for data.




...

## Acknowledgements

...

## References
