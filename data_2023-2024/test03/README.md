# Folder contents
## Overview
This folder contains the relevant data of the second run of first parsing experiment of the PIBIC project of 2023 and 2024. The file `yrl_complin-ud-test.conllu` contains all the 1750 sentences from the version of UD_Nheengatu-CompLin as of September 10, 2024 ([commit](https://github.com/CompLin/nheengatu/commit/eb6529a96166213db9de1bb020229cb85444a9b6). The file `sample.conllu` contains the same sentences, excepting those with the _Casasnovas2006_ `sent_id` prefix. It totals 1564 sentences. The files `test-1.conllu`, `train-1.conll`, `test-2.conllu`, `train-2.conll` etc. result sucessively spliting the `all.conllu` file. The split was performed 10 times by the `TestSuite.py` script, each time alocating 10% and 90% of the sentences from the `sample.conllu` file to the test set and train set, respectively.

The `sample.conllu` file was built with the following commands:

```python

>>> sents=Yauti.extractConlluSents(Yauti.TREEBANK_PATH)
>>> len(sents)
1750
>>> sents=Yauti.extractConlluSents(Yauti.TREEBANK_PATH)
>>> len(sents)
1750
>>> sample=[sent for sent in sents if not sent.metadata['sent_id'].startswith('Casasnovas2006')]
>>> len(sample)
1564
>>> import os
>>> USER=os.path.expanduser('~')
>>> Yauti.writeSentsConllu(sents,os.path.join(USER,'pibic/data_2023-2024/test03','sample.conllu'))

```

## The train and test files
test-10.conllu
test-1.conllu
test-2.conllu
test-3.conllu
test-4.conllu
test-5.conllu
test-6.conllu
test-7.conllu
test-8.conllu
test-9.conllu
train-10.conllu
train-1.conllu
train-2.conllu
train-3.conllu
train-4.conllu
train-5.conllu
train-6.conllu
train-7.conllu
train-8.conllu
train-9.conllu

## The model files
model-10.output
model-1.output
model-2.output
model-3.output
model-4.output
model-5.output
model-6.output
model-7.output
model-8.output
model-9.output

## Results for parsing with gold tokenization and gold tags
gold-tok-tags-10.txt
gold-tok-tags-1.txt
gold-tok-tags-2.txt
gold-tok-tags-3.txt
gold-tok-tags-4.txt
gold-tok-tags-5.txt
gold-tok-tags-6.txt
gold-tok-tags-7.txt
gold-tok-tags-8.txt
gold-tok-tags-9.txt

## Summary results in terms of mean LAS and standard deviation
results01.txt

