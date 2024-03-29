# DeblurGAN
[![forthebadge made-with-python](http://ForTheBadge.com/images/badges/made-with-python.svg)](https://www.python.org/)
[![forthebadge](https://forthebadge.com/images/badges/built-with-love.svg)](https://forthebadge.com)

<div align = center>
<img width="800" alt="image" src="https://github.com/dhruvpatel144/DeblurGAN/assets/76422222/5f92749f-39c8-4af8-a0b1-42615fc73180">
</div>

--------------------------------------------------------------------------------

This repository offers a comprehensive PyTorch-based implementation of the innovative research paper titled "Deep Generative Filter for Motion Deblurring," accessible at [link](https://openaccess.thecvf.com/content_ICCV_2017_workshops/papers/w43/Ramakrishnan_Deep_Generative_Filter_ICCV_2017_paper.pdf). Building upon the original model, we have integrated cutting-edge techniques to enhance its performance remarkably.

The model is designed to take a pair of blurred and deblurred images as input during training and produce the deblurred image for the unseen image fed during testing. By leveraging PyTorch's powerful capabilities, this implementation offers both reliability and flexibility, making it suitable for various motion deblurring applications. We have gone beyond the initial research to incorporate optimizations and improvements, ensuring the model's robustness and adaptability across different scenarios. 


## Features

1. In contrast to the VGG loss commonly used in generator networks, we employ the Learned Perceptual Image Patch Similarity (LPIPS) loss function in our approach, as it provides more accurate coverage of color contrast.

2. Implemented differential augmentation technique to ensure a consistent flow of gradients from the discriminator during training, preventing them from becoming zero and promoting effective learning and generalization of our model.

3. Incorporated WGAN loss as it introduces a gradient penalty to enforce the Lipschitz constraint on the discriminator. This helps to improve stability and convergence of training process.

Feel free to explore the code and experiment with different settings to achieve optimal results.

## How to Run the Code?

1. To train the model, execute the following command:
   ```shell
   python train.py
   ```
   This will initiate training and optimize the model parameters based on the provided dataset. Adjust the training settings and hyperparameters as needed.

2. To evaluate the performance of the trained model and generate various metrics, use the following command:
    ```shell
    python evaluate.py
    ```
    This will assess the model's performance on the test dataset and provide valuable metrics for analysis and comparison.

3. The additional files in the repository serve specific purposes:

    - **generator.py:** contains the code for the generator network responsible for motion deblurring.
    
    - **discriminator.py:** includes the code for the discriminator network used for adversarial training.
    
    - **utils.py:** provides utility functions and helper code used throughout the project.

