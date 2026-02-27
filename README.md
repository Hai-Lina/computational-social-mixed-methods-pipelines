# Computational Social Mixed Methods Pipelines
This is the tutorial code for the paper Herderich, A., Lasser, J., Galesic, M., Aroyehun, S., David, G., & Garland, J. (2026). Measuring complex constructs in large-scale text with computational social mixed methods. *Under review*.

The tutorial is stand-alone. The paper is not necessary for the learner's understanding. However, for a more in-depth explanation and discussion of the concepts presented in the tutorial, we recommend studying the paper in conjunction.

## What Are Computational Social Mixed Methods?

[*Abstract from the paper*] A growing convergence between social science and machine learning enables, in principle, large-scale analyses of complex social phenomena through text. Yet, approaches leveraging supervised text classification based on human-annotated data for statistical analysis often treat conceptual validity and technical performance as separate challenges impairing measurement quality. We provide guidelines to bridge this gap in what we call **computational social mixed methods pipelines** across three stages: data annotation, model training, and statistical analysis. Building on best practices and our own methodological innovations, such as "Iterative Annotation" and "Training on Confident Examples", we address recurring pitfalls like unbalanced training data or stagnant model performance. We also discuss when large language models constitute a viable alternative to transformer-based classifiers. Using a case study on countering online hate, we illustrate how consequently integrating social science and machine learning expertise improves the validity and comparability of computational social science.

## Social Science Use Case

The working example of this tutorial refers to Lasser, J.\*, Herderich, A.\*, Garland, J., Aroyehun, S., David, G., & Galesic, M. (2025). Collective moderation of hate, toxicity, and extremity in online discussions. *PNAS Nexus, 4*(11), pgaf369. https://doi.org/10.1093/pnasnexus/pgaf369. We investigated counter speech as a direct, citizen-based answer to hate in online political discussions. We asked, for example, how counter speech is naturally expressed in text, and whether some strategies (e.g., giving an opinion versus being sarcastic) are more effective than others in reducing hate.

## Structure of the Repository

- `binder`: Contains files for setting up the environment (see below).
- `data`: Sample data to run the code. The tweets are a selection of our corpus from the working example. We rephrased the tweet text using GPT-4 to abide to Twitter's terms of service.
- `figures`: Contains figures for illustration used in the notebooks.
- `finetuned models`: Saves pretrained models for inference. Includes a Support Vector Machine to illustrate "Iterative Annotation". To obtain the transformer model needed for notebook `3_statistical_analysis`, first run notebook `2_model_training`.
- `results`: Collects results for "LLMs as classifiers" and "Training on Confident Examples".
- `notesbooks 0 to 3`: Each jupyter notebook illustrates one step of computational social mixed methods pipelines including `data annotation`, `model training`, and `statistical analysis`.

## Setting Up the Environment

There are two options to run the tutorial.<br>
A) Recreating the virtual environment with `conda` locally (best for reproducibility).<br>
B) Running the notebooks on Google Colab (most beginner friendly).

### With conda

`conda` is an open-source package manager. Please follow the steps below to recreate the virtual environment to run the code.

**Step 1**<br>
If you don't have Anaconda (conda), you can install it via their website. Go to https://www.anaconda.com/download and choose the right installer for your operating system. Simply run the installer following the default settings. To check whether the installation worked, reopen a terminal (or Anaconda Prompt on Windows) and type `conda --version`. If a version number appears, installation was successful.

**Step 2**<br>
Open a terminal to clone this repository. In the terminal run:

`git clone https://github.com/Hai-Lina/computational-social-mixed-methods-pipelines.git`<br>
`cd computational-social-mixed-methods-pipelines`

Remember to `cd` into the directory, where you would like to have the repository stored beforehand.

**Step 3**<br>
In the terminal, run `conda env create -f binder/environment.yml` to recreate the environment. Activate the evironment by running `conda activate CSMM-pipeline`.

**Step 4**<br>
You can now start jupyter notebook by simply typing `jupyter notebook`. In the browser, navigate to the tutorial folder. You can now open the notebooks and run the code.

### With Google Colab

If you do not want to use conda on your local machine, you can also run the tutorial in Google Colab. Google Colab is a free, browser-based jupyter notebook environment hosted by Google and accessible to everyone with a Google account.

**Step 1**<br>
Upload the entire repository (including notebooks and folders) to your Google Drive. Rename the folder `CSMM-pipeline`. (This is important to smoothly access this folder later in the code.)

**Step 2**<br>
Open a tutorial notebook, for example `1_data_annotation`. Change the runtime to GPU by selecting `Runtime > Change runtime type > T4 GPU`. This will make your code run faster. Next, uncomment the code in the very first cell and click `Run all`. *Note*: In notebook `1_data_annotation` Google will install the package `irrCAC`. To make use of the package, please restart the session (Google will prompt you for it anyways).

**Step 3**<br>
Grant permissions for Google Colab to connect to your Google Drive. This makes sure you have access to necessary files like data.

*Note*: You do not need to run the `0_introduction` notebook. Necessary packages are either installed in the other notebooks directly or already available on Google Colab by default.

## Hardware Requirements

You do not necessarily need GPU access to run this tutorial. We provided minimal examples, such that the code can run on any standard laptop. However, GPU access will make the code run much faster.

## Contact Details

If you have any questions or feedback regarding this tutorial, feel free to get in touch with Alina Herderich, Leechgasse 34, 8010 Graz, Austria, alina.herderich@uni-graz.at.
