CUDA Denoiser For CUDA Path Tracer
==================================

**University of Pennsylvania, CIS 565: GPU Programming and Architecture, Project 4**


* Keyu Lu
* Tested on: Windows 10, Dell Oman, NVIDIA GeForce RTX 2060

## Feature Implemented:
I implemented the A-trous wavelet denoising filter from the "Edge-Avoiding A-Trous Wavelet Transform for fast Global Illumination Filtering" (https://jo.dreggn.org/home/2010_atrous.pdf) paper by Dammertz, Sewtz, Hanika. 

## Denoising Results: 

**Cornell Ceiling Light Scene:** 
| Undenoised Scene | Denoised Scene | GBuffer |
|---------------|------------------|------------------|
| ![](https://github.com/uluyek/Project4-CUDA-Denoiser/blob/base-code/img/without%20Denoiser.jpg) | ![](https://github.com/uluyek/Project4-CUDA-Denoiser/blob/base-code/img/With%20Denoiser.jpg) | ![](https://github.com/uluyek/Project4-CUDA-Denoiser/blob/base-code/img/GBuffer.jpg) |

**Custom Scene:** 
| Undenoised Scene | Denoised Scene (Iteration 10) |  
|---------------|------------------|
| ![](https://github.com/uluyek/Project4-CUDA-Denoiser/blob/base-code/img/undenoised%20scene.jpg) | ![](https://github.com/uluyek/Project4-CUDA-Denoiser/blob/base-code/img/denoised%20scene.jpg) |
| Denoised Scene (Iteration 100) | GBuffer |
|------------------|------------------|
| ![](https://github.com/uluyek/Project4-CUDA-Denoiser/blob/base-code/img/Iteration%20100%20denoised.jpg) | ![](https://github.com/uluyek/Project4-CUDA-Denoiser/blob/base-code/img/2Gbuffer.jpg) |

## Performance Analysis:

**Filter Size Analysis:** 
| Filter Size 10 | Filter Size 25 | 
|---------------|------------------|
| ![](https://github.com/uluyek/Project4-CUDA-Denoiser/blob/base-code/img/filter%20size%2010.jpg) | ![](https://github.com/uluyek/Project4-CUDA-Denoiser/blob/base-code/img/filter%20size%2025.jpg) | 
| Filter Size 50 | Filter Size 75 | 
|------------------|------------------|
| ![](https://github.com/uluyek/Project4-CUDA-Denoiser/blob/base-code/img/filter%20size%2050.jpg) | ![](https://github.com/uluyek/Project4-CUDA-Denoiser/blob/base-code/img/filter%20size%2075.jpg) |

**Material Analysis:** 
| Diffuse White | Diffuse Red | Diffuse Green | 
|---------------|------------------|------------------|
| ![](https://github.com/uluyek/Project4-CUDA-Denoiser/blob/base-code/img/Diffuse%20white.jpg) | ![](https://github.com/uluyek/Project4-CUDA-Denoiser/blob/base-code/img/Diffuse%20red.jpg) | ![](https://github.com/uluyek/Project4-CUDA-Denoiser/blob/base-code/img/Diffuse%20Green.jpg) | 
| Specular White | Mirror | Emissive |
|------------------|------------------|------------------|
| ![](https://github.com/uluyek/Project4-CUDA-Denoiser/blob/base-code/img/Specular%20white.jpg) | ![](https://github.com/uluyek/Project4-CUDA-Denoiser/blob/base-code/img/mirror.jpg) | ![](https://github.com/uluyek/Project4-CUDA-Denoiser/blob/base-code/img/emissive%20.jpg) |

**Scene Analysis:** 
| Cornell Undenoised | Cornell Denoised  | 
|---------------|------------------|
| ![](https://github.com/uluyek/Project4-CUDA-Denoiser/blob/base-code/img/Cornell%20Undenoised.jpg) | ![](https://github.com/uluyek/Project4-CUDA-Denoiser/blob/base-code/img/Cornell%20denoised.jpg) |
| Cornell Ceiling Light Undenoised | Cornell Ceiling Light Denoised | 
|------------------|------------------|
|![](https://github.com/uluyek/Project4-CUDA-Denoiser/blob/base-code/img/without%20Denoiser.jpg) | ![](https://github.com/uluyek/Project4-CUDA-Denoiser/blob/base-code/img/With%20Denoiser.jpg) | 



