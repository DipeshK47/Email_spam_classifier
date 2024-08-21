# NLP Email Spam Classifier

## Project Overview

This project is an implementation of an Email/SMS Spam Classifier using Natural Language Processing (NLP) techniques. The classifier is built using the Multinomial Naive Bayes algorithm and is deployed as a web application using Streamlit. The application allows users to input a message and predict whether it is "Spam" or "Not Spam."

## Table of Contents

- [Project Overview](#project-overview)
- [Features](#features)
- [Installation](#installation)
- [Usage](#usage)
- [Model Training](#model-training)
- [File Structure](#file-structure)
- [Technologies Used](#technologies-used)
- [Contributing](#contributing)
- [License](#license)

## Features

- **Message Classification:** Predicts whether the given message (email/SMS) is spam or not.
- **Text Preprocessing:** Includes tokenization, stopword removal, punctuation removal, and stemming.
- **Vectorization:** Uses TF-IDF (Term Frequency-Inverse Document Frequency) to convert text data into numerical features.
- **Model:** Utilizes the Multinomial Naive Bayes algorithm for classification.
- **User Interface:** A simple, interactive web interface using Streamlit.

## Installation

### Prerequisites

- Python 3.7 or higher
- Streamlit
- Scikit-learn
- NLTK
- Pickle

### Steps

1. **Clone the repository:**
   ```bash
   git clone 
   cd nlp-email-spam-classifier
   ```

2. **Create a virtual environment:**
   ```bash
   python3 -m venv venv
   source venv/bin/activate   # On Windows, use `venv\Scripts\activate`
   ```

3. **Install the required packages:**
   ```bash
   pip install -r requirements.txt
   ```

4. **Download NLTK data (stopwords and punkt):**
   ```python
   import nltk
   nltk.download('stopwords')
   nltk.download('punkt')
   ```

5. **Run the Streamlit app:**
   ```bash
   streamlit run app.py
   ```

## Usage

1. Launch the application by running the command `streamlit run app.py`.
2. Enter the message you want to classify in the text area provided.
3. Click on the "Predict" button.
4. The application will display whether the message is "Spam" or "Not Spam."

## Model Training

The model was trained on a labeled dataset consisting of spam and non-spam messages. The following steps were taken to build the model:

1. **Text Preprocessing:** 
   - Lowercasing
   - Tokenization
   - Removal of stopwords and punctuation
   - Stemming

2. **Vectorization:**
   - TF-IDF was used to convert the preprocessed text into numerical features.

3. **Modeling:**
   - The Multinomial Naive Bayes algorithm was chosen for its effectiveness in text classification tasks.
   - The model was trained and validated on the processed data.

4. **Saving the Model:**
   - The trained model and TF-IDF vectorizer were saved using the `pickle` module for later use in the Streamlit application.

## File Structure

```
nlp-email-spam-classifier/
│
├── app.py                   # Streamlit application
├── model.pkl                # Trained Multinomial Naive Bayes model
├── vectorizer.pkl           # TF-IDF vectorizer
├── README.md                # Project documentation
├── requirements.txt         # List of required Python packages               
```

## Technologies Used

- **Programming Language:** Python
- **Libraries:** NLTK, Scikit-learn, Pickle, Streamlit
- **Model:** Multinomial Naive Bayes
- **Vectorization:** TF-IDF
- **Deployment:** Streamlit

## Contributing

Contributions are welcome! Please open an issue or submit a pull request for any improvements or bug fixes.

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.
