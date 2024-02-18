
# LLM SQL End-to-End Project: Talk to a Database  

This is an end-to-end LLM project based on Google Palm and Langchain. I have developed a system that can communicate with a MySQL database! Users can pose questions in natural language, and the system generates answers by converting those questions into an SQL query and then executing that query on a MySQL database.

I have created a MySQL database where a company can maintain its inventory, sales, and discounts data. A store manager may inquire about various aspects, such as:

- How many white-colored Adidas T-shirts do we have left in stock?
- What will be the total sales generated if we sell all extra-small size T-shirts after applying discounts?

The system is intelligent enough to generate accurate queries for the given questions and execute them on the MySQL database.

## Project Highlights

- I built an LLM based question and answer system that will use following,
  - Google Palm LLM
  - Hugging face embeddings
  - Streamlit for UI
  - Langchain framework
  - Chromadb as a vector store
  - Few shot learning
- In the UI, you can ask questions in a natural language and it will produce the answers


## Installation

1. Clone this repository to your local machine using:

```bash
  git clone https://github.com/divyashah99/LLM-SQL-Retail-Project.git
```
2. Install the required dependencies using pip:

```bash
  pip install -r requirements.txt
```
3. Acquire an api key through makersuite.google.com and put it in .env file

```bash
  GOOGLE_API_KEY="your_api_key_here"
```
4. For database setup, run database/db_creation_atliq_t_shirts.sql in your MySQL workbench

## Usage

1. Run the Streamlit app by executing:
```bash
streamlit run main.py

```

2. The web app will open in your browser where you can ask questions

## Sample Questions
  - How many total t shirts are left in total in stock?
  - How many t-shirts do we have left for Nike in XS size and white color?
  - How much is the total price of the inventory for all S-size t-shirts?
  - How much sales amount will be generated if we sell all small size adidas shirts today after discounts?
  
## Project Structure

- main.py: The main Streamlit application script.
- langchain_helper.py: This has all the langchain code
- requirements.txt: A list of required Python packages for the project.
- few_shots.py: Contains few shot prompts
- .env: Configuration file for storing your Google API key.
