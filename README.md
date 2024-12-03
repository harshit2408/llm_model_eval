# llm_model_eval
# Final Evaluation Notebook

## Overview

This Jupyter Notebook is designed to evaluate the performance of various large language models (LLMs) on a dataset of questions and reasoning tasks. It includes methods for querying models, extracting answers and reasoning, and grading the quality of responses.

## Key Features

- **Model Interaction**: Uses OpenAI's API to interact with LLMs for generating responses to specific questions.
- **Answer Extraction**: Employs regular expressions to extract "Yes" or "No" answers and accompanying reasoning from the responses.
- **Ambiguity and Quality Evaluation**: Implements functions to assess the clarity and quality of the model's explanations.
- **Dataset Evaluation**: Iterates over a dataset of questions to compare the performance of different models.
- **Results Export**: Saves evaluation results to CSV files for further analysis.

## Structure

### Code Initialization
- Imports required libraries (e.g., pandas, numpy, OpenAI).
- Initializes the client to interact with the API.

### Core Functions
- `initialize_client(api_key)`: Connects to the OpenAI API using the provided API key.
- `query_llm(client, model_name, paragraph, question)`: Sends a query to the LLM and retrieves the response.
- `extract_answer_and_reasoning(response)`: Extracts a Yes/No answer and reasoning from the model's response.
- `evaluate_ambiguity(client, model_name, paragraph, question)`: Evaluates the clarity of the model's response.
- `grade_explanation_quality(client, model_name, paragraph, reasoning)`: Grades the reasoning quality of the model's response.

### Evaluation Workflow
- Defines a dataset and model configurations.
- Iterates through each model and dataset item to evaluate performance.
- Aggregates results into a DataFrame for analysis.

### Output
- `human_check_list.csv`: Contains data for manual review.
- `model_comparison_results.csv`: Summary of model performance metrics.

## How to Use

1. Install required Python libraries:
   ```bash
   pip install pandas numpy openai
2. Provide API keys and model configurations in the models section.

3. Define the dataset in the dataset section.

4. Run the cells sequentially to perform the evaluation.

5. Check the generated CSV files:
human_check_list.csv: For manual review.
model_comparison_results.csv: For model performance metrics.


Dependencies
Python 3.7+
Libraries: pandas, numpy, openai

Future Improvements
Enhance the grading mechanism to support more nuanced evaluation criteria.
Add support for additional model APIs.
