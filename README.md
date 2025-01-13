# Handling of Large Context in LLMs

## Overview

This repository accompanies the paper **"Handling of Large Context in LLMs"** by _Hardik Joshi_. It explores the limitations of Large Language Models (LLMs) in managing long-range dependencies and provides a comparative evaluation of models like Transformer-XL, Compressive Transformer, Hierarchical Attention Mechanism (HAM), and Hierarchical Attention Transformer Networks (HATN).

## Abstract

The paper addresses the context-length problem in LLMs due to quadratic complexities in attention mechanisms. Proposed solutions include:

- **Transformer-XL**: Introduces recurrence for extended memory retention.
- **Compressive Transformer**: Compresses past memory for efficiency.
- **Hierarchical Attention Mechanism (HAM)** and **Hierarchical Attention Transformer Networks (HATN)**: Employ hierarchical structures to capture interdependencies at various abstraction levels.

The document evaluates these approaches through tasks like text generation and document classification.

## Results

### Key Findings

1. **Text Generation (Perplexity)**:

   - Compressive Transformer outperforms Transformer-XL on the Wiki9 and BookCorpus datasets.
   - Lower Perplexity (PPL) scores highlight superior long-range dependency handling.

2. **Document Classification (Accuracy)**:
   - HATN achieves the highest accuracy on the Newsgroups dataset, followed by HAM, Compressive Transformer, and Transformer-XL.

### Dataset Results

| Dataset    | Model                    | Attention Heads | Perplexity (PPL) | Accuracy (%) |
| ---------- | ------------------------ | --------------- | ---------------- | ------------ |
| Wiki9      | Transformer-XL           | 2               | 35.1142          | -            |
|            | Transformer-XL           | 8               | 34.0151          | -            |
|            | Compressive Transformer  | 2               | 34.3316          | -            |
|            | Compressive Transformer  | 8               | 32.4866          | -            |
| BookCorpus | Similar to Wiki9 Results | -               | -                | -            |
| Newsgroups | Transformer-XL           | -               | -                | 38.78        |
|            | Compressive Transformer  | -               | -                | 41.47        |
|            | HAM                      | -               | -                | 42.09        |
|            | HATN                     | -               | -                | 44.23        |

## Insights

- **Compressive Transformer** demonstrates superior long-range coherence and context retention in sequence generation tasks.
- **HATN** excels in tasks requiring deep understanding of lengthy documents, showcasing the advantages of hierarchical attention.

## Code

### Implementations

The repository contains:

1. **Transformer-XL and Compressive Transformer**: Custom implementations for evaluating long-range dependencies.
2. **HAM and HATN**: Official implementations provided by respective authors.

### References

- [Hierarchical Attention Networks for Document Classification](https://www.cs.cmu.edu/~./hovy/papers/16HLT-hierarchical-attention-networks.pdf)
- [Hierarchical Attention Transformer Networks](https://ieeexplore.ieee.org/document/9533869)
- [Transformer-XL](https://arxiv.org/abs/1901.02860)
- [Compressive Transformer](https://arxiv.org/abs/1911.05507)
- [HATN Code](https://github.com/TengfeiLiu966/HATN)
- [HAM Code](https://github.com/vietnh1009/Hierarchical-attention-networks-pytorch)
- [Transformer-XL and Compressive Transformer Code](https://github.com/hardikjoshi009/transformerXl-and-compressive_transformer)

## Conclusion

The research highlights promising solutions to the context-length problem in LLMs. Model selection should be guided by specific NLP task requirements, such as text generation or document classification.

For further details, refer to the [paper](#) or explore the codebase.

---
