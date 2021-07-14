# Biomedical Question Answering Datasets

This is a list of datasets for biomedical question answering tasks. As for the classifications of approach, content, and format, we follow the settings in [*Biomedical Question Answering: A Comprehensive Review*](https://arxiv.org/abs/2102.05281).

![overview](https://github.com/Andy-jqa/biomedical-qa-datasets/blob/main/overview.png)

| Dataset               | Size                      | Metric                      | SOTA                                                     | Approach              | Content     | Format                      |
| --------------------- | ------------------------- | --------------------------- | -------------------------------------------------------- | --------------------- | ----------- | --------------------------- |
| [BioASQ Task B Phase A](#bioasq-task-b) | 3.7k                      | MAP                         | 33.04 (document) / 68.21 (snippet)                       | IR | Scientific  | Retrieval                   |
| [BiQA](#biqa)         | 7.4k                      | MAP                         |                                                          | IR | Consumer    | Retrieval                   |
| [EPIC-QA](#epic-qa)   | 45                        | MAP                         |                                                          | IR | Sci. & Con. | Retrieval                   |
| [HealthQA](#healthqa) | 7.5k                      | MAP                         | 87.88                                                    | IR | Consumer    | Retrieval                   |
| [TREC Genomics](#trecgenomics) | 28 (06), 36 (07)          | MAP                         | 54.39 (06) / 32.86 (07)                                  | IR | Scientific  | Retrieval                   |
| [BioASQ Task B Phase B](#bioasq-task-b) | 3.7k                      | F1; MRR; List F1; Manual    | 90.3; 39.7; 52.3; 4.39/5                                 | MRC                   | Scientific  | Y/N; Extraction; Generation |
| [Biomed-Cloze](#biomed-cloze) | 1M                        |                             |                                                          | MRC                   | Scientific  | Extraction                  |
| [BioRead](#bioread) | 16.4M | Acc | 47.06 (dev) / 51.52 (test) | MRC | Scientific | Extraction |
| [BioMRC](#biomrc)   | 812k                      | Acc                         | 80.06 (dev) / 79.97 (test)                               | MRC                   | Scientific  | Extraction                  |
| [BMKC](#bmkc)         | 473k (T); 370k (LS)       | Acc                         | T: 85.5 (val) / 83.6 (test); LS: 80.1(val) / 77.3 (test) | MRC                   | Scientific  | Extraction                  |
| [CliCR](#clicr)      | 100k                      | EM; F1                      | 55.2; 59.8                                               | MRC                   | Clinical    | Extraction                  |
| [COVIDQA](#covidqa)   | 124                       | P@1; R@3; MRR               | 30.6; 47.7; 41.5                                         | MRC                   | Scientific  | Extraction                  |
| [COVID-QA](#covid-qa) | 2k                        | EM; F1                      | 37.2; 64.7                                               | MRC                   | Scientific  | Extraction                  |
| [EBMSummariser](#ebmsummariser) | 456                       | ROUGE-1,2,SU4               | 39.85; 24.50; 22.59                                      | MRC                   | Clinical    | Generation                  |
| [emrQA](#emrqa)       | 455k                      | EM; F1                      | 76.1; 81.7                                               | MRC                   | Clinical    | Extraction                  |
| [MASH-QA](#mash-qa)   | 34.8k                     | EM; F1                      | 29.49; 64.94                                             | MRC                   | Consumer    | Extraction                  |
| [MEDHOP](#medhop)    | 2.5k                      | Acc                         | 63.2                                                     | MRC                   | Scientific  | Multi-choice                |
| [MEDIQA-AnS](mediqa-ans) | 552 (single); 156 (multi) | ROUGE-1,2,L; BLEU           | Extractive: 29; 15; 12; 9; Abstractive: 32; 12; 8; 9     | MRC                   | Consumer    | Generation                  |
| [MEDIQA-QA](#mediqa-qa) | 3k                        | Acc; P; MRR                 | 79.49; 84.02; 96.22                                      | MRC                   | Consumer    | Multi-choice                |
| [ProcessBank](#processbank) | 585                       | Acc                         | 66.7                                                     | MRC                   | Scientific  | Multi-choice                |
| [PubMedQA](#pubmedqa) | 212k                      | Acc; F1                     | 68.08; 52.72                                             | MRC                   | Scientific  | Y/N                         |
| [QA4MRE-Alz](#qa4mre-alz) | 40                        | c@1                         | 76                                                       | MRC                   | Scientific  | Multi-choice                |
| [Bioinformatics](#bioinformatics) | 30                        | F1                          | 60.0                                                     | KB                    | Scientific  | Generation                  |
| [QALD-4 task 2](#qald-4-task-2) | 50                        | F1                          | 99.0                                                     | KB                    | Consumer    | Generation                  |
| [PathVQA](#pathvqa) | 32.8k                     | Acc; BLEU-1; BLEU-2; BLEU-3 | 68.2; 32.4; 22.8; 17.4                                   | VQA                   | Clinical    | Generation                  |
| [VQA-Med](#vqa-med)   | 15.3k                     | Acc; BLEU                   | 64.0; 65.9                                               | VQA                   | Clinical    | Generation                  |
| [VQA-Rad](#vqa-rad)   | 3.5k                      | Acc                         | 60.0 (open) / 79.3 (close)                               | VQA                   | Clinical    | Generation                  |
| [ChiMed](#chimed) | 24.9k | Acc | 98.32 (rel.) / 84.24 (adopt.) |  | Consumer | Multi-choice |
| [cMedQA](#cmedqa) | 54k | P@1 | 65.35 (dev) / 64.75 (test) |  | Consumer | Multi-choice |
| [cMedQA v2](#cmedqa) | 108k | P@1 | 72.1 (dev) / 72.1 (test) |  | Consumer | Multi-choice |
| [HEAD-QA](#head-qa) | 6.8k | Acc | 44.4 (supervised) / 46.7 (unsupervised) |  | Examination | Multi-choice |
| [LiveQA-Med](#liveqa-med) | 738 | avgScore | 82.7 |  | Consumer | Generation |
| [MedQA](#medqa) | 235k | Acc | 75.8 (dev) / 75.3 (test) |  | Examination | Multi-choice |
| [MEDQA](#medqa) | 61k | Acc | MC: 69.3 (dev) / 70.1 (test); TW: 42.2 (dev) / 42.0 (test); US: 36.1 (dev) / 36.7 (test) |  | Examination | Multi-choice |
| [NLPEC](#nlpec) | 2.1k | Acc | 71.1 (dev) / 61.8 (test) |  | Examination | Multi-choice |
| [webMedQA](#webmedqa) | 63k | P@1, MAP | 66.0, 79.5 |  | Consumer | Multi-choice |

## BioASQ Task B

## BiQA

BiQA is an IR BQA dataset containing 7.4k questions and 14.2k relevant PubMed articles collected from online QA forums (Stack Exchange and Reddit). 

Access: https://github.com/lasigeBioTM/BiQA

## EPIC-QA

The Epidemic Question Answering (EPIC-QA) challenges are formatted as IR BQA, where the participants return a ranked list of sentences from expert-level (Task A) or consumer-level (Task B) corpora to answer approximately 45 questions about the COVID-19 pandemic.

Access: https://bionlp.nlm.nih.gov/epic_qa/

## HealthQA

HealthQA has 7.5k manually annotating questions that can be answered by one of the 7.3k articles scrapped from the [Patient](https://patient.info/) website.

Article: Ming Zhu, Aman Ahuja, Wei Wei, and Chandan K. Reddy. 2019. A Hierarchical Attention Retrieval Model for Healthcare Question Answering. In *The World Wide Web Conference* (San Francisco, CA, USA) (*WWW ’19*). Association for Computing Machinery, New York, NY, USA, 2472–2482. https://doi.org/10.1145/3308558.3313699

## TREC Genomics

The TREC Genomics Tracks in 2006 and 2007 tackle the BQA with IR approach: 28 and 36 topic questions (e.g.: “What [GENES] are genetically linked to alcoholism?") are released in 2006 and 2007, respectively, and the participating systems are required to retrieve passages from 162k full-text articles from [Highwire Press](https://www.highwirepress.com/)

Article: William Hersh, Aaron Cohen, Lynn Ruslen, and Phoebe Roberts. 2007. TREC 2007 Genomics Track Overview. In *TREC 2007*.

Access: https://trec.nist.gov/

## Biomed-Cloze

Biomed-Cloze is a automatically constructed cloze dataset created from PubMed academic papers (for the BioASQ challenge), consisting of 1M clozes. From analyzing the cloze data manually, the authors were able to answer 80% times for the PubMed set using the information in the passage. 

Article: Bhuwan Dhingra, Danish Danish, and Dheeraj Rajagopal. 2018. Simple and Effective Semi-Supervised Question Answering. In *Proceedings of the 2018 Conference of the North American Chapter of the Association for Computational Linguistics: Human Language Technologies, Volume 2 (Short Papers)*. Association for Computational Linguistics, New Orleans, Louisiana, 582–587. https://doi.org/10.18653/v1/N18-2092

## BioRead

BioRead is a publicly available cloze-style biomedical machine reading comprehension (MRC) dataset with approximately 16.4 million passage-question instances. Biomedical journal articles were used to construct BioRead and MetaMap was employed to identify UMLS concepts. The authors also provided a subset of BioRead, called BioReadLite, with 900k instances, for groups with fewer computational resources

Article: Dimitris Pappas, Ion Androutsopoulos, and Haris Papageorgiou. 2018. BioRead: A New Dataset for Biomedical Reading Comprehension. In *Proceedings of the Eleventh International Conference on Language Resources and Evaluation (LREC 2018)*. European Language Resources Association (ELRA), Miyazaki, Japan. https://www.aclweb.org/anthology/L18-1439

Access:  http://nlp.cs.aueb.gr/software.html

## BioMRC

BIOMRC is a new dataset for biomedical MRC that can be viewed as an improved version of BioREAD. Compared to the previous dataset, care was taken to reduce noise. To avoid crossing sections, extracting text from references, captions, tables etc., the authors used abstracts and titles of biomedical articles as passages and questions, respectively, which are clearly marked up in PUBMED data, instead of using the full text of the articles. They also released two versions of BioMRC, LARGE and LITE, containing 812k and 100k instances respectively for researchers with more or fewer resources, along with the 60 instances (TINY) humans answered.

Article: Dimitris Pappas, Petros Stavropoulos, Ion Androutsopoulos, and Ryan McDonald. 2020. BioMRC: A Dataset for Biomedical Machine Reading Comprehension. In *Proceedings of the 19th SIGBioMed Workshop on Biomedical Language Processing*. Association for Computational Linguistics, Online, 140–149. https://www.aclweb.org/anthology/2020.bionlp-1.15

Access:  http://nlp.cs.aueb.gr/publications.html

## BMKC

BioMedical Knowledge Comprehension (BMKC) is a large cloze-style dataset which consists of Biomedical Knowledge Comprehension Title (BMKC_T) and Biomedical Knowledge Comprehension Last Sentence (BMKC_LS). PubMed corpus was used to construct the dataset, which can be employed to train deep neural network models.

Article: Seongsoon Kim, Donghyeon Park, Yonghwa Choi, Kyubum Lee, Byounggun Kim, Minji Jeon, Jihye Kim, Aik Choon Tan, and Jaewoo Kang. 2018. A pilot study of biomedical text comprehension using an attention-based deep neural reader: Design and experimental analysis. *JMIR medical informatics* 6, 1 (2018), e2.

Access: https://www.webcitation.org/6wBRhfS7o

## CliCR

CliCR is a dataset for machine comprehension in the medical domain. For the dataset, the authors constructed queries, answers and supporting passages from BMJ Case Reports, the largest online repository of such documents. CliCR contains around 100,000 queries on 12,000 case reports, has long support passages (around 1,500 tokens on average) and includes answers which are single- or multi-word medical entities.

Article: Simon Šuster and Walter Daelemans. 2018. CliCR: a Dataset of Clinical Case Reports for Machine Reading Comprehension. In *Proceedings of the 2018 Conference of the North American Chapter of the Association for Computational Linguistics: Human Language Technologies, Volume 1 (Long Papers)*. Association for Computational Linguistics, New Orleans, Louisiana, 1551–1563. https://doi.org/10.18653/v1/N18-1140

Access: http://github.com/clips/clicr

## COVIDQA

COVIDQA is a QA dataset specifically designed for COVID-19. It has 124 question-article pairs translated from the literature review page of Kaggle’s COVID-19 Open Research Dataset Challenge 15, where relevant information for each category or subcategory in the review is presented.

Article: Raphael Tang, Rodrigo Nogueira, Edwin Zhang, Nikhil Gupta, Phuong Cam, Kyunghyun Cho, and Jimmy Lin. 2020. Rapidly Bootstrapping a Question Answering Dataset for COVID-19. *arXiv preprint arXiv:2004.11339 (2020)*.

Access: http://covidqa.ai/

## COVID-QA

COIVD-QA is a COVID-19 QA dataset with 2k question-answer pair annotated by biomedical experts. The annotation is similar to that of SQuAD while the answers in COVID-QA tend to be longer as they generally come from longer texts.

Article: Timo Moller, Anthony Reina, Raghavan Jayakumar, and Malte Pietsch. 2020. COVID-QA: A Question Answering Dataset for COVID-19. https://openreview.net/forum?id=JENSKEEzsoU

Access: https://github.com/deepset-ai/COVID-QA

## EBMSummariser

EBMSummariser is a summarization dataset of 456 instances for EBM, from the Clinical Inquiries section of the Journal of Family Practice16: each instance contains a clinical question, a long “bottom-line" answer, the answer’s evidence quality and a short justification of the long answer.

Article: Diego Mollá, María Elena Santiago-Martínez, Abeed Sarker, and Cécile Paris. 2016. A corpus for research in text processing for evidence based medicine. *Language Resources and Evaluation* 50, 4 (2016), 705–727.

Access: http://sourceforge.net/projects/ebmsumcorpus/

## emrQA

## MASH-QA

## MEDHOP

## MEDIQA-AnS

## MEDIQA-QA

## ProcessBank

## PubMedQA

## QA4MRE-Alz

## Bioinfomatics

## QALD-4 task 2

## PathVQA

## VQA-Med

## VQA-Rad

