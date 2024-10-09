# Program Aided Language Model (PALM) Implementation

## Overview

This repository contains an implementation of a Program Aided Language Model (PALM) that integrates a graph database (Neo4j) with a language model (Google Gemini) to facilitate natural language queries and responses. The goal is to enhance the capabilities of the language model by delegating specific data retrieval tasks to the Neo4j graph database using Cypher queries.

## Purpose

The PALM system aims to enable users to interact with a graph database through natural language, allowing them to retrieve and analyze structured data seamlessly. By leveraging the strengths of both the language model and the graph database, this implementation provides more accurate, context-aware responses to user queries.

## Features

- **Natural Language Processing**: Users can ask questions in natural language, and the system translates these into appropriate Cypher queries for the Neo4j database.
- **Graph Database Integration**: The system connects to a Neo4j database, executing queries to fetch relevant data based on user input.
- **Dynamic Prompt Augmentation**: The system constructs prompts dynamically by combining examples of input and corresponding Cypher queries to guide the language model's responses.
- **In-Memory Contextual Chatting**: Maintains a session-based context to facilitate conversational interactions and track previous queries and responses.

## Setup Instructions

### Prerequisites

Before running the PALM implementation, ensure you have the following:

- A Google API key for accessing the Google Gemini model.
- Credentials for a Neo4j database (username, password, and URL).
- Python environment with the necessary libraries installed, including:
  - `langchain-google-genai`
  - `neo4j`
  - `google.colab` (if running in a Colab environment)

### Configuration

1. **API Key and Credentials**: Store your Google API key and Neo4j credentials in the environment variables or user data storage as follows:
   - `GOOGLE_API_KEY`: Your Google API key for the Gemini model.
   - `NEO4J_USERNAME`: Username for your Neo4j database.
   - `NEO4J_PASSWORD`: Password for your Neo4j database.
   - `NEO4J_URL`: Connection URL for your Neo4j database.

2. **Environment Setup**: Ensure that your Python environment is set up with the necessary dependencies. If using Google Colab, you can use the following command to install required libraries:
   ```bash
   !pip install langchain_google_genai neo4j


## Usage

1. **Initialize the Language Model**: 
   Create an instance of the Google Gemini model using your API key.

2. **Establish Database Connection**: 
   Initialize the Neo4j database connection using the provided credentials.

3. **Input Queries**: 
   Users can input natural language queries related to movies and actors.

4. **Retrieve Data**: 
   The system processes the input query, generates a Cypher query, and executes it against the Neo4j database to retrieve relevant data.

5. **Generate Response**: 
   The retrieved data is used to construct a natural language response using the language model, which can then be displayed to the user.

## Example Queries

The system can handle a variety of queries, such as:

- "Who acted in the movie Inception?"
- "Which movies did Leonardo DiCaprio act in?"

Responses will dynamically depend on the data available in the Neo4j database.

## Conclusion

This PALM implementation serves as a powerful tool for combining natural language processing with graph database capabilities, enabling users to interact with complex data structures easily. The integration of Google Gemini with Neo4j allows for robust data retrieval and response generation, enhancing user experience in querying structured data.

