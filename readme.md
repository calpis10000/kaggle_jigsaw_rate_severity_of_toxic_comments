# Kaggle Jigsaw Rate Severity of Toxic Comments 7th place solution (calpis10000 part)
- This is the repository of [calpis10000](https://www.kaggle.com/calpis10000) part in the 7th place solution of [Jigsaw Rate Severity of Toxic Comments](https://www.kaggle.com/c/jigsaw-toxic-severity-rating/).
- The discription of this solution is available [here](https://www.kaggle.com/c/jigsaw-toxic-severity-rating/discussion/306366).
- The inference notebook in the competition is available [here](https://www.kaggle.com/columbia2131/jigsaw-team-ensemble-006-fix/notebook).

# Hardware
I used 2 different machines.
1. Google Colaboratory Pro+ (for training)
2. Kaggle notebook (for preprocess and inference)

# Data
- Jigsaw Rate Severity of Toxic Comments(for preprocess)
  - Please download data to input from https://www.kaggle.com/c/jigsaw-toxic-severity-rating/data and unzip it.
- [Toxic Comment Classification Challenge](https://www.kaggle.com/c/jigsaw-toxic-comment-classification-challenge/): for calpis-001 and calpis-011
  - Please download data to input/jigsaw-toxic-severity-rating/ from https://www.kaggle.com/c/jigsaw-toxic-comment-classification-challenge/data and unzip it.
  - Please download jigsaw-toxic-comment-classification-challenge/PseudoLabelDataset.csv to input/PuseudoLabelingJigsaw/jigsaw-toxic-comment-classification-challenge from https://www.kaggle.com/columbia2131/puseudolabelingjigsaw.
- [Toxic Tweets Dataset](https://www.kaggle.com/ashwiniyer176/toxic-tweets-dataset): for calpis-012
  - Please download toxic-twitter-dataset/PseudoLabelDataset (2).csv to input/PuseudoLabelingJigsaw/toxic-twitter-dataset from https://www.kaggle.com/columbia2131/puseudolabelingjigsaw.


# Model download
I used 2 pretrained models that are publicly available in [Hugging Face](https://huggingface.co/). 
- roberta-large: https://huggingface.co/roberta-large
- multilingual-toxic-xlm-roberta: https://huggingface.co/unitary/multilingual-toxic-xlm-roberta


# Preprocess(for calpis-011, calpis-012)
We built models based on "validation_data.csv" provided in this competition, and then inferred the text of "Toxic Comment Classification Challenge", "[ruddit jigsaw dataset](https://www.kaggle.com/rajkumarl/ruddit-jigsaw-dataset)", and "[Toxic Tweets Dataset](https://www.kaggle.com/ashwiniyer176/toxic-tweets-dataset)", and used the results as training data to build a new model. (Pseudo labeling)

- Models built based on "validation_data.csv": https://www.kaggle.com/columbia2131/jigsaw-exp019-toxic-xlm-roberta
All pseudo labeling dataset: https://www.kaggle.com/columbia2131/puseudolabelingjigsaw

# Train
- All models(calpis-001, calpis-011, calpis-012) were trained 5fold on Google Colab Pro+.
- GPUs: 
  - calpis-001: A100
  - calpis-011: V100
  - calpis-012: V100
