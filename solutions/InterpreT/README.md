<p align="center">
  <img src="./assets/interpret_title_centered.png" alt="InterpreT: An Interactive Visualization Tool for Interpreting Transformers"/>
</p>

 
### Part of NLP Architect by Intel® AI Lab

## Overview
With the increasingly widespread use of Transformer-based models for NLU/NLP tasks, there is growing interest in understanding the inner workings of these models, why they are so effective at a wide range of tasks, and how they can be further tuned and improved. In order to contribute to enhanced model explainability and comprehension, we present **InterpreT**, an Interactive visualization tool for interpreting transformers. While **InterpreT** is a task agnostic tool, its functionalities are demonstrated through analysis of model behaviours for two disparate tasks: the Winograd Schema Challenge (WSC) and Aspect Based Sentiment Analysis (ABSA). In addition to providing various mechanisms for investigating general model behaviours, **InterpreT** enables novel, granular analysis by probing and visualizing the hidden representations of tokens at the layer level, empowering users with new insights regarding how and what their models are learning. A [screencast video](https://youtu.be/np3cT9Xt9PE) and a [live demo](http://interpret.intel-research.net) illustrate these points.

## Screencast Video

<p align="center">
  <a href="https://youtu.be/np3cT9Xt9PE"><img src="./assets/video_demo_thumbnail.png" alt="Video Demo" width="548" height="362.5"/></a>
</p>


## InterpreT Live Demo
A live demo of **InterpreT** for analyzing pre-trained and fine-tuned BERT behavior on WSC can be accessed at the following link: 
**http://interpret.intel-research.net**

<br>

The [live demo](http://interpret.intel-research.net) allows comparison of pre-trained BERT with BERT fine-tuned on WSC. Specifically, the user can explore how the attention heads and the contextualized embeddings change between these two models. We highly encourage users to watch the [screencast video](https://youtu.be/np3cT9Xt9PE) to get a sense of how the application works and how to navigate the application.

Below are some interesting phenomena we encourage users to explore in the [live demo](http://interpret.intel-research.net):
- In our analysis, we found that the embeddings of tokens which are predicted to be coreferents are in closer proximity in the embedding space, especially when BERT is fine-tuned for the coreference resolution task. This behaviour can be seen in the "Average t-SNE Distance Per Layer" plot in the bottom left when using the multi-select feature on the t-SNE plot. 
- The metric "finetuned_coreference_intensity" (which can also be used with the multi-select) in the head summary plot shows that the 7th head of layer 10 often places high attention between coreferent mention spans. This attention head can also be visualized in the “Attention Matrix/Map" plot for various examples. 
