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
| ![](https://github.com/uluyek/Project3-CUDA-Path-Tracer/blob/main/img/BRDF%20Diffuse%20Demo.jpg) | ![](https://github.com/uluyek/Project3-CUDA-Path-Tracer/blob/main/img/Perfectly%20specular-reflective%20Demo.jpg) | ![](https://github.com/uluyek/Project3-CUDA-Path-Tracer/blob/main/img/Perfectly%20specular-reflective%20Demo.jpg) |

**Custom Scene:** 
| Undenoised Scene | Denoised Scene (Iteration 10) |  Denoised Scene (Iteration 100) | GBuffer |
|---------------|------------------|------------------|------------------|
| ![](https://github.com/uluyek/Project3-CUDA-Path-Tracer/blob/main/img/BRDF%20Diffuse%20Demo.jpg) | ![](https://github.com/uluyek/Project3-CUDA-Path-Tracer/blob/main/img/Perfectly%20specular-reflective%20Demo.jpg) | ![](https://github.com/uluyek/Project3-CUDA-Path-Tracer/blob/main/img/Perfectly%20specular-reflective%20Demo.jpg) | ![](https://github.com/uluyek/Project3-CUDA-Path-Tracer/blob/main/img/Perfectly%20specular-reflective%20Demo.jpg) |

## Performance Analysis:

**Filter Size Analysis:** 
| Filter Size 10 | Filter Size 25 | Filter Size 50 | Filter Size 75 |
|---------------|------------------|------------------|------------------|
| ![](https://github.com/uluyek/Project3-CUDA-Path-Tracer/blob/main/img/BRDF%20Diffuse%20Demo.jpg) | ![](https://github.com/uluyek/Project3-CUDA-Path-Tracer/blob/main/img/Perfectly%20specular-reflective%20Demo.jpg) | ![](https://github.com/uluyek/Project3-CUDA-Path-Tracer/blob/main/img/Perfectly%20specular-reflective%20Demo.jpg) | ![](https://github.com/uluyek/Project3-CUDA-Path-Tracer/blob/main/img/Perfectly%20specular-reflective%20Demo.jpg) |

**Material Analysis:** 
| Diffuse White | Diffuse Red | Diffuse Green | Specular White | Mirror | Emissive |
|---------------|------------------|------------------|------------------|------------------|------------------|
| ![](https://github.com/uluyek/Project3-CUDA-Path-Tracer/blob/main/img/BRDF%20Diffuse%20Demo.jpg) | ![](https://github.com/uluyek/Project3-CUDA-Path-Tracer/blob/main/img/Perfectly%20specular-reflective%20Demo.jpg) | ![](https://github.com/uluyek/Project3-CUDA-Path-Tracer/blob/main/img/Perfectly%20specular-reflective%20Demo.jpg) | ![](https://github.com/uluyek/Project3-CUDA-Path-Tracer/blob/main/img/Perfectly%20specular-reflective%20Demo.jpg) | ![](https://github.com/uluyek/Project3-CUDA-Path-Tracer/blob/main/img/Perfectly%20specular-reflective%20Demo.jpg) | ![](https://github.com/uluyek/Project3-CUDA-Path-Tracer/blob/main/img/Perfectly%20specular-reflective%20Demo.jpg) |

**Scene Analysis:** 
| Cornell Undenoised | Cornell Denoised  | Cornell Ceiling Light Undenoised | Cornell Ceiling Light Denoised | 
|---------------|------------------|------------------|------------------|
| ![](https://github.com/uluyek/Project3-CUDA-Path-Tracer/blob/main/img/BRDF%20Diffuse%20Demo.jpg) | ![](https://github.com/uluyek/Project3-CUDA-Path-Tracer/blob/main/img/Perfectly%20specular-reflective%20Demo.jpg) | ![](https://github.com/uluyek/Project3-CUDA-Path-Tracer/blob/main/img/Perfectly%20specular-reflective%20Demo.jpg) | ![](https://github.com/uluyek/Project3-CUDA-Path-Tracer/blob/main/img/Perfectly%20specular-reflective%20Demo.jpg) | 



