# Image Watermarks are Removable using Controllable Regeneration from Clean Noise

Official implementation of an invisible image watermark removing method presented in the paper:

["Image Watermarks Are Removable using Controllable Regeneration from Clean Noise"](https://arxiv.org/abs/2410.05470) by Yepeng Liu, Yiren Song, Hai Ci, Yu Zhang, Haofan Wang, Mike Zheng Shou, and Yuheng Bu.

## Introduction

Image watermark techniques provide an effective way to assert ownership, deter misuse, and trace content sources, which has become increasingly essential in the era of large generative models. A critical attribute of watermark techniques is their robustness against various manipulations. In this paper, we introduce a watermark removal approach capable of effectively nullifying the state-of-the-art watermarking techniques. Our primary insight involves regenerating the watermarked image starting from a **clean Gaussian noise** via a controllable diffusion model, utilizing the extracted semantic and spatial features from the watermarked image. The semantic control adapter and the spatial control network are specifically trained to control the denoising process towards ensuring image quality and enhancing consistency between the cleaned image and the original watermarked image. To achieve a smooth trade-off between watermark removal performance and image consistency, we further propose an adjustable and controllable regeneration scheme. This scheme adds varying numbers of noise steps to the latent representation of the watermarked image, followed by a controlled denoising process starting from this noisy latent representation. As the number of noise steps increases, the latent representation progressively approaches clean Gaussian noise, facilitating the desired trade-off. We apply our watermark removal methods across various watermarking techniques, and the results demonstrate that our methods offer superior visual consistency/quality and enhanced watermark removal performance compared to existing regeneration approaches.


![overview](https://github.com/user-attachments/assets/0776782c-e5d7-4fea-9600-c3ec6f58c812)


### Installation
```
# download the code
git clone https://github.com/yepengliu/CtrlRegen.git
cd CtrlRegen

# install the required environment
pip install -r requirements.txt
```

Note: I am still working on it.
