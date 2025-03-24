# Brain Tumor Detection
Building a detection model using a convolutional neural network in Tensorflow & Keras.<br>
Used a brain MRI images data founded on Kaggle. You can find it [here](https://www.kaggle.com/datasets/masoudnickparvar/brain-tumor-mri-dataset).<br>

**About the data:**<br>
The dataset contains 4 folders. For this test only two folder is used glicoma tumor and no tumor.

## Data Augmentation:

**Why did I use data augmentation?**

Since this is a small dataset, There wasn't enough examples to train the neural network. Also, data augmentation was useful in taclking the data imbalance issue in the data.<br>

Further explanations are found in the notebook.

## Data Split:

The data was split in the following way:
1. 70% of the data for training.
2. 50% of the data for validation.
3. 50% of the data for testing.

# Training the model
The model was trained for 30 epochs and these are the loss & accuracy plots:


![Loss plot](loss.PNG)


![Accuracy plot](acc.PNG)

# Results

Now, the best model (the one with the best validation accuracy) detects brain tumor with:<br>

**91.2%** accuracy on the **test set**.<br>
These resutls are very good considering that the data is balanced.

**Performance table of the best model:**

| <!-- -->  | Validation set | Test set |
| --------- | -------------- | -------- |
| Accuracy  | 91%            | 96%      |



# Final Notes

What's in the files?

1. The code in the IPython notebooks.
2. The arrangment of the dataset, you can remove it if you want try from begain.
3. The models are stored as *.model* files. They can be restored as follows:


```
from keras.models import load_model
model = load_model("bestmodel.h5")
```

> This code is test in colab, so if you want to try there, fix the path

***If you need any further help, please contract with me***


Contributes are welcome!
<br>Thank you!


