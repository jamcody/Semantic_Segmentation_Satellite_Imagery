# Semantic Segmentation of Satellite Imagery
The task is a semantic segmentation one requiring not only the prediction of of 27 different possible classes within an image but to generate masks to indicate where the classes exist within the images. Since the dataset is of images from Hurricane Harvey, the main objective would be to accurately determine segments of images that have been affected by flooding and identify the objects in the vicintiy of the flood. The project was a challenging one and a successful deployment could yield to an assistance in quicker indentification of flood zones to dispatch rescue teams.

## Project Content
1. Understanding of the Class Distribution within the images
2. Pre-processing I - new samples have been created for under represented classes
3. Pre-processing II - images and corresponding masks have been resized from 4000x3000 to 368x368 for faster processing
4. DataLoader - a custom implementation of DataLoaders allowed for uniform application of transformations (flips, rotations, altering brightness) to the images and corresponding masks
5. Model I - UNet has been built from scratch as a benchmark model
6. Model II - DeepLabv3+ architecture implemented from [segmentation models](https://github.com/qubvel/segmentation_models.pytorch) library
7. Model III - PSPNet architecture implemented from the same [segmentation models](https://github.com/qubvel/segmentation_models.pytorch) library
7. Training - models have been trained using Google Colab GPUs
- Loss function - CrossEntropy or Focal Loss
- Dynamic learning rate
- Adam optimizer
- Pre-trained encoder weights from imagenet
9. Evaluation - model performance was evaluated using multi-F1 dice score and Accuracy in Class Prediction
10. Results - the best model, DeepLabv3+, achieved **multi-F1 Dice Score of 0.7262** on 112 test images

## Results
A demonstration of the results can be found below. Each image (left) in the provided training set had an associated mask generated by humans (middle). The prediction of the best model's mask (DeepLabV3+) can then also be visualized (right). We can see that the model is able to correctly predict classers in general but fails to work with the finer details in an mask.

<img width="612" alt="image" src="https://user-images.githubusercontent.com/127489117/232487518-7f7fac2d-f231-4d30-b4fb-a2616b80f945.png">
