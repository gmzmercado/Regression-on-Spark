# Predicting Helpfulness of Product Reviews with Apache Spark ML

This repository contains a Jupyter notebook demonstrating the application of Apache Spark ML to predict the helpfulness rate of product reviews. The project leverages Spark's distributed computing capabilities to efficiently handle large-scale data and perform machine learning tasks.

## Introduction

In this notebook, we showcase a machine learning regression problem using Apache Spark to predict the helpfulness rate of product reviews. Apache Spark ML is crucial due to its ability to handle large-scale data processing and machine learning tasks efficiently. Spark’s distributed computing framework allows for the parallel processing of massive datasets, significantly reducing computation time compared to traditional single-machine tools.

### Tools and Skills Employed

In this project, the following skills were employed:

1. **Apache Spark ML**
   - Creating and managing ML pipelines for streamlined machine learning workflows.
   - Using `StringIndexer` and `VectorAssembler` for feature transformation in a distributed environment.
   - Building and evaluating machine learning models using Pipelines.

2. **Distributed Computing with Spark**
   - Leveraging Spark's in-memory computation for efficient processing of large-scale data.
   - Parallel processing of massive datasets using Spark's distributed architecture.

3. **Integration with AWS S3**
   - Downloading and managing datasets stored in AWS S3 using the `boto3` library.
   - Ensuring seamless data transfer between cloud storage and Spark.

4. **Big Data Tools Integration**
   - Integrating Spark with other big data tools and platforms like Hadoop and HDFS for enhanced data processing capabilities.

5. **Model Evaluation**
   - Assessing model performance using Mean Absolute Error (MAE) to ensure accuracy in predictions.

## Our Objective

Our goal is to achieve a Mean Absolute Error (MAE) of less than 0.5. An MAE below 0.5 indicates that our model’s predictions are close to the actual helpfulness scores, demonstrating high accuracy. Beating this threshold signifies that our model is effective at predicting helpfulness, making it a valuable tool for improving user experience on e-commerce platforms.

## Dataset

We use the Helpful Sentences from Reviews dataset from the AWS Open Data Registry, which comprises customer reviews from Amazon, focusing on sentences marked as helpful by users.

| Feature         | Description                                             |
|-----------------|---------------------------------------------------------|
| `asin`          | Amazon Standard Identification Number, uniquely identifies the product |
| `helpful`       | A numerical score indicating how helpful the sentence was rated by users |
| `main_image_url`| URL of the main image associated with the product       |
| `product_title` | Title of the product                                    |
| `sentence`      | The review sentence itself                              |

## Data Loading and Exploration

We download the `train.json` and `test.json` files from AWS S3 and load them into Spark DataFrames for processing and analysis. For this repository, these files are already included for convenience.

## Data Preprocessing

Categorical columns are converted into numerical indices using `StringIndexer`, and features are combined into a single vector column using `VectorAssembler`. Caching is employed to save computational power by storing data in memory for quick access.

## Model Development and Assessment

We build a linear regression model to predict the helpfulness score and evaluate it using the MAE metric. The model achieved a Test MAE of 0.3275, meeting the required threshold of 0.5.

## Pipelines

Pipelines are used to streamline the process of transforming data, fitting the model, and making predictions, thereby reducing overall runtime and increasing proficiency in developing machine learning models with Spark.

## Conclusion

We successfully demonstrated the application of Apache Spark ML for predicting the helpfulness rate of product reviews. The use of Spark ML Pipelines enhanced the efficiency and reproducibility of our machine learning process, resulting in a robust model capable of high accuracy predictions.