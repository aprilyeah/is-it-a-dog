# is it a dog???

For this project, I trained a Deep Neural Network for item/animal detection which is in the `make-model.ipynb` file. 

The aim is for the model to determine the probability that there is a dog label: 0 means a dog is not there, 1 means there is certainly a dog in there.


## What I have done:

1. Exploratory Data Analysis. I have showed the following:
    * The shape of the datasets
    * Rendered 5 images from each label to show that I know how to assemble an image from the dataset.
    * Chosen the `dog` label for probabability that the item/animal is there.

3. Data Processing. I have done the following:
    * Obtained training and testing dataset.
    * Ensured that there is no data imbalance between the images. In other words, there are 10000 data entries for training and 2000 for testing.

4. Data Modelling.
    * Created my Model.
        * Added hidden layers with their node counts and [activation types](https://keras.io/api/layers/activations/).
        * Chosen a [optimizer](https://keras.io/api/optimizers/), [loss](https://keras.io/api/losses/) and the [metric](https://keras.io/api/metrics/) for the output.
    * Fit my training and validation (testing in this case) dataset to the model.

5. Written a report about my model. This is in the `report.ipynb` file. The report includes the following:
    * Introduction.
        * Which label I picked for item/animal detection.
        * Why I picked the label.
    * Modelling Process.
        * What the shape of my model is.
        * The reason why I pick the selected loss and optimizer. 
    * Model Performance.
        * Shown the results of my training through the use of graphs. The graphs can be obtained from tensorboard. These include:
            * Accuracy
            * Loss
            * Validation Accuracy
            * Validation Loss
       *  Any comments about the results.
    * Conclusion.
        * Summary of the report without adding too much information.

6. Applied hyperparameter tuning to my model so I could find out the best possible model compilation parameters for accuracy.

7. Made a python application/function that can evaluate my model when given any PNG and/or JPEG image. This application is able to resize images to 32x32 before having the model evaluate said image.


# Required Software:
* [Python 3.9+](https://www.python.org/downloads/)
* Text Editor for Python ([Visual Studio Code](https://code.visualstudio.com/) with [Python extension](https://marketplace.visualstudio.com/items?itemName=ms-python.python) installed is recommended)

Recommended:
* [Anaconda](https://www.anaconda.com/)
* [Virtualenv](https://virtualenv.pypa.io/en/latest/installation.html)

# Setting Up:

Download the CIFAR-10 dataset from [here](https://www.cs.toronto.edu/~kriz/cifar.html) and place in your project directory. 

Install the libraries listed in the `requirements.txt` via the command:
```bash
pip install -r requirements.txt
```

Recommended to use a virtual environment either from either [virtualenv](https://docs.python.org/3/library/venv.html) or [anaconda](https://docs.conda.io/projects/conda/en/latest/user-guide/tasks/manage-environments.html). This setup helps isolate project dependencies from user dependencies as to avoid version conflicts.

# Tensorboard:
Run 
```
tensorboard --logdir output/logs/
``` 
to run [tensorboard](https://github.com/tensorflow/tensorboard/blob/master/README.md). The main points of interests are accuracy and loss graphs. The tensorboard application can then be opened via the site `http://localhost:6006/`.
