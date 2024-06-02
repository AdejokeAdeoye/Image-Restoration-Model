# Image-Restoration-Model
I implemented an image restoration routine in Keras. This task included training a suitable neural network to restore corrupted images.

The tasks included;
1. Corrupting the CIFAR-10 dataset with 10, 50 and 100 number of blocks.
The number of the corrupted image blocks and size is specified by max_no_blocks and by block_size arguments respectively.
2. Implement a suitable model that restored the corrupted images.
3. Visualized some of the reconstructions of my model applied to the test dataset.

## About the data

The Canadian Institute For Advanced Research(CIFAR-10) dataset is a widely-used benchmark dataset in machine learning. It consists of 60,000 RGB images across 10 different classes. Each image is 32x32 pixels in size, and the dataset is divided into 50,000 training images and 10,000 test images. The 10 classes are: airplane, automobile, bird, cat, deer, dog, frog, horse, ship, and truck. The dataset is easy accessible in popular Python libraries like TensorFlow, PyTorch, and Keras.
