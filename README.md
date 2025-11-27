# Computational Social Mixed Methods Pipelines

Accompanying material to the paper "Measuring Complex Constructs in Large-Scale Text with Computational Social Mixed Methods" 
[(Herderich, Lasser, et al., 2025)](https://osf.io/preprints/psyarxiv/tzc9p_v1).

## Abstract

A growing convergence between social science and machine learning enables, in principle, large-scale analyses of complex social phenomena through text. 
Yet, approaches leveraging supervised text classification based on human-annotated data for statistical analysis often treat conceptual validity and 
technical performance as separate challenges impairing measurement quality. We provide guidelines to bridge this gap in what we call 
*computational social mixed methods pipelines* across three stages: data annotation, model training, and statistical analysis. Building on 
best practices and our own methodological innovations, such as Iterative Sampling and Training on Confident Examples, we address recurring 
pitfalls like unbalanced training data or stagnant model performance. We also discuss when large language models constitute a viable alternative 
to transformer-based classifiers. Using a case study on countering online hate, we illustrate how consequently integrating social science and 
machine learning expertise improves the validity and comparability of computational social science.

## Structure of the Repository

- `01 to 05`: Each jupyter notebook illustrates a key problem of computational social mixed methods pipelines and how to overcome them.
- `data`: Sample data to run the code. The tweets are a selection of our corpus from the working example on countering online hate. We rephrased the tweet text using GPT-4 to abide to Twitter's terms of service.
- `finetuned models`: Saves pretrained models for inference. Includes a Support Vector Machine to illustrate "iterative sampling". To obtain the transformer model needed for notebook 5 "sampling groups for comparison", first run notebook 3 "training on confident examples".
- `results`: Collects results for "LLMs as classifiers" and "training on confident examples".
- `CSMM-pipeline.yml`: File to create a virtual environment to run the code. Includes all dependencies. Install with `condo env create -f CSMM-pipeline.yml`
