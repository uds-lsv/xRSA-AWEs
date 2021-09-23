
# How Familiar Does That Sound?  :speech_balloon: :ear:
### Cross-Lingual Representational Similarity Analysis of Acoustic Word Embeddings :coffee:

This is the code base to train different models acoustic word embeddings (AWEs), evaluation scripts, and the representational similarity analysis (RSA) experiments reported in our **BlackboxNLP** paper in **EMNLP 2021**.

:pencil: [How Familiar Does That Sound? Cross-Lingual Representational Similarity Analysis of Acoustic Word Embeddings](https://arxiv.org/pdf/2109.10179.pdf)

<!-- To cite the paper

```
@inproceedings{Abdullah2021HowFD,
  title={How Familiar Does That Sound? Cross-Lingual Representational Similarity Analysis of Acoustic Word Embeddings},
  author={Badr M. Abdullah and Iuliia Zaitova and T. Avgustinova and B. Mobius and D. Klakow},
  booktitle={Proc. BlackboxNLP},
  year={2021}
}
``` -->

### Dependencies :dna:

python 3.8, pytorch 1.1, numpy, scipy, faiss, pickle, pandas, yaml


### Speech Data :speech_balloon: :left_speech_bubble:
The data in our study is drawn from the Multilingual GlobalPhone read speech database. We experiment with seven Indo-European languages: Czech :czech_republic:, Polish :poland:, Russian :ru:, Bulgarian :bulgaria:, Brazilian Portuguese :brazil:, French :fr:, and German :de:. Because the data is distributed under a research license by Appen Butler Hill Pty Ltd., we cannot re-distribute the raw speech data. However, if you have already access to the GlobalPhone speech database and you would like to access to our word-alignment annotations, train/test splits, and word-level IPA transcriptions, please contact the first author.


### Working with the code :snake:
To run a training experiment, write down all hyperparameters and other info in the config file ```config_file_train_awe_bigru_seq2seq.yml```

Then ...

```
>>> cd AWEs_phon_sim
>>> python nn_train_seq2seq_embeddings.py config_files/config_file_train_awe_bigru_seq2seq.yml
```

To evaluate the model on the acoustic word discrimination task, make sure the path to the pre-trained model is in this config file ```config_file_eval_awe_bigru_seq2seq.yml```

Then ...


```
>>> cd AWEs_phon_sim
>>> python nn_eval/nn_eval_seq2seq_embeddings.py config_files/config_file_eval_awe_bigru_seq2seq.yml
```

The code is fairly documented and the vectorization logic, as well as the code for the models, should be useful for other speech technology tasks. If you use our code and encounter problems, please create an issue or contact the first author.


If you use our code in a work that leads to a publication, please cite our paper as

```
@inproceedings{Abdullah2021HowFD,
  title={How Familiar Does That Sound? Cross-Lingual Representational Similarity Analysis of Acoustic Word Embeddings},
  author={Badr M. Abdullah and Iuliia Zaitova and Tania Avgustinova and Bend Möbius and Dietrich Klakow},
  booktitle={Proc. BlackboxNLP},
  year={2021}
}
```
