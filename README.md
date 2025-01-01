# PyTorrent: A Python Library Corpus for Large-scale Language Models
A large scale collection of both semantic and natural language resources is essential to leverage active Software Engineering research areas such as code reuse and code comprehensibility. Existing machine learning models ingest data from Open Source repositories (like GitHub projects) and forum discussions (like Stackoverflow.com), whereas, in this showcase, we took a step backward to orchestrate a corpus titled PyTorrent that contains 218,814 Python package libraries from PyPI and Anaconda environment. This is because earlier studies have shown that much of the code is redundant and Python packages from these environments are better in quality and are well-documented. PyTorrent enables users (such as data scientists, students, etc.) to build off the shelf machine learning models directly without spending months of effort on large infrastructure.

The preprint version of the paper is available at: [https://arxiv.org/pdf/2110.01710](https://arxiv.org/pdf/2110.01710)

## PyTorrent Dataset
Package dataset contains a set of pairs of <NL,PL> in JSON format. We introduce PyTorrent for the first time, which is curated data of both metadata and all official Python packages as December 2020. We use CodeSearchNet data format as base schema ([detail](https://github.com/github/codesearchnet#data-details)). Therefore, the dataset can be easily plugin to CodeSearchNet Deep learning model architecture and other similar architectures such as [CodeBERT](https://github.com/microsoft/CodeBERT) for training or fine-tuning a code retrieval task and other language model based tasks.

## Download Dataset 
We processed 218,814 Python packages and generates a set of pairs of <NL,PL> in [JSONL format](https://jsonlines.org/). The datasets can be downloaded from Zenodo Archive as follows. Download the dataset that includes three Augmented Code Scenarios. 

- [Zenodo Archive](https://zenodo.org/record/4546290) 

[![DOI](https://zenodo.org/badge/DOI/10.5281/zenodo.4546290.svg)](https://doi.org/10.5281/zenodo.4546290)


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

A pretrained model based on 1M Python scripts from PyTorrent. It is a RoBERTa-MLM-based model and can be fine-tuned on any downstream task on Python programming language.

## More detail?
<a href="https://automlpodcast.com/episode/bert-sort-how-to-use-language-models-to-semantically-order-categorical-values"><img src="https://images.podcastpage.io/fetch/https%3A%2F%2Fstorage.buzzsprout.com%2Fvariants%2Flmm4qmbs2knbyqxpauluugywm8il%2F5cfec01b44f3e29fae1fb88ade93fc4aecd05b192fbfbc2c2f1daa412b7c1921.jpg?w=365&dpr=2.0" width="90"></img></a>

Checkout the second section of [BERT-Sort podcast episode](https://automlpodcast.com/episode/bert-sort-how-to-use-language-models-to-semantically-order-categorical-values) at the AutoML Podcast where Mehdi discusses objective of PyTorrent. 

## Contacting us
We processed only publicly available records of Python packages. However, if you need any information to be updated/removed from metadata of packages or source-codes, please raise an issue.

## Utilized PyTorrent
PyTorrent has been used by both practitioners and researchers as follows. Feel free to share with us how you utilize PyTorrent in your work.
- Dai et al. utilized PyTorrent in One Model, Multiple Modalities by creating a dataset which is translating the PyTorrent dataset. The authors translate English docstrings to Chinese by a translation toolkit Transmart. More detail can be found [here](https://arxiv.org/pdf/2205.06126.pdf).
- Dahal et al. utilized PyTorrent in SCOTCH where the author compare Python dataset against their work. More detail can be found [here](https://openreview.net/pdf?id=rSxfCiOZk-c)
- Bahrami et al. (the authors of PyTorrent) utilized PyTorrent in AugmentedCode where a large number of augmented code has been produced through PyTorrent to fine-tune and train a SOTA Python code search. More detail can be found [here](https://arxiv.org/pdf/2110.08512.pdf)
- Yang et al. used PyTorrent to evaluate their proposed approach of neuRAl coDe generAtor Robustifier (RADAR). More detail can be found [here](https://arxiv.org/pdf/2211.15844.pdf)
- Gong et al. utilized PyTorrent to train and evaluate MultiCoder whihc is a Multi-Programming-Lingual Pre-Training for Low-Resource Code Completion. More detail can be found [here](https://arxiv.org/pdf/2212.09666.pdf)
- Chen et al. used PyTorrent as a code base for the retrieval of Python code, and also used it as a source of queries when discussing the time efficiency of different retrievers. More detail can be found [here](https://dl.acm.org/doi/abs/10.1145/3597503.3639085).

## Citation
Mehdi Bahrami, N. C. Shrikanth, Shade Ruangwan, Lei Liu, Yuji Mizobuchi, Masahiro Fukuyori, Wei-Peng Chen, Kazuki Munakata, Tim Menzies, "PyTorrent: A Python Library Corpus for Large-scale Language Models", URL: [https://arxiv.org/pdf/2110.01710](https://arxiv.org/pdf/2110.01710)
```
@misc{bahrami2021pytorrent,
      title={PyTorrent: A Python Library Corpus for Large-scale Language Models}, 
      author={Mehdi Bahrami and N. C. Shrikanth and Shade Ruangwan and Lei Liu and Yuji Mizobuchi and Masahiro Fukuyori and Wei-Peng Chen and Kazuki Munakata and Tim Menzies},
      year={2021},
      eprint={2110.01710},
      archivePrefix={arXiv},
      primaryClass={cs.SE},
      howpublished={https://arxiv.org/abs/2110.01710},
}
```
