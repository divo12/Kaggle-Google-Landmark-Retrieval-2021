# Kaggle-Google-Landmark-Retrieval-2021
The repository contains the solution of [Google Landmark Retrieval](https://www.kaggle.com/c/landmark-retrieval-2021)
## Problem Description
In this Competition,our goal was to retrieve relevant database images to a given query image (i.e., the model should retrieve database images containing the same landmark as the query).It involved the concept of Image Retrieval-a central problem in computer vision, relevant to many applications. The problem is usually posed as follows: given a query image, can you find similar images in a large database? This is especially important for query images containing landmarks, which accounts for a large portion of what people like to photograph.

This challenge uses Images from the Google Landmark Dataset(1.66 million images in 81k classes)which has images of landmarks from different angles and augmentations.The Dataset is available publicly as [Google Landmark Dataset](https://www.kaggle.com/c/landmark-retrieval-2021/data)
## Models implemented and experiments
We implemented the Triplet Net to construct embeddings of the anchor,positive and negative Images.For the Triplet Net,we used three lines of ResNet18 from the torchvision library and passed the anchor,positive and negative
We used the KNN to calculate the similarity between the query and the image dataset.We then take the label of the most similar class and print all the images similar to the given image.
## Results during test case
The model successfully retrieved all the similar images to the given query image.
We trained our model on the first 1000 classes and it worked pretty well for the first 1000 classes retrieving all the similar images.

## References
[Image Retrieval and Pattern Spotting using Siamese Network](https://arxiv.org/abs/1906.09513)
