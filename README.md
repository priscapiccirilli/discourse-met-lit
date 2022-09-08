# DATASET_METLIT

This dataset contains 1,000 corpus-extracted discourses for which crowdsourced annotators provided (1) graded and binary judgements on whether they perceived the discourses as more metaphorical or more literal; (2) binary judgements on the choice between a synonymous pair of a literal and a metaphorical expression following the discourses in (1); and (3) lexical terms which triggered their binary decisions in (1). The judgements were collected and analyzed within two studies ([this paper](https://www.ims.uni-stuttgart.de/documents/team/schulte/publications/workshop/discann-21.pdf) and [this paper](http://www.lrec-conf.org/proceedings/lrec2022/pdf/2022.lrec-1.564.pdf)) in various ways.  

For questions/comments/suggestions, please contact Prisca Piccirilli: prisca.piccirilli@ims.uni-stuttgart.de

---------------------------------

### 1) SV-VO-pairs.txt

- Studied pairs of expressions.
- 50 pairs.

---------------------------------

### 2) original-discourses-ukwac

- Folder with text files: for each pair of expressions, 20 discourses (10 for each expression) extracted from ukWac corpus. 
- Total: 1,000 discourses.

---------------------------------

### 3) full-data-annotation1-task1.tsv

- Annotation study 1, task 1: Rate the degree of metaphoricity of the discourse on a scale from 1--6 (mostly literal--mostly metaphorical).
- 15,000 instances (15 judgements for each discourse).
- WorkerId: Id of annotator.
- DiscourseId : Id of discourse.
- Expression.Lit: literal expression from the pair which can follow the presented discourse.
- Expression.Met: metaphorical expression from the pair which can follow the presented discourse.
- Original.Expression: metaphoricity of expression which was present in the original collected discourse.
- Category.MetLit: rating of metaphoricity for the given discourse.

---------------------------------

### 4) full-data-annotation1-task2.tsv

- Annotation study 1, task 2: Pick the expression that fits best (synonymous metaphorical vs. literal expression from pair)
- 15,000 instances (15 judgements for each discourse - NOTE: 998 discourses).
- WorkerId: Id of annotator.
- DiscourseId : Id of discourse.
- Input.Expression.Lit: morphological form of literal expression which can follow the presented discourse.
- Input.Expression.Met: morphological form of metaphorical expression which can follow the presented discourse.
- Expression.Lit: literal expression from the pair which can follow the presented discourse.
- Expression.Met: metaphorical expression from the pair which can follow the presented discourse.
- Original.Expression: metaphoricity of expression which was present in the original collected discourse.
- Expression.MetLit: picked expression from the annotator.

---------------------------------

### 5a) study-set-annotation1-tasks1-2.tsv

- Set of 1,000 discourses analyzed in annotation study 1.
- We kept instances from annotators who had given 20 or more judgements in total.
- Information from tasks 1 and 2 combined.
- DiscourseId : Id of discourse.
- Expression.Lit: literal expression from the pair which can follow the presented discourse.
- Expression.Met: metaphorical expression from the pair which can follow the presented discourse.
- Original.Expression: metaphoricity of expression which was present in the original collected discourse.
- Expression.MetLit: majority picked expression from the considered annotators.
- Discourse.Median.MetLit: median for discourse metaphoricity from all the ratings on the given discourse.
- Discourse.MetLit: binary decision for metaphoricity of discourse based on threshold 3.5 (met >= 3.5; lit < 3.5).

---------------------------------

### 5b) study-subset-annotation1-tasks1-2.tsv

- Set of 287 discourses analyzed in annotation study 1.
- We kept instances from annotators who had given 20 or more judgements in total + instances for which 70% or more annotators agreed on the metaphoricity of the discourse.
- Information from tasks 1 and 2 combined.
- DiscourseId : Id of discourse.
- Expression.Lit: literal expression from the pair which can follow the presented discourse.
- Expression.Met: metaphorical expression from the pair which can follow the presented discourse.
- Original.Expression: metaphoricity of expression which was present in the original collected discourse.
- Expression.MetLit: majority picked expression from the considered annotators.
- Discourse.Median.MetLit: median from all the ratings on the given discourse.
- Discourse.MetLit: binary decision for metaphoricity of discourse based on threshold 3.5 (met >= 3.5; lit < 3.5).

---------------------------------

### 6) full-data-annotation2.tsv

- Annotation study 2: (i) is the discourse more literal or metaphorical (binary decision), (ii) list 5 words which triggered the decision in (i).
- 10,000 judgements (10 judgements for each discourse).
- WorkerId: Id of annotator.
- DiscourseId : Id of discourse.
- Expression.Lit : literal expression from the pair which can follow the presented discourse.
- Expression.Met : metaphorical expression from the pair which can follow the presented discourse.
- Original.Expression : metaphoricity of expression which was present in the original collected discourse.
- Discourse.MetLit : decision of the annotator regarding metaphoricity of given discourse.
- word1
- word2
- word3
- word4
- word5 
NOTE: '{}' is when the annotator did not give a word.

---------------------------------

### 7) study-set-annotation2.tsv

- Set of 711 discourses analyzed in annotation study 2.
- We kept instances from annotators who had given 20 or more judgements in total + instances for which 70% or more annotators agreed on the metaphoricity of the discourse.
- We integrated information from annotation study 1 that we also looked at in annotation study 2.
- DiscourseId : Id of discourse.
- Expression.Lit : literal expression from the pair which can follow the presented discourse.
- Expression.Met : metaphorical expression from the pair which can follow the presented discourse.
- Original.Expression: metaphoricity of expression which was present in the original collected discourse.
- Discourse.MetLit : decision of the considered annotators regarding metaphoricity of given discourse.
- Abstr.all : median abstractness score of the given discourse associated with all lexical items listed by annotators.
- Abstr.N : median abstractness score of the given discourse associated with nouns only listed by annotators.
- Abstr.V : median abstractness score of the given discourse associated with verbs only listed by annotators.
- Abstr.ADJ : median abstractness score of the given discourse associated with adjectives only listed by annotators.
- Emotionality : median emotionality score of the given discourse associated with all lexical items listed by annotators.
- Emotion : main referred emotion from emotionality scores of the given discourse.
- List.Words : list of the lexical items given by all annotators on the given discourse.
NOTE: '-' is when no abstractness/emotionality score was available for the listed lexical items.

---------------------------------

### 8) discourses_id.tsv

- 1,000 discourses:
- DiscourseId: Id of discourse, used in all files.
- Discourse: Discourse referring to Id.

---------------------------------
### CITATIONS

If you use this dataset, please cite the following publications: 

```
@inproceedings{Piccirilli-SchulteImWalde:2021,
  author    = {Piccirilli, Prisca and {Schulte im Walde}, Sabine},
  title     = {{Synonymous Pairs of Metaphorical and Literal Expressions in Context: An Empirical Study and Dataset \textit{to tackle} or \textit{to address the question}}},
  booktitle = {Proceedings of the Workshop DiscAnn},
  year      = {2021},
  address   = {T\"ubingen, Germany},
  url={https://www.ims.uni-stuttgart.de/documents/team/schulte/publications/workshop/discann-21.pdf},
}
```

```
@inproceedings{Piccirilli-SchulteImWalde:2022,
author  =   {Piccirilli, Prisca and {Schulte im Walde}, Sabine},
title   =   {{Features of Perceived Metaphoricity on the Discourse Level:
Abstractness and Emotionality}},
booktitle   =   {Proceedings of the 13th Conference on Language Resources and Evaluation},
year    =   {2022},
address =   {Marseille, France},
publisher = {European Language Resources Association},
note    =   {http://www.lrec-conf.org/proceedings/lrec2022/pdf/2022.lrec-1.564.pdf},
}
```

---------------------------------

### REFERENCES


Brysbaert, M., Warriner, A. B., & Kuperman, V. (2014). Concreteness ratings for 40 thousand generally known English word lemmas. Behavior research methods, 46(3), 904-911.

Buechel, S., Ruecker, S., Hahn, U. (2020). Learning and evaluating emotion lexicons for 91 languages. In Proceedings of the 58th Annual Meeting of the Association for Computational Linguistics, 1202-1217.

Ferraresi, A., Zanchetta, E., Baroni, M., & Bernardini, S. (2008). Introducing and evaluating ukWaC, a very large web-derived corpus of English. In Proceedings of the 4th Web as Corpus Workshop, Can we beat Google, 47-54.

Piccirilli, P., Schulte im Walde, S. (2021). Contextual Choice between Synonymous Pairs of Metaphorical and Literal Expressions: An Empirical Study and Novel Dataset to tackle or to address the question. In Proceedings of the Workshop on Integrating Perspectives on Discourse Annotation (DiscAnn).Tübingen, Germany.

Piccirilli, P., Schulte im Walde, S. (2022). Features of Perceived Metaphoricity on the
Discourse Level: Abstractness and Emotionality. In Proceedings of the 13th Conference on Language Resources and Evaluation (LREC). Marseille, France.
