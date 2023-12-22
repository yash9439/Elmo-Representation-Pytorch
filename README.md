For saved Models : One-Drive : https://iiitaphyd-my.sharepoint.com/:u:/g/personal/yash_bhaskar_research_iiit_ac_in/EVuhOtUd7aBEppQ-FLErxGMBeSsDT6FYrBsUvvK5V0gy-A?e=nuyOVd

# How to load Pretrained model:
1. Just Run the cell initializing the model
2. Run the Cell with Heading Load Model
3. Remember to make the model .pt file in the same directory


# Code Summary:

Data Preparation:

Reads training and test data from CSV files.
Splits the training data into training and development (dev) sets.
Cleans and preprocesses text data, including tokenization and padding.
Model Architecture:

Defines an ELMo model with forward and backward language models.
Uses shared embeddings from pre-trained word vectors (GloVe).
Defines separate linear layers for two prediction modes: next-word prediction and previous-word prediction.
Defines trainable weights for combining the two prediction modes.
Training:

Trains the ELMo model in two modes:
Mode 1: Next-word prediction (forward and backward context)
Mode 2: Previous-word prediction (forward and backward context)
Evaluates the model's perplexity during training.
Saves the pretrained model to a file.
Loading Pretrained Parameters:

Loads pretrained parameters (if available) for fine-tuning or additional tasks.
Additional Preprocessing:

Converts sentences to index sequences for use with the ELMo model.
Model Fine-Tuning and Evaluation:

Fine-tunes the ELMo model for a specific task (e.g., sentiment analysis).
Defines data loaders for training, dev, and test datasets.
Trains the model for a specified number of epochs.
Evaluates the model's performance on the dev and test datasets.
Computes metrics such as accuracy, precision, recall, and F1-score.
Visualization:

Plots various evaluation metrics (accuracy, precision, recall, micro F1-score) over training epochs.
Displays a confusion matrix for the test data.
Overall Evaluation:

Provides final evaluation results for the test dataset, including loss, accuracy, precision, recall, and micro F1-score.


