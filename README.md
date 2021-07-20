# Biomedical Question Answering Datasets

A summary of biomedical QA datasets surveyed in our paper [Biomedical Question Answering: A Comprehensive Review](https://arxiv.org/abs/2102.05281).

![overview](https://github.com/Andy-jqa/biomedical-qa-datasets/blob/main/overview.png)

| Dataset               | Size                      | Metric                      | SOTA                                                     | Approach              | Content     | Format                      | Last Update           |
| --------------------- | ------------------------- | --------------------------- | -------------------------------------------------------- | --------------------- | ----------- | --------------------------- | --------------------------- |
| [BioASQ Task B Phase A](#bioasq-task-b) | 3.7k                      | MAP                         | 33.04 (document) / 68.21 (snippet)                       | IR | Scientific  | Retrieval                   | 2021.3             |
| [BiQA](#biqa)         | 7.4k                      | MAP                         | -- | IR | Consumer    | Retrieval                   | 2021.3             |
| [EPIC-QA](#epic-qa)   | 45                        | MAP                         | -- | IR | Sci. & Con. | Retrieval                   | 2021.3             |
| [HealthQA](#healthqa) | 7.5k                      | MAP                         | [87.88](https://doi.org/10.1145/3308558.3313699)        | IR | Consumer    | Retrieval                   | 2021.3             |
| [TREC Genomics](#trec-genomics) | 28 (06), 36 (07)          | MAP                         | [54.39 (06) / 32.86 (07)](https://doi.org/10.1007/s10791-008-9076-6) | IR | Scientific  | Retrieval                   | 2021.3             |
| [BioASQ Task B Phase B](#bioasq-task-b) | 3.7k                      | F1, MRR, List F1, Manual | [90.3, 39.7, 52.3, 4.39/5](https://link.springer.com/chapter/10.1007/978-3-030-58219-7_16) | MRC                   | Scientific  | Y/N; Extraction; Generation | 2021.3 |
| [Biomed-Cloze](#biomed-cloze) | 1M                        | -- | -- | MRC                   | Scientific  | Extraction                  | 2021.3            |
| [BioRead](#bioread) | 16.4M | Acc | [47.06 (dev) / 51.52 (test)](https://www.aclweb.org/anthology/L18-1439) | MRC | Scientific | Extraction | 2021.3 |
| [BioMRC](#biomrc)   | 812k                      | Acc                         | [80.06 (dev) / 79.97 (test)](https://www.aclweb.org/anthology/2020.bionlp-1.15) | MRC                   | Scientific  | Extraction                  | 2021.3            |
| [BMKC](#bmkc)         | 473k (T); 370k (LS)       | Acc                         | [T: 85.5 (val) / 83.6 (test); LS: 80.1(val) / 77.3 (test)](https://medinform.jmir.org/2018/1/e2?utm_source=TrendMD&utm_medium=cpc&utm_campaign=JMIR_TrendMD_0) | MRC                   | Scientific  | Extraction                  | 2021.3            |
| [CliCR](#clicr)      | 100k                      | EM, F1                     | [55.2, 59.8](https://dspace.mit.edu/handle/1721.1/127443) | MRC                   | Clinical    | Extraction                  | 2021.3            |
| [COVIDQA](#covidqa)   | 124                       | P@1, R@3, MRR             | [30.6](https://www.aclweb.org/anthology/2020.coling-industry.9), [47.7](https://doi.org/10.18653/v1/2020.nlpcovid19-2.14), [41.5](https://arxiv.org/abs/2004.11339) | MRC                   | Scientific  | Extraction                  | 2021.3            |
| [COVID-QA](#covid-qa) | 2k                        | EM, F1                     | [37.2, 64.7](https://arxiv.org/abs/2012.01414)          | MRC                   | Scientific  | Extraction                  | 2021.3            |
| [EBMSummariser](#ebmsummariser) | 456                       | ROUGE-1,2,SU4               | [39.85, 24.50, 22.59](https://www.aclweb.org/anthology/C16-1050) | MRC                   | Clinical    | Generation                  | 2021.3            |
| [emrQA](#emrqa)       | 455k                      | EM, F1                     | [76.1, 81.7](https://ui.adsabs.harvard.edu/abs/2020arXiv200402288R/abstract) | MRC                   | Clinical    | Extraction                  | 2021.3            |
| [MASH-QA](#mash-qa)   | 34.8k                     | EM, F1                     | [29.49, 64.94](https://doi.org/10.18653/v1/2020.findings-emnlp.342) | MRC                   | Consumer    | Extraction                  | 2021.3            |
| [MEDHOP](#medhop)    | 2.5k                      | Acc                         | [63.2](https://ieeexplore.ieee.org/abstract/document/9203847/) | MRC                   | Scientific  | Multi-choice                | 2021.3          |
| [MEDIQA-AnS](#mediqa-ans) | 552 (single); 156 (multi) | ROUGE-1,2,L; BLEU           | [Extractive: 29, 15, 12, 9; Abstractive: 32, 12, 8, 9](https://arxiv.org/abs/2005.09067) | MRC                   | Consumer    | Generation                  | 2021.3            |
| [MEDIQA-QA](#mediqa-qa) | 3k                        | Acc, P, MRR               | [79.49](https://doi.org/10.18653/v1/2020.emnlp-main.372), [84.02](https://doi.org/10.18653/v1/2020.emnlp-main.372), [96.22](https://doi.org/10.18653/v1/W19-5041) | MRC                   | Consumer    | Multi-choice                | 2021.3          |
| [ProcessBank](#processbank) | 585                       | Acc                         | [66.7](https://doi.org/10.3115/v1/D14-1159)              | MRC                   | Scientific  | Multi-choice                | 2021.3          |
| [PubMedQA](#pubmedqa) | 212k                      | Acc, F1                    | [68.08, 52.72](https://doi.org/10.18653/v1/D19-1259)    | MRC                   | Scientific  | Y/N                         | 2021.3                   |
| [QA4MRE-Alz](#qa4mre-alz) | 40                        | c@1                         | [76](https://www.academia.edu/download/50471011/Question_Answering_System_for_QA4MRECLEF20161121-7106-ea5kdk.pdf) | MRC                   | Scientific  | Multi-choice                | 2021.3          |
| [Bioinformatics](#bioinformatics) | 30                        | F1                          | [60.0](https://arxiv.org/abs/2104.13744)                 | KB                    | Scientific  | Generation                  | 2021.3            |
| [QALD-4 task 2](#qald-4-task-2) | 50                        | F1                          | [99.0](https://content.iospress.com/articles/semantic-web/sw223) | KB                    | Consumer    | Generation                  | 2021.3            |
| [PathVQA](#pathvqa) | 32.8k                     | Acc | [13.4 (open-ended) / 84.0 (yes/no)](https://arxiv.org/abs/2105.08913) | VQA                   | Clinical    | Generation                  | 2021.7            |
| [VQA-Med](#vqa-med)   | 15.3k                     | Acc, BLEU                  | [64.0, 65.9](https://ieeexplore.ieee.org/abstract/document/9032109/) | VQA                   | Clinical    | Generation                  | 2021.3            |
| [VQA-Rad](#vqa-rad)   | 3.5k                      | Acc                         | [60.0 (open) / 79.3 (close)](https://doi.org/10.1145/3394171.3413761) | VQA                   | Clinical    | Generation                  | 2021.3            |
| [ChiMed](#chimed) | 24.9k | Acc | [98.32 (rel.) / 84.24 (adopt.)](https://doi.org/10.18653/v1/W19-5027) | Open-domain | Consumer | Multi-choice | 2021.3 |
| [cMedQA](#cmedqa) | 54k | P@1 | [65.35 (dev) / 64.75 (test)](https://www.mdpi.com/212454) | Open-domain | Consumer | Multi-choice | 2021.3 |
| [cMedQA v2](#cmedqa-v2) | 108k | P@1 | [72.1 (dev) / 72.1 (test)](https://ieeexplore.ieee.org/abstract/document/8548603/) | Open-domain | Consumer | Multi-choice | 2021.3 |
| [HEAD-QA](#head-qa) | 6.8k | Acc | [44.4 (supervised) / 46.7 (unsupervised)](https://arxiv.org/abs/2008.02434) | Open-domain | Examination | Multi-choice | 2021.3 |
| [LiveQA-Med](#liveqa-med) | 738 | avgScore | [82.7](https://www.ncbi.nlm.nih.gov/pmc/articles/pmc5333286/) | Open-domain | Consumer | Generation | 2021.3 |
| [MEDQA](#medqa) | 61k | Acc | [MC: 69.3 (dev) / 70.1 (test); TW: 42.2 (dev) / 42.0 (test); US: 36.1 (dev) / 36.7 (test)](https://doi.org/10.3390/app11146421) | Open-domain | Examination | Multi-choice | 2021.3 |
| [NLPEC](#nlpec) | 2.1k | Acc | [71.1 (dev) / 61.8 (test)](https://doi.org/10.18653/v1/2020.emnlp-main.111) | Open-domain | Examination | Multi-choice | 2021.3 |
| [webMedQA](#webmedqa) | 63k | P@1, MAP | [66.0, 79.5](https://doi.org/10.1186/s12911-019-0761-8) | Open-domain | Consumer | Multi-choice | 2021.3 |

## BioASQ Task B

BioASQ Task B is named “Biomedical Semantic Question Answering" and contains two phases correspond to the IR and MRC BQA approaches in our BQA classification: in the phase A (IR phase), systems retrieve relevant documents for the given question; in the phase B (MRC phase), systems use gold standard relevant documents and ontological data to answer the given questions. Specifically, for the given question, **BioASQ Task B Phase A** participants shall return the relevant: 1. Concepts from certain ontologies such as MeSH; 2. Articles from PubMed and text snippets within the articles; 3. RDF triples from the Linked Life Data. Mean average precision (MAP) is used as a main metric for the BioASQ retrieval phase, with slight modifications for snippet retrieval. **BioASQ Task B Phase B** provides the largest and most widely used manually-annotated MRC BQA dataset: Starting from 2013, BioASQ annotates about 500 test QA instances each year, which will be included in the training set of the following years. Currently, BioASQ 2020 consists of 3,243 training QA instances and at least 500 test instances. Questions in BioASQ are typically scientific questions. There are 4 types of QA instances in BioASQ: factoid, list, yes/no and summary. Factoid, list and yes/no instances have both exact and ideal answers: Exact answers are short answers that directly answer the questions, e.g.: single and multiple biomedical entities for factoid and list questions, respectively; “yes" or “no" for yes/no questions. Ideal answers are exact answers written in complete sentences, e.g.: “Yes, because [...]". The main evaluation metrics for yes/no, factoid, list and summary questions are accuracy, MRR, mean F-score and manual score, respectively. 

Paper: George Tsatsaronis, Georgios Balikas, Prodromos Malakasiotis, Ioannis Partalas, Matthias Zschunke, Michael R Alvers, DirkWeissenborn, Anastasia Krithara, Sergios Petridis, Dimitris Polychronopoulos, et al. 2015. An overview of the BIOASQ large-scale biomedical semantic indexing and question answering competition. *BMC bioinformatics* 16, 1 (2015), 138.

Access: http://www.bioasq.org/

## BiQA

BiQA is an IR BQA dataset containing 7.4k questions and 14.2k relevant PubMed articles collected from online QA forums (Stack Exchange and Reddit). 

Paper: A. Lamurias, D. Sousa, and F. M. Couto. 2020. Generating Biomedical Question Answering Corpora From Q A Forums. *IEEE Access* 8 (2020), 161042–161051. https://doi.org/10.1109/ACCESS.2020.3020868

Access: https://github.com/lasigeBioTM/BiQA

## EPIC-QA

The Epidemic Question Answering (EPIC-QA) challenges are formatted as IR BQA, where the participants return a ranked list of sentences from expert-level (Task A) or consumer-level (Task B) corpora to answer approximately 45 questions about the COVID-19 pandemic.

Access: https://bionlp.nlm.nih.gov/epic_qa/

## HealthQA

HealthQA has 7.5k manually annotating questions that can be answered by one of the 7.3k articles scrapped from the [Patient](https://patient.info/) website.

Paper: Ming Zhu, Aman Ahuja, Wei Wei, and Chandan K. Reddy. 2019. A Hierarchical Attention Retrieval Model for Healthcare Question Answering. In *The World Wide Web Conference* (San Francisco, CA, USA) (*WWW ’19*). Association for Computing Machinery, New York, NY, USA, 2472–2482. https://doi.org/10.1145/3308558.3313699

## TREC Genomics

The TREC Genomics Tracks in 2006 and 2007 tackle the BQA with IR approach: 28 and 36 topic questions (e.g.: “What [GENES] are genetically linked to alcoholism?") are released in 2006 and 2007, respectively, and the participating systems are required to retrieve passages from 162k full-text articles from [Highwire Press](https://www.highwirepress.com/)

Paper: William Hersh, Aaron Cohen, Lynn Ruslen, and Phoebe Roberts. 2007. TREC 2007 Genomics Track Overview. In *TREC 2007*.

Access: https://trec.nist.gov/

## Biomed-Cloze

Biomed-Cloze is a automatically constructed cloze dataset created from PubMed academic papers (for the BioASQ challenge), consisting of 1M clozes. From analyzing the cloze data manually, the authors were able to answer 80% times for the PubMed set using the information in the passage. 

Paper: Bhuwan Dhingra, Danish Danish, and Dheeraj Rajagopal. 2018. Simple and Effective Semi-Supervised Question Answering. In *Proceedings of the 2018 Conference of the North American Chapter of the Association for Computational Linguistics: Human Language Technologies, Volume 2 (Short Papers)*. Association for Computational Linguistics, New Orleans, Louisiana, 582–587. https://doi.org/10.18653/v1/N18-2092

Access: http://bit.ly/semi-supervised-qa

## BioRead

BioRead is a publicly available cloze-style biomedical machine reading comprehension (MRC) dataset with approximately 16.4 million passage-question instances. Biomedical journal articles were used to construct BioRead and MetaMap was employed to identify UMLS concepts. The authors also provided a subset of BioRead, called BioReadLite, with 900k instances, for groups with fewer computational resources

Paper: Dimitris Pappas, Ion Androutsopoulos, and Haris Papageorgiou. 2018. BioRead: A New Dataset for Biomedical Reading Comprehension. In *Proceedings of the Eleventh International Conference on Language Resources and Evaluation (LREC 2018)*. European Language Resources Association (ELRA), Miyazaki, Japan. https://www.aclweb.org/anthology/L18-1439

Access:  http://nlp.cs.aueb.gr/software.html

## BioMRC

BioMRC is a new dataset for biomedical MRC that can be viewed as an improved version of BioREAD. Compared to the previous dataset, care was taken to reduce noise. To avoid crossing sections, extracting text from references, captions, tables etc., the authors used abstracts and titles of biomedical articles as passages and questions, respectively, which are clearly marked up in PUBMED data, instead of using the full text of the articles. They also released two versions of BioMRC, LARGE and LITE, containing 812k and 100k instances respectively for researchers with more or fewer resources, along with the 60 instances (TINY) humans answered.

Paper: Dimitris Pappas, Petros Stavropoulos, Ion Androutsopoulos, and Ryan McDonald. 2020. BioMRC: A Dataset for Biomedical Machine Reading Comprehension. In *Proceedings of the 19th SIGBioMed Workshop on Biomedical Language Processing*. Association for Computational Linguistics, Online, 140–149. https://www.aclweb.org/anthology/2020.bionlp-1.15

Access:  http://nlp.cs.aueb.gr/publications.html

## BMKC

BioMedical Knowledge Comprehension (BMKC) is a large cloze-style dataset which consists of Biomedical Knowledge Comprehension Title (BMKC_T) and Biomedical Knowledge Comprehension Last Sentence (BMKC_LS). PubMed corpus was used to construct the dataset, which can be employed to train deep neural network models.

Paper: Seongsoon Kim, Donghyeon Park, Yonghwa Choi, Kyubum Lee, Byounggun Kim, Minji Jeon, Jihye Kim, Aik Choon Tan, and Jaewoo Kang. 2018. A pilot study of biomedical text comprehension using an attention-based deep neural reader: Design and experimental analysis. *JMIR medical informatics* 6, 1 (2018), e2.

Access: https://www.webcitation.org/6wBRhfS7o

## CliCR

CliCR is a dataset for machine comprehension in the medical domain. For the dataset, the authors constructed queries, answers and supporting passages from BMJ Case Reports, the largest online repository of such documents. CliCR contains around 100,000 queries on 12,000 case reports, has long support passages (around 1,500 tokens on average) and includes answers which are single- or multi-word medical entities.

Paper: Simon Šuster and Walter Daelemans. 2018. CliCR: a Dataset of Clinical Case Reports for Machine Reading Comprehension. In *Proceedings of the 2018 Conference of the North American Chapter of the Association for Computational Linguistics: Human Language Technologies, Volume 1 (Long Papers)*. Association for Computational Linguistics, New Orleans, Louisiana, 1551–1563. https://doi.org/10.18653/v1/N18-1140

Access: http://github.com/clips/clicr

## COVIDQA

COVIDQA is a QA dataset specifically designed for COVID-19. It has 124 question-article pairs translated from the literature review page of Kaggle’s COVID-19 Open Research Dataset Challenge 15, where relevant information for each category or subcategory in the review is presented.

Paper: Raphael Tang, Rodrigo Nogueira, Edwin Zhang, Nikhil Gupta, Phuong Cam, Kyunghyun Cho, and Jimmy Lin. 2020. Rapidly Bootstrapping a Question Answering Dataset for COVID-19. *arXiv preprint arXiv:2004.11339 (2020)*.

Access: http://covidqa.ai/

## COVID-QA

COIVD-QA is a COVID-19 QA dataset with 2k question-answer pair annotated by biomedical experts. The annotation is similar to that of SQuAD while the answers in COVID-QA tend to be longer as they generally come from longer texts.

Paper: Timo Moller, Anthony Reina, Raghavan Jayakumar, and Malte Pietsch. 2020. COVID-QA: A Question Answering Dataset for COVID-19. https://openreview.net/forum?id=JENSKEEzsoU

Access: https://github.com/deepset-ai/COVID-QA

## EBMSummariser

EBMSummariser is a summarization dataset of 456 instances for EBM, from the Clinical Inquiries section of the Journal of Family Practice16: each instance contains a clinical question, a long “bottom-line" answer, the answer’s evidence quality and a short justification of the long answer.

Paper: Diego Mollá, María Elena Santiago-Martínez, Abeed Sarker, and Cécile Paris. 2016. A corpus for research in text processing for evidence based medicine. *Language Resources and Evaluation* 50, 4 (2016), 705–727.

Access: http://sourceforge.net/projects/ebmsumcorpus/

## emrQA

EmrQA is a domain-specific large-scale question answering (QA) datasets by re-purposing existing expert annotations on clinical notes for various NLP tasks from the community shared i2b2 datasets. The corpus has 1 million questions-logical form and 400,000+ question-answer evidence pairs. 

Paper: Anusri Pampari, Preethi Raghavan, Jennifer Liang, and Jian Peng. 2018. emrQA: A Large Corpus for Question Answering on Electronic Medical Records. In *Proceedings of the 2018 Conference on Empirical Methods in Natural Language Processing*. Association for Computational Linguistics, Brussels, Belgium, 2357–2368. https://doi.org/10.18653/v1/D18-1258

Access: https://github.com/panushri25/emrQA

## MASH-QA

MASH-QA, a dataset based on consumer health domain, is designed for extracting information from texts that span across a long document. It utilizes long and comprehensive healthcare articles as context to answer generally non-factoid questions. Different from the existing MRC datasets with short single-span answers, many answers in MASH-QA are several sentences long and excerpted from multiple parts or spans of the long context.

Paper: Ming Zhu, Aman Ahuja, Da-Cheng Juan, Wei Wei, and Chandan K. Reddy. 2020. Question Answering with Long Multiple-Span Answers. In *Findings of the Association for Computational Linguistics: EMNLP 2020*. Association for Computational Linguistics, Online, 3840–3849. https://doi.org/10.18653/v1/2020.findings-emnlp.342

Access: https://github.com/mingzhu0527/MASHQA

## MEDHOP

MEDHOP is a multi-hop MRC BQA dataset, where each instance contains a query of a subject and a predicate (e.g.: “Leuprolide, interacts_with, ?"), multiple relevant and linking documents and a set of answer options extracted from the documents. Reasoning over multiple documents is required for the model to answer the question.

Paper: Johannes Welbl, Pontus Stenetorp, and Sebastian Riedel. 2018. Constructing Datasets for Multi-hop Reading Comprehension Across Documents. *Transactions of the Association for Computational Linguistics* 6 (2018), 287–302. https://doi.org/10.1162/tacl_a_00021

Access: http://qangaroo.cs.ucl.ac.uk

## MEDIQA-QA

MEDIQA-QA is the dataset of the QA subtask of MEDIQA 2019 shared task. It is obtained by submitting medical questions to the consumer health QA system CHiQA then re-rank the answers by medical experts. The training, validation and test set altogether have 400 questions and 3k associate answers. The task of MEDIQA-QA dataset is, however, to filter and improve the ranking of answers, making it a multi-choice QA task.

Paper: Asma Ben Abacha, Chaitanya Shivade, and Dina Demner-Fushman. 2019. Overview of the MEDIQA 2019 Shared Task on Textual Inference, Question Entailment and Question Answering. In *Proceedings of the 18th BioNLP Workshop and Shared Task. Association for Computational Linguistics*, Florence, Italy, 370–379. https://doi.org/10.18653/v1/W19-5039

Access: https://sites.google.com/view/mediqa2019

## MEDIQA-AnS

MEDIQA-AnS is a summarization dataset, which provides extractive and abstractive versions of single and multi-document summary of the answer passages from MEDIQA-QA.

Paper: Max Savery, Asma Ben Abacha, Soumya Gayen, and Dina Demner-Fushman. 2020. Question-Driven Summarization of Answers to Consumer Health Questions. *arXiv e-prints* (May 2020). arXiv:2005.09067 [cs.CL] https://arxiv.org/abs/2005.09067

Access: https://www.github.com/saverymax/qdriven-chiqa-summarization

## ProcessBank

ProcessBank contains multi-choice questions along with relevant biological paragraphs. The paragraphs are annotated with "process", a directed graph (𝒯,𝒜,ℰ𝑡𝑡 ,ℰ𝑡𝑎), where nodes 𝒯 are token spans denoting the occurrence of events, nodes 𝒜 are token spans denoting entities in the process, and the latter two are edges describing event relations and semantic roles respectively.

Paper: Jonathan Berant, Vivek Srikumar, Pei-Chun Chen, Abby Vander Linden, Brittany Harding, Brad Huang, Peter Clark, and Christopher D. Manning. 2014. Modeling Biological Processes for Reading Comprehension. In *Proceedings of the 2014 Conference on Empirical Methods in Natural Language Processing (EMNLP)*. Association for Computational Linguistics, Doha, Qatar, 1499–1510. https://doi.org/10.3115/v1/D14-1159 

Access: http://www-nlp.stanford.edu/software/bioprocess

## PubMedQA

PubMedQA dataset is built from PubMed articles that use binary questions as titles (e.g.: “Do preoperative statins reduce atrial fibrillation after coronary artery bypass grafting?") and have structured abstracts. The conclusive parts of the abstracts are the long answers, while the main task of PubMedQA is to predict their short forms, i.e.: yes/no/maybe, using the abstracts without the conclusive parts as contexts.

Paper: Qiao Jin, Bhuwan Dhingra, Zhengping Liu, William Cohen, and Xinghua Lu. 2019. PubMedQA: A Dataset for Biomedical Research Question Answering. In *Proceedings of the 2019 Conference on Empirical Methods in Natural Language Processing and the 9th International Joint Conference on Natural Language Processing (EMNLP-IJCNLP)*. Association for Computational Linguistics, Hong Kong, China, 2567–2577. https://doi.org/10.18653/v1/D19-1259

Access: https://pubmedqa.github.io

## QA4MRE-Alz

Question Answering for Machine Reading Evaluation (QA4MRE) holds a sub-task on machine reading of biomedical texts about Alzheimer’s disease. This task provides only a test dataset with 40 QA instances, and each instance contains one question, one context and 5 answer choices.

Paper: Roser Morante, Martin Krallinger, Alfonso Valencia, and Walter Daelemans. 2012. Machine reading of biomedical texts about Alzheimers disease. In *CLEF 2012 Conference and Labs of the Evaluation Forum-Question Answering For Machine Reading Evaluation (QA4MRE), Rome/Forner, J.[edit.]; ea*. 1–14.

## Bioinformatics

Bioinformatics contains biomedical queries with different complexity, and the database searching are restricted in Bgee and OMA. The natural language questions include multiple concepts which leads to longer and more complicated SPARQL queries.

Paper: Ana Claudia Sima, Tarcisio Mendes de Farias, Maria Anisimova, Christophe Dessimoz, Marc Robinson-Rechavi, Erich Zbinden, and Kurt Stockinger. 2021. Bio-SODA: Enabling Natural Language Question Answering over Knowledge Graphs without Training Data. *arXiv preprint arXiv:2104.13744* (2021).

Access: https://github.com/anazhaw/Bio-SODA

## QALD-4 task 2

QALD-4 task 2 contains 50 natural language biomedical question and requests SPARQL queries to retrieve answers from SIDER, Drugbank and Diseasome, where most questions require integrating knowledge from multiple databases to answer. 

Paper: Christina Unger, Corina Forascu, Vanessa Lopez, Axel-Cyrille Ngonga Ngomo, Elena Cabrio, Philipp Cimiano, and SebastianWalter. 2014. Question answering over linked data (QALD-4). In *Working Notes for CLEF 2014 Conference*.

Access: http://qald.aksw.org/index.php?x=task2&q=4

## PathVQA

PathVQA semi-automatically extracts 32.8K pathology images and generates the corresponding answers from textbooks.

Paper: Xuehai He, Yichen Zhang, Luntian Mou, Eric Xing, and Pengtao Xie. 2020. PathVQA: 30000+ Questions for Medical Visual Question Answering. *arXiv preprint arXiv:2003.10286* (2020).

Access: https://github.com/UCSD-AI4H/PathVQA

## VQA-Med

The VQA-Med dataset is automatically constructed using captions of the radiology images. There are 15.3K questions in VQA-Med that are restricted to be about only one element and should be answerable from the corresponding images. VQA-Med concentrates on the most common questions in radiology, which include categories of modality, plane, organ system and abnormality. Yes/no and WH-questions are included in VQA-Med.

Paper: Asma Ben Abacha, Sadid A Hasan, Vivek V Datla, Joey Liu, Dina Demner-Fushman, and Henning Müller. 2019. VQA-Med: Overview of the Medical Visual Question Answering Task at ImageCLEF 2019.

Access: https://github.com/abachaa/VQA-Med-2019

## VQA-Rad

VQA-Rad is the first VQA dataset for radiology. It contains 3.5K QA pairs that are annotated by clinicians and the images are from MedPix. Questions in VQA-Rad are classified into modality, plane, organ system, abnormality, object/condition presence, etc. Answer formats include multi-choices and generations in VQA-Rad.

Paper: Jason J Lau, Soumya Gayen, Asma Ben Abacha, and Dina Demner-Fushman. 2018. A dataset of clinically generated visual questions and answers about radiology images. *Scientific data* 5, 1 (2018), 1–10.

Access: https://osf.io/89kps/

## ChiMed

ChiMed is a Chinese medical QA corpus which is built by crawling data from a big Chinese medical forum. In the forum, the questions are asked by web users and all the answers are provided by accredited physicians. In addition to (Q, A) pairs, the corpus contains rich information such as the title of the question, key phrases, age and gender of the user, the name and affiliation of the accredited physicians who answer the question, and so on.

Paper: Yuanhe Tian, Weicheng Ma, Fei Xia, and Yan Song. 2019. ChiMed: A Chinese Medical Corpus for Question Answering. In *Proceedings of the 18th BioNLP Workshop and Shared Task*. Association for Computational Linguistics, Florence, Italy, 250–260. https://doi.org/10.18653/v1/W19-5027

Access: https://github.com/yuanheTian/ChiMed

## cMedQA

CMedQA is a Chinese medical questions and answers dataset acquired from an online Chinese medical question answering forum (http://www.xywy.com/). Questions are proposed by users and are responded to by qualified medical doctors. Each question is often answered by several doctors, and only certified doctors are eligible to answer questions. The dataset consists of 54, 000 questions and more than 101, 000 answers

Paper: Sheng Zhang, Xin Zhang, Hui Wang, Jiajun Cheng, Pei Li, and Zhaoyun Ding. 2017. Chinese medical question answer matching using end-to-end character-level multi-scale CNNs. *Applied Sciences* 7, 8 (2017), 767.

Access: https://github.com/zhangsheng93/cMedQA

## cMedQA v2

CMedQA v2.0 is the extension and amendment of cMedQA dataset, which has more samples and fine-tuned preprocessing.

Paper: Sheng Zhang, Xin Zhang, Hui Wang, Lixiang Guo, and Shanshan Liu. 2018. Multi-Scale Attentive Interaction Networks for Chinese Medical Question Answer Selection. *IEEE Access* 6 (2018), 74061–74071.

Access: https://github.com/zhangsheng93/cMedQA2

## HEAD-QA

HEAD-QA is a multi-choice question answering testbed to encourage research on complex reasoning. The questions come from exams to access a specialized position in the Spanish healthcare system, and are challenging even for highly specialized humans.

Paper: David Vilares and Carlos Gómez-Rodríguez. 2019. HEAD-QA: A Healthcare Dataset for Complex Reasoning. In *Proceedings of the 57th Annual Meeting of the Association for Computational Linguistics*. Association for Computational Linguistics, Florence, Italy, 960–966. https://doi.org/10.18653/v1/P19-1092

Access: http://aghie.github.io/head-qa/

## LiveQA-Med

LiveQA-Med contains two training sets with 634 pairs of medical questions and answers and one test set with 104 NLM questions. In training sets, the authors provided additional annotations for the Question Focus and the Question Type to define each subquestion. Training questions cover four categories of foci (Disease, Drug, Treatment and Exam) and 23 question types (e.g. Treatment, Cause, Indication, dosage). The subquestion, focus and type annotations of test questions were not provided to the participants. For each medical question, participants were tasked to retrieve a correct answer for each subquestion. If the question includes more than one subquestion, answers should be ranked according to the order of the subquestions.

Paper: Asma Ben Abacha, Eugene Agichtein, Yuval Pinter, and Dina Demner-Fushman. 2017. Overview of the Medical Question Answering Task at TREC 2017 LiveQA.

Access: https://github.com/abachaa/LiveQA_MedicalTask_TREC2017

## MEDQA

MEDQA is the first free-form multiple-choice OpenQA dataset for solving medical problems, which is collected from the professional medical board exams. It covers three languages: English, simplified Chinese, and traditional Chinese, and contains 12,723, 34,251, and 14,123 questions for the three languages, respectively.

Paper: Di Jin, Eileen Pan, Nassim Oufattole, Wei-Hung Weng, Hanyi Fang, and Peter Szolovits. 2020. What Disease does this Patient Have? A Large-scale Open Domain Question Answering Dataset from Medical Exams. *arXiv preprint arXiv:2009.13081* (2020).

Access: https://github.com/jind11/MedQA

## NLPEC

NLPEC uses the National Licensed Pharmacist Examination in China as the source of questions. Examples of the pharmacy comprehensive knowledge and skills part of the exam in the five years (2015-2019) are used as the test set, where questions of multiple-answer type are excluded. In addition to that, the authors also collected over 24,000 problems from the Internet and exercise books. After removing duplicates and incomplete questions (e.g. no answer), they randomly divide it into training, development sets according to a certain ratio, and remove the problems similar to the test set according to the condition that the edit distance is less than 0.1

Paper: Dongfang Li, Baotian Hu, Qingcai Chen, Weihua Peng, and Anqi Wang. 2020. Towards Medical Machine Reading Comprehension with Structural Knowledge and Plain Text. In *Proceedings of the 2020 Conference on Empirical Methods in Natural Language Processing (EMNLP)*. Association for Computational Linguistics, Online, 1427–1438. https://doi.org/10.18653/v1/2020.emnlp-main.111

## webMedQA

WebMedQA is a large Chinese medical non-factoid QA dataset formulated in natural language. Its data are collected from professional health-related consultancy websites such as Baidu Doctor and 120Ask. There are 23 categories of consultancy in the dataset, covering most of the clinical departments of common diseases and health problems.

Paper: Junqing He, Mingming Fu, and Manshu Tu. 2019. Applying deep matching networks to Chinese medical question answering: a study and a dataset. *BMC medical informatics and decision making* 19, 2 (2019), 52.

Access: https://github.com/hejunqing/webMedQA
