WASTE MANAGEMENT ASSISTANT
Module 8 Summative Lab

PROJECT OVERVIEW
This project focuses on building an AI-powered waste management assistant that helps users identify waste materials and understand how to dispose of or recycle them correctly.

The assistant supports two ways of identifying waste:
1. Image classification: Users can upload an image of waste for classification.
2. Text classification: Users can describe a waste item using text.

After identifying the material, the system retrieves relevant information from recycling policy documents and generates disposal or recycling instructions.

PROJECT OBJECTIVES
- Build a CNN-based image classification model.
- Build a machine learning model that classifies waste from text descriptions.
- Implement Retrieval-Augmented Generation (RAG) to retrieve relevant recycling policies.
- Generate recycling instructions grounded in retrieved policy documents.
- Integrate the different components into a single waste management assistant.
- Evaluate the system using classification metrics and practical test cases.

DATASETS
1. RealWaste Image Dataset
   Used to train and evaluate the image classification model.

2. Waste Description Dataset
   Contains text descriptions of waste items and their corresponding categories. Used to train the text classification model.

3. Recycling Policy Documents
   Used as the knowledge source for retrieving relevant recycling information and generating instructions.

WASTE CATEGORIES
The system recognises nine waste categories:
- Cardboard
- Food Organics
- Glass
- Metal
- Miscellaneous Trash
- Paper
- Plastic
- Textile Trash
- Vegetation

MODELS AND TECHNIQUES

Image Classification:
- MobileNetV2 with transfer learning.
- Image preprocessing and data augmentation.
- Class weighting to address class imbalance.
- Hyperparameter tuning and fine-tuning.
- Evaluation using accuracy, precision, recall, F1-score, and a confusion matrix.

Text Classification:
- TF-IDF vectorisation.
- Word and character n-grams.
- Comparison of multiple machine learning classifiers.
- Linear Support Vector Classification (LinearSVC).
- Cross-validation and hyperparameter tuning.

Recycling Instruction Generation:
- Retrieval-Augmented Generation (RAG).
- Document chunking.
- TF-IDF-based policy retrieval.
- FLAN-T5 for instruction generation.
- Faithfulness checking and extractive fallback.

INTEGRATED ASSISTANT
The final system combines the image classifier, text classifier, and RAG pipeline through a unified WasteAssistant interface.

It supports:
- Image-based waste identification.
- Text-based waste identification.
- Confidence-based prediction handling.
- Recycling instruction generation.
- Policy-based fallback responses.
- Feedback logging and model updates.
- Input validation and error handling.

KEY RESULTS
- Image classification achieved approximately 82.5% test accuracy.
- Text classification achieved 100% test accuracy on the held-out test set.
- LinearSVC was the best-performing text classification model.
- The RAG pipeline generated instructions for some categories and used extractive fallback for others when the faithfulness threshold was not met.
- Integrated image testing achieved approximately 82% accuracy.

TECHNOLOGIES USED
- Python
- TensorFlow / Keras
- Scikit-learn
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Hugging Face Transformers
- TF-IDF
- Jupyter Notebook

PROJECT STRUCTURE
The notebook is organised into five main parts:

Part 1: Data Exploration and Preparation
Part 2: Waste Material Classification with CNN
Part 3: Waste Description Classification
Part 4: Recycling Instruction Generation with RAG
Part 5: Integrated Waste Management Assistant

LIMITATIONS
- The text dataset contains synthetic descriptions and may not fully represent real-world user input.
- The image classifier still confuses visually similar materials.
- High prediction confidence does not always mean an input belongs to a recognised waste category.
- Generated recycling instructions require further validation against the original policy documents.
- More diverse real-world data would help improve generalisation.

CONCLUSION
This project demonstrates how computer vision, natural language processing, machine learning, and retrieval-augmented generation can work together to solve a practical waste management problem.

Rather than relying on a single model, the assistant combines multiple components to identify waste and provide relevant recycling guidance.

The project also highlights the importance of evaluating individual models, handling uncertainty, and grounding generated responses in reliable information.
