# Prompt Engineering Setup Guide

This repository is dedicated to the setup and configuration of a prompt engineering environment for AI models. It provides a step-by-step guide to installing Anaconda, setting up a conda environment, and configuring necessary environment variables. The setup primarily focuses on the use of Hugging Face models. The repository is designed to facilitate collaboration and discussion among our teams, with the aim of optimizing AI model development and usage.

## Prerequisites

### Anaconda Installation

Download and install Anaconda from the official [Anaconda website](https://www.anaconda.com/download). For Windows users, the following version has been tested and confirmed to work: [Anaconda3-2023.07-2-Windows-x86_64.exe](https://repo.anaconda.com/archive/Anaconda3-2023.07-2-Windows-x86_64.exe).

### Environment Setup

Create a new conda environment using the provided `env.yml` file. This can be done in the terminal or an Anaconda Prompt with the following command:

```bash
conda env create -f env.yml
```

Ensure that you're in the same directory as the `env.yml` file, or provide the full path to the file.

### Environment Variables Configuration

Set up the necessary environment variables. Note that you'll need a Hugging Face account and an API key to use the Hugging Face models. Register for an account at [Hugging Face](https://huggingface.co/join) if you don't have one.

```bash
conda env config vars set -n prompt_engineering OPENAI_MODEL=openchat/openchat-3.5-0106
conda env config vars set -n prompt_engineering OPENAI_API_KEY=sk-your_api_key
```

Replace `your_api_key` with your actual Hugging Face API key.

### Environment Activation and Jupyter Notebook Launch

Activate the newly created environment and start Jupyter Notebook:

```bash
conda activate prompt_engineering
jupyter notebook
```

### Visual Studio Code Setup

Open Visual Studio Code and install the Python and Jupyter extensions.

### Jupyter Kernel Selection

Open the `techniques.ipynb` notebook and select the `prompt-engineering` Jupyter server kernel:

- Click on `Select Kernel`.
- Choose `Select Another Kernel`.
- Opt for `Existing Jupyter Server`.
- Finally, select `localhost`.
