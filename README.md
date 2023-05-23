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

We used different transformer modles namely: monolingual transformer models as well as multilingual transformer model for our experiment. Monolingual Nepali transformer models are trained from scratch using Nepali text while multilingual models are trained to combine other languages. All of the transformers model used are available on HuggingFace. The different transformer based modles used are as follows:
- NPVec1-BERT (baseline)
- NepaliBERT
- NepBERT
- DB-BERT
- BERT-bbmu

Model comparison on DanfeNER-test

|Model |Pre. |Rec. |F1|
| --- | --- | --- | --- |
|NPVec1-BERT|0.63 |0.62| 0.63|
|NepaliBERT|0.72| 0.69| 0.70|
|NepBERT|0.71 |0.69 |0.70|
|DB-BERT|**0.80** |**0.80** |**0.80**|
|BERT-bbmu|0.76 |0.74 |0.75|


Performance evaluation of the best performing model (DB-BERT) per named entities: 
|Model|Pre. |Rec. |F1| Support|
| --- | --- | --- | --- |--- |
|PER|0.81|0.77|0.79|444|
|LOC|0.83|0.86|0.84|389|
|ORG|0.79|0.79|0.79|356|
|EVT|0.53|0.29|0.37|28|
|DAT|0.78|0.84|0.81|286|


# License 
Non-commercial purposes only. For commercial usages, permissions must be taken from the authors and the relevant parties. See the contact address below. 

Unless required by applicable law or agreed to in writing, software and data distributed here is on an "AS IS" BASIS, WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.

# Cite Our Work
If you use the EverestNER data set, please cite [our publication]((https://journals.flvc.org/FLAIRS/article/download/133384/137473)):
```bibtex
@inproceedings{niraula2023danfener,
  title={DanfeNER-Named Entity Recognition in Nepali Tweets},
  author={Niraula, Nobal and Chapagain, Jeevan},
  booktitle={The International FLAIRS Conference Proceedings},
  volume={36},
  year={2023}
}
```

# Contact 
Feel free to contact nobal @AT nowalab .DOT com and cjeevaniam @AT gmail .DOT com for any inquiries regarding this work.

# Acknowledgments
Nepali Shabdakosh - https://nepalishabdakosh.com 
