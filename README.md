# AI_generated_Images_Classifier

Swayam Pal 
21411036
Bitgrit username - palswayam5

# Intro
In project I created a classifier that can distinguish between AI generated Images and the original Images.So it becomes one of classical problems of computer vision in which we have to correctly classify the images as being 0 or 1 (Binary Classification).

# So I have used :-
1.ResNet50 (one of the famous CNN Architecture)
2.Vision Transformers (Basis on the concept of Transformers).

# Vision Transformer (ViT)
1. In ViT, the input image is divided into small patches, which are treated as individual tokens.
2. These patches are then flattened into a sequence and fed into the Transformer model.
3.  The Transformer encoder, which is the main component used in ViT, consists of stacked layers.
4.Each layer in the encoder contains two sub-components: the multi-head self-attention mechanism and the feed-forward neural network.
5.The self-attention mechanism computes attention weights for each patch, allowing the model to capture global relationships between different parts of the image.
6. The feed-forward neural network applies non-linear transformations to the patch embeddings, enabling the model to learn complex representations.

During training, ViT is typically pretrained on large-scale image datasets using self-supervised learning techniques. This pretraining phase helps the model learn useful visual features and general representations. The pretrained model can then be fine-tuned on specific computer vision tasks, such as image classification, object detection, or image segmentation.

Since we, had only a few thousand images as a training dataset this hindered the accuracy as well as the f1 score of the model a bit.
But still I managed to get an **f1 score of around 0.75** on 'bitgrit.com' using vision transformers.

# ResNet50

1. It is based on the residual block, which is the fundamental building block of the ResNet architecture.
2. A residual block includes a shortcut connection, also known as a skip connection, that allows the model to learn residual mappings by directly propagating the input to the output.
3. This skip connection enables the network to bypass and learn only the incremental changes in the intermediate layers, making it easier to train very deep networks. 
4. By mitigating the vanishing gradient problem, ResNet50 can effectively train deep models with improved performance.
5. The architecture of ResNet50 consists of multiple residual blocks, each containing convolutional layers, batch normalization, and ReLU activation functions.
6. The number of filters in the convolutional layers gradually increases, allowing the model to capture both low-level and high-level features in the input image.

Using this although I got an hight **f1_score of around 0.92** on my validation set but I could only get an f1 score of arounf 0.67 on bitgrit which can be explained by the fact that test set had very few number of images which were real and also the final results are still not out yet these f1 scores are based upon only the 60% of the submission data.
