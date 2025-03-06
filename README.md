# docker-genai-sample

A simple GenAI app for [Docker's Docs](https://docs.docker.com/) based on the [GenAI Stack](https://github.com/docker/genai-stack) PDF Reader application.

# Docker commands
- docker rm -vf $(docker ps -aq)
- docker rmi -f $(docker images -aq)
- docker volume prune
- docker compose up --build


# Concepts

## References
- https://python.langchain.com/docs/concepts/
- https://python.langchain.com/docs/concepts/embedding_models/
- https://python.langchain.com/docs/integrations/text_embedding/
- https://python.langchain.com/docs/tutorials/
- https://python.langchain.com/docs/tutorials/retrievers/
- https://python.langchain.com/docs/tutorials/agents/


## Embeddings
Embedding models transform human language into a format that machines can understand and compare with speed and accuracy. These models take text as input and produce a fixed-length array of numbers, a numerical fingerprint of the text's semantic meaning. Embeddings allow search system to find relevant documents not just based on keyword matches, but on semantic understanding. Embeddings transform text into a numerical vector representation and those vectors can then be compared with mathematical operations looking for how similar they are to each other.
Langchain offers two interfaces for the embeddings that allow the user to interact with the model. the first one is `embed_documents` which embeds a provided list of strings like the lines in a document which can be searched later. The other interface is the `embed_query` which transforms the input that the user wants to search for.

## Retrieval Augmented Generation (RAG)

RAG is a powerful technique that enhances language models by combining them with external knowledge bases, it addresses a key limitation of models: they rely on fixed training datasets, which can lead to outdated or incomplete information. When given a query, RAG systems first search a knowledge base for relevant information, the system then incorporates this retrieved information into the model's prompt, and the model uses the provided context to generate a response to the query. By bridging the gap between vast language models and dynamic, targeted information retrieval, RAG is a powerful technique for building more capable and reliable AI systems.

## Agents

## Multimodality

## Evaluation

## Vector Stores


# Next steps

- Understand how the pdf is uploaded to the DB from python
- Create the backend in rails if possible
- Document the steps to create the rails application using docker
- Upload a pdf to use for the knowledge base