# PyTorrent: A Python Library Corpus for Large-scale Language Models
A large scale collection of both semantic and natural language resources is essential to leverage active Software Engineering research areas such as code reuse and code comprehensibility. Existing machine learning models ingest data from Open Source repositories (like GitHub projects) and forum discussions (like Stackoverflow.com), whereas, in this showcase, we took a step backward to orchestrate a corpus titled PyTorrent that contains 218,814 Python package libraries from PyPI and Anaconda environment. This is because earlier studies have shown that much of the code is redundant and Python packages from these environments are better in quality and are well-documented. PyTorrent enables users (such as data scientists, students, etc.) to build off the shelf machine learning models directly without spending months of effort on large infrastructure.

## PyTorrent Dataset
Package dataset contains a set of pairs of <NL,PL> in JSON format. We introduce PyTorrent for the first time, which is curated data of both metadata and all official Python packages as December 2020. We use CodeSearchNet data format as base schema ([detail](https://github.com/github/codesearchnet#data-details)). Therefore, the dataset can be easily plugin to CodeSearchNet Deep learning model architecture and other similar architectures such as [CodeBERT](https://github.com/microsoft/CodeBERT) for training or fine-tuning a code retrieval task and other language model based tasks.

## Download Dataset 
We processed 218,814 Python packages and generates a set of pairs of <NL,PL> in [JSONL format](https://jsonlines.org/). The datasets can be downloaded from Zenodo Archive as follows. Download the dataset that includes three Augmented Code Scenarios. 

- [Zenodo Archive](https://zenodo.org/record/4451357#.YBUhTOhKifQ) 

[![DOI](https://zenodo.org/badge/DOI/10.5281/zenodo.4451357.svg)](https://doi.org/10.5281/zenodo.4451357): 



## Dataset Schema
Dataset schema explains the structure of dataset and different fields' definitions.
- [Dataset schema](https://github.com/fla-sil/PyTorrent/blob/main/schema.md)

## Metadata of all Python Packages
- [All packages](https://github.com/fla-sil/PyTorrent/tree/main/Package_Metadata)
- PyTorrent Metadata Schema
  + [Updated PyPI schema](https://github.com/fla-sil/PyTorrent/blob/main/anaconda_schema.json)

  + [Updated Anaconda schema](https://github.com/fla-sil/PyTorrent/blob/main/schema.json) 

Each package metadata includes the detail of Python software package. The packages have been collected from PyPI and Anaconda Package distribution. It includes features such as Software Package License, website, publisher, description and etc. Each packages saves as a JSON file.

## Mapping Records to Package Metadata
You may simply map each record of datasets to metadata by using [`repo`](https://github.com/fla-sil/PyTorrent/blob/main/schema.md) or [`path`](https://github.com/fla-sil/PyTorrent/blob/main/schema.md) fields to [metadata package title](https://github.com/fla-sil/PyTorrent/tree/main/Package_Metadata).

## PyTorrent Transformer-based Model
- [RoBERTa-MLM model at HuggingFace](https://huggingface.co/Fujitsu/pytorrent)  <img src="https://huggingface.co/front/assets/huggingface_logo.svg" width="40">

A pre-trained model based on 1M Python scripts from PyTorrent. It is a RoBERTa-MLM-based model and can be fine-tuned on any downstream task on Python programming language.

