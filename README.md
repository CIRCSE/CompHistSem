## Computational Historical Semantics

* co-operative project originally developed by an interdisciplinary team led by Bernhard Jussen and Alexander Mehler at the Goethe University in Frankfurt am Main, and funded by the German Federal Ministry for Education and Research. The project aims to define new methods and tools for historical-semantic analysis
* associated website: https://lta.bbaw.de/ of the Latin Text Archive (\textsc{lta}), hosted by the Berlin-Brandenburg Academy of Sciences and Humanities
* corpus: more than 4000 texts spanning from the 2nd to the 15th Century \textsc{ad}, put together thanks to the support of digitalised collections such as the Patrologia Latina Database (http://pld.chadwyck.co.uk/), the Monumenta Germaniae Historica (https://www.mgh.de/), the Corpus Corporum (https://mlat.uzh.ch/) and the Bibliotheca Augustana (http://www.hs-augsburg.de/~harsch/augustana.html)

## CompHistSem in LiLa
We linked a subset of 5 texts from the original corpus:

1. **Capitularia Regum Francorum** (6th–9th c. AD), various authors, from MGH Capitularia 1 & 2. Total of `10 826 sentences` and `18 343 024 tokens` (including `53 161 punctuation marks`)
2. **De ecclesiasticis officiis** (9h c. AD) by Amalarius of Metz, from Patrologia Latina vol. 105. Total of `4 279 sentences` and `125 475 tokens` (including 2`0 845 punctuation marks`)
3. **Vita Karoli Imperatoris** (9th c. AD) by Eginhard, from mgh Scriptores rerum Germanicarum 25. Total of `247 sentences` and `8 393 tokens` (including` 1 224 punctuation marks`)
4. **Gesta Hludowici imperatoris** (9th c. AD) by Thegan of Trier, from mgh Scriptores rerum Germanicarum 64. Total of `451 sentences` and `8 355 tokens` (including `1 403 punctuation marks`)
5. **Decretum Gratiani i to iii** (treated as distinct documents), also known as **Concordia
discordantium canonum** (12th c. AD) by Gratian, from Corpus Corporum through Patrologia
Latina vol. 187. Total of `31 804 sentences` and `572 830 tokens` (including `124 656 punctuation marks`)

TOTAL: `47607 sentences` for `1058077 tokens` (including `201289 punctuation marks`), the vast majority of which lemmatised and tagged for parts of speech and morphological features by means of the Frankfurt Latin Lexicon, which uses its own tagset, in line with the grammatical categories traditionally recognised for Latin. All texts but the **Decretum Gratiani** (Corpus Corporum, transcription under Creative Commons Share-Alike license: https://creativecommons.org/licenses/by-sa/4.0/) are retrievable from the Latin Text Archive and are under the Creative Commons license: https://creativecommons.org/licenses/by/4.0/. The texts are encoded in the tei-p5 format, so as xml.

## Linking process
* conversion from TSV files to the CoNLL-U format by means of a Phyton script (coming soon)
* tagset mapping: morphological tags and POS tags already correspond to the UD formalism or are easily subsumed under more general classes (e.g. CompHistSem's distributives and ordinals merge into UD's adjectives)
* lemmatization: the texts came already lemmatized. We detected only 2697 tokens lacking a lemma (0.25% of the total), most of which are proper nouns

## Analysis
* unambiguous matches: `720860` tokens
* ambiguous matches: `54903` tokens
* missing: `81032` tokens: either the token does not possess a lemma or: 1) the lemma is unknown to LiLa 2) there is a mismatch between lemma and PoS from the LiLa lemma bank standpoint. A total of `699` words are ready to be added to the lemma bank: those are mainly proper nouns, adjectives (often derived from proper nouns), common nouns, adverbs and numerals

## Acknowledgements

The LiLa project has received funding from the European Research Council (ERC) under the European Union’s Horizon 2020 research and innovation programme – Grant Agreement No. 769994
