In this notebook, I have outlined how sharpened cosine similarity could be utilised for image classification purposes while receiving a high validation accuracy. In past papers and examples on MNIST dataset sharpened cosine similarity (SCS) received a 80% accuracy. unable to break convolutional networks score. 

To overcome this, I used transfer learning: a method where large pre-trained image classification models (with frozen trainable layers) are utilised with a combination of custom architecture to train Image Classification models for downstream and domain specific tasks. 

I was able to achieve 98% training and 91% validation accuracy using the default architecture outlined by Ralph Pisoni, Optimizer and hyperparameters from AlexNet paper and without dropout layer. 

Making it a considerable achievement for Sharpened Cosine Similarity in Image Classification domain. 

### Dataset
In this experiment, a simple Alien vs Predator Kaggle dataset was utilised. Highlighting, it was a very noisy and small dataset. Making the results look more impressive. 

#### Implementing Sharpened Cosine layers
I had used the Keras edition scs that was available on Ralph Pisoni and brohrer’s blog and repository respectively. With a combination of Brohrer’s MaxAbsPool layer. 

Although a significant contribution was writing a python library to wrap these layers. available: https://pypi.org/project/sharpcosine/0.1.1/

### Experiment
It was a straightforward experiment where I had utilised a combination of pretrained ResNet architecture and Ralph’s custom SCS architecture. 

Highlight: Choosing the optimizer and hyperparameters was  a choice, I was inspired from the original AlexNet paper.

Although, I did not divide the learning rate by 10 after a certain period of time like AlexNet authors for simplicity sake. 

#### Results
It is quite evident from looking at the Jupyter Notebook. Where I reached a staggering 91% validation accuracy without using cross-validation. Noting, no activation function and fancy layers were utilised in the custom architecture. 

#### Credits
1. https://github.com/brohrer/sharpened-cosine-similarity
2. https://www.rpisoni.dev/posts/cossim-convolution-part2/

```
@misc{sleepingcat4-resnet-scs,
  author       = {sleepingcat4},
  title        = {resnet-scs},
  howpublished = {\url{https://github.com/sleepingcat4/resnet-scs}},
  year         = {2023},
  note         = {GitHub repository},
}
```
