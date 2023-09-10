# FocusGAN

Introduction:   

Visual saliency is the initial detection of the dominant parts of a visual scene to humans. It is the parts of a scene that grabs their attention. It is a subjective perceptual quality. Visual saliency detection has shown importance in advancing computer vision tasks such as object recognition and image segmentation. With as low as 20% attention modulation, a model using spatial attention and object recognition successively recognizes various objects in an image(Walther et al., 2002). The use of different saliency metrics and traditional convolutional neural networks lacks the ability to generalize well due to several reasons. The first being that saliency is subjective and thus difficult to be generated by the use of a metric. Secondly, the abundance of saliency metrics results in models trained on one metric having poor generalization to other metrics. A data-driven approach using saliency maps generated by eye trackers solves this problem. Furthermore, utilizing a GAN architecture with binary cross entropy loss to account for several parts of the image being salient has been proven to be effective(Pan et al., 2018). Our approach builds upon this by employing a UNet architecture in the generator of the SalGAN model. Employing a UNet architecture allows the decoder to generate saliency maps using features extracted in the encoding phase. This way, the encoder-decoder architecture in our generator preserves contextual information well which creates fine grain saliency maps. Our FocusGAN architecture outperformed the SalGAN architecture due to this. FocusGAN is able to generate saliency maps with a higher correlation coefficient. Furthermore, the generated saliency maps visually appeared closer to the ground truth saliency map.  


# FocusGAN Architecture 

![FocusGAN Architecture Diagram](images/Screen%20Shot%202023-09-10%20at%203.42.38%20PM.png) 

# CAT2000 Dataset 

![CAT2000 Dataset Visualization](images/Screen%20Shot%202023-09-10%20at%203.49.46%20PM.png)

# Results 

![Results Visualization](images/Screen%20Shot%202023-09-10%20at%203.43.59%20PM.png)


# References
1 - Pan, Junting, et al. "Salgan: Visual saliency prediction with generative adversarial networks." arXiv preprint arXiv:1701.01081 (2017).

2 - Bylinskii, Zoya, et al. "MIT Saliency Benchmark."

3- Borji, Ali, and Laurent Itti. "CAT2000: A Large Scale Fixation Dataset for Boosting Saliency Research." CVPR 2015 workshop on "Future of Datasets", 2015, arXiv preprint arXiv:1505.03581.
