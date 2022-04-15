# Summary

UD_Marathi-CMUPAN is a semi-automatically created treebank, it is based on the treebanks released by KCIS, IIIT-Hyderabad (https://ltrc.iiit.ac.in/showfile.php?filename=downloads/kolhi/)


# Introduction

UD_Marathi-CMUPAN is a semi-automatically created treebank that were created as part of project by KCIS, IIIT-Hyderabad, India.
These treebanks are originally are based on the Paninan Grammar Framework, and follow a different annotation standard.
We have semi-automatically converted it (e.g. POS tags, morphology, tokenization, lemmas, affix) to the UD schema with also adding some additional information (e.g. dependency links).
Specifically, we wrote a mapping function to convert the existing POS annotations to the UD POS and morphology analysis.
Original POS tags are much more fine-grained and we have retained that information in the XPOS field. We retain original tokenization and lemmatization.
We couldn't utitlize the dependency information from existing treebank, instead we automatically annotated the dependency labels and heads, by training a dependency analysis model (https://github.com/Hyperparticle/udify) on a related language (UD_Hindi-HDTB).
Additionally, the original treebanks also contained suffix information in some cases, which we have added in the MISC column, an example sentence is shown below:
```
1	बार्लीची	बार्ली	PROPN	N_NNP	Case=Acc|Gender=Fem	2	nmod	_	affix=ची
2	वैरण	वैरण	NOUN	N_NN	Case=Nom|Gender=Fem|Number=Sing	6	nsubj	_	affix=_
3	जनावरांसाठी	जनावर	NOUN	N_NN	Case=Acc|Gender=Neut|Number=Plur	6	obl	_	affix=साठी
4	बिछाना	बिछाना	NOUN	N_NN	Case=Nom|Gender=Masc|Number=Sing	6	obj	_	affix=_
5	सदृश	सदृश	ADJ	JJ	_	6	compound	_	affix=_
6	पसरवतात	पसरव	VERB	V_VM	Aspect=Hab|Gender=Fem|Number=Plur|Person=3|Tense=Pres|VerbForm=Fin	0	root	_	affix=तात
7	.	.	PUNCT	RD_PUNC	_	6	punct	_	affix=_
```
The original treebanks covered data from following domains: Agriculture, General, Grammar, Tourism
We note that the final converted data has not been verified by language experts.
The train/dev/test split is the same as followed by the original treebanks.

# Acknowledgments

We would like to acknowledge Pruthwik Mishra and Prof. Dipti Sharma from IIIT-Hyderabad, who very kindly shared the original treebanks with us and helped answer all relevant questions very promptly.
We would also like acknowledge Ministry of Electronics and Information Technology (MeitY), Government of India, as the funding agency for the development of original Marathi and Kannada treebanks.
We would also like to acknowledge the Waibel Presidential Fellowship, which enabled the contributing author in this research.

## References

Please cite the following references:

### Paninian Treebank annotation effort, similar annotation techniques were followed for Marathi, Bengali and Kannada.

```
@incollection{bhat2017hindi,
  title={The hindi/urdu treebank project},
  author={Bhat, Riyaz Ahmad and Bhatt, Rajesh and Farudi, Annahita and Klassen, Prescott and Narasimhan, Bhuvana and Palmer, Martha and Rambow, Owen and Sharma, Dipti Misra and Vaidya, Ashwini and Ramagurumurthy Vishnu, Sri and others},
  booktitle={Handbook of linguistic annotation},
  pages={659--697},
  year={2017},
  publisher={Springer}
}
```
```
@article{xia2008towards,
  title={Towards a multi-representational treebank},
  author={Xia, Fei and Rambow, Owen and Bhatt, Rajesh and Palmer, Martha and Misra Sharma, Dipti},
  journal={LOT Occasional Series},
  volume={12},
  pages={159--170},
  year={2008},
  publisher={LOT, Netherlands Graduate School of Linguistics}
}
```
```
@inproceedings{bhatt2009multi,
  title={A multi-representational and multi-layered treebank for hindi/urdu},
  author={Bhatt, Rajesh and Narasimhan, Bhuvana and Palmer, Martha and Rambow, Owen and Sharma, Dipti Misra and Xia, Fei},
  booktitle={Proceedings of the Third Linguistic Annotation Workshop (LAW III)},
  pages={186--189},
  year={2009}
}
```
Additional relevant references are [here](http://verbs.colorado.edu/hindiurdu/publications.html)

### Converting Paninian annotation to UD annotation
```
@inproceedings{tandon-etal-2016-conversion,
    title = "Conversion from Paninian Karakas to {U}niversal {D}ependencies for {H}indi Dependency Treebank",
    author = "Tandon, Juhi  and
      Chaudhry, Himani  and
      Bhat, Riyaz Ahmad  and
      Sharma, Dipti",
    booktitle = "Proceedings of the 10th Linguistic Annotation Workshop held in conjunction with {ACL} 2016 ({LAW}-X 2016)",
    month = aug,
    year = "2016",
    address = "Berlin, Germany",
    publisher = "Association for Computational Linguistics",
    url = "https://aclanthology.org/W16-1716",
    doi = "10.18653/v1/W16-1716",
    pages = "141--150",
}
```

### Automatic Parser used for dependency analysis
UDIFY Model:
```
@inproceedings{kondratyuk-straka-2019-75,
    title = {75 Languages, 1 Model: Parsing Universal Dependencies Universally},
    author = {Kondratyuk, Dan and Straka, Milan},
    booktitle = {Proceedings of the 2019 Conference on Empirical Methods in Natural Language Processing and the 9th International Joint Conference on Natural Language Processing (EMNLP-IJCNLP)},
    year = {2019},
    address = {Hong Kong, China},
    publisher = {Association for Computational Linguistics},
    url = {https://www.aclweb.org/anthology/D19-1279},
    pages = {2779--2795}
}
```

# Changelog

* 2022-05-15 v2.10
  * Initial release in Universal Dependencies.


<pre>
=== Machine-readable metadata (DO NOT REMOVE!) ================================
Data available since: UD v2.10
License: CC BY-SA 4.0
Includes text: yes
Genre: agriculture, grammar, general, tourism
Lemmas: annotated manually in Paninian Grammar Framework
UPOS: annotated manually in Paninian Grammar Framework, automatic converted to UD
XPOS: annotated manually in Paninian Grammar Framework
Features: annotated manually in Paninian Grammar Framework, automatic converted to UD
Relations: automatic parsed to UD
Contributors: Chaudhary, Aditi
Contributing: here
Contact: aschaudh@andrew.cmu.edu, aditi138@gmail.com
===============================================================================
</pre>