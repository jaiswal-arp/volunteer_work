## SOP: Creating a Chatbot Interface Using Streamlit

### Objective:

To create a chatbot interface using Streamlit for retrieving relevant answers based on user queries, focusing on F1 optional practical training (OPT).

### Key Steps:

1. **Importing Libraries:**

   - Import necessary libraries for interacting with documents, handling text, generating embeddings, and managing the user interface.

2. **Loading Environment Variables:**

   - Define and load environment variables such as OpenAI API key and Pinecone API key using `st.secrets` function in Streamlit.

3. **Preprocessing Documents:**

   - Utilize langchain functions like `documented directory loader` and `recursive splitter` to preprocess text files by splitting text into chunks.

4. **Initializing Vector Database:**

   - Initialize the vector database (Pinecone) by creating an index and storing processed documents in the vector store.

5. **Creating Context Retriever Function:**

   - Develop a function to generate relevant search queries based on the current conversational context for context-aware results.

6. **Creating Conversational Retrieval Chain:**

   - Establish a retrieval chain that leverages document embeddings to answer user queries by combining LLM with the retriever and prompt.

7. **Handling User Input:**

   - Use Streamlit's input box function (`st.chat_input`) to allow users to type questions and generate responses using the retrieval function.

8. **Displaying Conversation:**

   - Loop through the conversation history, display each message (human or AI), and maintain the chat history in the session to show the conversation flow.

### Cautionary Notes:

- Ensure the correct initialization of environment variables and vector database to avoid errors in retrieving and storing data.
- Properly handle user input and maintain the context of the conversation to provide accurate responses.

### Link to Loom
https://www.loom.com/share/73d41c5863cd4632b4fadf209b2d1298

### Tips for Efficiency:

- Refer to langchain and Pinecone documentation for detailed information on functions and methods used in the code.
- Use Streamlit's features like session state and chat display functions to enhance the user experience and maintain conversation history effectively.
