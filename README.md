<h1>Active Learning for Image Classification</h1>

Active learning approach for classifing images in the classic MNIST dataset, using Convolutional Neural Networks. 
The pool-based sampling approach is used, which consists in iteratively choosing samples to label according to some selection 
function. We then start with a training set that only contains $k$ images, and we iteratively increase it with the images that 
could be the most informative for the network, according to some criterion.

Three different selection functions are tested:

- Random selection: select $k$ random samples

- Entropy selection: select the $k$ samples with the highest entropy

- Margin selection: select the $k$ samples with the lowest difference between the two highest class probability.

Three exactly equal CNNs are trained with this three different approaches and are compared with the same CNN trained using
fully supervised learning. All three active models achieve really good performances (above 90% accuracy) using only 1000 4
training images (which is only the 14% of all available images in the dataset). This proves the strength of active learning!

## Data

You can download the MNIST dataset directly from Lecun's site [http://yann.lecun.com/exdb/mnist/] and place it inside the directory
/data/MNIST/

## Acknowledgments

This work is based on this excellent tutorial [https://towardsdatascience.com/active-learning-tutorial-57c3398e34d]
