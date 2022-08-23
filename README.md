# Unsupervised Domain Adaptation Task
## Deep Learning Course Project 
### University of Trento, A.Y. 2021/22
___

The project has been developed as final assignment of the Deep Learning Course course, offered by the University of Trento. 

## Project objective 
In this notebook, we tackle the Unsupervised Domain Adaptation (UDA) task on the reduced version of Adaptiope dataset (Ringwald & Stiefelhagen, 2021). This version considers the real world (R) and product (P) domains and narrow down the classes to .

Our solution is inspired by the Domain-Symmetric Networks (SymNets), proposed by Zhang et al. (2019), and suggests additional architectural refinements to overcome model overfitting and overconfidence.

The deployed version of the architecture outperforms both the external baseline (i.e., from the assignment description) and the internal one, namely the source-only model. However, it is worth noting how the gain's magnitude varies depending on source and target domain definition, meaning the direction of the adaptation.

## Prerequisites 

In order to run this project, the following tools have to be installed on your machine: 
- Python, preferably [3.9](https://www.python.org/downloads/release/python-390/) 

or: 
- [Google Colab](https://colab.research.google.com/)

## Run the project locally 

### Clone the repository in a local machine

Clone this repository in a local directory typing in the command line: 

```
git clone https://github.com/detch-for-shor/deep-learning-proj.git
```

### Environment 
The creation of a virtual environment is highly suggested. If not already installed, install virtualenv:

- in Unix systems:
    ```
    python3 -m pip install --user virtualenv
    ```

- in Windows systems:
    ```
    python -m pip install --user virtualenv
    ```

And then create the virtual environment named *venv* typing in the command line (inside the project folder): 

- in Unix systems:
    ```
    python3 -m venv venv
    ```

- in Windows systems:
    ```
    python -m venv venv
    ```

The virtual environment can be activated as follow: 

- in Unix systems:
    ```
    source venv/bin/activate
    ```

- in Windows systems:
    ```
    venv\Scripts\activate
    ```
### Requirements 

In the active virtual environment, install all libraries contained in the `requirements.txt` file:

```
pip install -r requirements.txt
```
---
## Run the project on Google Colab  

### Clone the repository 

Clone the repository and open it as a notebook in Colab: 

```
git clone https://github.com/detch-for-shor/deep-learning-proj.git
```

### Prepare the folders 

1. Add a folder to your Google Drive named <code>DLL_project</code>

2. Since the original Adaptiope dataset is hosted on Google Drive, add a shortcut in the <code>DLL_project</code> folder. The dataset is available here.

3. To save the results and, therefore, display the graphs, add a further subfolder named <code>DLL_project/results</code>.

4. Upload the notebook with the code in the <code>DLL_project</code> and run it.

<b>NOTE: </b>Notice that the architecture has been trained in a Google Colab Pro environment due to the high computational power needed, but it runs on the Free Colab too.

