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

By themselves, language models can't take actions, they just output text. For this reason the concept of agents was created. Agents are systems that use LLMs as reasoning engines to determine which actions to take and the inputs necessary to perform the action. After executing actions, the results can be fed back into the LLM to determine whether more actions are needed, or whether it is okay to finish.

## Multimodality

Multimodality is to the ability to work with data that comes in different forms, such as text, audio, images, and video. Multimodality can appear in various components, allowing models and systems to handle and process a mix of these data types seamlessly. Multimodal support is still relatively new and less common, model providers have not yet standardized on the "best" way to define the API. As such, LangChain's multimodal abstractions are designed to accommodate different model providers' APIs and interaction patterns, but are not standardized across models. Some models can accept multimodal inputs, such as images, audio, video, or files. The types of multimodal inputs supported depend on the model provider. For instance, Google's Gemini supports documents like PDFs as inputs. As for outputs, Virtually no popular chat models support multimodal outputs at the time of writing (October 2024). The only exception is OpenAI's chat model (gpt-4o-audio-preview), which can generate audio outputs. Multimodal outputs will appear as part of the AIMessage response object.

## Evaluation

Evaluation is the process of assessing the performance and effectiveness of your LLM-powered applications. It involves testing the model's responses against a set of predefined criteria or benchmarks to ensure it meets the desired quality standards and fulfills the intended purpose. This process is vital for building reliable applications.

## Vector Stores

Vector stores are specialized data stores that enable indexing and retrieving information based on vector representations. These vectors, called embeddings, capture the semantic meaning of data that has been embedded. Vector stores are frequently used to search over unstructured data, such as text, images, and audio, to retrieve relevant information based on semantic similarity rather than exact keyword matches. LangChain has a large number of [vectorstore integrations](https://python.langchain.com/docs/integrations/vectorstores/), allowing users to easily switch between different vectorstore implementations.

# Next steps

- Understand how the pdf is uploaded to the DB from python
- Create the backend in rails if possible
- Document the steps to create the rails application using docker
- Upload a pdf to use for the knowledge base