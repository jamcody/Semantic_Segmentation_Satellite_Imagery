# Semantic Segmentation of Satellite Imagery
he task is a semantic segmentation one requiring not only the prediction of of 26 different possible classes within an image but to generate masks to indicate where the classes exist within the images. Since the dataset is of images from Hurricane Harvey, the main objective would be to accurately determine segments of images that have been affected by flooding and identify the objects in the vicintiy of the flood. The project was a challenging one and a successful deployment could yield to an assistance in quicker indentification of flood zones to dispatch rescue teams.

## Project Content
1 - Understanding of the Class Distribution within the images

2 - Image Augmentation and Patching: Training Images are augmented using several techniques and split into segment patches

3 - Modeling, Evaluation, and Comparison: The model is trained using PSPNet and evalauted using a weighted multi-F1 dice score and Accuracy in Class Prediction

4- Demonstration of Algorithm: A few demonstration of the model's predictive capabilities compared to the True masks

## Results
A demonstration of the results can be found below. Each image (left) in the provided training set had an associated mask generated by humans (middle). The prediction of the model's mask can then also be visualized (right). The best model trained was a model with a PSP-Net architecture acheiving a F1 dice score of 74% on an unseen testing set. We can see that the model is able to correctly predict classers in general but fails to work with the finer details in an mask.

<img width="612" alt="image" src="https://user-images.githubusercontent.com/127489117/232487518-7f7fac2d-f231-4d30-b4fb-a2616b80f945.png">
