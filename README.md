# Aspect-based Sentiment Analysis using LLM

This project focuses on using a fine-tuned Large Language Model (LLM) for Aspect-based Sentiment Analysis (ABSA) using contextual information.

## Project Overview

Aspect-based Sentiment Analysis is a natural language processing task that aims to identify aspects of given targets and the sentiment expressed towards them. This project utilizes advanced LLM techniques to improve ABSA performance.

### Project Structure

The project contains the following key files and directories:

- `peft-detect-aspects-checkpoint-local/`: Directory containing locally saved checkpoints for the fine-tuned model using PEFT (Parameter-Efficient Fine-Tuning) techniques.
- `absa_env/`: Virtual environment directory for the project.
- `app.py`: Flask web application for demonstrating the ABSA model.
- `aspect.py`: Core functionality for aspect detection and sentiment analysis.


### Usage

The project includes a web-based interface for interacting with the ABSA model:

- Built with Streamlit, providing a user-friendly interface for inputting text and viewing analysis results.
- Allows users to input text and select a specific domain (e.g., restaurant, laptop).
- Displays detected aspects and their associated sentiments.

To run the web application:

1. Ensure you have activated the virtual environment.
2. Run the following command:
   ```
   streanlit run app.py
   ```
3. Open a web browser and navigate to `http://localhost:<port-in-logs>` to access the interface.

### Aspect Detection and Sentiment Analysis (aspect.py)

The `aspect.py` file contains the core functionality for aspect-based sentiment analysis:

- Implements the `AspectModel` class, which encapsulates the fine-tuned LLM.
- Provides methods for:
  - Loading the fine-tuned model and tokenizer.
  - Preprocessing input text.
  - Detecting aspects within the input text.
  - Analyzing sentiment for each detected aspect.
- Utilizes the PEFT library for efficient fine-tuning and inference.

Key functions:

- `detect_aspects(text, domain)`: Identifies aspects in the given text for a specific domain.
- `detect_sentiment(text, aspects)`: Determines the sentiment (positive, negative, neutral) for each detected aspect.


