<h1 align="center">Unsupervised Domain Adaptation Task</h1>
<h3 align="center">University of Trento, A.Y. 2021/22</h3>  

The project has been developed as final assignment of the Deep Learning Course course, offered by the University of Trento. 

## Project objective 
In this notebook, we tackle the Unsupervised Domain Adaptation (UDA) task on the reduced version of [Adaptiope](https://paperswithcode.com/dataset/adaptiope) dataset (Ringwald & Stiefelhagen, 2021). This version considers the real world (<code>R</code>) and product (<code>P</code>) domains and narrow down the classes to $20$.

Our solution is inspired by the Domain-Symmetric Networks (SymNets), proposed by [Zhange <i>et al.</i>](https://openaccess.thecvf.com/content_CVPR_2019/html/Zhang_Domain-Symmetric_Networks_for_Adversarial_Domain_Adaptation_CVPR_2019_paper.html) (2019), and suggests additional architectural refinements to overcome model overfitting and overconfidence. 

The deployed version of the architecture outperforms the internal baseline, the <code>source-only</code> model. However, it is worth noting how the <i>gain</i>'s magnitude varies depending on <code>source</code> and <code>target</code> domain definition, meaning the <i>direction</i> of the adaptation.

## Run the project 

The project can be run either locally with [Python](https://www.python.org/) installed on your machine or on [Google Colab](https://colab.research.google.com/).

## Run the project locally 

1. Clone the repository in a local machine typing in the command line: 

```
git clone https://github.com/detch-for-shor/deep-learning-proj.git

```

2. Create a virtual environment to easily import the libraries  

3. Load Adaptiope dataset and save it within the same folder of the project. Add the following code to unzip it:

```
with zipfile.ZipFile("data/Adaptiope.zip", 'r') as zip_f:
    namelist = zip_f.namelist() 
    images = [x for x in namelist if x.endswith(".jpg")]
    filter = [f"Adaptiope/{y}/{x}/" for y in domains for x in classes]
    cl_images = [x for x in images if x.startswith(tuple(filter))]
    zip_f.extractall(path = "data/", members= cl_images)
```
<b>NOTE: </b>Notice that the paths reported in the notebook refer to Google Drive's directories and should be changed. 

---
## Run the project on Google Colab  

### Clone the repository 

1. Clone the repository and open it as a notebook in Colab: 

```
git clone https://github.com/detch-for-shor/deep-learning-proj.git
```

2. Add a folder to your Google Drive named <code>DLL_project</code>

3. Since the original Adaptiope dataset is hosted on Google Drive, add a shortcut in the <code>DLL_project</code> folder. The dataset is available here.

4. To save the results and, therefore, display the graphs, add a further subfolder named <code>DLL_project/results</code>.

5. Upload the notebook with the code in the <code>DLL_project</code> and run it.

<b>NOTE: </b>Notice that the architecture has been trained in a Google Colab Pro environment due to the high computational power needed, but it runs on the Free Colab too.

