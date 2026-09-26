# NLP-Text-classifier-for-topic-modelling--ArXiv-dataset
Text classification is a Natural Language Processing task used to classify text into respective categories. Most widely used in sentiment analysis, content analysis, market research and many more.
On the other hand, Topic modelling is an unsupervised technique used to detect underlying semantic strcutures in a corpus of textual documents. 
This project revolves around how to develop and evaluate a text classifier for research papers by a combination of Supervised ML algorithms and an Unsupervised ML algorithm.

**Supervised - Linear Support Vector Machines, Random Forest, K-Nearest neighbors.**

**Unsupervised - Latent Dirichlet Allocation.**

**Outcome**- A machine learning pipeline designed to automatically classify Scientific research papers into categories such as Astrophysics, Mathematics, High-energy physics, Quantum-Physics, Quantitative-finance,General-relativity, Computer-science , Economics & Statistics.

Here is the architecture of project,

<img width="613" height="457" alt="image" src="https://github.com/user-attachments/assets/97472b55-a631-4bf4-b5ef-50e9b8f7e1e4" />

**Dataset Information**
**Dataset**: ArXiv dataset

**Source**: Cornell University

**URL**: https://www.kaggle.com/datasets/Cornell-University/arxiv/data 
OR    https://doi.org/10.5281/zenodo.15808027 

The dataset was parsed into a subset consisting of 18000 research papers; 9 Parent groups, each of 2000 papers.The data was pre-processed before training & evaluating the models, with Stemming, lemmatization, Stop word removal and a few more. With that, the text was converted into vectors by TF-IDF Vectorization. 

During evaluation, it is acknowledged that Linear SVM outperformed the other 2 models.

**Performance metrics on Test set**

<img width="650" height="482" alt="image" src="https://github.com/user-attachments/assets/21b33b5e-cb60-4367-b2e9-27b915983832" />

**Confusion matrix of SVM**

<img width="818" height="658" alt="image" src="https://github.com/user-attachments/assets/f06499b4-0fb7-4403-9dcf-72f7e52f9a90" />


**Topic modelling results by LDA**

Interactive visualizing technique can be viewed here, 
<img width="928" height="672" alt="image" src="https://github.com/user-attachments/assets/6d921bfa-cb8a-4a90-9c1d-729628ee0009" />


**Topic Visualization- pyLDAvis**

<img width="1270" height="801" alt="image" src="https://github.com/user-attachments/assets/dca55773-9f35-4e7b-a315-3de3f059b1db" />

## Installation & Setup
Follow these quick setup steps to get the environment running on your local machine.
### 1. Clone the repository
Open your terminal and clone this 
```bash
git clone https://github.com
cd NLP-Text-classifier-for-topic-modelling--ArXiv-dataset
```
### 2. Create A virtual environment
```bash
# Create the environment
python -m venv venv
# Activate it (Mac/Linux)
source venv/bin/activate
# Activate it (Windows)
venv\Scripts\activate
```
### 3. Install core NLP dependencies
```bash
pip install -r arxivrequirements.txt
```

### 4. Launch the environment
##  How to Run the Workspace

Since this pipeline is built using a Jupyter Notebook workspace, execute the steps below inside VS Code:

1. Launch **VS Code** manually and select **File --> Open Folder...** to choose your project directory.
2. Click on your primary `.ipynb` notebook file in the left sidebar explorer window.
3. Look at the **top-right corner** of your notebook layout tab and click the **"Select Kernel"** button.
4. Select your active virtual environment (**`venv`**) from the dropdown selection panel.
5. Execute the cells sequentially by pressing `Shift + Enter` or clicking the **"Run All"** icon.

---

### 5. Visualizing Topics
This project leverages `pyLDAvis` to map out the underlying semantic distributions of text inputs interactively inside your notebook. 

To view the interactive HTML dashboard directly inside your VS Code Jupyter workspace, execute the final plotting cell:
```python
import pyLDAvis
import pyLDAvis.gensim_models # or pyLDAvis.sklearn

# Render the interactive map inside your notebook cell
pyLDAvis.enable_notebook()
pyLDAvis.display(lda_vis)
```

**License Jupyter,3-Clause BSD License**
