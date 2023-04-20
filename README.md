# land-use-classification
Classifying low resolution satelite images by use.

# Business case and Data
In this project, we worked on a land-use classification task using satellite images obtained through Landsat with a low spatial resolution. Landsat images are not tagged in anyway, so we will try to create a model to classify it for us. The dataset was obtained from <a href="https://www.kaggle.com/datasets/apollo2506/landuse-scene-classification">kaggle</a> who got it from UC Merced. We started by exploring the dataset and setting up a data pipeline using the Keras ImageDataGenerator and flow_from_dataframe functions to load and augment the images.

# Methods
We then trained a simple convolutional neural network (CNN) model on the augmented data and evaluated its performance on the test set. We found that the CNN model achieved a test accuracy of around 84%.

To improve the performance of the model, we then created a new ResNet50-based model using transfer learning. We loaded the pre-trained ResNet50 model, froze its layers, added new classification layers on top of the pre-trained layers, and trained the model on the augmented data. We found that the ResNet50-based model achieved much worse accuracy, so we stuck with the CNN model.

# Conclusions
Overall, we were able to successfully build and train a model for the land-use classification task and achieve reasonable performance on the test set.

Governmental agencies can use this to request specific types of images from NASA/USGS instead of just requesting specific locations, making it easier to conduct wide area audits and do industrial and infrastructure planning.

# Next steps
This model was trained on only one type of image from one satellite program. I would like to train on different sizes, resolutions, and sources of images going foward.

All files in this project are in the root directory, I am not pushing the data because it is large, but again, it can be found at kaggle.

├── data
├── .gitignore
├── README.md
├── Notebook.ipynb
└── Presentation.pdf
