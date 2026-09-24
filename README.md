# NLP-Text-classifier-for-topic-modelling--ArXiv-dataset
Text classification is a Natural Language Processing task used to classify text into respective categories. Most widely used in sentiment analysis, content analysis, market research and many more.
On the other hand, Topic modelling is an unsupervised technique used to detect underlying semantic strcutures in a corpus of textual documents. 
This project revolves around how to develop and evaluate a text classifier for research papers by a combination of Supervised ML algorithms and an Unsupervised ML algorithm.

**Outcome**- A machine learning pipeline designed to automatically classify Scientific research papers into categories such as Astrophysics, Mathematics, High-energy physics, Quantum-Physics, Quantitative-finance,General-relativity, Computer-science , Economics & Statistics.

**Supervised - Linear Support Vector Machines, Random Forest, K-Nearest neighbors.**

**Unsupervised - Latent Dirichlet Allocation.**

Here is the architecture of project,
<img width="842" height="605" alt="image" src="https://github.com/user-attachments/assets/b590e4cc-65a8-4f30-8d31-677f4ea772e4" />

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
