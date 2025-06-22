# SemanticBookRecommender
The Semantic Book Recommender uses BART for zero-shot classification and RoBERTa for sentiment analysis, combined with Hugging Face embeddings and vector search, to deliver personalized book suggestions. With a Gradio interface, it customizes recommendations based on your interests and emotional tone, ensuring a perfect match every time. 📚✨

Overview

The Semantic Book Recommender utilizes state-of-the-art models and frameworks to enhance your book discovery experience:

BART (Bidirectional and Auto-Regressive Transformers) for zero-shot classification to classify books into various categories without requiring task-specific training data.
RoBERTa (A Robustly Optimized BERT Pretraining Approach) for sentiment analysis, determining the emotional tone (e.g., joyful, sad, angry) of book descriptions.
Hugging Face Embeddings and Chroma vector database for semantic search, enabling personalized and context-aware book suggestions.
Gradio for an intuitive, interactive user interface, where you can simply enter a book description or select emotions to get recommendations.

Features

Personalized Recommendations: Get tailored book suggestions based on your interests and emotional tone.
Emotion-Based Filtering: Filter book recommendations by emotions like happy, sad, surprising, and angry.
Zero-Shot Classification: Classify books into different categories without needing domain-specific labeled data.
Sentiment Analysis: Understand the emotional tone of book descriptions using RoBERTa.
Gradio Interface: An easy-to-use web interface for seamless interaction.
Installation & Setup

Prerequisites:
Python 3.8 or later
Libraries:
Hugging Face’s transformers
langchain
gradio
torch (for sentiment analysis)
pandas and numpy

How It Works

1. Data Preprocessing:
The dataset of 7,000+ books is cleaned, with missing values addressed and the books' metadata parsed.
Features like word count in descriptions and emotion scores are added to enhance recommendations.
2. Semantic Search:
TextLoader loads book descriptions.
Descriptions are then split using a CharacterTextSplitter, and Hugging Face embeddings are used to represent the text in vector space.
Chroma performs efficient semantic search, retrieving books that are contextually similar to your query.
3. Zero-Shot Classification (BART):
Books are classified into categories (e.g., Fiction, Nonfiction) without the need for traditional training, thanks to the BART model.
4. Sentiment Analysis (RoBERTa):
The RoBERTa model performs sentiment analysis on the descriptions to classify their emotional tone (e.g., joy, sadness, anger).
5. Gradio Interface:
Gradio provides a simple, interactive interface for users to input their queries and receive personalized book recommendations.

Usage

Once the application is running, you can interact with the recommender using the Gradio interface.

Input Options:
Query: Enter a description of a book or a theme you're interested in.
Category: Select a book category (e.g., All, Children's Fiction).
Tone: Select an emotional tone (e.g., Happy, Sad, Suspenseful).
Example:
Enter a description like: “A thrilling mystery novel about a detective solving a complex crime”.
Select the emotional tone: Suspenseful.
Get recommendations based on your preferences!

Results

The Semantic Book Recommender successfully:

Classifies books into predefined categories like Fiction, Nonfiction, and Children's Fiction without the need for manual labeling.
Performs sentiment analysis using RoBERTa, providing insights into the emotional tone of book descriptions.
Generates personalized book recommendations based on the semantic similarity of descriptions, helping users discover books that align with their interests.
Filters recommendations by emotion (happy, sad, suspenseful, etc.), creating a tailored reading experience.

Future Improvements

Multi-Language Support: Extend the recommender to support books in multiple languages.
Enhanced Emotion Classification: Improve the accuracy of sentiment analysis for a wider range of emotions.
User Ratings Integration: Integrate user ratings and reviews to further personalize recommendations.
Genre-based Filtering: Allow users to filter recommendations by specific genres.
