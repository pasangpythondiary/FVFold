# FVFold
FvFold Model is highly inspired from DeepAb model (https://github.com/RosettaCommons/DeepAb )
## Environment Setup

 Create and activate a python virtual environment

Then install necessary packages from this file
```
pip install -r requirements.txt
```

_Note_: PyRosetta should be installed following the instructions [here](http://pyrosetta.org/downloads).

## Download FvFold pretrained weight and unzip and copy the weight in trained_models/ensemble/
Two Trained weight has been given 
1)	Trained weights for evaluating therapeutic and rosetta benchmark dataset
Link: 
2)	Trained weights for evaluating Igfold benchmark
Link:

## Common workflows

Additional options for all scripts are available by running with `--help`.

_Note_: This project is tested with Python 3.7.9

_Note_: Using `--renumber` option will send your antibody to the [AbNum server](http://www.bioinf.org.uk/abs/abnum/).

## To predict fv structure of antibody
Put fasta files in pred folder inside data folder. Note the fasta file must contain >:H and >:L for indicating heavy and light chain
```
python predict.py –renumber
```
output will be saved in root pred folder

## To predict Nanobody structure of antibody
```
python predict.py --single_chain
```

