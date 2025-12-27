# Multi-Task Learning for News Analytics: NER + Event Classification / Проект «Многоцелевая модель для новостной аналитики: NER и классификации»
## Overview
This repository contains a reproducible experiment on Multi-Task Learning (MTL) designed for a news analytics platform. The goal is to unify token-level extraction and document-level classification into a single efficient pipeline.
## The Challenge
Currently, Named Entity Recognition (NER) and Event Classification (CLS) are performed by separate models. This results in:
Redundant feature extraction.
Inefficient computational resource usage.
Lack of shared context between tasks.
## Proposed Solution
We implement a Shared Encoder Architecture where a single transformer backbone feeds into two task-specific heads:
NER Head: Extracts entities (Persons, Orgs, Dates).
CLS Head: Detects global events and incident types.
## Hypothesis: 
Joint training will reduce inference latency and potentially improve model performance by leveraging shared representations between local entities and global document context.
## Goals
Implement a unified PyTorch/HuggingFace model for simultaneous NER and Classification.
Evaluate the trade-offs between single-task and multi-task performance.
Provide a quantitative analysis of task interaction.
## Dataset:
wget -O train.jsonl "https://huggingface.co/datasets/iluvvatar/NEREL/resolve/main/data/train.jsonl"
wget -O dev.jsonl   "https://huggingface.co/datasets/iluvvatar/NEREL/resolve/main/data/dev.jsonl"
wget -O test.jsonl  "https://huggingface.co/datasets/iluvvatar/NEREL/resolve/main/data/test.jsonl"

wget -O ent_types.jsonl"https://huggingface.co/datasets/iluvvatar/NEREL/resolve/main/ent_types.jsonl"
wget -O rel_types.jsonl "https://huggingface.co/datasets/iluvvatar/NEREL/resolve/main/rel_types.jsonl" 
## Architecture:

## Installation & Usage: 

## Results: