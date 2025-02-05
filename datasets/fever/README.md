---
language:
- en
paperswithcode_id: fever
annotations_creators:
- crowdsourced
language_creators:
- found
license:
- cc-by-sa-3.0
- gpl-3.0
multilinguality:
- monolingual
pretty_name: FEVER
size_categories:
- 100K<n<1M
source_datasets:
- extended|wikipedia
task_categories:
- text-classification
task_ids:
- text-classification-other-knowledge-verification
---

# Dataset Card for "fever"

## Table of Contents
- [Dataset Description](#dataset-description)
  - [Dataset Summary](#dataset-summary)
  - [Supported Tasks and Leaderboards](#supported-tasks-and-leaderboards)
  - [Languages](#languages)
- [Dataset Structure](#dataset-structure)
  - [Data Instances](#data-instances)
  - [Data Fields](#data-fields)
  - [Data Splits](#data-splits)
- [Dataset Creation](#dataset-creation)
  - [Curation Rationale](#curation-rationale)
  - [Source Data](#source-data)
  - [Annotations](#annotations)
  - [Personal and Sensitive Information](#personal-and-sensitive-information)
- [Considerations for Using the Data](#considerations-for-using-the-data)
  - [Social Impact of Dataset](#social-impact-of-dataset)
  - [Discussion of Biases](#discussion-of-biases)
  - [Other Known Limitations](#other-known-limitations)
- [Additional Information](#additional-information)
  - [Dataset Curators](#dataset-curators)
  - [Licensing Information](#licensing-information)
  - [Citation Information](#citation-information)
  - [Contributions](#contributions)

## Dataset Description

- **Homepage:** [https://fever.ai/](https://fever.ai/)
- **Repository:** [More Information Needed](https://github.com/huggingface/datasets/blob/master/CONTRIBUTING.md#how-to-contribute-to-the-dataset-cards)
- **Paper:** [More Information Needed](https://github.com/huggingface/datasets/blob/master/CONTRIBUTING.md#how-to-contribute-to-the-dataset-cards)
- **Point of Contact:** [More Information Needed](https://github.com/huggingface/datasets/blob/master/CONTRIBUTING.md#how-to-contribute-to-the-dataset-cards)
- **Size of downloaded dataset files:** 1677.26 MB
- **Size of the generated dataset:** 6959.34 MB
- **Total amount of disk used:** 8636.60 MB

### Dataset Summary

With billions of individual pages on the web providing information on almost every conceivable topic, we should have the ability to collect facts that answer almost every conceivable question. However, only a small fraction of this information is contained in structured sources (Wikidata, Freebase, etc.) – we are therefore limited by our ability to transform free-form text to structured knowledge. There is, however, another problem that has become the focus of a lot of recent research and media coverage: false information coming from unreliable sources. [1] [2]

The FEVER workshops are a venue for work in verifiable knowledge extraction and to stimulate progress in this direction.

It consists of claims generated by altering sentences extracted from Wikipedia and subsequently verified without knowledge of the sentence they were derived from. The claims are classified as SUPPORTED, REFUTED or NOTENOUGHINFO by annotators.

### Supported Tasks and Leaderboards

The task is verification of textual claims against textual sources.

When compared to textual entailment (TE)/natural language inference, the key difference is that in these tasks the passage to verify each claim is given, and in recent years it typically consists a single sentence, while in verification systems it is retrieved from a large set of documents in order to form the evidence.

### Languages

The dataset is in English.

## Dataset Structure

### Data Instances

#### v1.0

- **Size of downloaded dataset files:** 42.78 MB
- **Size of the generated dataset:** 38.39 MB
- **Total amount of disk used:** 81.17 MB

An example of 'train' looks as follows.
```
'claim': 'Nikolaj Coster-Waldau worked with the Fox Broadcasting Company.',
 'evidence_wiki_url': 'Nikolaj_Coster-Waldau',
 'label': 'SUPPORTS',
 'id': 75397,
 'evidence_id': 104971,
 'evidence_sentence_id': 7,
 'evidence_annotation_id': 92206}
```

#### v2.0

- **Size of downloaded dataset files:** 0.37 MB
- **Size of the generated dataset:** 0.29 MB
- **Total amount of disk used:** 0.67 MB

An example of 'validation' looks as follows.
```
{'claim': "There is a convicted statutory rapist called Chinatown's writer.",
  'evidence_wiki_url': '',
  'label': 'NOT ENOUGH INFO',
  'id': 500000,
  'evidence_id': -1,
  'evidence_sentence_id': -1,
  'evidence_annotation_id': 269158}
```

#### wiki_pages

- **Size of downloaded dataset files:** 1634.11 MB
- **Size of the generated dataset:** 6920.65 MB
- **Total amount of disk used:** 8554.76 MB

An example of 'wikipedia_pages' looks as follows.
```
{'text': 'The following are the football -LRB- soccer -RRB- events of the year 1928 throughout the world . ',
  'lines': '0\tThe following are the football -LRB- soccer -RRB- events of the year 1928 throughout the world .\n1\t',
  'id': '1928_in_association_football'}
```

### Data Fields

The data fields are the same among all splits.

#### v1.0

- `id`: a `int32` feature.
- `label`: a `string` feature.
- `claim`: a `string` feature.
- `evidence_annotation_id`: a `int32` feature.
- `evidence_id`: a `int32` feature.
- `evidence_wiki_url`: a `string` feature.
- `evidence_sentence_id`: a `int32` feature.

#### v2.0

- `id`: a `int32` feature.
- `label`: a `string` feature.
- `claim`: a `string` feature.
- `evidence_annotation_id`: a `int32` feature.
- `evidence_id`: a `int32` feature.
- `evidence_wiki_url`: a `string` feature.
- `evidence_sentence_id`: a `int32` feature.

#### wiki_pages

- `id`: a `string` feature.
- `text`: a `string` feature.
- `lines`: a `string` feature.

### Data Splits

#### v1.0

|    |train |unlabelled_dev|labelled_dev|paper_dev|unlabelled_test|paper_test|
|----|-----:|-------------:|-----------:|--------:|--------------:|---------:|
|v1.0|311431|         19998|       37566|    18999|          19998|     18567|

#### v2.0

|    |validation|
|----|---------:|
|v2.0|      2384|

#### wiki_pages

|          |wikipedia_pages|
|----------|--------------:|
|wiki_pages|        5416537|

## Dataset Creation

### Curation Rationale

[More Information Needed](https://github.com/huggingface/datasets/blob/master/CONTRIBUTING.md#how-to-contribute-to-the-dataset-cards)

### Source Data

#### Initial Data Collection and Normalization

[More Information Needed](https://github.com/huggingface/datasets/blob/master/CONTRIBUTING.md#how-to-contribute-to-the-dataset-cards)

#### Who are the source language producers?

[More Information Needed](https://github.com/huggingface/datasets/blob/master/CONTRIBUTING.md#how-to-contribute-to-the-dataset-cards)

### Annotations

#### Annotation process

[More Information Needed](https://github.com/huggingface/datasets/blob/master/CONTRIBUTING.md#how-to-contribute-to-the-dataset-cards)

#### Who are the annotators?

[More Information Needed](https://github.com/huggingface/datasets/blob/master/CONTRIBUTING.md#how-to-contribute-to-the-dataset-cards)

### Personal and Sensitive Information

[More Information Needed](https://github.com/huggingface/datasets/blob/master/CONTRIBUTING.md#how-to-contribute-to-the-dataset-cards)

## Considerations for Using the Data

### Social Impact of Dataset

[More Information Needed](https://github.com/huggingface/datasets/blob/master/CONTRIBUTING.md#how-to-contribute-to-the-dataset-cards)

### Discussion of Biases

[More Information Needed](https://github.com/huggingface/datasets/blob/master/CONTRIBUTING.md#how-to-contribute-to-the-dataset-cards)

### Other Known Limitations

[More Information Needed](https://github.com/huggingface/datasets/blob/master/CONTRIBUTING.md#how-to-contribute-to-the-dataset-cards)

## Additional Information

### Dataset Curators

[More Information Needed](https://github.com/huggingface/datasets/blob/master/CONTRIBUTING.md#how-to-contribute-to-the-dataset-cards)

### Licensing Information

FEVER license:

```
These data annotations incorporate material from Wikipedia, which is licensed pursuant to the Wikipedia Copyright Policy. These annotations are made available under the license terms described on the applicable Wikipedia article pages, or, where Wikipedia license terms are unavailable, under the Creative Commons Attribution-ShareAlike License (version 3.0), available at http://creativecommons.org/licenses/by-sa/3.0/ (collectively, the â€œLicense Termsâ€). You may not use these files except in compliance with the applicable License Terms.
```

### Citation Information

```bibtex
@inproceedings{Thorne18Fever,
    author = {Thorne, James and Vlachos, Andreas and Christodoulopoulos, Christos and Mittal, Arpit},
    title = {{FEVER}: a Large-scale Dataset for Fact Extraction and VERification},
    booktitle = {NAACL-HLT},
    year = {2018}
}
```


### Contributions

Thanks to [@thomwolf](https://github.com/thomwolf), [@lhoestq](https://github.com/lhoestq), [@mariamabarham](https://github.com/mariamabarham), [@lewtun](https://github.com/lewtun) for adding this dataset.