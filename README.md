# Google-Fast-or-Slow?Predict-AI-Model-Runtime
Predict how fast an AI model runs
## Overview
Alice is an AI model developer, but some of the models her team developed run very slow. She recently discovered compiler's configurations that change the way the compiler compiles and optimizes the models, and hence make the models run faster (or slower)! My task is to help Alice find the best configuration for each model.

**My goal**: Train a machine learning model based on the runtime data provided in the training dataset and further predict the runtime of graphs and configurations in the test dataset.
---
## Description
A bit of technical background on an AI compiler will help you get started! An AI model can be represented as a graph, where a node is a tensor operation (e.g. matrix multiplication, convolution, etc), and an edge represents a tensor. A compilation configuration controls how the compiler transforms the graph for a specific optimization pass. In particular, Alice can control two types of configurations/optimizations:

A layout configuration control how tensors in the graph are laid out in the physical memory, by specifying the dimension order of each input and output of an operation node.
A tile configuration controls the tile size of each fused subgraph.


![inbox_16062769_c2b9a5de5a6951582f570cab63c1db83_layout](https://github.com/JessMog/Google---Fast-or-Slow-Predict-AI-Model-Runtime/assets/40331541/bb94a580-a7f7-4690-aa12-cadb6bd07d90)

![inbox_16062769_f6b4a1efcb148741fdda047ab608899f_tile](https://github.com/JessMog/Google---Fast-or-Slow-Predict-AI-Model-Runtime/assets/40331541/a4104570-cfc5-4bb0-9718-fdcbc1ecb6b8)
---
Being able to predict an optimal configuration for a given graph will not only help Alice's team but also improve the compiler's heuristic to select the best configuration without human's intervention. This will make AI models run more efficiently, consuming less time and resources overall!

In this competition, your aim is to train a machine learning model based on the runtime data provided to you in the training dataset and further predict the runtime of graphs and configurations in the test dataset.
