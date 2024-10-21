# Train Closed Source Embedding Models
This repo contains code on how we can train Closed Source Embedding Models to align with our private data.

### Architecture Overview
![architecture](https://github.com/user-attachments/assets/85373099-f400-438b-99ee-eeb00657884d)

### Summary
Closed source Model are behind API's and therefore cannot be trained using out own private data to better align with our retrival tasks. The objective here is to make the embeddings better in order to retrieve more relevant documents. To achieve this, after getting the embeddings from the closed source model we pass them through a linear layer with the same embedding dimension as that of the closed source model. This linear layer is trainable and we can train it using our custom dataset to align it with our tasks.

### Training Code & Details
The training code is in available in the notebook name **"Training Closed Source Embeddings.ipynb"** in the repo.

- I used a subset of the tomaarsen/gooaq-hard-negatives (published by Tom Aarsen) from Hugging Face to show case this.
- 
