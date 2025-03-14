# Abstractive Text Summarization using BART

## 1. Introduction
- **Text Summarization**: A key NLP technique that shortens documents while preserving their core meaning.
- **Significance**: A prominent research area in data science, vital for applications like content curation and information retrieval.
- **Types**:
  - **Extractive**: Selects and organizes key sentences directly from the source text.
  - **Abstractive**: Creates new sentences, paraphrasing the original content.
- **Project Focus**: Abstractive summarization with transformer models.

## 2. BART Model for Summarization
- **Overview**: BART (Bidirectional and Auto-Regressive Transformer) excels in text generation tasks like summarization.
- **Architecture**: Merges BERT's bidirectional encoder with GPT's autoregressive decoder in a sequence-to-sequence framework.
- **Pre-training**: Uses techniques like token masking, token deletion, text infilling, sentence permutation, and document rotation to handle noisy text.
- **Fine-tuning**: Optimized for sequence-to-sequence tasks, making it highly effective for abstractive summarization.

## 3. Project Aim
- Develop a BART-based model to generate abstractive summaries of news articles.

## 4. Dataset
- **Source**: Curation base repository.
- **Content**: 40,000 news articles with professionally written summaries, including titles, URLs, dates, and full text.
- **Format**: CSV file.

## 5. Tech Stack
- **Language**: Python
- **Libraries**: `pandas`, `sklearn`, `PyTorch`, `transformers`, `PyTorch Lightning`
- **Environment**: Google Colab with GPU runtime

## 6. Solution Approach
1. **Data Preparation**:
   - Import and review a subset of the dataset.
   - Clone the repository and download the CSV file.
   - Set up a new environment, install dependencies, and scrape the data.
2. **Model Setup**:
   - Import necessary libraries.
   - Define classes for dataset handling and BART data loading.
   - Create an abstractive summarization model class.
   - Initialize the BART tokenizer and data loader.
3. **Training**:
   - Load and preprocess the data, then split into training and testing sets.
   - Implement the `BARTForConditionalGeneration` model with the tokenizer.
   - Define and train the model using a trainer class.
4. **Evaluation**:
   - Generate summaries on test data.
   - Assess performance using the ROUGE metric.
5. **Web Application**:
   - Create a new environment and install required packages.
   - Run `app.py` from the output folder.
   - Access `localhost:5000` to input article URLs and view generated summaries.
