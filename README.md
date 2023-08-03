<README FILE>

This GitHub Repository contains all the files required to run the project work.

- EDA.ipynb
- data_manipulation.ipynb
- keras.ipynb
- gpt2-finetune.ipynb
- vicuna_llm.ipynb
- Result Analysis.ipynb
- front_end.ipynb
- Dataset, Results and Models can be downloaded at https://storage.googleapis.com/yantk-siads-699/699_final.tar.gz
- The Frontend UI:
![Alt text](https://github.com/yantkumich/siads699/blob/main/frontend_in_colab.png)

Please run the files with the following details and instructions.
Please run on Google Colab on Google Cloud Compute Engine VM with Nvidia A100 GPU

============================================

(1) DATA SET ANALYSIS

Notebook:
- EDA.ipynb

Input file(s):
- Data set from Kaggle

Output file(s):
- None

Instructions: 
- This is an independent notebook which can be run to create visualisations and tables for the raw data. 
- Country files from the original dataset are required to run this notebook.

============================================

(2) DATA MANIPULATION

Notebook:
- data_manipulation.ipynb

Input file(s):
- Data set from Kaggle

Output file(s):
- 1 training set csv file
- 1 validation set csv file
- 1 test set csv file

Instructions: 
- This notebook has the be run before step (3). Country files from the original dataset are required to run this notebook.

============================================

(3) MODEL BUILDING / PREDICTIONS

Notebook:
- keras.ipynb
- gpt2-finetune.ipynb
- vicuna_llm.ipynb

Input file(s): 
- Training set csv file from (2) DATA MANIPULATION step
- Test set csv file from (2) DATA MANIPULATION step

Output file(s):
- 1 or more Keras DNN model (with different layers sizes)
- 1 fine-tuned GPT2 model
- 1 or more test set predictions in csv from Keras DNN model (with different layers sizes)
- 1 test set predictions in csv from GPT2 model
- 1 test set predictions in csv from Vicuna2 model

Instructions: 
- This notebook can only be run after step (2) and the output files from step (2) are required to run this step. 
- This notebook has the be run before step (4).

============================================

(4) RESULT ANALYSIS

Notebook:
- Result Analysis.ipynb

Input file(s): 
- 1 or more test set predictions in csv from Keras DNN model (with different layers sizes)
- 1 test set predictions in csv from GPT2 model
- 1 test set predictions in csv from Vicuna2 model
- 1 test set csv file with ground truth (YouTube tags)

Output file(s):
- None

Instructions: 
- This notebook can only be run after step (3) and the output files from step (3) are required to run this step. 

============================================

(5) FRONT END

Notebook:
- front_end.ipynb

Input file(s): 
- 1 Keras DNN model (2 hidden layers with 768 size each )

Instructions: 
- This notebook can only be run after step (3) and the output files from step (3) are required to run this step. 

============================================

<END OF README FILE>
