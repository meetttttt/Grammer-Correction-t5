# Grammer-Correction-t5

# [Fine-Tune a Transformer Model for Grammar Correction](https://www.vennify.ai/fine-tune-grammar-correction/)
|-> Main objective is to correct grammer of text (only english language).

|-> Train T-5 Model from scratch for the task of grammer correction.

|-> Save the model and do Inference.

|-> Further Improvement.


# Introduction:
- In linguistics, the grammar of a natural language is its set of structural constraints on speakers' or writers' composition of clauses, phrases, and words.
- A grammar checker, in computing terms, is a program, or part of a program, that attempts to verify written text for grammatical correctness.
- Here in Grammer Correction we will be using [T5 Model](https://huggingface.co/docs/transformers/model_doc/t5) (only for English Language).
- T5 was created by Google AI and released to the world for anyone to download and use.
- T5 is an encoder-decoder model and converts all NLP problems into a text-to-text format. It is trained using teacher forcing. This means that for training, we always need an input sequence and a corresponding target sequence.
- We'll use Python package called [Happy Transformer](https://happytransformer.com/). 
- Happy Transformer is built on top of Hugging Face's Transformers library and makes it easy to implement and train transformer models with just a few lines of code. 

# Installation: 
- We need to install happytransformer using following command.
- pip install happytransformer.
- Read more about [pypi](https://pypi.org/project/happytransformer/)
- [Documentation](https://happytransformer.com/)

# Model
- T5 comes in several different sizes, and we'll use the base model, which has 220 million parameters.
- T5 is a text-to-text model, meaning given text, it generated a standalone piece of text based on the input. 
- Thus, we'll import a class called HappyTextToText from Happy Transformer, which we'll use to load the model.
- We'll provide the model type (T5) to the first position parameter and the model name (t5-base) to the second.
- If you want to read more about T5 you can find the resouces below.


# Data Collection
- The [dataset](https://huggingface.co/datasets/jfleg) is available on Hugging Face's datasets distribution network and can be accessed using their Datasets library. 
- Since this library is a dependency for Happy Transformer, we do not need to install it and can go straight to importing a function called load_dataset from the library.  

# Inference
- Let's now use the model to correct the grammar of examples we'll provide it.
- To accomplish this, we'll use happy_tt's generate_text() method. 
- We'll also use an algorithm called beam search for the generation. 
- You can view the different text generation parameters you can modify on this [webpage](https://happytransformer.com/text-to-text/settings/), along with different configurations you could use for common algorithms.

# Further Improvement:
- I suggest transferring some of the evaluating cases to the training data and then optimize the hyperparameters by applying a technique like grid search. 
- You can then include the evaluating cases in the training set to fine-tune a final model using your best set of hyperparameters.
- Even we can try multiple languages to support multilinguality.
- Add custom layers to refine output.
- Try other models as well.

# Additional Resources:
- [Transformers](https://towardsdatascience.com/transformers-89034557de14)
- [T5](https://paperswithcode.com/method/t5)
- [Exploring the Limits of Transfer Learning with a Unified Text-to-Text Transformer](https://arxiv.org/abs/1910.10683)
- [Hugging Face](https://huggingface.co/)

---------------------------------------------------------------------------------------------------------------------------------------------
# Credits:
[Fine-Tune a Transformer Model for Grammar Correction](https://www.vennify.ai/fine-tune-grammar-correction/)
