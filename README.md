

# SEO Content Detector

## Project Overview
This project provides a real-time web content analysis pipeline that scrapes a given URL, extracts textual features, evaluates content quality, and detects duplicate content against a reference corpus. It is designed to help SEO professionals and content managers identify high-quality and potentially duplicated web content quickly.

## Setup Instructions
```bash
git clone https://github.com/Ravichandra-D/seo-content-detector
cd seo-content-detector
pip install -r requirements.txt
jupyter notebook notebooks/seo_pipeline.ipynb

Key Decisions

Choice of Libraries: requests and BeautifulSoup for robust web scraping, textstat for readability metrics, scikit-learn for TF-IDF and similarity calculations.

HTML Parsing Approach: Removed scripts, styles, and non-visible tags to extract meaningful text only.

Similarity Threshold: Set to 0.8 for cosine similarity to flag near-duplicate content while avoiding false positives.

Model Selection: Rule-based quality scoring was used for the demo; optional ML model can be integrated for advanced scoring.

Results Summary

Model Accuracy/F1: N/A for rule-based demo; ML model optional.

Number of Duplicates Found: Varies based on reference CSV; detected using TF-IDF cosine similarity.

Sample Quality Scores: High-quality content example → word count: 1450, readability: 65.2, quality label: High, is_thin: False.

Limitations

Limited to English-language content; other languages may produce inaccurate readability scores.

Quality scoring is currently rule-based; ML model integration required for predictive accuracy.

Duplicate detection relies on reference CSV; new unseen content may not be flagged if the corpus is incomplete.
