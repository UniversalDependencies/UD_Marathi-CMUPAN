# Summary

This treebank is a modified version of a semi-automatically treebank authord by Aditi Chaudhary, which in turn is based on the treebanks released by KCIS, IIIT-Hyderabad. It addresses several validation errors present in the original treebank through semi-automatic correction to ensure compliance with Universal Dependencies standards.

Additionally, the treebank also contains Marathi-Discourse: A manually annotated 35-sentence corpus covering political discourse. The Marathi-Discourse sentences have been integrated directly into the training set of the CMUPAN treebank


# Introduction

The sentences are based on treebanks released by KCIS, IIIT-Hyderabad . The primary goal of this version is to provide a clean, validated treebank by fixing structural inconsistencies, morphological feature errors, and dependency relation violations in the original treebank. The corrections were performed using python script-based semi-automatic logics. (For eg. Identifying and fixing invalid upos-deeprel, correcting lemmas, correcting/removing invalid morphological feature, etc). For transliteration Indic Transliteration python library was used.

Marathi-Discourse: The corpus also contains 35 Discourse sentences. Data for this is sourced from the official Marathi translation of Prime Minister (of India) Narendra Modi’s address to the nation regarding the COVID-19 pandemic, delivered on May 12, 2020.

To maintain traceability, each sentence ID in the carries a specific prefix:

*cmupan_*: Sentences from the CMU/IIIT-Hyderabad treebank.

*DISC_*: Discourse sentences.


# Acknowledgments

Original work by Aditi Chaudhary. The treebank was semi-automatically corrected by Pranav Kushare. Supervision and revision by Luigi Talamo, Annemarie Verkerk, Helena Vaz.



## References

* (citation)
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
```
@misc{modi_speech_2020,
  author = {{Prime Minister's Office, India}},
  title = {पंतप्रधानांचे देशाला संबोधन (Address to the Nation on COVID-19 and Atmanirbhar Bharat)},
  year = {2020},
  month = {May 12},
  howpublished = {\url{https://www.pmindia.gov.in/mr/news_updates/पंतप्रधानांचे-देशाला-उद्/}}
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
```
@misc{googletrans,
  author = {Suhun Han},
  title = {Googletrans: Free and Unlimited Google translate API for Python},
  year = {2020},
  publisher = {PyPI},
  howpublished = {\url{https://pypi.org/project/googletrans/}},
}
```
```
@misc{indic_transliteration,
  author = {{Vishvas Vasuki}},
  title = {indic-transliteration: Python package for Indic script transliteration},
  year = {2025},
  publisher = {GitHub},
  journal = {GitHub repository},
  howpublished = {\url{https://github.com/indic-transliteration/indic_transliteration_py}},
  note = {Version 2.3.75}
}
```

# Changelog

* 2026-05-15 v2.18
  * Initial release in Universal Dependencies.


<pre>
=== Machine-readable metadata (DO NOT REMOVE!) ================================
Data available since: UD v2.18
License: CC BY-SA 4.0
Includes text: yes
Parallel: no
Genre: agriculture, grammar, general, tourism
Lemmas: automatic with corrections
UPOS: automatic with corrections
XPOS: automatic with corrections
Features: automatic with corrections
Relations: automatic with corrections
Contributors: Kushare, Pranav; Chaudhary, Aditi; Talamo, Luigi; Verkerk, Annemarie; Vaz, Helena
Contributing: here
Contact: annemarie.verkerk@uni-saarland.de
===============================================================================
</pre>
