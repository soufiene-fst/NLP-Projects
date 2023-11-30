# BBC Headlines Multi-Label Classifier

This is a multi-label classifier built to classify BBC headlines into one or more of five categories: business, entertainment, politics, sport, and tech. 
The model is built using Embeddings, Recurrent Neural Networks (RNNs) like Long Short-Term Memory (LSTM) architecture. The project was developed in Python, 
using NLTK and TensorFlow libraries.


## Dataset
Two news article datasets, originating from BBC News, provided for use as benchmarks for machine learning research.
These datasets are made available for non-commercial and research purposes only. 

The dataset used for training the model consists of a collection of [BBC headlines from 2004 to 2005](http://mlg.ucd.ie/datasets/bbc.html). 
It contains a total of 2225 headlines, with each headline belonging to one or more of the five categories. The dataset is split into training 
and testing sets with a ratio of 80:20.

D. Greene and P. Cunningham. "Practical Solutions to the Problem of Diagonal Dominance in Kernel Document Clustering", Proc. ICML 2006. [[PDF]](http://mlg.ucd.ie/files/publications/greene06icml.pdf) [[BibTeX]](http://mlg.ucd.ie/files/bib/greene06icml.bib).

## Dependencies
This project requires the following dependencies:

* Python 3.x
* TensorFlow 2.x
* Keras
* NumPy
* NLTK

You can install these dependencies using pip.
```
pip install tensorflow keras numpy nltk
```

## Results
The model achieves an accuracy of 93.05% on the test set. The confusion matrix and classification report can be found in the Jupyter Notebook.

## Future Work
* Improve the accuracy of the model by fine-tuning the hyperparameters and using a larger dataset.
* Develop a web application for easy access to the model for healthcare professionals.
* Explore the use of other deep learning architectures for this task.
