## Ambigious handwritten digits in the MNIST dataset

Using a convolutional neural network, by analysing where it struggled the most to classify handwritten digits we can gain insight to the most ambiguous digits in the dataset. Notebook `mnist_notebook.ipynb` steps through how to find these ambiguous digits and the results are saved in `imgs` where the filename is the index of the image in the test data set.

## Results

## Requirements

Located inside of `requirements.txt`. These are standard machine learning libraries.

## Questions

> Describe your model

This solution uses a convolutional nerual network as this is the best architecture to extract patterns from a visual input. When designing the model care was taken to not make the model too large (Too many layers) and overfit, nor too small and underfit. Numerious iterations were used until the final solution was found.

A dropout layer was used to reduce overfitting, and max pooling to reduce the dimesion size and extract higher level patterns.

> Analyse your results

The 10 images found are all very ambiguous which fits with my expectations. Most ambiguous was defined as "digits that the model classified incorrectly, but was most confident about" as these incorrect digits would most likely be outliers of the test dataset. Another potential definition was "digits that the model was least confident about" which is also explored in the notebook, again leading to ambiguous digits.

> Impact of the images and improvements

The impact of these ambiguous digits is small, shown directly by the model achieving 99.2% accuracy, thus this classifier is a successful digit classifier. However as this did not take too much time, to be the "best handwritten digit classifer on earth" more time should be taken. Perhaps feeding in these ambiguous digits to the model for a 2nd training could be used, as well as data augmentation on the digits (particularly the ambiguous digits) to create other copies which are similar to it, yet not identical. This way the model would have a larger dataset to learn from for the tricker digits to classify, improving its accuracy. 

## References
- [Original dataset](http://yann.lecun.com/exdb/mnist/)
- Numerous Stackoverflow pages for specific inquiries
