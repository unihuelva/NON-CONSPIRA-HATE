## Introduction

The hateRADAR-es (Anti-Hate Refugees Annotated Dataset and Analysis Resource) dataset is a corpus of Spanish-language Twitter messages meticulously compiled for the purpose of identifying content containing both hateful and negative expressions directed towards refugees. 

Thousands of tweets were extracted daily from the search string “refugees” in six different languages: Spanish (“refugiados”), English (“refugees”), German (“fluechtlinge”), French (“réfugiés”), Italian (“rifugiati”) and Portuguese (“refugiados”), during a period from December 2015 to December 2016. The original collection of tweets was collected with the help of NodeXL. The daily extractions were merged by language to obtain six different datasets. Once merged, any duplicated tweets were removed by considering the “id” of the tweet, which confers a unique identification number to each one. In this work, we have used the Spanish dataset composed of 355,810 tweets. Since our interest was not in the dissemination patterns of the tweets, we excluded retweeted messages to avoid repetition of tweets, finally obtaining a sample of 90,144 tweets.

This collection of tweet messages was previously labelled with the perspective of knowing the diversity of different discourses about refugees in different languages (Gualda and Rebollo, 2016; Rebollo, 2021). At that time, the qualitative software "Atlas ti" (https://atlasti.com/) was used. An extensive codebook was produced at that moment, which can be found in the annexes of Rebollo (2021).

With the description of the hateRADAR-es dataset, we elaborate on the methods employed for extracting and annotating the documents, providing comprehensive statistical insights into the collection. We want to offer the scientific community a useful resource for researching and deepening new approaches for the automatic detection of hate speech towards this group. We are confident that this dataset will be an invaluable resource for researchers who are seeking to understand the impact of hate speech on refugees. By providing access to this data, we hope to contribute to a greater understanding of this issue and to promote positive change in our communities. 

The hateRADAR-es dataset is available for research purposes. Researchers and analysts can utilize these labels for sentiment analysis, natural language processing (NLP), and other tasks related to grief and emotions. 

## Corpus Annotation

The dataset was created through a meticulous labelling process involving 5,000 tweets. Each tweet was carefully categorized to form a training dataset suitable for the supervised classification task. To carry out a manual labelling process by human experts, we used the Doccano tool (https://github.com/doccano/doccano), an open-source text annotation platform designed for human users. 

## Label Interpretation

In a first stage, the dataset was labelled by two experts on sociology and social work with the initial aim of distinguishing between tweets containing hate speech, racist or xenophobic discourse towards refugees (label “1”), and tweets that did not contain such an issue (label “0”). Given the subjective nature and the level of difficulty of the task, manual labelling of this dataset was facilitated with the support of an annotation guide specifically designed by domain experts (Gualda and Rebollo Díaz, 2024). The overall inter-annotation agreement during this phase reached a satisfactory correlation index of 0.66 of the Cohen’s Kappa coefficient. Out of 5000 labelled tweets, annotators reached an 85% agreement, with a 15% disagreement rate. In a subsequent stage, tweets where there was no consensus among annotators or raised uncertainties were meticulously analysed and evaluated by a third person, also an expert in sociology of migrations and social work, to resolve disagreements. This thorough review and discussion of the most challenging classification cases assisted in addressing certain subtleties in tweets posted on Twitter in this domain. 

## File Description

The hateRADAR-es dataset contains a collection of 5,000 tweets, exhaustively labelled for detecting hate speech, racist or xenophobic discourse towards refugees. 

The dataset is divided into two sets to ensure the reproducibility of experiments: a training dataset and a testing dataset. Both datasets are provided in CSV format and include the following fields:

- **Id_tweet**: The unique identifier for each tweet. You can use this ID to retrieve individual tweets from the Twitter API of your choice.
- **Text**: Represents the content of the tweet.
- **Label**: Binary label where 0 represents "No hate speech" and 1 represents "Hate speech detected".

### Train Dataset:
- **Number of Rows**: 4000. This set is intended for model training and validation, ensuring comprehensive learning and robustness against overfitting.
- **Class Distribution**:
  - 0 (No hate speech): 3048 entries, accounting for 76.2% of the dataset.
  - 1 (Hate speech detected): 952 entries, making up 23.8% of the dataset.

### Test Dataset:
- **Number of Rows**: 1000. This set is used for model evaluation, providing an unbiased assessment of the model's performance on unseen data.
- **Class Distribution**:
  - 0 (No hate speech): 762 entries, representing 76.2% of the dataset.
  - 1 (Hate speech detected): 238 entries, constituting 23.8% of the dataset.

In this dataset, the original usernames have been substituted with the placeholder '@user' to ensure privacy and prevent the identification of individuals. This measure has been taken to comply with privacy regulations and to maintain the anonymity of the users involved.

## Elaboration Process of the Annotation Guide and Annotation Process

The annotation process begins with an initial coding of 500 tweets. The original dataset, composed of 90,000 organic tweets in Spanish, had been used for a different purpose than this research for the elaboration of a doctoral thesis and other publications. On this R+D+i project, an initial sample of 500 cases previously tagged with "Atlas ti" and containing both hate and support tags for immigrants and refugees was selected to start a new annotation process, now adapted to the objectives of this project, basically, the identification of hatred towards refugees. In a later phase, after having initially tested this annotation guide with 500 cases, the annotation of 5000 tweets from the previously mentioned data set was carried out. For this purpose, two annotators (Jonás González Díaz and Laura Cabrera Álvarez) and a person who refereed the collection (Carolina Rebollo Díaz) did the annotation.

A first systematic test of the tool was carried out by annotating a first dataset of 200 tweets. The annotators were, in this case, Laura Cabrera Álvarez, Jonás González Díaz, Carolina Rebollo Díaz, Elena Ruiz Ángel (†), and Francisco Javier Santos Fernández. In all cases, they were research staff or students linked to the University of Huelva. We thank all the participants in this project for their contribution to this process, as well as the feedback received on the different versions and, especially, the comments received from the people who carried out the annotation process of this dataset, Jonás González Díaz and Laura Cabrera Álvarez. For more details, the annotation guide is available in Gualda and Rebollo (2024).

## Author Contributions

Jacinto Mata-Vázquez (JMV), Estrella Gualda (EG), Victoria Pachón-Álvarez (VPA), Carolina Rebollo-Díaz (CRD), and Juan Luis Domínguez (JLD) conceived the original idea and designed the paper.

- JMV was responsible for the global coordination of the research, and EG coordinated the team in charge of the annotation.
- CR collected the data from Twitter through NodeXL (https://nodexl.com/).
- JMV & VPA, based on the original dataset, built the hateRADAR-es dataset to develop the models for detecting hate speech against refugees messages described in the paper.
- EG & CR designed the annotation guide that was tested and applied to annotate the tweets.
- Jonás González Díaz and Laura Cabrera Álvarez annotated the dataset, and CRD acted as referee of the collection of 5,000 tweets.
- Pablo Cordón Hidalgo and Javier Román Pásaro designed the scripts for exporting, cleaning, and normalizing the data from the annotation tool.

## Citation

If you find the hateRADAR-es dataset useful in your research or projects, please acknowledge its use. A formal citation format will be provided once our related research paper is published. For now, you can reference this dataset as follows:

‘[Jacinto Mata, Estrella Gualda, Victoria Pachón, Carolina Rebollo, and Juan Luis Domínguez] Deep Learning Approaches for Identifying Anti-Refugee Speech in Spanish Texts, Under revision.’

## Contact 

If you have any questions, feedback, or need further information about the hateRADAR-es dataset, please feel free to contact us. 

If needed, you can request the non-anonymized dataset.

You can reach us via email at vpachon@uhu.es or mata@uhu.es.

We are open to collaboration or any suggestions to improve the dataset and its usability. Your input is valuable, and we look forward to hearing from you!

Thank you for using the hateRADAR-es dataset.
