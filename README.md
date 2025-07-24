## Project Description

The **Next Word Predictor** is a deep learning-based Natural Language Processing (NLP) project designed to predict the next most likely word in a given input sentence. Built using **PyTorch** and **LSTM (Long Short-Term Memory)** networks, this model demonstrates how sequence modeling techniques can be applied to language understanding and generation.

### What the Project Does

This project takes a body of text (in this case, a real-world document such as FAQs or course information), learns the sequence patterns from it, and uses this knowledge to generate context-aware predictions for what the next word should be when a user types part of a sentence.

### How It Works

1. **Text Preprocessing**:
   - The raw document is cleaned and normalized to lowercase.
   - Using **NLTK**, the text is tokenized into individual words.
   - A vocabulary is created by assigning a unique index to each token.

2. **Sequence Generation**:
   - For each sentence, multiple training sequences are generated using a sliding window.
   - Each sequence includes a partial sentence, with the last word used as the prediction target.
   - Sequences are padded to a uniform length using PyTorch tensors.

3. **Model Architecture**:
   - An **Embedding layer** converts words into dense vector representations.
   - An **LSTM layer** learns dependencies between words in a sequence.
   - A **Fully Connected (Linear) layer** maps LSTM outputs to vocabulary scores.
   - The model is designed to be simple, interpretable, and efficient.

4. **Training Loop**:
   - The model is trained for 50 epochs using **CrossEntropyLoss** and the **Adam optimizer**.
   - Loss decreases steadily across epochs, reaching high performance.
   - The final model achieves approximately **95% accuracy** on the training dataset.

5. **Prediction Phase**:
   - The model allows dynamic input: you provide a partial sentence, and it predicts the next word.
   - Example:
     ```
     Input: "The course follows a monthly"
     Output: "subscription"
     ```
   - It can be run iteratively to generate multiple words and build entire sentences.

### Highlights

- Trained on a realistic, domain-specific document
- End-to-end NLP pipeline from raw text to prediction
- Demonstrates practical LSTM usage in PyTorch
- Achieves ~95% accuracy
- Educational and easy to understand

### Applications

- Chatbots and conversational assistants
- Smart typing and email autocompletion
- AI writing assistants
- NLP education and research

