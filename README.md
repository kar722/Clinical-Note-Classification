# Clinical-Note-Classification

Current Project Workflow
1. Data Access
   → Apply for i2b2/MIMIC/n2c2 datasets

2. Data Preprocessing
   → Sentence splitting, tokenization (e.g., `BertTokenizerFast`)
   → Label mapping (e.g., section headings to category indices)

3. Model Fine-Tuning
   → Use `TFBertForSequenceClassification` or `AutoModelForSequenceClassification`
   → Early stopping, learning rate scheduler

4. Evaluation
   → F1, Precision, Recall (macro for imbalanced datasets)

5. Application
   → Use Gradio/Streamlit to demo classification on user-input notes
