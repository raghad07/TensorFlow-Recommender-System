# recommendation-system

# Recommendation System with TensorFlow Recommenders
This code demonstrates the implementation of a recommendation system using TensorFlow Recommenders (TFRS). The recommendation system is built using user and product embeddings and utilizes the Factorized Top K metric for evaluation.

# Data Preprocessing
The code begins with a data preprocessing step to convert text values to numerical values. The create_unique_id function is used to create unique IDs for users and products. These IDs are then used to convert the user and product values in the dataset to their corresponding numerical IDs.

The data is then prepared for the recommendation model using the pipline_data function. It creates a TensorFlow dataset from the user and product IDs, shuffles the data, converts the IDs to numerical values using the converter_users_product function, and batches the data for training.

# Modeling
The recommendation model consists of two components: the User Model and the Product Model. The User Model is responsible for embedding user IDs, and the Product Model embeds product IDs. Both models use an embedding layer to map the IDs to dense vectors.

The User Model and Product Model are then used in the Retrieval Model, which combines them with the Factorized Top K metric for recommendation. The Retrieval Model computes the loss using the user and product embeddings and the Factorized Top K metric.

# Training
The model is compiled using the Adam optimizer and trained using the fit method on the input data pipeline. The training process is run for a specified number of epochs.

To get recommendations, a user ID is passed to the index to retrieve the top recommended product IDs. The numerical IDs are then converted back to their original text values using the id_product dictionary.

# Gradio Integration
The code also includes integration with Gradio, a Python library for creating UIs for machine learning models. Gradio allows users to interact with the recommendation system by entering a user ID and receiving a list of recommended products.

]
