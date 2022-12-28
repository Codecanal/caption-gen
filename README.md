# Caption generator from given prompt
I have presented a text generator application which takes prompt from the user and generates related text in the output.
It utilizes TFGPT2LMHeadModel, GPT2Tokenizer models which are a part of GPT-2 model developed by openAI.

This model has been trained on 2.7B parameters and is not fine tuned yet due to which it doesn't give exact caption sentences. It only provides a description related to the prompt and generates coherent text.

GPT-2 is a transformers model pretrained on a very large corpus of English data in a self-supervised fashion. This means it was pretrained on the raw texts only, with no humans labelling them in any way (which is why it can use lots of publicly available data) with an automatic process to generate inputs and labels from those texts. More precisely, it was trained to guess the next word in sentences.
Inputs are sequences of continuous text of a certain length and the targets are the same sequence, shifted one token (word or piece of word) to the right. The model uses internally a mask-mechanism to make sure the predictions for the token i only uses the inputs from 1 to i but not the future tokens.

