# PopCon
This project is a PyTorch implementation of PopCon which is submitted to PAKDD 2023.

## Prerequisties
Our implementation is based on Python 3.8 and Pytorch 1.8.1. Please see the full list of packages required to our codes in `requirements.txt`.

## Datasets
We use 3 datasets in our work: Steam, Youshu, and NetEase.
We include the preprocessed datasets in the repository: `data/{data_name}`.

## Backbone model
We provide DAM, which is one of the state-of-the-art bundle recommendation model, as a backbone.
It is defined in `models.py`.

## Running the code
You can run the pretraining code by `python pretrain.py` with arguments `--epochs` and `--alpha`.
You can also run the reranking code by `python reranking.py` with arguments `--beta` and `--n`.
To run `reranking.py`, running `pretrain.py` must precede because it returns a recommendation results of a model.
We provide `demo.sh`, which reproduces the experiments of our work.
