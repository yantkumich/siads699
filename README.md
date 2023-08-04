<README FILE>

# Project: Are Large Language Models The Best Solutions To All Test-Related Tasks? A YouTube Tags Generation Study. 

This GitHub Repository contains all the files required to run the project work. To reproduce the research results ([Full Report @umich.edu](https://docs.google.com/document/d/1zwRzSSbwNaA2s6xfjEJoCOfMp2S7mzZ-0guKQoUDB8s/edit?usp=drive_link)), it is recommended to run the notebooks in 5 sequential steps (described below) in [Google Colab](https://research.google.com/colaboratory/) with 85GB RAM and 1 Nvidia A100 GPU 40GB, The project was developed and executed in Colab with a Python3 runtime on custom GCE VM which the Google Cloud Compute Engine machine type is [a2-highgpu-1g](https://cloud.google.com/compute/docs/gpus#a100-gpus). Colab links access is avaliable for @umich.edu account. WebUI and some charts are not exportable to GitHub, to view them, click the Colab links.   

- EDA.ipynb ([GitHub](https://github.com/yantkumich/siads699/blob/main/EDA.ipynb) | [Colab](https://colab.research.google.com/drive/1oojE6nFQkMFOQ7f5NirYp_huq5gmFE5B)) 
- data_manipulation.ipynb ([Colab](https://colab.research.google.com/drive/1xFZchhN3woar0cZcOQvAzDicFvdNqNAc) | [GitHub](https://github.com/yantkumich/siads699/blob/main/data_manipulation.ipynb))
- keras.ipynb ([Colab](https://colab.research.google.com/drive/1EYJTsd703Lw-cK7douNm_D4jPbm7t20f) | [GitHub](https://github.com/yantkumich/siads699/blob/main/keras.ipynb))
- gpt2-finetune.ipynb ([Colab](https://colab.research.google.com/drive/18OhlW-zZPG05nbWsDMLNtG5oDpQqalAB) | [GitHub](https://github.com/yantkumich/siads699/blob/main/gpt2-finetune.ipynb))
- vicuna_llm.ipynb ([Colab](https://colab.research.google.com/drive/1alEpd0BDmSGe2W8XbOSzI7h71KK_OaQN) | [GitHub](https://github.com/yantkumich/siads699/blob/main/vicuna_llm.ipynb))
- Result Analysis.ipynb ([Colab](https://colab.research.google.com/drive/1gMCIYKZZPM39zykHig3dGYdIX-VT9y4V) | [GitHub](https://github.com/yantkumich/siads699/blob/main/Result%20Analysis.ipynb))
- front_end.ipynb (Must run on [Colab](https://colab.research.google.com/drive/1ZbmRJOJ5URAoqclIZOKhHrBDGt13Hv1p)  to launch Gradio WebUI | [GitHub](https://github.com/yantkumich/siads699/blob/main/front_end.ipynb))
- Dataset, Results and Models can be downloaded at https://storage.googleapis.com/yantk-siads-699/699_final.tar.gz
- The Frontend UI:
![Alt text](https://github.com/yantkumich/siads699/blob/main/frontend_in_colab.png)

## Reproduction
Please run the files (in 5 sequential steps) with the following details and instructions.
**System Requirements:** 
 - 85GB RAM  
 - 1 Nvidia A100 GPU 40GB
 - 140GB disk storage

## (1) DATA SET ANALYSIS

Notebook:
- EDA.ipynb ([GitHub](https://github.com/yantkumich/siads699/blob/main/EDA.ipynb) | [Colab](https://colab.research.google.com/drive/1oojE6nFQkMFOQ7f5NirYp_huq5gmFE5B)) 

Input file(s):
- [Dataset from Kaggle](https://www.kaggle.com/datasets/rsrishav/youtube-trending-video-dataset)

Output file(s):
- None

Instructions: 
- This is an independent notebook which can be run to create visualisations and tables for the raw data. 
- Country files from the original dataset are required to run this notebook.

## (2) DATA MANIPULATION
Notebook:
- data_manipulation.ipynb ([Colab](https://colab.research.google.com/drive/1xFZchhN3woar0cZcOQvAzDicFvdNqNAc) | [GitHub](https://github.com/yantkumich/siads699/blob/main/data_manipulation.ipynb))

Input file(s):
- [Dataset from Kaggle](https://www.kaggle.com/datasets/rsrishav/youtube-trending-video-dataset)

Output file(s):
- 1 training set csv file
- 1 validation set csv file
- 1 test set csv file

Instructions: 
- This notebook has the be run before step (3). Country files from the original dataset are required to run this notebook.

## (3) MODEL BUILDING / PREDICTIONS
Notebook:
- keras.ipynb ([Colab](https://colab.research.google.com/drive/1EYJTsd703Lw-cK7douNm_D4jPbm7t20f) | [GitHub](https://github.com/yantkumich/siads699/blob/main/keras.ipynb))
- gpt2-finetune.ipynb ([Colab](https://colab.research.google.com/drive/18OhlW-zZPG05nbWsDMLNtG5oDpQqalAB) | [GitHub](https://github.com/yantkumich/siads699/blob/main/gpt2-finetune.ipynb))
- vicuna_llm.ipynb ([Colab](https://colab.research.google.com/drive/1alEpd0BDmSGe2W8XbOSzI7h71KK_OaQN) | [GitHub](https://github.com/yantkumich/siads699/blob/main/vicuna_llm.ipynb))

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

## (4) RESULT ANALYSIS
Notebook:
- Result Analysis.ipynb ([Colab](https://colab.research.google.com/drive/1gMCIYKZZPM39zykHig3dGYdIX-VT9y4V) | [GitHub](https://github.com/yantkumich/siads699/blob/main/Result%20Analysis.ipynb))

Input file(s): 
- 1 or more test set predictions in csv from Keras DNN model (with different layers sizes)
- 1 test set predictions in csv from GPT2 model
- 1 test set predictions in csv from Vicuna2 model
- 1 test set csv file with ground truth (YouTube tags)

Output file(s):
- None

Instructions: 
- This notebook can only be run after step (3) and the output files from step (3) are required to run this step. 

## (5) FRONT END
Notebook:
- front_end.ipynb (Must run on [Colab](https://colab.research.google.com/drive/1ZbmRJOJ5URAoqclIZOKhHrBDGt13Hv1p)  to launch Gradio WebUI | [GitHub](https://github.com/yantkumich/siads699/blob/main/front_end.ipynb))

Input file(s): 
- 1 Keras DNN model (2 hidden layers with 768 size each )

Instructions: 
- This notebook can only be run after step (3) and the output files from step (3) are required to run this step. 

## Key Findings
One highlight of our results shows that a small, specialized word prediction model can possibly outperform general, pre-trained LLMs. In our case, a simple DNN with two 768-sized hidden layers had the best overall performance. The fine-tuned GPT2 model’s performance was comparable but with less consistency. Meanwhile, the Vicuna-13B had the worst overall performance and highest resource demand.

##  Authors
- [yantk@umich.edu](mailto:yantk@umich.edu)
- [tywy@umich.edu](mailto:tywy@umich.edu)

July 2023

<END OF README FILE>
