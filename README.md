# BasqueParl: A Bilingual Corpus of Basque Parliamentary Transcriptions

This repository contains **BasqueParl**, a bilingual corpus for political discourse analysis. It covers transcriptions from the Parliament of the Basque Autonomous Community for eight years and two legislative terms (2012-2020), and its main characteristic is the presence of Basque-Spanish code-switching speeches.

For instance, the following unprocessed speech combines a **Basque** text (plain) with **Spanish** fragments (highlighted):

> Bai, zure baimenarekin hemendik.
>
> Ba zure desioak, Guanche andrea, gureak ere badira. Harritu nau eta ez nau harritu hitza berriro hartzeak, zeren hitz egiten nengoen bitartean esan diozu albokoari `le voy a contestar. Le voy a contestar`, ondo iruditzen, zure eskubidean zaude, baino beno, ez dut uste inongo astakeriarik esan dudanik.
>
> Gauzak egiten dira eta uste dut nik, nik ere eskubidea dudala Gobernuak eta beste erakundeek egiten dutena esateko. Zeren beti `ver el vaso medio vacío o medio lleno, pues cambia un poco la perspectiva y vernos siempre en modo Gobierno, creo que no es nada objetivo. Se hacen cosas, se harán cosas y esta vez creo que me deberían reconocer que de la iniciativa primera a lo que hemos acordado, no nos hemos dejado nada o creo que casi nada. Entonces, bueno, sólo querı́a aclarar eso` eta eskerrak berriro.
>
> Eta ziur egon emakumea dokumentu horietan ez bada agertzen hitzetan, zeren uste dut hori ez dela garrantzitsuena, bai politiketan egongo dela eta dagoela.
>
> Eskerrik asko.

The specificities of the **BasqueParl** corpus are:

- **14 M words** of bilingual parliamentary transcriptions
- **Speech paragraphs** as units
- Metadata such as **date** and **speaker's name**, **year of birth**, **gender** and **party** for each paragraph
- **Language** of each paragraph (either Basque or Spanish)
- **Lemmas** and **named entities** of each paragraph, with and without stopwords

## Data Fields

The **BasqueParl** corpus is written as a Tab Separated Values (TSV) file. Each unit presents the next fields:

- **"date"**: Date corresponding to the speech, e.g. _2020-02-07_
- **"speech_id"**: Number that identifies the speech within its date, e.g. _3_
- **"text_id"**: Number that identifies the paragraph within its speech, e.g. _3_
- **"speaker"**: Family names of the speaker, including their position if any, e.g. _Tejeria Otermin LEHENDAKARIA_
- **"birth"**: Year of birth of the speaker, e.g. _1971_
- **"gender"**: Gender of the speaker, either _E_ (_emakumea_) for female or _G_ (_gizona_) for male
- **"party"**: Political group of the speaker, e.g. _EAJ_
- **"language"**: Language assigned to a paragraph, either _eu_ for Basque or _es_ for Spanish
- **"text"**: Paragraph of the speech text
- **"lemmas"**: Lemmatized paragraph
- **"lemmas_stw"**: Lemmatized paragraph without stopwords
- **"entities"**: Named entities extracted from the paragraph
- **"entities_stw"**: Named entities extracted from the paragraph without stopwords

## Methodological Information

**Lemmas** and **named entities** of each paragraph have been extracted with these state-of-the-art Flair [lemmatization](ixa2.si.ehu.es/ragerri/flair-es-eu-lemma-models.tar.gz) and [NER](ixa2.si.ehu.es/ragerri/flair-es-eu-ner-models.tar.gz) models:

> R. Agerri, I. S. Vicente, J. A. Campos, A. Barrena, X. Saralegi, A. S. Etxabe, and E. Agirre (2020). Give your text representation models some love: the case for basque. In LREC.
> 
> R. Agerri (2020). Projecting heterogeneous annotations for named entity recognition. In Iber-LEF@SEPLN.

**Language detection** was performed by means of [langdetect](https://github.com/fedelopez77/langdetect).

## If you use this resource please cite the following paper:

+ Nayla Escribano, Jon Ander Gonzalez, Julen Orbegozo-Terradillos, Ainara Larrondo-Ureta, Simón Peña-Fernández, Olatz Perez-de-Viñaspre and Rodrigo Agerri  (2022). [BasqueParl: A Bilingual Corpus of Basque Parliamentary Transcriptions](http://www.lrec-conf.org/proceedings/lrec2022/pdf/2022.lrec-1.361.pdf). In *LREC 2022*.
