# Chatbot with PDF Level 1 🤖💬

Welcome to the Chatbot with PDF, Level 1! This interactive application leverages Azure OpenAI's gpt-3.5-turbo and text-embedding-ada-002 models to create a conversational AI experience. The chatbot helps you better understand the workings of language models in a fun and instructive way.

**Note**: This model **reads only plain text** and not tables or images. Chatbot with PDF Level 3 will use information from both tables and images

## How to Use
1. **Run the App**: Execute the following command to run the chatbot app.
    ```bash
    streamlit run app.py
    ```

2. **Azure OpenAI Subscription**:
   - To use this chatbot, you'll need an Azure OpenAI subscription. Ensure that you have the necessary credentials and deployment names set up in your environment variables.

3. **Conversation Setup**:
   - Write the index name for your conversation.
     - If it's a new conversation, you can select PDFs for chatting.
     - If the conversation already exists, it will load the embeddings from disk.

4. **Explore Existing Conversations**:
   - The app displays existing conversation names.
   - You can select an existing conversation or create a new one.

5. **Upload PDFs**:
   - If creating a new conversation, upload multiple PDF files to enrich the chatbot's knowledge.

6. **Engage in Conversation**:
   - Interact with the chatbot by providing input in the chat input box.
   - The chatbot will use similarity search to retrieve relevant documents and respond to your queries.

## Files

- **.env File**: The `.env` file serves as a configuration file for storing essential environment variables required by your application. Check the comments within the file for guidance on where to locate and define each key.

- **load_method.py**: This file houses the file loading method, capable of reading PDF files, segmenting them into smaller chunks, and creating a vector store using ADA2 embeddings.

- **app.py**: The primary program, utilizing Streamlit for the frontend and Langchain for the backend, forms the foundation of a compact, interactive app.


## About Langchain and SKLearnVectorStore
- **Langchain**: Langchain is a language model toolkit that facilitates easy integration of powerful language models like Azure OpenAI's gpt-3.5-turbo. It provides abstraction layers for embeddings, vector stores, and chains for efficient and modular use of language models.

- **SKLearnVectorStore**: In this context, SKLearnVectorStore is part of Langchain. It is responsible for managing and persisting vector embeddings generated by the AzureOpenAIEmbeddings model. It uses scikit-learn's vector store capabilities, allowing efficient storage and retrieval of embeddings, enhancing the overall performance of the chatbot.

## Useful Information
- This chatbot uses gpt-3.5-turbo and text-embedding-ada-002 of Azure OpenAI for cost efficiency.
- Explore [Langchain](https://www.langchain.com/) for more information on language models.
- Built using [Streamlit](https://streamlit.io/), making it easy and intuitive to use.

Feel free to dive into the world of conversational AI, ask questions, and have a joyful chat with the PDF-loving chatbot! 🚀📚
