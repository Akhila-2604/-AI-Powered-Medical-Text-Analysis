# -AI-Powered-Medical-Text-Analysis

Project Name: Medical & Pharma Text Analytics Using AI
Project Summary:
This project aims to analyze and categorize medical and pharmaceutical-related text data from media articles and Twitter posts using AI models. The system extracts entities such as drugs, diseases, and study names, classifies topics, and determines sentiment to gain insights from healthcare-related discussions. It utilizes OpenAI's GPT and Google's Gemini AI models to process textual data effectively.

Code Explanation:
1. Importing Required Libraries & Setting Up APIs
    Installs and imports Pandas for data manipulation.
    Uses OpenAI API for entity extraction, topic classification, and sentiment analysis.
    Uses Google's Gemini AI for extracting drugs, diseases, and study names.
     Sets up API keys for OpenAI and Google Generative AI.
2. Loading & Cleaning Data
  Reads two datasets:
  Media articles (Media & Research Articles data.xlsx)
  Twitter posts (Twitter Posts Data.xlsx)
  Cleans tweets by removing hashtags, mentions, special characters, and URLs.
  Renames columns for consistency.
  Drops unnecessary columns like Post link, Article link, and HCP Handle.
  Merges the two datasets into merged_df.
3. Text Processing
  Combines title and Content columns into a single "Combined" column for easier analysis.
4. AI-Powered Entity Extraction & Classification
  Calls OpenAI's GPT to:
  Extract medical entities (drugs, diseases, study names).
  Classify topics into predefined categories (e.g., Efficacy-General, Safety-General, PFS, OS).
  Perform sentiment analysis (positive, negative, or neutral).
Uses Google's Gemini AI to extract medical entities more efficiently.
5. Iterative Processing & API Calls
  Loops through each row in merged_df, calling analyze_text_gemini() to extract entities.
  Introduces time.sleep(1) to prevent API rate limits.
6. Final Output
  Displays the merged_df with new columns:
  Entities (Drugs, Diseases, Study Names)
  Topic Classification
  Sentiment Analysis
