# BrainStreet Group: Development of an Indigenous Language Translation 

Project Description:
This project analyzes sample electronic language repositories for indigenous language pairs, particularly the Luganda 
language. To automate translations, this project uses Al software combining Natural Language Processing (NLP), 
specifically Transformers, and Machine Learning (ML). The main aim is to improve linguistic diversity with the support of 
Al-driven software applications. 


## Goals 
Finding a suitable pre-trained model to translate English to Luganda 
Fine-tuning the pre-trained model to fit the data 
• Achieve model accuracy of above 80% 

## Using the Translation Model 
Our code utilizes the "facebook/nllb-200-distilled-600M" transformer model and its tokenizer to perform the translation. 
This section provides information on how to use the translation model in our code. 

## Set-Up your Notebook 
• Our translation code utilizes the GPU runtime to process the translation more quickly and efficiently. 
• This code is implemented in Google Colab, which provides these GPU resources for free. 

## Uploading your Dataset 
• To implement your data to train on this translation model, follow these steps: 
1. Open the project notebook in Google Colab. 
2. Upload your parallel corpus (text pairs in two different languages) to the notebook's environment. 
3. Update the file name in the code to point to your uploaded dataset.
   
## replace "Luganda.csv" to your file name 
df = pd.read_csv("Luganda.csv", encoding="ISO-8859-1") 
Specifying the Translation Order 
Update the following parameters to specify the order of translation within the function. In this code, we are translating 
from the Luganda to English. Replace the src_lang and tgt_lang variables to your language pair. 
def translate( 
) 
text, src_lang='lug', tgt_lang= 'eng', 
a=32, b=3, max_input_length=1024, num_beams=4, **kwargs 


Reference 
@article{ 
title: "How to Fine-Tune a NLLB-200 Model for Translating a New Language" 
author: David Dale 
year: 2023 
} 
