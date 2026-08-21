**Project Title "Live SocialTruth AI: Hallucination-Aware Fake News and OCR Screenshot Verification Chatbot"**

1. Project Milestones: (6-7 Days)
- 1.1 Data Preparation : 1 days
- 1.2 Working on Coding using colab : 3 days
 - Part 1: Data uploading, Data Checking, and Data Preparation
 - Part 2: Training, Testing, and Validating split (70/15/15) Across 3 Models
 - Part 3: PCA-Style Text Visualization Using TruncatedSVD
 - Part 4: Launched Tex-SocialTruth Chatbot 1.0 (Prototype)
 - Part 5: Embedded Optical Character Recognition for Chatbot extension
 - Part 6: Integrated Responsible AI with evalaution features to Chatbot
 - Part 7: Launched Text and OCR- SocialTruth Chatbot 2.0 (Prototype)
 - Part 8: Launched Live Text and OCR-SocialTruth Chatbot 3.0 (Prototype)
 - Part 9: Main Findings and Key Results
 - Part 10: Key Takeaways
- 1.3 Working on ChatPRD for product manager report, scope, ideas, business goal, user target, MCP, and UI/UX : 1 day
- 1.4 Working on MVP Live Chat hosted by Gemini. Migrate python code, logic, fine-tuning, testing, validating, approve the MVP product: 1 Day
      

3. Objective: Build an end-to-end chatbot that detects suspicious news text, retrieves supporting/contradicting evidence, checks hallucination risk, and verifies OCR-extracted text from social-media screenshots and launched live SocialTruth application via gradio and hosted by gemini for web base for real-world problem.

4. Real-World Relevance:  The project addresses misinformation on news articles and social media. Instead of only saying “fake” or “real,” the system gives cautious, evidence-aware judgments such as Likely Fake, Likely Real, Unverifiable, or Needs Verification. The live Chatbot is integrating quantitative for LLMs and qualitative of Responsible AI into algorithm. 

5. Course Concepts Applied
- NLP preprocessing and text classification
- TF-IDF text representation
- Transformer model using DistilBERT
- Hugging Face transformers
- Retrieval-Augmented Generation (RAG) style evidence retrieval
- Cosine similarity retrieval (UI react)
- Hallucination-aware response design
- Responsible AI and uncertainty handling
- OCR as a lightweight multimodal extension
- Chatbot Application Prototype
- Auto news feeding with Reddit API Model Context Protocol (MCP)   

5. Models / Systems Compared for fake/real news
5.1 Model 1: TF-IDF + Logistic Regression baseline
 - Activation function: not directly used like a neural network.
 - Logistic Regression uses a sigmoid-style probability function internally for binary classification.
 - Epochs: not used.
 - Max_Iter = 1000
   
<img width="628" height="534" alt="Confusion Model 1" src="https://github.com/user-attachments/assets/dbfdeefb-47a6-4709-8ac2-64ccc7cf18ec" />
<img width="884" height="534" alt="Model 1_5" src="https://github.com/user-attachments/assets/03cbfbba-4228-45b3-b63c-5905224ba2cd" />
<img width="884" height="534" alt="Model 1_4" src="https://github.com/user-attachments/assets/c3fe3063-6563-4764-85dd-f022be1a9ff7" />
<img width="884" height="534" alt="Model 1_3" src="https://github.com/user-attachments/assets/dbbdc280-4730-41a2-8f0c-7430da14be59" />
<img width="834" height="534" alt="Model 1_2" src="https://github.com/user-attachments/assets/f425868c-cc79-431c-b357-8008a2ddd88a" />

   
5.2 Model 2: DistilBERT Transformer classifier
- Activation functions: inside DistilBERT, the Transformer uses neural-network activations, mainly GELU.
- The final classification layer outputs logits, then probabilities are calculated with "Softmax" due to Fake or Real label
- Epoch = 2 (optimization)

<img width="843" height="282" alt="Model 2_1" src="https://github.com/user-attachments/assets/9aad5619-3609-49b9-813e-e2ce255beda4" />
<img width="1035" height="287" alt="Model 2" src="https://github.com/user-attachments/assets/ccb2aabf-8955-4784-8a12-bc3529a4101e" />

5.3 Model 3: RAG + Hallucination Checker
- Activation function: none.
- Epochs: none.
- Model 3 is not trained as a neural network. It is a system using:Model 1 prediction
- TF-IDF retrieval
- cosine similarity
- rule-based hallucination checker
(Important: Model 3 is not a separate trained neural network. It is an end-to-end system combining classifier prediction, retrieved evidence, hallucination checking, and responsible response generation.)

