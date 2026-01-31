# DataByte-Laterals-Tasks-for-NLP

Machine Learning and Deep Learning Portfolio
This portfolio contains two projects. The first project focuses on Natural Language Processing and classification. The second project involves building a Recurrent Neural Network from the ground up using linear algebra to generate text.

Project 1: Disaster Tweet Classification
Objective
The goal is to develop a system that can analyze social media posts and determine if they are reporting a real-world emergency or using disaster-related language in a figurative way.

Implementation Phases
1. Data Cleaning
The raw text data is processed through a cleaning pipeline. This involves removing web links, user mentions, and special characters. The text is converted to lowercase to ensure the model treats similar words identically regardless of capitalization.

2. Feature Engineering
Text is converted into numerical data using the Term Frequency-Inverse Document Frequency method. This statistical approach assigns a weight to each word based on its importance within a specific tweet relative to the entire collection of tweets.

3. Classification Models
Two different types of models were implemented for this task:

Logistic Regression: A classic statistical model used to establish a baseline performance level.

Multi-Layer Perceptron: A deep learning model consisting of three hidden layers. This allows the system to identify more complex relationships between words that a simple linear model might miss.

4. Evaluation
The models are evaluated using the F1-Score, which measures the balance between precision and recall. A confusion matrix is generated to visualize how many real disasters were correctly identified versus how many false alarms were triggered.

Project 2: Character-Level Text Generator
Objective
The goal is to build a Recurrent Neural Network from scratch to generate new text based on a provided dataset of song lyrics.

Technical Constraints
This project follows strict rules to ensure a deep understanding of the underlying mathematics:

No High-Level Layers: Standard pre-built layers such as those found in deep learning libraries are strictly avoided.

Manual Matrix Operations: All logic is implemented using basic linear algebra. This includes manually defining weight matrices for the input, the hidden state, and the output.

System Architecture
1. Data Representation
The text corpus is converted into a vocabulary of unique characters. Each character is mapped to a unique integer index. These indices are used to represent inputs during the training process.

2. The RNN Cell
The core of the system is the recurrent cell, which computes a hidden state for every step in a sequence. The hidden state acts as the memory of the network. It is calculated by multiplying the current input and the previous hidden state by their respective weight matrices and applying a non-linear activation function.

3. Training and Optimization
The model learns by iterating through sequences of text and comparing its predicted next character to the actual character.

Gradient Clipping: A mandatory step where gradients are capped to a specific range to prevent the mathematical instability known as exploding gradients.

Loss Calculation: Cross-entropy loss is used to measure the difference between the predicted probabilities and the true targets.

4. Text Generation
To generate text, a seed character is provided to the model. The model calculates the probability for every possible next character. Instead of simply picking the highest probability, the system samples from the distribution to ensure the generated text remains varied and mimics the structure of the original lyrics.
