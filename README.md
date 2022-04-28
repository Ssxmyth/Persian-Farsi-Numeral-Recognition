# Persian-Farsi-Numeral-Recognition
A Jupyter-Notebook (Python) to recognize handwritten images of Persian-Farsi numerals and translate them into their English equivalent. It uses a Convolutional Neural Network trained using the dataset provided by Tarbiat Modarres University and Hoda Systems Corporation. This was done as a proof of concept for a BSCS capstone project. This project used the open source project "Hoda Dataset Reader" created by Amir Saniyan to extra the images from the original .cdb file and save them into a numpy array. 

The "Descriptive Analysis" file in the "Main" folder shows 25 examples of images from the dataset, shows a bargraph of the frequency of each number (6000 each), and finally a Principal Component Analysis(PCA). A PCA is a dimensionality-reduction method that is supposed to transform a large set of variables into a smaller ones that still contains most of the information from the large set. Unfortunately my method of PCA was flawed and it showed all of the numbers grouped up together as similar, so I would need to reform the PCA to be more strict with its dimentionality reduction if I wanted the graph to be of use.

# Dataset
Hoda dataset is the first dataset of handwritten Farsi digits that has been developed during an MSc. project in Tarbiat Modarres University entitled: Recognizing Farsi Digits and Characters in SANJESH Registration Forms. This project has been carried out in cooperation with Hoda System Corporation. It was finished in summer 2005 under supervision of Prof. Ehsanollah Kabir. Samples of the dataset are handwritten characters extracted from about 12000 registration forms of university entrance examination in Iran. The dataset specifications is as follows:

Resolution of samples: 200 dpi\
Total samples: 102,352 samples\
Training samples: 60,000 samples\
Test samples: 20,000 samples\
Remaining samples: 22,352 samples

This project used the 60,000 training samples; 50,000 for training and the remaining 10,000 for testing the CNN.

# Instructions
The "Hoda Dataset Reader" folder contains the original program created by Amir Saniyan but repurposed to run in a Jupyter-Notebook. That is where the original dataset is saved in a .cdb format.

The dataset is saved in a 7zipped .npy file because Github's size constraints. The X_train_reg.7z is the zipped images and the Y_train_reg.7z contains the labels. You will have to either unzip the files or use the Hoda Dataset Reader to extract the images into .npy files. 

Ensure the unzipped files, test images, and main.ipynb are all in the same directory. The test images are seperate from the dataset, they are just random images off the internet. If everything is extracted and placed properly, when you run Main.ipynb then it should sucesfully complete. It will show images of the Persian numerals "7" and "4" as well as the English number "7" and "4" above it, showing that the CNN model was able to accurately predict on new data.

# Dependencies
  Python 3.8.10\
  Jupyter-Lab 3.2.5\
  Tensorflow 2.7.0\
  Numpy\
  Matplotlib\
  OpenCV\
  SkLearn\
  Pandas\
  Seaborn 