<img width="1247" height="462" alt="Model 3_1" src="https://github.com/user-attachments/assets/2b56abab-2e49-49da-b8e5-0ac0d2118fca" />
<img width="984" height="583" alt="Model 3" src="https://github.com/user-attachments/assets/b6a94945-42b4-40fe-98a0-1ea8ed304513" />



6. Datasets / Knowledge Base
6.1 Main Fake/ Real news dataset for training/testing fake vs real classification
  - (Kaggle: https://www.kaggle.com/code/therealsampat/fake-news-detection/input?select=True.csv)
6.2 Extra news dataset used later as the RAG evidence knowledge base
  - (Kaggle : https://www.kaggle.com/code/ruchi798/how-do-you-recognize-fake-news/input)
6.3 Testing Chatbot: Images generation and Global News
  - https://globalnews.ca/news/12023905/earthquakes-intensity-2026/
  - https://globalnews.ca/news/12026846/donald-trump-tariff-pause/

7. Exploratory Data Analysis (Basic EDA): Checking missing data, count, check type, and labelling

8. OCR screenshot/image examples used as prototype input for social-media misinformation verification

9. Evaluation Metrics:
9.1 Accuracy
9.2 Precision
9.3 Recall
9.4 F1-score
9.5 Confusion matrix
9.63 Hallucination rate
9.7 Supported evidence rate
9.8 Average top retrieved similarity
9.9 Qualitative chatbot test cases
9.10 Test Cases

<img width="984" height="583" alt="Model 3" src="https://github.com/user-attachments/assets/13d2590b-8f86-4929-9618-53b147860885" />
<img width="1179" height="583" alt="Comparison among 3 models" src="https://github.com/user-attachments/assets/c3d1f8f7-4dff-4db2-97eb-df005c0d3054" />


10. The project includes:
- Sample fake-news headlines
- Sample real-news style text
- Suspicious social-media claims
- OCR screenshot examples
- RAG chatbot outputs with retrieved evidence
- Live chatbot interactions (on Gradio, Colba)
- Visualizations and Performance Comparisons
- Live Chat MVP (Gemini Browser)

11. The notebook includes:
- Confusion matrix
- Model comparison bar charts
- RAG-specific metrics plot
- PCA-style document visualization
- PCA-style word visualization
- TensorBoard Projector TSV export
- Word cosine distance explorer
- Dashboard-style Gradio results

12. Why These Models Were Selected
- TF-IDF + Logistic Regression: fast, explainable, strong baseline
- DistilBERT: modern Transformer model aligned with course topics
- RAG + hallucination checker: improves factual grounding and makes the chatbot more responsible
- OCR: allows social-media screenshots to be analyzed while keeping the project focused on text/RAG instead of unrelated image classification
- **IMPORTANT MESSAGES: While Model 2 (DistilBERT) performed best for fake-news classification metrics, the final SocialTruth application uses Model 3 (RAG + hallucination-aware system) because the project goals is not only classificatino accuracy, but also grounded explanation, evidence retrieval, uncertainty handling, and Responsible AI.**

13. Success Criteria
- Examples of measurable success criteria:
- Classification F1-score for fake news is strong and comparable across models
- RAG retrieves relevant evidence with meaningful similarity scores
- Chatbot avoids unsupported “definitely fake/real” claims
- Hallucination-aware system flags unsupported or contradicted cases
- OCR pipeline successfully extracts enough text for verification in clear screenshots
- Failure Criteria
- Help understand how to applied LLMs and Chatbot in Real world.
- Successfully launched prototype SocialTruth development application from version 1 to version 3 and migrate to MVP via gemini host.

  <img width="1865" height="898" alt="SocialTruth Chatbot 9 live" src="https://github.com/user-attachments/assets/36179765-e3d4-45e9-ba72-549daf307c89" />

14. Examples of measurable failure criteria:
- Low F1-score or poor fake-news recall
- Retrieved evidence is irrelevant or low similarity
- Chatbot gives unsupported confident answers
- OCR text is too noisy or too short for verification
- System fails to show uncertainty for weak evidence
- Go Live Chatbot (Prototype and MVP) with MCP reddit connection



15. Implementation Details

15.1 The Colab notebook builds the full pipeline:
- Install libraries and create folders
- Download and inspect fake/real data
- Clean and combine text data
- Train/test split
- Train Model 1
- Train Model 2
- Build RAG knowledge base
- Build hallucination checker
- Evaluate Model 3
- Compare all models
- Save artifacts to Google Drive
- Add PCA and word cosine analysis
- Add OCR prototype
- Add Responsible AI policy

Principle Component Analysis (PCA) with word distance and word coside solution.

<img width="1148" height="765" alt="Wrod Distance Model 2" src="https://github.com/user-attachments/assets/71b0af5e-ded3-4a66-baa4-6c5c288c857c" />
<img width="1642" height="633" alt="word cosine distance 2" src="https://github.com/user-attachments/assets/281b0035-e9ed-423e-b8fa-ba60d8d3f441" />
<img width="1086" height="712" alt="PCA" src="https://github.com/user-attachments/assets/9dd744cc-ec1e-4896-8fdb-eb8b0898e820" />
<img width="1724" height="525" alt="newplot" src="https://github.com/user-attachments/assets/dabb7688-59bc-4808-8cba-546e5fc8b4e6" />
<img width="1724" height="525" alt="newplot (2)" src="https://github.com/user-attachments/assets/7d802738-7449-4e08-abe5-40d53a630182" />
<img width="1712" height="525" alt="newplot (1)" src="https://github.com/user-attachments/assets/c0ab7acd-3fa2-4462-9eeb-a238ae523fe3" />


15.2 Launch final Gradio SocialTruth chatbot
- Live Chatbot Prototype on Gradio
- Live Chatbot MVP Application hosted by gemini

<img width="1702" height="888" alt="Chatbot OCR3" src="https://github.com/user-attachments/assets/cb591509-3e49-4ebc-a10f-3b4062a797bc" />

<img width="1062" height="903" alt="SocialTruth Gemini" src="https://github.com/user-attachments/assets/dc2ed855-1395-414b-b412-b22721ead62b" />

15.3 The final prototype is the SocialTruth Live Chat Application, which includes:
- Text detection
- OCR screenshot verification
- Live chatbot
- Retrieved evidence table
- Responsible AI warnings
- Dashboard-style output

15.4 Application link: SocialTruth Gemini App
- MCP Reddit Backend Extension
- The live application can be described as extending the Colab prototype with an MCP Reddit backend for social-context retrieval. Reddit should be framed as an additional social-signal source, not as final trusted evidence.

16. Challenges
- Balancing useful detection with Responsible AI caution
- Preventing hallucinated or overconfident chatbot answers
- Handling noisy OCR text from screenshots
- Explaining Model 3 clearly as a system, not a separate trained model
- Keeping the project focused on LLM/RAG instead of drifting into unrelated image detection
- Although AI is a strong predictor, human oversight remains critical.
- While Model 2 (DistilBERT) scored highest on classification metrics, SocialTruth implements Model 3 (RAG + hallucination-aware system) to satisfy broader requirements: grounded explanations, evidence retrieval, uncertainty handling, and Responsible AI.
  
  
17. Ethics, Bias, Privacy, Safety
- The system is educational only
- It does not provide legal, medical, political, or financial advice
- It avoids saying “definitely fake” or “definitely real”
- It recommends human verification for sensitive topics
- OCR verifies text from images, not whether the image itself is manipulated
- User-uploaded content should be handled carefully and deleted after processing in future deployment

18. Conclusion
- Although AI is a strong predictor, human oversight remains critical.
- While Model 2 (DistilBERT) scored highest on classification metrics, SocialTruth implements Model 3 (RAG + hallucination-aware system) to satisfy broader requirements: grounded explanations, evidence retrieval, uncertainty handling, and Responsible AI.
- SocialTruth AI satisfies the final project expectations because it combines course concepts, multiple model comparisons, RAG, hallucination awareness, OCR-based multimodal input, Responsible AI, evaluation metrics, visualizations, and a working chatbot application.

19. Future Work
- Improve OCR accuracy
- Add trusted fact-checking APIs
- Add stronger citation verification
- Add LLM-based claim extraction
- Add latency evaluation
- Add human evaluation
Expand Reddit MCP as social-context retrieval
Add true image-forensics or AI-generated image detection as a separate future extension

20. Live Chatbot Application looks like:
    
- Prototype: https://colab.research.google.com/drive/1R8VYcG7Q9-L-s3RXJxcW1IVcKWieWbUs?usp=sharing
- MVP: https://gemini.google.com/share/88ca2decc389?skid=d9de2296-e120-41fb-bbef-844a57ca0a73

