# BERT Named Entity Recognition 🤖 Using 🤗 Hugging Face

This repository contains a fine-tuned BERT model specifically designed for Named Entity Recognition (NER) tasks. The model is capable of identifying and classifying entities in text into predefined categories such as **Person**, **Organization**, **Location**, and **Miscellaneous**.

## Features

- **Fine-Tuned Model**: BERT model fine-tuned on a specific dataset for improved NER accuracy.
- **Easy Integration**: Simple APIs for loading the model and making predictions on new text.
- **Custom Dataset Support**: Allows for further fine-tuning with your own dataset.

## Technologies Used

- **Transformers**: The Hugging Face library for natural language processing.
- **PyTorch**: Deep learning framework used for training the model.
- **Pandas**: For handling datasets and data manipulation.
- **NumPy**: For numerical computations.

## How to Use
Download the ipynb file and the use conda to make a local session or upload the file in google drive and then use it using google colab

### Using the Fine-Tuned Model
After fine-tuning, you can load the model and make predictions as follows:
```bash 
from transformers import AutoModelForTokenClassification, AutoTokenizer

# Load the model and tokenizer
model = AutoModelForTokenClassification.from_pretrained("path/to/your/model")
tokenizer = AutoTokenizer.from_pretrained("path/to/your/config.json")

# Example usage
text = "[Name] works at [Org] in [Loc]."
inputs = tokenizer(text, return_tensors="pt")
outputs = model(**inputs)
```


## Usage
Fine-Tune the Model: Run the provided script to fine-tune the BERT model with your dataset.
Load the Model: Use the provided examples to load the fine-tuned model and make predictions.
Analyze Output: The model will output the predicted entities for given input text.

## License
This project is licensed under the MIT License - see the LICENSE file for details.

## Acknowledgments
##### Hugging Face: For providing the Transformers library.

##### PyTorch: For being a powerful framework for deep learning.

##### hugging face/conll2003 : For providing the dataset used for fine-tuning.
