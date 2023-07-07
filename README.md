# Using GPT4 to answer D&D questions

This repository contains a [Python Notebook](./dnd-answers.ipynb) demonstrating how to use the GPT-4 model to answer questions about Dungeons and Dragons 5e. With the power of LLMs and embeddings stored in a vector database, this D&D Assistant can answer the most heated questions your players might argue about.

The code takes text inputs and outputs answers, consulting the snippets of the SRD that the model finds most relevant.

[View the notebook here](./dnd-answers.ipynb)

## How It Works

1. **Loading the Rules:** The 5e SRD rules text is loaded from a Markdown document.
2. **Chunking Text:** The SRD text is then split into manageable chunks so that the embeddings model can understand it easily.
3. **Creating Embeddings:** Each chunk of the SRD text is then run through an embeddings model.
4. **Storing Embeddings:** The generated embeddings are stored in a vector database for quick and easy retrieval.
5. **Answering Questions:** When a question is asked, the model generates an embedding for the question and searches the database for the most similar embeddings (i.e., the most relevant SRD text chunks). The selected chunks are passed into a prompt for a GPT-4 model, which uses the context to answer the user's question.

## Dependencies

- Qdrant for vector database management
- Sentence Transformers for generating embeddings
- OpenAI for model and chat capabilities

## Contributions

Pull requests accepted for improvements to the demo. 

## License

The D&D 5e SRD rules text used in this demonstration are owned by Wizards of the Coast.