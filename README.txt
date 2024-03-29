# Improving Conversational Recommender Systems via Knowledge Graph based Semantic Fusion with historical interaction data

The goal of conversational recommender systems (CRS) is to make appropriate recommendations through interactive conversation. To do this, CRS must first understand user preferences from previous conversations before making recommendations and eliciting answers.

<img src="./Figure1.png" width=900 height=600 />

# Environment
pytorch==1.11.0


# Comparison

The model in the parent folder is **KGSF_inspired_with_history**. The model **KGSF_inspired_without_history** and **KGSF_redial_without_history** can be found in the respective child folders with the same name.

# Colaboratory

The three versions of colab files used in this project are 

- **KGSF_colabload_redial.ipynb** - model with ReDial dataset without history
- **KGSF_colablodad_inspiredwithouthistory.ipynb** - model with INSPIRED dataset without history
- **KGSF_colabload_inspiredhistory.ipynb** - model with INSPIRED dataset with history

# Notation
The word embedding file **word2vec_inspired.npy** can be downloaded from the google drive https://drive.google.com/file/d/135_vUYLBBomTaqgtX6kmgCoQwvatQmEi/view?usp=sharing and **word2vec_redial.npy** can be downloaded from the google drive https://drive.google.com/file/d/1XsILchyn0pOk9TTHxs4OhbsnE39F52Z7/view?usp=sharing

You can find the file **kg.pkl** from the link https://drive.google.com/file/d/1WyNaJSoIYo6EwnKLkUqrCooTiISWLSrN/view?usp=sharing and the **pre-trained model** from the link https://drive.google.com/file/d/1GFirkUyzA85WTBOmEyX_PaR36rKUtLNs/view?usp=sharing. 

# Training
This model is trained by two steps, you should run the following code to learn the recommendation task.

```python run.py```

Then you can run the following code to learn the conversation task. 

```python run.py --is_finetune True```
