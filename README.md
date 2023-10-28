# Multi-Doc-Summarization

Attention: This project has not been completed yet!


This Multi-Document-Summarization project has 3 main phases:
   1) Creating Multi-Document Dataset: This dataset is created with the help of ReQuEST Project entailment task. Opinions with the N-largest RQE-Logits are supposed        as opinions with similar aspect and sentiment. Results prove that this method competes with state-of-the-art methods of creating Synthetic Multi-Doc Datasets.
   2) Changing Attention mechanisms in BART: BART Conditional Generation is pre-trained for Single-Document Summarization Task. Preparing this model for Multi-Doc 
      Summarization needs Changes in attention in both Encoder and Decoder.
      - Encoder: Converting Self-Attention to Hierarchical-Self-Attention
      - Decoder: Not implemented (converting Cross-Attention to Hierarchical-Cross-Attention)
  3) Fine-Tuning BART with new dataset


# ReQuEST: A compact multi-task model of Question Entailment, Query-focused Summarization, and Tag Generation

   This model is composed of 3 main layers:
      1) BART based Shared Encoder
      2) Two Partially Shared Decoders
      3) three task-specific heads

   - Question Entailment: contains an encoder and a multilayer neural network
   - Query-Focused Summarization: contains the same encoder accompanied by a decoder component and a linear head
   - Tag Generation: components are identical to Query-Focused Summarization except for the last decoder layers and the task-specific head
