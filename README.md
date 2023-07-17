# Customer Complaints Classification using NLP and Topic Modelling

## Problem Statement

For a financial company, customer complaints play a crucial role in identifying areas for improvement in their products and services. Efficiently resolving these complaints can minimize customer dissatisfaction and enhance customer loyalty. However, manually evaluating and assigning each customer support ticket to the relevant department becomes increasingly challenging as the company grows and acquires a larger customer base.

The goal of this case study is to automate the customer support ticket system for a financial company by building a model that can classify customer complaints based on the products and services mentioned in the ticket. By categorizing these tickets, the company can quickly address the issues and improve their services.

## Business Goal

Develop a model that utilizes non-negative matrix factorization (NMF), a topic modeling technique, to classify customer complaints into the following five clusters based on their products/services:

1.  Credit card / Prepaid card
2.  Bank account services
3.  Theft/Dispute reporting
4.  Mortgages/loans
5.  Others

The model will analyze the patterns and recurring words present in each ticket using NMF, enabling the identification of important features for each category. By segregating the clusters, the model will reveal the topics of customer complaints.

The model will be trained on unlabeled data in JSON format provided by the company. Once trained, it will be able to classify new customer support tickets into the relevant department/category using supervised learning algorithms such as logistic regression, decision trees, or random forests.

## Approach

1.  Data Preprocessing:
    -   Load the customer support ticket data from the provided JSON file.
    -   Perform necessary preprocessing steps, such as removing stop words, punctuation, and converting text to lowercase.
2.  Topic Modelling using Non-Negative Matrix Factorization (NMF):
    -   Apply NMF on the preprocessed text data to identify patterns and recurring words.
    -   Determine the optimal number of topics based on coherence scores or domain knowledge.
    -   Obtain the topic-word matrix and document-topic matrix.
3.  Clustering and Topic Interpretation:
    -   Cluster the tickets using the document-topic matrix to identify distinct categories.
    -   Analyze the top words associated with each cluster to understand the topics of customer complaints.
    -   Map each cluster to its relevant department/category:
        -   Credit card / Prepaid card
        -   Bank account services
        -   Theft/Dispute reporting
        -   Mortgages/loans
        -   Others
4.  Training a Supervised Model:
    -   Split the preprocessed data into training and testing sets.
    -   Extract relevant features from the document-topic matrix.
    -   Train a supervised learning model (e.g., logistic regression, decision tree, random forest) on the training data.
    -   Evaluate the model's performance using appropriate metrics (e.g., accuracy, precision, recall, F1 score).
5.  Model Deployment and Classification:
    -   Save the trained model for future use.
    -   Deploy the model to classify new customer support tickets into the relevant department/category.
    -   Preprocess the new ticket text, apply NMF, and extract the document-topic matrix.
    -   Use the trained model to predict the category of the new ticket.
6.  Model Evaluation and Iteration:
    -   Continuously evaluate the model's performance using feedback from support employees and monitoring its predictions.
    -   Collect new labeled data to improve the model's accuracy and handle emerging complaint categories.
    -   Iterate on the model by retraining and fine-tuning it with the updated dataset.

## Conclusion

Automating the customer support ticket system using NLP and topic modeling techniques like NMF can significantly improve the efficiency of resolving customer complaints for a financial company. By accurately classifying the tickets into relevant categories, the company can provide quick and targeted solutions to customer issues, leading to higher customer satisfaction and loyalty. Regular evaluation and iteration of the model will ensure its effectiveness and adaptability to changing complaint patterns.
