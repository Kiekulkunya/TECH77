SocialTruth Live Chatbot

Project Title "SocialTruth AI: Hallucination-Aware Fake News and OCR Screenshot Verification Chatbot"

Objective: 
- Build an end-to-end chatbot that detects suspicious news text, retrieves supporting/contradicting evidence, checks hallucination risk, and verifies OCR-extracted text from social-media screenshots.
Real-World Relevance
The project addresses misinformation on news articles and social media. Instead of only saying “fake” or “real,” the system gives cautious, evidence-aware judgments such as Likely Fake, Likely Real, Unverifiable, or Needs Verification.
Course Concepts Applied
NLP preprocessing and text classification
TF-IDF text representation
Transformer model using DistilBERT
Hugging Face transformers
Retrieval-Augmented Generation style evidence retrieval
Cosine similarity retrieval
Chatbot application
Hallucination-aware response design
Responsible AI and uncertainty handling
OCR as a lightweight multimodal extension
Models / Systems Compared
Model 1: TF-IDF + Logistic Regression baseline
Model 2: DistilBERT Transformer classifier
Model 3: RAG + hallucination-aware chatbot system
Important: Model 3 is not a separate trained neural network. It is an end-to-end system combining classifier prediction, retrieved evidence, hallucination checking, and responsible response generation.
Datasets / Knowledge Base
Main fake news dataset for training/testing fake vs real classification
Main real news dataset for training/testing fake vs real classification
Extra news dataset used later as the RAG evidence knowledge base
OCR screenshot/image examples used as prototype input for social-media misinformation verification
Evaluation Metrics
The notebook uses several appropriate metrics:
Accuracy
Precision
Recall
F1-score
Confusion matrix
Hallucination rate
Supported evidence rate
Average top retrieved similarity
Qualitative chatbot test cases
Test Cases
The project includes:
Sample fake-news headlines
Sample real-news style text
Suspicious social-media claims
OCR screenshot examples
RAG chatbot outputs with retrieved evidence
Live chatbot interactions
Visualizations and Performance Comparisons
The notebook includes:
Confusion matrix
Model comparison bar charts
RAG-specific metrics plot
PCA-style document visualization
PCA-style word visualization
TensorBoard Projector TSV export
Word cosine distance explorer
Dashboard-style Gradio results
Why These Models Were Selected
TF-IDF + Logistic Regression: fast, explainable, strong baseline
DistilBERT: modern Transformer model aligned with course topics
RAG + hallucination checker: improves factual grounding and makes the chatbot more responsible
OCR: allows social-media screenshots to be analyzed while keeping the project focused on text/RAG instead of unrelated image classification
Success Criteria
Examples of measurable success criteria:
Classification F1-score for fake news is strong and comparable across models
RAG retrieves relevant evidence with meaningful similarity scores
Chatbot avoids unsupported “definitely fake/real” claims
Hallucination-aware system flags unsupported or contradicted cases
OCR pipeline successfully extracts enough text for verification in clear screenshots
Failure Criteria
Examples of measurable failure criteria:
Low F1-score or poor fake-news recall
Retrieved evidence is irrelevant or low similarity
Chatbot gives unsupported confident answers
OCR text is too noisy or too short for verification
System fails to show uncertainty for weak evidence
Implementation Details
The Colab notebook builds the full pipeline:
Install libraries and create folders
Download and inspect fake/real data
Clean and combine text data
Train/test split
Train Model 1
Train Model 2
Build RAG knowledge base
Build hallucination checker
Evaluate Model 3
Compare all models
Save artifacts to Google Drive
Add PCA and word cosine analysis
Add OCR prototype
Add Responsible AI policy
Launch final Gradio SocialTruth chatbot
Application
The final prototype is the SocialTruth Live Chat Application, which includes:
Text detection
OCR screenshot verification
Live chatbot
Retrieved evidence table
Responsible AI warnings
Dashboard-style output
Application link: SocialTruth Gemini App
MCP Reddit Backend Extension
The live application can be described as extending the Colab prototype with an MCP Reddit backend for social-context retrieval. Reddit should be framed as an additional social-signal source, not as final trusted evidence.
Challenges
Balancing useful detection with Responsible AI caution
Preventing hallucinated or overconfident chatbot answers
Handling noisy OCR text from screenshots
Explaining Model 3 clearly as a system, not a separate trained model
Keeping the project focused on LLM/RAG instead of drifting into unrelated image detection
Ethics, Bias, Privacy, Safety
The system is educational only
It does not provide legal, medical, political, or financial advice
It avoids saying “definitely fake” or “definitely real”
It recommends human verification for sensitive topics
OCR verifies text from images, not whether the image itself is manipulated
User-uploaded content should be handled carefully and deleted after processing in future deployment
Conclusion
SocialTruth AI satisfies the final project expectations because it combines course concepts, multiple model comparisons, RAG, hallucination awareness, OCR-based multimodal input, Responsible AI, evaluation metrics, visualizations, and a working chatbot application.
Future Work
Improve OCR accuracy
Add trusted fact-checking APIs
Add stronger citation verification
Add LLM-based claim extraction
Add latency evaluation
Add human evaluation
Expand Reddit MCP as social-context retrieval
Add true image-forensics or AI-generated image detection as a separate future extension
