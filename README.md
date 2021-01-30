# PyTorrent: A Python Library Corpus for Large-scale Language Models
A large scale collection of both semantic and natural language resources is essential to leverage active Software Engineering research areas such as code reuse and code comprehensibility. Existing machine learning models ingest data from Open Source repositories (like GitHub projects) and forum discussions (like Stackoverflow.com),  whereas, in this showcase, we took a step backward to orchestrate a corpus titled PyTorrent that contains 218,814 Python package libraries from PyPI and Anaconda environment. This is because earlier studies have shown that much of the code is redundant and Python packages from these environments are better in quality and are well-documented. PyTorrent enables users (such as data scientists, students, etc.) to build off the shelf machine learning models directly without spending months of effort on large infrastructure.

## PyTorrent Dataset
Package dataset contains a set of pairs of <NL,PL> in JSON format. We use CodeSearchNet data format as described [here](https://github.com/github/codesearchnet#data-details). Therefore, the dataset can be easily plugin to CodeSearchNet Deep learning model architecture and other similar architectures such as [CodeBERT](https://github.com/microsoft/CodeBERT) for fine-tuning a code retrieval task.
- [Zenodo Archive](https://zenodo.org/record/4451357#.YBUhTOhKifQ) 

[![DOI](https://zenodo.org/badge/DOI/10.5281/zenodo.4451357.svg)](https://doi.org/10.5281/zenodo.4451357)

- Schema of Dataset: TBA 

## Package Metadata
- [All packages](https://github.com/fla-sil/PyTorrent/tree/main/Package_Metadata)

## PyTorrent Transformer-based Model
- [RoBERTa-MLM model at HuggingFace](https://huggingface.co/Fujitsu/pytorrent)

## PyTorrent Schema
- [Updated PyPI schema](https://github.com/fla-sil/PyTorrent/blob/main/anaconda_schema.json)

- [Updated Anaconda schema](https://github.com/fla-sil/PyTorrent/blob/main/schema.json) 



