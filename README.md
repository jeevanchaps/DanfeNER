# DanfeNER - Named Entity Recognition in Nepali Tweets
We have created the largest human annotated Named Entity Recognition (NER) data set for Nepali tweets available to date.


## Data Set Stats
|Data |No. Tweets |Tokens |Avg. Len | LOC| ORG| PER| EVT| DAT|Total Entities|
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| Train | 5,366| 92,425| 17.22| 923| 782| 1,061| 34| 663| 3,463|
|Test| 2,301| 39,133| 17.00| 389| 356| 444| 28| 286| 1,503| 
|Total| 7,667| 131,558| 17.11| 1,312| 1,138| 1,505| 62| 949| 4,966|

## Data Format
The DanfeNER data set is divided into train (DanfeNER-train) and test (DanfeNER-test) sets. Each data set has character level as well as token leven annotations. Please read [our paper](https://journals.flvc.org/FLAIRS/article/download/133384/137473) to get more information on this.
* Character Level
    * Train: [DanfeNER-train-char.txt](DanfeNER-train-char.txt)
    * Test:  [DanfeNER-test-char.txt](DanfeNER-train-char.txt)

* Token Level 
    * Train: [DanfeNER-train-bio.txt](DanfeNER-train-bio.txt)
    * Test: [DanfeNER-test-bio.txt](DanfeNER-train-bio.txt)


## Our Results
