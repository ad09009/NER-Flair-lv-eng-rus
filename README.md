# Fine-Tuning Pre-Trained NER Models

##### Course project
##### NLP and AI seminar 2021 
##### University of Latvia


## About

The repo holds 3 NER models that where fine-tuned as part of this project, several Jupyter Notebooks that demonstrate the results of the training as well as the basic usage of the models and some that depict the training steps. 

All datasets that the 3 models were trained on, were first cleared from all labels but those that describe personal names (B-PER, I-PER and similar). For example:
```console
2021-12-15 00:11:37,789 Created (for label 'ner') Dictionary with 4 tags: <unk>, O, B-PER, I-PER 
Dictionary with 4 tags: <unk>, O, B-PER, I-PER
```

This project uses the [Flair](https://github.com/flairNLP/flair) framework - a powerful and easy to use NLP library.


## Models

| Language | Dataset | F-score | Folder | Embeddings used
|  ---  | ----------- | ---------------- | ------------- | ------------- |
| English | Conll-03 (originally 4-class, reduced to 1)   |  **0.9694**  | [eng-ner-flair-edit](https://github.com/ad09009/NER-Flair-lv-eng-rus/tree/main/resources/taggers/eng-ner-flair-edit) | [Flair embeddings, news-X](https://github.com/flairNLP/flair/blob/master/resources/docs/embeddings/FLAIR_EMBEDDINGS.md)  |
| Latvian | [LUMII AILab](https://github.com/LUMII-AILab) data |  **0.9391**  | [lv-ner-flair-edit](https://github.com/ad09009/NER-Flair-lv-eng-rus/tree/main/resources/taggers/lv-ner-flair-edit) | [BERT Emoji Latvian Twitter ](https://huggingface.co/FFZG-cleopatra/bert-emoji-latvian-twitter) |
| Russian  | MultiCoNER: SemEval-2022   |  **0.7358**  | [rus-ner-flair-edit](https://github.com/ad09009/NER-Flair-lv-eng-rus/tree/main/resources/taggers/rus-ner-flair-edit) | [DeepPavlov RuBERT Base Cased](https://huggingface.co/DeepPavlov/rubert-base-cased)  |


## Requirements and how to

The project is based on Flair 0.10 which runs on PyTorch 1.5+.
Python 3.8 was used.
Also JupyterLab 3.2.4.

#### How to: 

In your favorite virtual environment run: 
```
pip install flair
pip install jupyterlab
```

Or, alternatively:

```python
pip install -r /path/to/requirements.txt
```

Download the model files and place them into corresponding folders:

| Model | Filename | Folder | Download link |
|  ---  | ----------- | ---------------- | ------------- |
| English | final-model.pt   |  resources/taggers/eng-ner-flair-edit  | [eng-ner-flair-edit](https://drive.google.com/file/d/1couddFD6xFhN-Kvj-FdyTPYn6YVWJ60i/view?usp=sharing) |
| Latvian | final-model.pt |  resources/taggers/lv-ner-flair-edit  | [lv-ner-flair-edit](https://drive.google.com/file/d/1cNTEqA3WLJ5iROztW6BlQ2npb4bGwAwI/view?usp=sharing) |
| Russian  | final-model.pt   |  resources/taggers/rus-ner-flair-edit  | [rus-ner-flair-edit](https://drive.google.com/file/d/1-8v5o_IoqZ20NJXC43wzDjI-jMlTF0Ba/view?usp=sharing) |


## Contact

Please contact [Me](https://github.com/ad09009) if any comments or questions arise.
