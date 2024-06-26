# Awesome Evaluation of Visual Generation

[![Visitor](https://hits.seeyoufarm.com/api/count/incr/badge.svg?url=https%3A%2F%2Fgithub.com%2Fziqihuangg%2FAwesome-Evaluation-of-Visual-Generation&count_bg=%23FFA500&title_bg=%23555555&icon=&icon_color=%23E7E7E7&title=visitors&edge_flat=false)](https://hits.seeyoufarm.com)

*This repository collects methods for evaluating visual generation.*

![overall_structure](./figures/fig_teaser_combined.jpg)

## Overview

### What You'll Find Here

Within this repository, we collect works that aim to answer some critical questions in the field of evaluating visual generation, such as:

- **Model Evaluation**: How does one determine the quality of a specific image or video generation model?
- **Sample/Content Evaluation**: What methods can be used to evaluate the quality of a particular generated image or video?
- **User Control Consistency Evaluation**: How to tell how well the generated images and videos align with the user controls or inputs?

### Updates

This repository is updated periodically. If you have suggestions for additional resources, updates on methodologies, or fixes for expiring links, please feel free to do any of the following:
- raise an [Issue](https://github.com/ziqihuangg/Awesome-Evaluation-of-Visual-Generation/issues),
- nominate awesome related works with [Pull Requests](https://github.com/ziqihuangg/Awesome-Evaluation-of-Visual-Generation/pulls),
- We are also contactable via email (`ZIQI002 at e dot ntu dot edu dot sg`).

### Table of Contents
- [1. Evaluation Metrics of Generative Models](#1.)
  - [1.1. Evaluation Metrics of Image Generation](#1.1.)
  - [1.2. Evaluation Metrics of Video Generation](#1.2.)
  - [1.3. Evaluation Metrics for Latent Representation](#1.3.)
- [2. Evaluation Metrics of Condition Consistency](#2.)
  - [2.1 Evaluation Metrics of Multi-Modal Condition Consistency](#2.1.)
  - [2.2. Evaluation Metrics of Image Similarity](#2.2.)
- [3. Evaluation Systems of Generative Models](#3.)
  - [3.1. Evaluation of Unconditional Image Generation](#3.1.)
  - [3.2. Evaluation of Text-to-Image Generation](#3.2.)
  - [3.3. Evaluation of Text-Based Image Editing](#3.3.)
  - [3.4. Evaluation of Video Generation](#3.4.)
  - [3.5. Evaluation of Text-to-Motion Generation](#3.5.)
  - [3.6. Evaluation of Model Trustworthiness](#3.6.)
  - [3.7. Evaluation of Entity Relation](#3.7.)
- [4. Improving Visual Generation with Evaluation / Feedback / Reward](#4.)
- [5. Quality Assessment for AIGC](#5.)
- [6. Study and Rethinking](#6.)
- [7. Other Useful Resources](#7.)

<a name="1."></a>
## 1. Evaluation Metrics of Generative Models
<a name="1.1."></a>
### 1.1. Evaluation Metrics of Image Generation


| Metric | Paper | Code |
| -------- |  -------- |  ------- |
| Inception Score (IS) | [Improved Techniques for Training GANs](https://arxiv.org/abs/1606.03498) (NeurIPS 2016) |  |
| Fréchet Inception Distance (FID) | [GANs Trained by a Two Time-Scale Update Rule Converge to a Local Nash Equilibrium](https://arxiv.org/abs/1706.08500) (NeurIPS 2017) | [![Code](https://img.shields.io/github/stars/bioinf-jku/TTUR.svg?style=social&label=Official)](https://github.com/bioinf-jku/TTUR) [![Code](https://img.shields.io/github/stars/mseitzer/pytorch-fid.svg?style=social&label=PyTorch)](https://github.com/mseitzer/pytorch-fid) |
| Kernel Inception Distance (KID) | [Demystifying MMD GANs](https://arxiv.org/abs/1801.01401) (ICLR 2018) |   [![Code](https://img.shields.io/github/stars/toshas/torch-fidelity.svg?style=social&label=Unofficial)](https://github.com/toshas/torch-fidelity) [![Code](https://img.shields.io/github/stars/NVlabs/stylegan2-ada-pytorch.svg?style=social&label=Unofficial)](https://github.com/NVlabs/stylegan2-ada-pytorch/blob/main/metrics/kernel_inception_distance.py) 
| CLIP-FID | [The Role of ImageNet Classes in Fréchet Inception Distance](https://arxiv.org/abs/2203.06026) (ICLR 2023) | [![Code](https://img.shields.io/github/stars/kynkaat/role-of-imagenet-classes-in-fid.svg?style=social&label=Official)](https://github.com/kynkaat/role-of-imagenet-classes-in-fid)  [![Code](https://img.shields.io/github/stars/GaParmar/clean-fid.svg?style=social&label=Official)](https://github.com/GaParmar/clean-fid?tab=readme-ov-file#computing-clip-fid) |
| Precision-and-Recall |[Assessing Generative Models via Precision and Recall](https://arxiv.org/abs/1806.00035) (2018-05-31, NeurIPS 2018) <br> [Improved Precision and Recall Metric for Assessing Generative Models](https://arxiv.org/abs/1904.06991) (NeurIPS 2019) |    [![Code](https://img.shields.io/github/stars/msmsajjadi/precision-recall-distributions.svg?style=social&label=Official)](https://github.com/msmsajjadi/precision-recall-distributions) [![Code](https://img.shields.io/github/stars/kynkaat/improved-precision-and-recall-metric.svg?style=social&label=OfficialTensowFlow)](https://github.com/kynkaat/improved-precision-and-recall-metric)   |
| Renyi Kernel Entropy (RKE) | [An Information-Theoretic Evaluation of Generative Models in Learning Multi-modal Distributions](https://openreview.net/forum?id=PdZhf6PiAb) (NeurIPS 2023) | [![Code](https://img.shields.io/github/stars/mjalali/renyi-kernel-entropy.svg?style=social&label=Official)](https://github.com/mjalali/renyi-kernel-entropy)   |
| CLIP Maximum Mean Discrepancy (CMMD) | [Rethinking FID: Towards a Better Evaluation Metric for Image Generation](https://arxiv.org/abs/2401.09603) (CVPR 2024) | [![Code](https://img.shields.io/github/stars/google-research/google-research.svg?style=social&label=Official)](https://github.com/google-research/google-research/tree/master/cmmd) |






+ [Global-Local Image Perceptual Score (GLIPS): Evaluating Photorealistic Quality of AI-Generated Images](https://arxiv.org/abs/2405.09426) (2024-05-15)

+ [Unifying and extending Precision Recall metrics for assessing generative models](https://arxiv.org/abs/2405.01611) (2024-05-02)

+ Virtual Classifier Error (VCE) from [Virtual Classifier: A Reversed Approach for Robust Image Evaluation](https://openreview.net/forum?id=IE6FbueT47) (2024-03-04)

+ [An Interpretable Evaluation of Entropy-based Novelty of Generative Models](https://arxiv.org/abs/2402.17287) (2024-02-27)

+ [Fréchet Wavelet Distance: A Domain-Agnostic Metric for Image Generation](https://arxiv.org/abs/2312.15289) (2023-12-23) 

+ [Attribute Based Interpretable Evaluation Metrics for Generative Models](https://arxiv.org/abs/2310.17261) (2023-10-26) 

+ [Training-Free Location-Aware Text-to-Image Synthesis](https://arxiv.org/abs/2304.13427) (2023-04-26)  

+ [LGSQE: Lightweight Generated Sample Quality Evaluatoin](https://arxiv.org/abs/2211.04590) (2022-11-08)

+ [Layout-Bridging Text-to-Image Synthesis](https://arxiv.org/abs/2208.06162) (2022-08-12)

+ [Rarity Score: A New Metric to Evaluate the Uncommonness of Synthesized Images](https://arxiv.org/abs/2206.08549) (2022-06-17) 
[![Code](https://img.shields.io/github/stars/hichoe95/Rarity-Score.svg?style=social&label=Official)](https://github.com/hichoe95/Rarity-Score)

+ [Mutual Information Divergence: A Unified Metric for Multimodal Generative Models](https://arxiv.org/abs/2205.13445) (2022-05-25)
[![Code](https://img.shields.io/github/stars/naver-ai/mid.metric.svg?style=social&label=Official)](https://github.com/naver-ai/mid.metric)
> **_NOTE:_** evaluates text to image and utilizes vision language models (VLM)


+ [TREND: Truncated Generalized Normal Density Estimation of Inception Embeddings for GAN Evaluation](https://arxiv.org/abs/2104.14767) (2021-04-30, ECCV 2022)

+ CFID from [Conditional Frechet Inception Distance](https://arxiv.org/abs/2103.11521) (2021-03-21)
[![Code](https://img.shields.io/github/stars/Michael-Soloveitchik/CFID.svg?style=social&label=Official)](https://github.com/Michael-Soloveitchik/CFID/)
[![Website](https://img.shields.io/badge/Website-9cf)](https://michael-soloveitchik.github.io/CFID/)

+ [Random Network Distillation as a Diversity Metric for Both Image and Text Generation](https://arxiv.org/abs/2010.06715) (2020-10-13)
> **_NOTE:_** RND metric introduced

+ [The Vendi Score: A Diversity Evaluation Metric for Machine Learning](https://arxiv.org/abs/2210.02410) (2022-10-05) 
[![Code](https://img.shields.io/github/stars/vertaix/Vendi-Score.svg?style=social&label=Official)](https://github.com/vertaix/Vendi-Score)

+ CIS from [Evaluation Metrics for Conditional Image Generation](https://arxiv.org/abs/2004.12361) (2020-04-26)

+ [Text-To-Image Synthesis Method Evaluation Based On Visual Patterns](https://arxiv.org/abs/1911.00077) (2020-04-09) 

+ [Cscore: A Novel No-Reference Evaluation Metric for Generated Images](https://dl.acm.org/doi/abs/10.1145/3373509.3373546) (2020-03-25)  


+ SceneFID from [Object-Centric Image Generation from Layouts](https://arxiv.org/abs/2003.07449) (2020-03-16)

+ [Reliable Fidelity and Diversity Metrics for Generative Models](https://arxiv.org/abs/2002.09797) (2020-02-23, ICML 2020)  
[![Code](https://img.shields.io/github/stars/clovaai/generative-evaluation-prdc.svg?style=social&label=Official)](https://github.com/clovaai/generative-evaluation-prdc) 

+ [Effectively Unbiased FID and Inception Score and where to find them](https://arxiv.org/abs/1911.07023) (2019-11-16, CVPR 2020)  
[![Code](https://img.shields.io/github/stars/mchong6/FID_IS_infinity.svg?style=social&label=Official)](https://github.com/mchong6/FID_IS_infinity)

+ [On the Evaluation of Conditional GANs](https://arxiv.org/abs/1907.08175) (2019-07-11)
> **_NOTE:_** Fréchet Joint Distance (FJD), which is able to assess image quality, conditional consistency, and intra-conditioning diversity within a single metric.

+ [A domain agnostic measure for monitoring and evaluating GANs](https://arxiv.org/abs/1811.05512) (2018-11-13) 



<a name="1.2."></a>
### 1.2. Evaluation Metrics of Video Generation


| Metric | Paper | Code |
| -------- |  -------- |  ------- |
| FID-vid | [GANs Trained by a Two Time-Scale Update Rule Converge to a Local Nash Equilibrium](https://arxiv.org/abs/1706.08500) (NeurIPS 2017) |  |
| Fréchet Video Distance (FVD) | [Towards Accurate Generative Models of Video: A New Metric & Challenges](https://arxiv.org/abs/1812.01717) (arXiv 2018) <br> [FVD: A new Metric for Video Generation](https://openreview.net/forum?id=rylgEULtdN) (2019-05-04)  <i> (Note: ICLR 2019 Workshop DeepGenStruct Program Chairs)</i>| [![Code](https://img.shields.io/github/stars/songweige/TATS.svg?style=social&label=Unofficial)](https://github.com/songweige/TATS/blob/main/tats/fvd/fvd.py) |

<a name="1.3."></a>
### 1.3. Evaluation Metrics for Latent Representation

+ Linear Separability & Perceptual Path Length (PPL) from [A Style-Based Generator Architecture for Generative Adversarial Networks](https://arxiv.org/abs/1812.04948) (2020-01-09)
[![Code](https://img.shields.io/github/stars/NVlabs/stylegan.svg?style=social&label=Official)](https://github.com/NVlabs/stylegan?tab=readme-ov-file)
[![Code](https://img.shields.io/github/stars/NVlabs/ffhq-dataset.svg?style=social&label=Official)](https://github.com/NVlabs/ffhq-dataset)


<a name="2."></a>
## 2. Evaluation Metrics of Condition Consistency
<a name="2.1."></a>
### 2.1 Evaluation Metrics of Multi-Modal Condition Consistency


| Metric | Condition | Pipeline | Code | References | 
| -------- |  -------- |  ------- | -------- |  -------- |  
| CLIP Score (`a.k.a.` CLIPSIM) | Text | cosine similarity between the CLIP image and text embeddings |  [![Code](https://img.shields.io/github/stars/openai/CLIP.svg?style=social&label=CLIP)](https://github.com/openai/CLIP) [PyTorch Lightning](https://lightning.ai/docs/torchmetrics/stable/multimodal/clip_score.html) | [CLIP Paper](https://arxiv.org/abs/2103.00020) (ICML 2021). Metrics first used in [CLIPScore Paper](https://arxiv.org/abs/2104.08718) (arXiv 2021) and [GODIVA Paper](https://arxiv.org/abs/2104.14806) (arXiv 2021) applies it in video evaluation. |
| Mask Accuracy | Segmentation Mask | predict the segmentatio mask, and compute pixel-wise accuracy against the ground-truth segmentation mask | any segmentation method for your setting |
| DINO Similarity | Image of a Subject (human / object *etc*) | cosine similarity between the DINO embeddings of the generated image and the condition image | [![Code](https://img.shields.io/github/stars/facebookresearch/dino.svg?style=social&label=DINO)](https://github.com/facebookresearch/dino) | [DINO paper](https://arxiv.org/abs/2104.14294). Metric is proposed in [DreamBooth](https://arxiv.org/abs/2208.12242).
<!-- | Identity Consistency | Image of a Face |  | - | -->

<!-- 
Papers for CLIP Similarity:
[Learning Transferable Visual Models From Natural Language Supervision](https://arxiv.org/abs/2103.00020) (ICML 2021), [CLIPScore: A Reference-free Evaluation Metric for Image Captioning](https://arxiv.org/abs/2104.08718) (arXiv 2021), [GODIVA: Generating Open-DomaIn Videos from nAtural Descriptions](https://arxiv.org/abs/2104.14806) (arXiv 2021) | [![Code](https://img.shields.io/github/stars/openai/CLIP.svg?style=social&label=CLIP)](https://github.com/openai/CLIP) [PyTorch Lightning](https://lightning.ai/docs/torchmetrics/stable/multimodal/clip_score.html) -->

+ Manipulation Direction (MD) from [Manipulation Direction: Evaluating Text-Guided Image Manipulation Based on Similarity between Changes in Image and Text Modalities](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC10675000/) (2023-11-20)

+ [Semantic Similarity Distance: Towards better text-image consistency metric in text-to-image generation](https://www-sciencedirect-com.remotexs.ntu.edu.sg/science/article/pii/S0031320323005812?via%3Dihub) (2022-12-02)

+ [On the Evaluation of Conditional GANs](https://arxiv.org/abs/1907.08175) (2019-07-11)
> **_NOTE:_** Fréchet Joint Distance (FJD), which is able to assess image quality, conditional consistency, and intra-conditioning diversity within a single metric.

+ Visual-Semantic (VS) Similarity from [Photographic Text-to-Image Synthesis with a Hierarchically-nested Adversarial Network](https://arxiv.org/abs/1802.09178v2) (2018-12-26)
[![Code](https://img.shields.io/github/stars/ypxie/HDGan.svg?style=social&label=Official)](https://github.com/ypxie/HDGan)
[![Website](https://img.shields.io/badge/Website-9cf)](https://alexhex7.github.io/2018/05/30/Photographic%20Text-to-Image%20Synthesis%20with%20a%20Hierarchically-nested%20Adversarial%20Network/)


+ [Semantically Invariant Text-to-Image Generation](https://arxiv.org/abs/1809.10274) (2018-09-06)
[![Code](https://img.shields.io/github/stars/sxs4337/MMVR.svg?style=social&label=Official)](https://github.com/sxs4337/MMVR)
    > <i>Note: They evaluate image-text similarity via image captioning</i>

+ [Inferring Semantic Layout for Hierarchical Text-to-Image Synthesis](https://arxiv.org/abs/1801.05091v2) (2018-01-16) 
    > <i>Note: An object detector based metric is proposed.</i>



<a name="2.2."></a>
### 2.2. Evaluation Metrics of Image Similarity

| Metrics | Paper | Code |
| -------- |  -------- |  ------- |
| Learned Perceptual Image Patch Similarity (LPIPS) | [The Unreasonable Effectiveness of Deep Features as a Perceptual Metric](https://arxiv.org/abs/1801.03924) (2018-01-11) (CVPR 2018) | [![Code](https://img.shields.io/github/stars/richzhang/PerceptualSimilarity.svg?style=social&label=Official)](https://github.com/richzhang/PerceptualSimilarity) [![Website](https://img.shields.io/badge/Website-9cf)](https://richzhang.github.io/PerceptualSimilarity/) |
| Structural Similarity Index (SSIM) | [Image quality assessment: from error visibility to structural similarity](https://ieeexplore.ieee.org/document/1284395) (TIP 2004) |   [![Code](https://img.shields.io/github/stars/open-mmlab/mmagic.svg?style=social&label=MMEditing)](https://github.com/open-mmlab/mmagic/blob/main/tests/test_evaluation/test_metrics/test_ssim.py) [![Code](https://img.shields.io/github/stars/Po-Hsun-Su/pytorch-ssim.svg?style=social&label=Unofficial)](https://github.com/Po-Hsun-Su/pytorch-ssim) |
| Peak Signal-to-Noise Ratio (PSNR) | - |   [![Code](https://img.shields.io/github/stars/open-mmlab/mmagic.svg?style=social&label=MMEditing)](https://github.com/open-mmlab/mmagic/blob/main/tests/test_evaluation/test_metrics/test_psnr.py) |
| Multi-Scale Structural Similarity Index (MS-SSIM) | [Multiscale structural similarity for image quality assessment](https://ieeexplore.ieee.org/document/1292216) (SSC 2004) | [PyTorch-Metrics](https://lightning.ai/docs/torchmetrics/stable/image/multi_scale_structural_similarity.html#:~:text=Compute%20MultiScaleSSIM%2C%20Multi%2Dscale%20Structural,details%20at%20different%20resolution%20scores.&text=a%20method%20to%20reduce%20metric%20score%20over%20labels.) |
| Feature Similarity Index (FSIM) | [FSIM: A Feature Similarity Index for Image Quality Assessment](https://ieeexplore.ieee.org/document/5705575) (TIP 2011) | [![Code](https://img.shields.io/github/stars/mikhailiuk/pytorch-fsim.svg?style=social&label=Unofficial)](https://github.com/mikhailiuk/pytorch-fsim)



The community has also been using [DINO](https://arxiv.org/abs/2104.14294) or [CLIP](https://arxiv.org/abs/2103.00020) features to measure the semantic similarity of two images / frames.


There are also recent works on new methods to measure visual similarity (more will be added):

+ [DreamSim: Learning New Dimensions of Human Visual Similarity using Synthetic Data](https://arxiv.org/abs/2306.09344) (2023-06-15)  
  [![Code](https://img.shields.io/github/stars/ssundaram21/dreamsim.svg?style=social&label=Official)](https://github.com/ssundaram21/dreamsim)
  [![Website](https://img.shields.io/badge/Website-9cf)](https://dreamsim-nights.github.io)
  
<a name="3."></a>
## 3. Evaluation Systems of Generative Models

<a name="3.1."></a>
### 3.1. Evaluation of Unconditional Image Generation

+ [Anomaly Score: Evaluating Generative Models and Individual Generated Images based on Complexity and Vulnerability](https://arxiv.org/abs/2312.10634) (2023-12-17, CVPR 2024)  

+ [HYPE: A Benchmark for Human eYe Perceptual Evaluation of Generative Models](https://arxiv.org/abs/1904.01121) (2019-04-01)  
[![Website](https://img.shields.io/badge/Website-9cf)](https://stanfordhci.github.io/gen-eval/)




<a name="3.2."></a>
### 3.2. Evaluation of Text-to-Image Generation

+ [GenAI Arena: An Open Evaluation Platform for Generative Models](https://arxiv.org/abs/2406.04485) (2024-06-06) 
[![Code](https://img.shields.io/github/stars/TIGER-AI-Lab/VideoGenHub.svg?style=social&label=Official)](https://github.com/TIGER-AI-Lab/VideoGenHub?tab=readme-ov-file)

+ [A-Bench: Are LMMs Masters at Evaluating AI-generated Images?](https://arxiv.org/abs/2406.03070) (2024-06-05)  
  [![Code](https://img.shields.io/github/stars/Q-Future/A-Bench.svg?style=social&label=Official)](https://github.com/Q-Future/A-Bench)  [![Website](https://img.shields.io/badge/Website-9cf)](https://a-bench-sjtu.github.io/)  [![Hugging Face](https://img.shields.io/badge/%F0%9F%A4%97%20Hugging%20Face-blue)](https://huggingface.co/datasets/q-future/A-Bench)

+ Multidimensional Preference Score from [Learning Multi-dimensional Human Preference for Text-to-Image Generation](https://arxiv.org/abs/2405.14705) (2024-05-23)

+ [Evolving Storytelling: Benchmarks and Methods for New Character Customization with Diffusion Models](https://arxiv.org/abs/2405.11852) (2024-05-20) 
> **_NOTE:_** NewEpisode benchmark introduced

+ [Training-free Subject-Enhanced Attention Guidance for Compositional Text-to-image Generation](https://arxiv.org/abs/2405.06948) (2024-05-11) 
> **_NOTES:_** GroundingScore metric introduced

+ [Revisiting Text-to-Image Evaluation with Gecko: On Metrics, Prompts, and Human Ratings](https://arxiv.org/abs/2404.16820) (2024-04-25)  

+ [Multimodal Large Language Model is a Human-Aligned Annotator for Text-to-Image Generation](https://arxiv.org/abs/2404.15100) (2024-04-23)  


+ [TAVGBench: Benchmarking Text to Audible-Video Generation](https://arxiv.org/abs/2404.14381) (2024-04-22)  
  [![Code](https://img.shields.io/github/stars/OpenNLPLab/TAVGBench.svg?style=social&label=Official)](https://github.com/OpenNLPLab/TAVGBench)

+ [Object-Attribute Binding in Text-to-Image Generation: Evaluation and Control](https://arxiv.org/abs/2404.13766) (2024-04-21)  

+ [GenAI-Bench: A Holistic Benchmark for Compositional Text-to-Visual Generation](https://openreview.net/forum?id=hJm7qnW3ym) (2024-04-09)
  > <i>Note: GenAI-Bench was introduced in a previous paper 'Evaluating Text-to-Visual Generation with Image-to-Text Generation'</i>

+ Detect-and-Compare from [Identity Decoupling for Multi-Subject Personalization of Text-to-Image Models](https://arxiv.org/abs/2404.04243) (2024-04-05) 
[![Code](https://img.shields.io/github/stars/agwmon/MuDI.svg?style=social&label=Official)](https://github.com/agwmon/MuDI)
[![Website](https://img.shields.io/badge/Website-9cf)](https://mudi-t2i.github.io/)


+ [Evaluating Text-to-Visual Generation with Image-to-Text Generation](https://arxiv.org/abs/2404.01291) (2024-04-01)  
  [![Code](https://img.shields.io/github/stars/linzhiqiu/t2v_metrics.svg?style=social&label=Official)](https://github.com/linzhiqiu/t2v_metrics)
  [![Website](https://img.shields.io/badge/Website-9cf)](https://linzhiqiu.github.io/papers/vqascore)

+ [Measuring Style Similarity in Diffusion Models](https://arxiv.org/abs/2404.01292) (2024-04-01)  
  [![Code](https://img.shields.io/github/stars/learn2phoenix/CSD.svg?style=social&label=Official)](https://github.com/learn2phoenix/CSD)

+ [FlashEval: Towards Fast and Accurate Evaluation of Text-to-image Diffusion Generative Models](https://arxiv.org/abs/2403.16379) (2024-03-25)

+ [Exploring GPT-4 Vision for Text-to-Image Synthesis Evaluation](https://openreview.net/forum?id=xmQoodG82a) (2024-03-20)

+ [Evaluating Text-to-Image Generative Models: An Empirical Study on Human Image Synthesis](https://arxiv.org/abs/2403.05125) (2024-03-08) 

+ [An Information-Theoretic Evaluation of Generative Models in Learning Multi-modal Distributions](https://openreview.net/forum?id=PdZhf6PiAb) (2024-02-13)  
  [![Code](https://img.shields.io/github/stars/mjalali/renyi-kernel-entropy.svg?style=social&label=Official)](https://github.com/mjalali/renyi-kernel-entropy)

+ [CAS: A Probability-Based Approach for Universal Condition Alignment Score](https://openreview.net/forum?id=E78OaH2s3f) (2024-01-16)  
  [![Code](https://img.shields.io/github/stars/unified-metric/unified_metric.svg?style=social&label=Official)](https://github.com/unified-metric/unified_metric)  [![Website](https://img.shields.io/badge/Website-9cf)](https://unified-metric.github.io/)
    > <i>Note: Condition alignment of text-to-image, {instruction, image}-to-image, edge-/scribble-to-image, and text-to-audio</i>

+ [EmoGen: Emotional Image Content Generation with Text-to-Image Diffusion Models](https://arxiv.org/abs/2401.04608) (2024-01-09) 
[![Code](https://img.shields.io/github/stars/JingyuanYY/EmoGen.svg?style=social&label=Official)](https://github.com/JingyuanYY/EmoGen)
> **_NOTE:_** emotion accuracy, semantic clarity and semantic diversity are not core contributions of this paper

+ [VIEScore: Towards Explainable Metrics for Conditional Image Synthesis Evaluation](https://arxiv.org/abs/2312.14867) (2023-12-22)  
  [![Code](https://img.shields.io/github/stars/TIGER-AI-Lab/VIEScore.svg?style=social&label=Official)](https://github.com/TIGER-AI-Lab/VIEScore)  [![Website](https://img.shields.io/badge/Website-9cf)](https://tiger-ai-lab.github.io/VIEScore/)

+ [Stellar: Systematic Evaluation of Human-Centric Personalized Text-to-Image Methods](https://arxiv.org/abs/2312.06116) (2023-12-11)  
  [![Code](https://img.shields.io/github/stars/stellar-gen-ai/stellar-metrics.svg?style=social&label=Official)](https://github.com/stellar-gen-ai/stellar-metrics)
  [![Website](https://img.shields.io/badge/Website-9cf)](https://stellar-gen-ai.github.io/)


+ [A Contrastive Compositional Benchmark for Text-to-Image Synthesis: A Study with Unified Text-to-Image Fidelity Metrics](https://arxiv.org/abs/2312.02338) (2023-12-04)  
  [![Code](https://img.shields.io/github/stars/zhuxiangru/Winoground-T2I.svg?style=social&label=Official)](https://github.com/zhuxiangru/Winoground-T2I)


+ [SelfEval: Leveraging the discriminative nature of generative models for evaluation](https://arxiv.org/abs/2311.10708) (2023-11-17)


+ [GPT-4V(ision) as a Generalist Evaluator for Vision-Language Tasks](https://arxiv.org/abs/2311.01361) (2023-11-02)

+ [Davidsonian Scene Graph: Improving Reliability in Fine-grained Evaluation for Text-to-Image Generation](https://arxiv.org/abs/2310.18235) (2023-10-27, ICLR 2024)  
  [![Code](https://img.shields.io/github/stars/j-min/DSG.svg?style=social&label=Official)](https://github.com/j-min/DSG)
  [![Website](https://img.shields.io/badge/Website-9cf)](https://google.github.io/dsg/)

+ [DEsignBench: Exploring and Benchmarking DALL-E 3 for Imagining Visual Design](https://arxiv.org/abs/2310.15144) (2023-10-23)  
  [![Website](https://img.shields.io/badge/Website-9cf)](https://design-bench.github.io)
  

+ [GenEval: An Object-Focused Framework for Evaluating Text-to-Image Alignment](https://arxiv.org/abs/2310.11513) (2023-10-17)  
  [![Code](https://img.shields.io/github/stars/djghosh13/geneval.svg?style=social&label=Official)](https://github.com/djghosh13/geneval)  

+ [Hypernymy Understanding Evaluation of Text-to-Image Models via WordNet Hierarchy](https://arxiv.org/abs/2310.09247) (2023-10-13)  
  [![Code](https://img.shields.io/github/stars/yandex-research/text-to-img-hypernymy.svg?style=social&label=Official)](https://github.com/yandex-research/text-to-img-hypernymy)  

+ [SingleInsert: Inserting New Concepts from a Single Image into Text-to-Image Models for Flexible Editing](https://arxiv.org/abs/2310.08094) (2023-10-12)  
  [![Code](https://img.shields.io/github/stars/JarrentWu1031/SingleInsert.svg?style=social&label=Official)](https://github.com/JarrentWu1031/SingleInsert)  [![Website](https://img.shields.io/badge/Website-9cf)](https://jarrentwu1031.github.io/SingleInsert-web/)
  > <i> Note: New Metric: Editing Success Rate </i>

+ [ImagenHub: Standardizing the evaluation of conditional image generation models](https://arxiv.org/abs/2310.01596) (2023-10-02)  
  [![Code](https://img.shields.io/github/stars/TIGER-AI-Lab/ImagenHub.svg?style=social&label=Official)](https://github.com/TIGER-AI-Lab/ImagenHub) [![Website](https://img.shields.io/badge/Website-9cf)](https://tiger-ai-lab.github.io/ImagenHub/) 
  [![Hugging Face](https://img.shields.io/badge/%F0%9F%A4%97%20Hugging%20Face-blue)](https://huggingface.co/ImagenHub)

+ [Navigating Text-To-Image Customization: From LyCORIS Fine-Tuning to Model Evaluation](https://arxiv.org/abs/2309.14859) (2023-09-26, ICLR 2024)  
  [![Code](https://img.shields.io/github/stars/KohakuBlueleaf/LyCORIS.svg?style=social&label=Official)](https://github.com/KohakuBlueleaf/LyCORIS)

+ Concept Score from [Text-to-Image Generation for Abstract Concepts](https://paperswithcode.com/paper/text-to-image-generation-for-abstract) (2023-09-26) 

+ [OpenLEAF: Open-Domain Interleaved Image-Text Generation and Evaluation](https://openreview.net/forum?id=SeiL55hCnu) (2023-09-23) 
  [![Hugging Face](https://img.shields.io/badge/%F0%9F%A4%97%20Hugging%20Face-blue)](https://huggingface.co/ImagenHub) [GenAI-Arena](https://huggingface.co/papers/2310.07749)
  > <i>Note: Evaluates task of image and text generation</i>
  

<!-- + [JourneyDB: A Benchmark for Generative Image Understanding](https://arxiv.org/abs/2307.00716) (2023-07-03, NeurIPS 2023)  
  [![Code](https://img.shields.io/github/stars/JourneyDB/JourneyDB.svg?style=social&label=Official)](https://github.com/JourneyDB/JourneyDB)
  [![Website](https://img.shields.io/badge/Website-9cf)](https://journeydb.github.io/) -->


+ LEICA from [Likelihood-Based Text-to-Image Evaluation with Patch-Level Perceptual and Semantic Credit Assignment](https://arxiv.org/abs/2308.08525) (2023-08-16)
  
+ [Let's ViCE! Mimicking Human Cognitive Behavior in Image Generation Evaluation](https://arxiv.org/abs/2307.09416) (2023-07-18)  

+ [T2I-CompBench: A Comprehensive Benchmark for Open-world Compositional Text-to-image Generation](https://arxiv.org/abs/2307.06350) (2023-07-12)  
  [![Code](https://img.shields.io/github/stars/Karine-Huang/T2I-CompBench.svg?style=social&label=Official)](https://github.com/Karine-Huang/T2I-CompBench)
  [![Website](https://img.shields.io/badge/Website-9cf)](https://karine-h.github.io/T2I-CompBench/)

+ [TIAM -- A Metric for Evaluating Alignment in Text-to-Image Generation](https://arxiv.org/abs/2307.05134) (2023-07-11, WACV 2024)  
  [![Code](https://img.shields.io/github/stars/grimalPaul/TIAM.svg?style=social&label=Official)](https://github.com/grimalPaul/TIAM)

+ [Divide, Evaluate, and Refine: Evaluating and Improving Text-to-Image Alignment with Iterative VQA Feedback](https://arxiv.org/abs/2307.04749) (2023-07-10, NeurIPS 2023)  
  [![Code](https://img.shields.io/github/stars/1jsingh/Divide-Evaluate-and-Refine.svg?style=social&label=Official)](https://github.com/1jsingh/Divide-Evaluate-and-Refine) [![Website](https://img.shields.io/badge/Website-9cf)](https://1jsingh.github.io/divide-evaluate-and-refine)

+ [Human Preference Score v2: A Solid Benchmark for Evaluating Human Preferences of Text-to-Image Synthesis](https://arxiv.org/abs/2306.09341) (2023-06-15)  
  [![Code](https://img.shields.io/github/stars/tgxs002/HPSv2.svg?style=social&label=Official)](https://github.com/tgxs002/HPSv2)

+ [ConceptBed: Evaluating Concept Learning Abilities of Text-to-Image Diffusion Models](https://arxiv.org/abs/2306.04695) (2023-06-07, AAAI 2024)  
  [![Code](https://img.shields.io/github/stars/ConceptBed/evaluations.svg?style=social&label=Official)](https://github.com/ConceptBed/evaluations) [![Website](https://img.shields.io/badge/Website-9cf)](https://conceptbed.github.io/) [![Hugging Face](https://img.shields.io/badge/%F0%9F%A4%97%20Hugging%20Face-blue)](https://huggingface.co/spaces/mpatel57/ConceptBed)

+ [Visual Programming for Text-to-Image Generation and Evaluation](https://arxiv.org/abs/2305.15328) (2023-05-24, NeurIPS 2023)  
  [![Code](https://img.shields.io/github/stars/aszala/VPEval.svg?style=social&label=Official)](https://github.com/aszala/VPEval) [![Website](https://img.shields.io/badge/Website-9cf)](https://vp-t2i.github.io/)

+ [LLMScore: Unveiling the Power of Large Language Models in Text-to-Image Synthesis Evaluation](https://arxiv.org/abs/2305.11116) (2023-05-18, NeurIPS 2023)  
  [![Code](https://img.shields.io/github/stars/YujieLu10/LLMScore.svg?style=social&label=Official)](https://github.com/YujieLu10/LLMScore)

+ [X-IQE: eXplainable Image Quality Evaluation for Text-to-Image Generation with Visual Large Language Models](https://arxiv.org/abs/2305.10843) (2023-05-18)  
  [![Code](https://img.shields.io/github/stars/Schuture/Benchmarking-Awesome-Diffusion-Models.svg?style=social&label=Official)](https://github.com/Schuture/Benchmarking-Awesome-Diffusion-Models)

+ [What You See is What You Read? Improving Text-Image Alignment Evaluation](https://arxiv.org/abs/2305.10400) (2023-05-17, NeurIPS 2023)  
  [![Code](https://img.shields.io/github/stars/yonatanbitton/wysiwyr.svg?style=social&label=Official)](https://github.com/yonatanbitton/wysiwyr) [![Website](https://img.shields.io/badge/Website-9cf)](https://wysiwyr-itm.github.io/) [![Hugging Face](https://img.shields.io/badge/%F0%9F%A4%97%20Hugging%20Face-blue)](https://huggingface.co/datasets/yonatanbitton/SeeTRUE) 

+ [Pick-a-Pic: An Open Dataset of User Preferences for Text-to-Image Generation](https://arxiv.org/abs/2305.01569) (2023-05-02)  
  [![Code](https://img.shields.io/github/stars/yuvalkirstain/PickScore.svg?style=social&label=Official)](https://github.com/yuvalkirstain/PickScore)

+ [HRS-Bench: Holistic, Reliable and Scalable Benchmark for Text-to-Image Models](https://arxiv.org/abs/2304.05390) (2023-04-11, ICCV 2023)  
  [![Code](https://img.shields.io/github/stars/eslambakr/HRS_benchmark.svg?style=social&label=Official)](https://github.com/eslambakr/HRS_benchmark)  [![Website](https://img.shields.io/badge/Website-9cf)](https://eslambakr.github.io/hrsbench.github.io/)

+ [Human Preference Score: Better Aligning Text-to-Image Models with Human Preference](https://arxiv.org/abs/2303.14420) (2023-03-25, ICCV 2023)  
  [![Code](https://img.shields.io/github/stars/tgxs002/align_sd.svg?style=social&label=Official)](https://github.com/tgxs002/align_sd)
  [![Website](https://img.shields.io/badge/Website-9cf)](https://tgxs002.github.io/align_sd_web/)

+ [TIFA: Accurate and Interpretable Text-to-Image Faithfulness Evaluation with Question Answering](https://arxiv.org/abs/2303.11897) (2023-03-21, ICCV 2023)  
  [![Code](https://img.shields.io/github/stars/Yushi-Hu/tifa.svg?style=social&label=Official)](https://github.com/Yushi-Hu/tifa) [![Website](https://img.shields.io/badge/Website-9cf)](https://tifa-benchmark.github.io/)

+ [Is This Loss Informative? Faster Text-to-Image Customization by Tracking Objective Dynamics](https://arxiv.org/abs/2302.04841) (2023-02-09) 
[![Code](https://img.shields.io/github/stars/yandex-research/DVAR.svg?style=social&label=Official)](https://github.com/yandex-research/DVAR)
> **_NOTE:_** an evaluation approach for early stopping criterion in T2I customization

+ [Benchmarking Spatial Relationships in Text-to-Image Generation](https://arxiv.org/abs/2212.10015) (2022-12-20)  
  [![Code](https://img.shields.io/github/stars/microsoft/VISOR.svg?style=social&label=Official)](https://github.com/microsoft/VISOR)

+ MMI and MOR from from [Benchmarking Robustness of Multimodal Image-Text Models under Distribution Shift](https://arxiv.org/abs/2212.08044) (2022-12-15)
[![Website](https://img.shields.io/badge/Website-9cf)](https://mmrobustness.github.io/)

+ [TeTIm-Eval: a novel curated evaluation data set for comparing text-to-image models](https://arxiv.org/abs/2212.07839) (2022-12-15)  


+ [Human Evaluation of Text-to-Image Models on a Multi-Task Benchmark](https://arxiv.org/abs/2211.12112) (2022-11-22)

+ [Re-Imagen: Retrieval-Augmented Text-to-Image Generator](https://arxiv.org/abs/2209.14491) (2022-09-29)

+ [Vision-Language Matching for Text-to-Image Synthesis via Generative Adversarial Networks](https://arxiv.org/abs/2208.09596) (2022-08-20)

+ [Scaling Autoregressive Models for Content-Rich Text-to-Image Generation](https://arxiv.org/abs/2206.10789) (2022-06-22)
 [![Code](https://img.shields.io/github/stars/google-research/parti.svg?style=social&label=Official)](https://github.com/google-research/parti) [![Website](https://img.shields.io/badge/Website-9cf)](https://sites.research.google/parti/)

+ [GR-GAN: Gradual Refinement Text-to-image Generation](https://arxiv.org/abs/2205.11273) (2022-05-23) 
[![Code](https://img.shields.io/github/stars/BoO-18/GR-GAN.svg?style=social&label=Unofficial)](https://github.com/BoO-18/GR-GAN)
> **_NOTE:_** new metric Cross-Model Distance introduced 

+ [DrawBench from Photorealistic Text-to-Image Diffusion Models with Deep Language Understanding](https://arxiv.org/abs/2205.11487) (2022-05-23)
[![Website](https://img.shields.io/badge/Website-9cf)](https://imagen.research.google/)

+ [StyleT2I: Toward Compositional and High-Fidelity Text-to-Image Synthesis](https://arxiv.org/abs/2203.15799) (2022-03-29, CVPR 2024)
 [![Code](https://img.shields.io/github/stars/zhihengli-UR/StyleT2I.svg?style=social&label=Official)](https://github.com/zhihengli-UR/StyleT2I)


+ [Benchmark for Compositional Text-to-Image Synthesis](https://openreview.net/forum?id=bKBhQhPeKaF) (2021-07-29)  
  [![Code](https://img.shields.io/github/stars/Seth-Park/comp-t2i-dataset.svg?style=social&label=Official)](https://github.com/Seth-Park/comp-t2i-dataset)

+ [TISE: Bag of Metrics for Text-to-Image Synthesis Evaluation](https://arxiv.org/abs/2112.01398) (2021-12-02, ECCV 2022)  
[![Code](https://img.shields.io/github/stars/VinAIResearch/tise-toolbox.svg?style=social&label=Official)](https://github.com/VinAIResearch/tise-toolbox)

+ [Leveraging Visual Question Answering to Improve Text-to-Image Synthesis](https://arxiv.org/abs/2010.14953) (2020-10-28)

+ [Improving Generation and Evaluation of Visual Stories via Semantic Consistency](https://arxiv.org/abs/2105.10026) (2021-05-20)
[![Code](https://img.shields.io/github/stars/adymaharana/StoryViz.svg?style=social&label=Official)](https://github.com/adymaharana/StoryViz)

+ [Semantic Object Accuracy for Generative Text-to-Image Synthesis](https://arxiv.org/abs/1910.13321) (2019-10-29)  
  [![Code](https://img.shields.io/github/stars/tohinz/semantic-object-accuracy-for-generative-text-to-image-synthesis.svg?style=social&label=Official)](https://github.com/tohinz/semantic-object-accuracy-for-generative-text-to-image-synthesis?tab=readme-ov-file)  [![Website](https://img.shields.io/badge/Website-9cf)](https://www.tobiashinz.com/2019/10/30/semantic-object-accuracy-for-generative-text-to-image-synthesis)


<a name="3.3."></a>
### 3.3. Evaluation of Text-Based Image Editing

+ [MultiEdits: Simultaneous Multi-Aspect Editing with Text-to-Image Diffusion Models](https://arxiv.org/abs/2406.00985) (2024-06-03)
 [![Website](https://img.shields.io/badge/Website-9cf)](https://mingzhenhuang.com/projects/MultiEdits.html) [![Hugging Face](https://img.shields.io/badge/%F0%9F%A4%97%20Hugging%20Face-blue)](https://huggingface.co/datasets/UB-CVML-Group/PIE_Bench_pp)

+ [HQ-Edit: A High-Quality Dataset for Instruction-based Image Editing](https://arxiv.org/abs/2404.09990) (2024-04-15) 
[![Code](https://img.shields.io/github/stars/UCSC-VLAA/HQ-Edit.svg?style=social&label=Official)](https://github.com/UCSC-VLAA/HQ-Edit)
[![Website](https://img.shields.io/badge/Website-9cf)](https://thefllood.github.io/HQEdit_web/) 
[![Hugging Face Code](https://img.shields.io/badge/Hugging%20Face-Code-blue)](https://huggingface.co/datasets/UCSC-VLAA/HQ-Edit)

+ [FlexEdit: Flexible and Controllable Diffusion-based Object-centric Image Editing](https://arxiv.org/abs/2403.18605) (2024-03-27) 
[![Website](https://img.shields.io/badge/Website-9cf)](https://flex-edit.github.io/) 
> **_NOTE:_** novel automatic mask-based evaluation metric tailored to various object-centric editing scenarios

+ TransformationOriented Paired Benchmark from [InstructBrush: Learning Attention-based Instruction Optimization for Image Editing](https://arxiv.org/abs/2403.18660) (2024-03-27)
[![Code](https://img.shields.io/github/stars/RoyZhao926/InstructBrush.svg?style=social&label=Official)](https://github.com/RoyZhao926/InstructBrush)
  [![Website](https://img.shields.io/badge/Website-9cf)](https://royzhao926.github.io/InstructBrush/)

+ ImageNet Concept Editing Benchmark from [Editing Massive Concepts in Text-to-Image Diffusion Models](https://arxiv.org/abs/2403.13807) (2024-03-20) 
[![Code](https://img.shields.io/github/stars/SilentView/EMCID.svg?style=social&label=Official)](https://github.com/SilentView/EMCID)
[![Website](https://img.shields.io/badge/Website-9cf)](https://silentview.github.io/EMCID/)


+ [Diffusion Model-Based Image Editing: A Survey](https://arxiv.org/abs/2402.17525) (2024-02-27)  
  [![Code](https://img.shields.io/github/stars/SiatMMLab/Awesome-Diffusion-Model-Based-Image-Editing-Methods.svg?style=social&label=Official)](https://github.com/SiatMMLab/Awesome-Diffusion-Model-Based-Image-Editing-Methods)

+ [LEDITS++: Limitless Image Editing using Text-to-Image Models](https://arxiv.org/abs/2311.16711) (2023-11-28)  
  [![Hugging Face Code](https://img.shields.io/badge/Hugging%20Face-Code-blue)](https://huggingface.co/spaces/editing-images/leditsplusplus/tree/main)  [![Website](https://img.shields.io/badge/Website-9cf)](https://leditsplusplus-project.static.hf.space/index.html)  [![Hugging Face Space](https://img.shields.io/badge/Hugging%20Face-Space-blue)](https://huggingface.co/spaces/editing-images/leditsplusplus)

+ [Emu Edit: Precise Image Editing via Recognition and Generation Tasks](https://arxiv.org/abs/2311.10089) (2023-11-16)
[![Hugging Face Code](https://img.shields.io/badge/Hugging%20Face-Code-blue)](https://huggingface.co/datasets/facebook/emu_edit_test_set)
[![Website](https://img.shields.io/badge/Website-9cf)](https://emu-edit.metademolab.com/)


+ [EditVal: Benchmarking Diffusion Based Text-Guided Image Editing Methods](https://arxiv.org/abs/2310.02426) (2023-10-03)  
  [![Code](https://img.shields.io/github/stars/deep-ml-research/editval_code.svg?style=social&label=Official)](https://github.com/deep-ml-research/editval_code)
  [![Website](https://img.shields.io/badge/Website-9cf)](https://deep-ml-research.github.io/editval/)

+ PIE-Bench from [Direct Inversion: Boosting Diffusion-based Editing with 3 Lines of Code](https://arxiv.org/abs/2310.01506) (2023-10-02) 
[![Code](https://img.shields.io/github/stars/cure-lab/PnPInversion.svg?style=social&label=Official)](https://github.com/cure-lab/PnPInversion)
  [![Website](https://img.shields.io/badge/Website-9cf)](https://cure-lab.github.io/PnPInversion/)

+ [MagicBrush: A Manually Annotated Dataset for Instruction-Guided Image Editing](https://arxiv.org/abs/2306.10012) (2023-06-16) 
[![Code](https://img.shields.io/github/stars/OSU-NLP-Group/MagicBrush.svg?style=social&label=Official)](https://github.com/OSU-NLP-Group/MagicBrush)
  [![Website](https://img.shields.io/badge/Website-9cf)](https://osu-nlp-group.github.io/MagicBrush/)
  [![Hugging Face Code](https://img.shields.io/badge/Hugging%20Face-Code-blue)](https://huggingface.co/datasets/osunlp/MagicBrush)
  > <i>Note: dataset only</i>

  
+ [Imagen Editor and EditBench: Advancing and Evaluating Text-Guided Image Inpainting](https://arxiv.org/abs/2212.06909) (2022-12-13, CVPR 2023)  
  [![Website](https://img.shields.io/badge/Website-9cf)](https://research.google/blog/imagen-editor-and-editbench-advancing-and-evaluating-text-guided-image-inpainting/)

+ [Imagic: Text-Based Real Image Editing with Diffusion Models](https://arxiv.org/abs/2210.09276) (2022-10-17)  
  [![Code](https://img.shields.io/github/stars/imagic-editing/imagic-editing.github.io.svg?style=social&label=Official)](https://github.com/imagic-editing/imagic-editing.github.io/tree/main/tedbench)  [![Website](https://img.shields.io/badge/Website-9cf)](https://imagic-editing.github.io/)  [![Hugging Face](https://img.shields.io/badge/Hugging%20Face-blue)](https://huggingface.co/datasets/bahjat-kawar/tedbench)

+ [Predict, Prevent, and Evaluate: Disentangled Text-Driven Image Manipulation Empowered by Pre-Trained Vision-Language Model](https://arxiv.org/abs/2111.13333) (2021-11-26)
[![Code](https://img.shields.io/github/stars/zipengxuc/PPE.github.io.svg?style=social&label=Official)](https://github.com/zipengxuc/PPE)

+ [Knowledge-Driven Generative Adversarial Network for Text-to-Image Synthesis](https://ieeexplore.ieee.org/abstract/document/9552559) (2021-09-29)
 [![Code](https://img.shields.io/github/stars/pengjunn/KD-GAN.svg?style=social&label=Official)](https://github.com/pengjunn/KD-GAN)

+ [ManiGAN: Text-Guided Image Manipulation](https://arxiv.org/abs/1912.06203) (2019-12-12) 
[![Code](https://img.shields.io/github/stars/mrlibw/ManiGAN.svg?style=social&label=Official)](https://github.com/mrlibw/ManiGAN)
> **_NOTE:_** manipulative precision metric introduced 

<a name="3.4."></a>
### 3.4. Evaluation of Video Generation

#### 3.4.1. Evaluation of Text-to-Video Generation
+ [VideoPhy: Evaluating Physical Commonsense for Video Generation](https://arxiv.org/abs/2406.03520v1) (2024-06-05) 
  [![Website](https://img.shields.io/badge/Website-9cf)](https://videophy.github.io)
  [![Code](https://img.shields.io/github/stars/Hritikbansal/videophy.svg?style=social&label=Official)](https://github.com/Hritikbansal/videophy)

+ [The Lost Melody: Empirical Observations on Text-to-Video Generation From A Storytelling Perspective](https://arxiv.org/abs/2405.08720) (2024-05-13)  
  > <i>Note: New evaluation framework T2Vid2T, Evaluation for storytelling aspects of videos</i>

+ [Exposing AI-generated Videos: A Benchmark Dataset and a Local-and-Global Temporal Defect Based Detection Method](https://arxiv.org/abs/2405.04133) (2024-05-07)  

+ [Sora Detector: A Unified Hallucination Detection for Large Text-to-Video Models](https://arxiv.org/abs/2405.04180) (2024-05-07) 
[![Website](https://img.shields.io/badge/Website-9cf)](https://bytez.com/docs/arxiv/2405.04180/llm)
  > <i>Note: hallucination detection</i>

+ [Exploring AIGC Video Quality: A Focus on Visual Harmony, Video-Text Consistency and Domain Distribution Gap](https://arxiv.org/abs/2404.13573) (2024-04-21)  
  [![Code](https://img.shields.io/github/stars/Coobiw/TriVQA.svg?style=social&label=Official)](https://github.com/Coobiw/TriVQA)

+ [Subjective-Aligned Dataset and Metric for Text-to-Video Quality Assessment](https://arxiv.org/abs/2403.11956) (2024-03-18)  
  [![Code](https://img.shields.io/github/stars/QMME/T2VQA.svg?style=social&label=Official)](https://github.com/QMME/T2VQA)

+ [A dataset of text prompts, videos and video quality metrics from generative text-to-video AI models](https://www.sciencedirect.com/science/article/pii/S2352340924004839) (2024-02-22)  
  [![Code](https://img.shields.io/github/stars/Chiviya01/Evaluating-Text-to-Video-Models.svg?style=social&label=Official)](https://github.com/Chiviya01/Evaluating-Text-to-Video-Models)

+ [Sora Generates Videos with Stunning Geometrical Consistency](https://arxiv.org/abs/2402.17403) (2024-02-27)  
  [![Code](https://img.shields.io/github/stars/meteorshowers/Sora-Generates-Videos-with-Stunning-Geometrical-Consistency.svg?style=social&label=Official)](https://github.com/meteorshowers/Sora-Generates-Videos-with-Stunning-Geometrical-Consistency)
  [![Website](https://img.shields.io/badge/Website-9cf)](https://sora-geometrical-consistency.github.io)


+ [STREAM: Spatio-TempoRal Evaluation and Analysis Metric for Video Generative Models](https://arxiv.org/abs/2403.09669) (2024-01-30)  
  [![Code](https://img.shields.io/github/stars/pro2nit/STREAM.svg?style=social&label=Official)](https://github.com/pro2nit/STREAM)


+ [Towards A Better Metric for Text-to-Video Generation](https://arxiv.org/abs/2401.07781) (2024-01-15)  
  [![Code](https://img.shields.io/github/stars/showlab/T2VScore.svg?style=social&label=Official)](https://github.com/showlab/T2VScore) [![Website](https://img.shields.io/badge/Website-9cf)](https://showlab.github.io/T2VScore/) [![Hugging Face](https://img.shields.io/badge/%F0%9F%A4%97%20Hugging%20Face-blue)](https://huggingface.co/datasets/jayw/t2v-gen-eval)

+ [PEEKABOO: Interactive Video Generation via Masked-Diffusion](https://arxiv.org/abs/2312.07509) (2023-12-12)  
  [![Code](https://img.shields.io/github/stars/microsoft/Peekaboo.svg?style=social&label=Official)](https://github.com/microsoft/Peekaboo)
  > <i> Note: Benchmark for interactive video generation </i>

+ [VBench: Comprehensive Benchmark Suite for Video Generative Models](https://arxiv.org/abs/2311.17982) (2023-11-29)  
  [![Code](https://img.shields.io/github/stars/Vchitect/VBench.svg?style=social&label=Official)](https://github.com/Vchitect/VBench) [![Website](https://img.shields.io/badge/Website-9cf)](https://vchitect.github.io/VBench-project/) [![Hugging Face](https://img.shields.io/badge/%F0%9F%A4%97%20Hugging%20Face-blue)](https://huggingface.co/spaces/Vchitect/VBench_Leaderboard)

+ [SmoothVideo: Smooth Video Synthesis with Noise Constraints on Diffusion Models for One-shot Video Tuning](https://arxiv.org/abs/2311.17536) (2023-11-29) 
[![Code](https://img.shields.io/github/stars/SPengLiang/SmoothVideo.svg?style=social&label=Official)](https://github.com/SPengLiang/SmoothVideo)


+ [FETV: A Benchmark for Fine-Grained Evaluation of Open-Domain Text-to-Video Generation](https://arxiv.org/abs/2311.01813) (2023-11-03)  
  [![Code](https://img.shields.io/github/stars/llyx97/FETV.svg?style=social&label=Official)](https://github.com/llyx97/FETV)

+ [EvalCrafter: Benchmarking and Evaluating Large Video Generation Models](https://arxiv.org/abs/2310.11440) (2023-10-17)  
  [![Code](https://img.shields.io/github/stars/EvalCrafter/EvalCrafter.svg?style=social&label=Official)](https://github.com/EvalCrafter/EvalCrafter)
  [![Website](https://img.shields.io/badge/Website-9cf)](https://evalcrafter.github.io) [![Hugging Face Dataset](https://img.shields.io/badge/Hugging%20Face-Dataset-blue)](https://huggingface.co/datasets/RaphaelLiu/EvalCrafter_T2V_Dataset) [![Hugging Face Space](https://img.shields.io/badge/Hugging%20Face-Space-blue)](https://huggingface.co/spaces/AILab-CVC/EvalCrafter)

+ [Measuring the Quality of Text-to-Video Model Outputs: Metrics and Dataset](https://arxiv.org/abs/2309.08009) (2023-09-14)

+ [StoryBench: A Multifaceted Benchmark for Continuous Story Visualization](https://arxiv.org/abs/2308.11606) (2023-08-22, NeurIPS 2023)  
  [![Code](https://img.shields.io/github/stars/google/storybench.svg?style=social&label=Official)](https://github.com/google/storybench)

+ [CelebV-Text: A Large-Scale Facial Text-Video Dataset](https://arxiv.org/abs/2303.14717) (2023-03-26, CVPR 2023)  
  [![Code](https://img.shields.io/github/stars/CelebV-Text/CelebV-Text.svg?style=social&label=Official)](https://github.com/CelebV-Text/CelebV-Text)  [![Website](https://img.shields.io/badge/Website-9cf)](https://celebv-text.github.io/)  

+ [Make It Move: Controllable Image-to-Video Generation with Text Descriptions](https://arxiv.org/abs/2112.02815) (2021-12-06, CVPR 2022)  
  [![Code](https://img.shields.io/github/stars/Youncy-Hu/MAGE.svg?style=social&label=Official)](https://github.com/Youncy-Hu/MAGE)

#### 3.4.2. Evaluation of Image-to-Video Generation

+ I2V-Bench from [ConsistI2V: Enhancing Visual Consistency for Image-to-Video Generation](https://arxiv.org/abs/2402.04324) (2024-02-06)  
  [![Code](https://img.shields.io/github/stars/TIGER-AI-Lab/ConsistI2V.svg?style=social&label=Official)](https://github.com/TIGER-AI-Lab/ConsistI2V) [![Website](https://img.shields.io/badge/Website-9cf)](https://tiger-ai-lab.github.io/ConsistI2V/) [![Hugging Face](https://img.shields.io/badge/%F0%9F%A4%97%20Hugging%20Face-blue)](https://huggingface.co/spaces/TIGER-Lab/ConsistI2V)

+ [AIGCBench: Comprehensive Evaluation of Image-to-Video Content Generated by AI](https://arxiv.org/abs/2401.01651) (2024-01-03)  
  [![Code](https://img.shields.io/github/stars/BenchCouncil/AIGCBench.svg?style=social&label=Official)](https://github.com/BenchCouncil/AIGCBench)
  [![Website](https://img.shields.io/badge/Website-9cf)](https://www.benchcouncil.org/AIGCBench/) [![Hugging Face](https://img.shields.io/badge/%F0%9F%A4%97%20Hugging%20Face-blue)](https://huggingface.co/datasets/stevenfan/AIGCBench_v1.0)

+ [VBench-I2V](https://github.com/Vchitect/VBench/tree/master/vbench2_beta_i2v) (2024-03) from [VBench: Comprehensive Benchmark Suite for Video Generative Models](https://arxiv.org/abs/2311.17982) (2023-11-29)  
  [![Code](https://img.shields.io/github/stars/Vchitect/VBench.svg?style=social&label=Official)](https://github.com/Vchitect/VBench)
  [![Website](https://img.shields.io/badge/Website-9cf)](https://vchitect.github.io/VBench-project/)

+ [A Benchmark for Controllable Text-Image-to-Video Generation](https://ieeexplore.ieee.org/abstract/document/10148799) (2023-06-12)


#### 3.4.3. Evaluation of Talking Face Generation

+ [OpFlowTalker: Realistic and Natural Talking Face Generation via Optical Flow Guidance](https://arxiv.org/abs/2405.14709) (2024-05-23)

+ [Audio-Visual Speech Representation Expert for Enhanced Talking Face Video Generation and Evaluation](https://arxiv.org/abs/2405.04327) (2024-05-07)  

+ [VASA-1: Lifelike Audio-Driven Talking Faces Generated in Real Time](https://arxiv.org/abs/2404.10667) (2024-04-16)
[![Website](https://img.shields.io/badge/Website-9cf)](https://www.microsoft.com/en-us/research/project/vasa-1/)
> **_NOTE:_** Contrastive Audio and Pose Pretraining (CAPP) score introduced

+ [THQA: A Perceptual Quality Assessment Database for Talking Heads](https://arxiv.org/abs/2404.09003) (2024-04-13)  
  [![Code](https://img.shields.io/github/stars/zyj-2000/THQA.svg?style=social&label=Official)](https://github.com/zyj-2000/THQA)

+ [A Comparative Study of Perceptual Quality Metrics for Audio-driven Talking Head Videos](https://arxiv.org/abs/2403.06421) (2024-03-11)  
  [![Code](https://img.shields.io/github/stars/zwx8981/ADTH-QA.svg?style=social&label=Official)](https://github.com/zwx8981/ADTH-QA)

+ [Seeing What You Said: Talking Face Generation Guided by a Lip Reading Expert](https://arxiv.org/abs/2303.17480) (2023-03-29, CVPR 2023)  
  [![Code](https://img.shields.io/github/stars/Sxjdwang/TalkLip.svg?style=social&label=Official)](https://github.com/Sxjdwang/TalkLip)

+ [Responsive Listening Head Generation: A Benchmark Dataset and Baseline](https://arxiv.org/abs/2112.13548) (2021-12-27, ECCV 2022)  
  [![Code](https://img.shields.io/github/stars/dc3ea9f/vico_challenge_baseline.svg?style=social&label=Official)](https://github.com/dc3ea9f/vico_challenge_baseline)  [![Website](https://img.shields.io/badge/Website-9cf)](https://project.mhzhou.com/vico/)

+ [What comprises a good talking-head video generation?: A Survey and Benchmark](https://arxiv.org/abs/2005.03201) (2020-05-07) 
[![Code](https://img.shields.io/github/stars/lelechen63/talking-head-generation-survey.svg?style=social&label=Official)](https://github.com/lelechen63/talking-head-generation-survey)

<a name="3.5."></a>
### 3.5. Evaluation of Text-to-Motion Generation

+ [MoDiPO: text-to-motion alignment via AI-feedback-driven Direct Preference Optimization](https://arxiv.org/abs/2405.03803) (2024-05-06)  

+ [What is the Best Automated Metric for Text to Motion Generation?](https://arxiv.org/abs/2309.10248) (2023-09-19) 

+ [Text-to-Motion Retrieval: Towards Joint Understanding of Human Motion Data and Natural Language](https://arxiv.org/abs/2305.15842) (2023-05-25)  [![Code](https://img.shields.io/github/stars/mesnico/text-to-motion-retrieval.svg?style=social&label=Official)](https://github.com/mesnico/text-to-motion-retrieval)

+ [Establishing a Unified Evaluation Framework for Human Motion Generation: A Comparative Analysis of Metrics](https://arxiv.org/abs/2405.07680) (2024-05-13) 
[![Code](https://img.shields.io/github/stars/MSD-IRIMAS/Evaluating-HMG.svg?style=social&label=Official)](https://github.com/MSD-IRIMAS/Evaluating-HMG)

+ [Evaluation of text-to-gesture generation model using convolutional neural network](https://www.sciencedirect.com/science/article/pii/S0893608022001198) (2021-10-11)
[![Code](https://img.shields.io/github/stars/GestureGeneration/text2gesture_cnn.svg?style=social&label=Official)](https://github.com/GestureGeneration/text2gesture_cnn)


<a name="3.6."></a>
### 3.6. Evaluation of Model Trustworthiness

#### 3.6.1. Evaluation of Visual-Generation-Model Trustworthiness

+ [AI-Face: A Million-Scale Demographically Annotated AI-Generated Face Dataset and Fairness Benchmark](https://arxiv.org/abs/2406.00783) (2024-06-02)  
  [![Code](https://img.shields.io/github/stars/Purdue-M2/AI-Face-FairnessBench.svg?style=social&label=Official)](https://github.com/Purdue-M2/AI-Face-FairnessBench)

+ [FAIntbench: A Holistic and Precise Benchmark for Bias Evaluation in Text-to-Image Models](https://arxiv.org/abs/2405.17814) (2024-05-28)

+ [ART: Automatic Red-teaming for Text-to-Image Models to Protect Benign Users](https://arxiv.org/abs/2405.19360) (2024-05-24) 

+ Condition Likelihood Discrepancy from [Membership Inference on Text-to-Image Diffusion Models via Conditional Likelihood Discrepancy](https://arxiv.org/abs/2405.14800) (2024-05-23)

+ [Could It Be Generated? Towards Practical Analysis of Memorization in Text-To-Image Diffusion Models](https://arxiv.org/abs/2405.05846) (2024-05-09)  


+ [Towards Geographic Inclusion in the Evaluation of Text-to-Image Models](https://arxiv.org/abs/2405.04457) (2024-05-07)  

+ [UnsafeBench: Benchmarking Image Safety Classifiers on Real-World and AI-Generated Images](https://arxiv.org/abs/2405.03486) (2024-05-06)  

+ [Espresso: Robust Concept Filtering in Text-to-Image Models](https://arxiv.org/abs/2404.19227) (2024-04-30)  
  > <i> Note:  Paper is about filtering unacceptable concepts, not evaluation.</i>

+ [Ethical-Lens: Curbing Malicious Usages of Open-Source Text-to-Image Models](https://arxiv.org/abs/2404.12104) (2024-04-18)  
  [![Code](https://img.shields.io/github/stars/yuzhu-cai/Ethical-Lens.svg?style=social&label=Official)](https://github.com/yuzhu-cai/Ethical-Lens)

+ [OpenBias: Open-set Bias Detection in Text-to-Image Generative Models](https://arxiv.org/abs/2404.07990) (2024-04-11) 
[![Code](https://img.shields.io/github/stars/Picsart-AI-Research/OpenBias.svg?style=social&label=Official)](https://github.com/Picsart-AI-Research/OpenBias)

+ [Survey of Bias In Text-to-Image Generation: Definition, Evaluation, and Mitigation](https://arxiv.org/abs/2404.01030) (2024-04-01)

+ [VBench-Trustworthiness](https://github.com/Vchitect/VBench/tree/master/vbench2_beta_trustworthiness) (2024-03) from [VBench: Comprehensive Benchmark Suite for Video Generative Models](https://arxiv.org/abs/2311.17982) (2023-11-29)  
  [![Code](https://img.shields.io/github/stars/Vchitect/VBench.svg?style=social&label=Official)](https://github.com/Vchitect/VBench)
  [![Website](https://img.shields.io/badge/Website-9cf)](https://vchitect.github.io/VBench-project/)

+ [Lost in Translation? Translation Errors and Challenges for Fair Assessment of Text-to-Image Models on Multilingual Concepts](https://arxiv.org/abs/2403.11092) (2024-03-17, NAACL 2024)

+ [Evaluating Text-to-Image Generative Models: An Empirical Study on Human Image Synthesis](https://arxiv.org/abs/2403.05125) (2024-03-08) 

+ [The Male CEO and the Female Assistant: Probing Gender Biases in Text-To-Image Models Through Paired Stereotype Test](https://arxiv.org/abs/2402.11089) (2024-02-16) 

+ [Multilingual Text-to-Image Generation Magnifies Gender Stereotypes and Prompt Engineering May Not Help You](https://arxiv.org/abs/2401.16092) (2024-01-29) 
[![Code](https://img.shields.io/github/stars/felifri/magbig.svg?style=social&label=Official)](https://github.com/felifri/magbig)

+ [Benchmarking the Fairness of Image Upsampling Methods](https://arxiv.org/abs/2401.13555) (2024-01-24) 

+ [ViSAGe: A Global-Scale Analysis of Visual Stereotypes in Text-to-Image Generation](https://arxiv.org/abs/2401.06310) (2024-01-02)

+ [New Job, New Gender? Measuring the Social Bias in Image Generation Models](https://arxiv.org/abs/2401.00763) (2024-01-01)

+ Distribution Bias, Jaccard Hallucination, Generative Miss Rate from [Quantifying Bias in Text-to-Image Generative Models](https://arxiv.org/abs/2312.13053) (2023-12-20)
[![Hugging Face](https://img.shields.io/badge/%F0%9F%A4%97%20Hugging%20Face-blue)](https://huggingface.co/spaces/JVice/try-before-you-bias)
[![Code](https://img.shields.io/github/stars/JJ-Vice/TryBeforeYouBias.svg?style=social&label=Official)](https://github.com/JJ-Vice/TryBeforeYouBias)

+ [TIBET: Identifying and Evaluating Biases in Text-to-Image Generative Models](https://arxiv.org/abs/2312.01261) (2023-12-03) 
> **_NOTE:_** CAS and BAV novel metric introduced

+ [Holistic Evaluation of Text-To-Image Models](https://arxiv.org/abs/2311.04287) (2023-11-07)  
  [![Code](https://img.shields.io/github/stars/stanford-crfm/helm.svg?style=social&label=Official)](https://github.com/stanford-crfm/helm)
  [![Website](https://img.shields.io/badge/Website-9cf)](https://crfm.stanford.edu/helm/heim/v1.1.0/)

+ [Sociotechnical Safety Evaluation of Generative AI Systems](https://arxiv.org/abs/2310.11986) (2023-10-18) 
[![Website](https://img.shields.io/badge/Website-9cf)](https://deepmind.google/discover/blog/evaluating-social-and-ethical-risks-from-generative-ai/)

+ [Navigating Cultural Chasms: Exploring and Unlocking the Cultural POV of Text-To-Image Models](https://arxiv.org/abs/2310.01929) (2023-10-03)

+ [ITI-GEN: Inclusive Text-to-Image Generation](https://arxiv.org/abs/2309.05569) (2023-09-11, ICCV 2023)  
  [![Website](https://img.shields.io/badge/Website-9cf)](https://czhang0528.github.io/iti-gen)  
  [![Code](https://img.shields.io/github/stars/humansensinglab/ITI-GEN.svg?style=social&label=Official)](https://github.com/humansensinglab/ITI-GEN)  

+ [DIG In: Evaluating Disparities in Image Generations with Indicators for Geographic Diversity](https://arxiv.org/abs/2308.06198) (2023-08-11)  
  [![Code](https://img.shields.io/github/stars/facebookresearch/DIG-In.svg?style=social&label=Official)](https://github.com/facebookresearch/DIG-In)

+ [On the Cultural Gap in Text-to-Image Generation](https://arxiv.org/abs/2307.02971) (2023-07-06)
[![Code](https://img.shields.io/github/stars/longyuewangdcu/C3-Bench.svg?style=social&label=Official)](https://github.com/longyuewangdcu/C3-Bench)

+ [Evaluating the Robustness of Text-to-image Diffusion Models against Real-world Attacks](https://arxiv.org/abs/2306.13103) (2023-06-16)  

+ [Disparities in Text-to-Image Model Concept Possession Across Languages](https://dl.acm.org/doi/abs/10.1145/3593013.3594123) (2023-06-12)

+ [Evaluating the Social Impact of Generative AI Systems in Systems and Society](https://arxiv.org/abs/2306.05949) (2023-06-09) 

+ [Word-Level Explanations for Analyzing Bias in Text-to-Image Models](https://arxiv.org/abs/2306.05500) (2023-06-03) 

+ [Multilingual Conceptual Coverage in Text-to-Image Models](https://arxiv.org/abs/2306.01735) (2023-06-02, ACL 2023)  
  [![Code](https://img.shields.io/github/stars/michaelsaxon/CoCoCroLa.svg?style=social&label=Official)](https://github.com/michaelsaxon/CoCoCroLa)  
  [![Website](https://img.shields.io/badge/Website-9cf)](https://saxon.me/coco-crola/)

+ [T2IAT: Measuring Valence and Stereotypical Biases in Text-to-Image Generation](https://arxiv.org/abs/2306.00905) (2023-06-01) 
[![Code](https://img.shields.io/github/stars/eric-ai-lab/T2IAT.svg?style=social&label=Official)](https://github.com/eric-ai-lab/T2IAT)  

+ [SneakyPrompt: Jailbreaking Text-to-image Generative Models](https://arxiv.org/abs/2305.12082) (2023-05-20)  
  [![Code](https://img.shields.io/github/stars/Yuchen413/text2image_safety.svg?style=social&label=Official)](https://github.com/Yuchen413/text2image_safety)

+ [Inspecting the Geographical Representativeness of Images from Text-to-Image Models](https://arxiv.org/abs/2305.11080) (2023-05-18)

+ [Multimodal Composite Association Score: Measuring Gender Bias in Generative Multimodal Models](https://arxiv.org/abs/2304.13855) (2023-04-26) 

+ [Uncurated Image-Text Datasets: Shedding Light on Demographic Bias](https://arxiv.org/abs/2304.02828) (2023-04-06, CVPR 2023)  
  [![Code](https://img.shields.io/github/stars/noagarcia/phase.svg?style=social&label=Official)](https://github.com/noagarcia/phase)

+ [Auditing Gender Presentation Differences in Text-to-Image Models](https://arxiv.org/abs/2302.03675) (2023-02-07)
 [![Code](https://img.shields.io/github/stars/SALT-NLP/GEP_data.svg?style=social&label=Official)](https://github.com/SALT-NLP/GEP_data) [![Website](https://img.shields.io/badge/Website-9cf)](https://salt-nlp.github.io/GEP/)

+ [Towards Equitable Representation in Text-to-Image Synthesis Models with the Cross-Cultural Understanding Benchmark (CCUB) Dataset](https://arxiv.org/abs/2301.12073) (2023-01-28)  

+ [How well can Text-to-Image Generative Models understand Ethical Natural Language Interventions?](https://arxiv.org/abs/2210.15230) (2022-10-27)
[![Code](https://img.shields.io/github/stars/j-min/DallEval.svg?style=social&label=Official)](https://github.com/j-min/DallEval)

+ [Exploiting Cultural Biases via Homoglyphs in Text-to-Image Synthesis](https://arxiv.org/abs/2209.08891) (2022-09-19)
 [![Code](https://img.shields.io/github/stars/LukasStruppek/Exploiting-Cultural-Biases-via-Homoglyphs.svg?style=social&label=Official)](https://github.com/LukasStruppek/Exploiting-Cultural-Biases-via-Homoglyphs)


+ [DALL-Eval: Probing the Reasoning Skills and Social Biases of Text-to-Image Generation Models](https://arxiv.org/abs/2202.04053) (2022-02-08, ICCV 2023)  
  [![Code](https://img.shields.io/github/stars/Hritikbansal/entigen_emnlp.svg?style=social&label=Official)](https://github.com/Hritikbansal/entigen_emnlp)

#### 3.6.2. Evaluation of Non-Visual-Generation-Model Trustworthiness
Not for visual generation, but related evaluations of other models like LLMs

+ [HarmBench: A Standardized Evaluation Framework for Automated Red Teaming and Robust Refusal](https://arxiv.org/abs/2402.04249) (2024-02-06)  
  [![Code](https://img.shields.io/github/stars/centerforaisafety/HarmBench.svg?style=social&label=Official)](https://github.com/centerforaisafety/HarmBench)
  [![Website](https://img.shields.io/badge/Website-9cf)](https://www.harmbench.org)

+ [FACET: Fairness in Computer Vision Evaluation Benchmark](https://arxiv.org/abs/2309.00035) (2023-08-31) 
[![Website](https://img.shields.io/badge/Website-9cf)](https://ai.meta.com/research/publications/facet-fairness-in-computer-vision-evaluation-benchmark/)
[![Website](https://img.shields.io/badge/Website-9cf)](https://facet.metademolab.com/)


+ [Gender Biases in Automatic Evaluation Metrics for Image Captioning](https://arxiv.org/abs/2305.14711) (2023-05-24) 

+ [Fairness Indicators for Systematic Assessments of Visual Feature Extractors](https://arxiv.org/abs/2202.07603) (2022-02-15)
[![Code](https://img.shields.io/github/stars/facebookresearch/vissl.svg?style=social&label=Official)](https://github.com/facebookresearch/vissl/tree/main/projects/fairness_indicators)
[![Website](https://img.shields.io/badge/Website-9cf)](https://ai.meta.com/blog/meta-ai-research-explores-new-public-fairness-benchmarks-for-computer-vision-models/)


<a name="3.7."></a>
### 3.7. Evaluation of Entity Relation

+ Scene Graph(SG)-IoU, Relation-IoU, and Entity-IoU (using GPT-4v) from [SG-Adapter: Enhancing Text-to-Image Generation with Scene Graph Guidance](https://arxiv.org/abs/2405.15321) (2024-05-24)

+ Relation Accuracy & Entity Accuracy from [ReVersion: Diffusion-Based Relation Inversion from Images](https://arxiv.org/abs/2303.13495) (2023-03-23)
[![Code](https://img.shields.io/github/stars/ziqihuangg/ReVersion.svg?style=social&label=Official)](https://github.com/ziqihuangg/ReVersion)
[![Website](https://img.shields.io/badge/Website-9cf)](https://ziqihuangg.github.io/projects/reversion.html)
[![Hugging Face](https://img.shields.io/badge/%F0%9F%A4%97%20Hugging%20Face-blue)](https://huggingface.co/spaces/Ziqi/ReVersion)

+ [Testing Relational Understanding in Text-Guided Image Generation](https://arxiv.org/abs/2208.00005) (2022-07-29)  



<a name="4."></a>
## 4. Improving Visual Generation with Evaluation / Feedback / Reward

+ [ReNO: Enhancing One-step Text-to-Image Models through Reward-based Noise Optimization](https://arxiv.org/abs/2406.04312) (2024-06-06) 
[![Code](https://img.shields.io/github/stars/ExplainableML/ReNO.svg?style=social&label=Official)](https://github.com/ExplainableML/ReNO)

+ [Step-aware Preference Optimization: Aligning Preference with Denoising Performance at Each Step](https://arxiv.org/abs/2406.04314) (2024-06-06)

+ [Improving GFlowNets for Text-to-Image Diffusion Alignment](https://arxiv.org/abs/2406.00633) (2024-06-02)

+ [Boost Your Own Human Image Generation Model via Direct Preference Optimization with AI Feedback](https://arxiv.org/abs/2405.20216) (2024-05-30)

+ [T2V-Turbo: Breaking the Quality Bottleneck of Video Consistency Model with Mixed Reward Feedback](https://arxiv.org/abs/2405.18750) (2024-05-29)  
  [![Code](https://img.shields.io/github/stars/Ji4chenLi/t2v-turbo.svg?style=social&label=Official)](https://github.com/Ji4chenLi/t2v-turbo)  [![Website](https://img.shields.io/badge/Website-9cf)](https://t2v-turbo.github.io/)

+ [Curriculum Direct Preference Optimization for Diffusion and Consistency Models](https://arxiv.org/abs/2405.13637) (2024-05-22) 

+ [Class-Conditional self-reward mechanism for improved Text-to-Image models](https://arxiv.org/abs/2405.13473) (2024-05-22)  
  [![Code](https://img.shields.io/github/stars/safouaneelg/SRT2I.svg?style=social&label=Official)](https://github.com/safouaneelg/SRT2I)

+ [Understanding and Evaluating Human Preferences for AI Generated Images with Instruction Tuning](https://arxiv.org/abs/2405.07346) (2024-05-12)

+ [Deep Reward Supervisions for Tuning Text-to-Image Diffusion Models](https://arxiv.org/abs/2405.00760) (2024-05-01)  

+ [ID-Aligner: Enhancing Identity-Preserving Text-to-Image Generation with Reward Feedback Learning](https://arxiv.org/abs/2404.15449) (2024-04-23)  
  [![Code](https://img.shields.io/github/stars/Weifeng-Chen/ID-Aligner.svg?style=social&label=Official)](https://github.com/Weifeng-Chen/ID-Aligner)   [![Website](https://img.shields.io/badge/Website-9cf)](https://idaligner.github.io)


+ [ControlNet++: Improving Conditional Controls with Efficient Consistency Feedback](https://arxiv.org/abs/2404.07987) (2024-04-11)  

+ [UniFL: Improve Stable Diffusion via Unified Feedback Learning](https://arxiv.org/abs/2404.05595) (2024-04-08)  

+ [ByteEdit: Boost, Comply and Accelerate Generative Image Editing](https://arxiv.org/abs/2404.04860) (2024-04-07)  
  [![Website](https://img.shields.io/badge/Website-9cf)](https://byte-edit.github.io/)

+ [Aligning Diffusion Models by Optimizing Human Utility](https://arxiv.org/abs/2404.04465) (2024-04-06)  

+ [Dynamic Prompt Optimizing for Text-to-Image Generation](https://arxiv.org/abs/2404.04095) (2024-04-05) 
[![Code](https://img.shields.io/github/stars/Mowenyii/PAE.svg?style=social&label=Official)](https://github.com/Mowenyii/PAE)

+ [Pixel-wise RL on Diffusion Models: Reinforcement Learning from Rich Feedback](https://arxiv.org/abs/2404.04356) (2024-04-05) 

+ [CoMat: Aligning Text-to-Image Diffusion Model with Image-to-Text Concept Matching](https://arxiv.org/abs/2404.03653) (2024-04-04)  
  [![Code](https://img.shields.io/github/stars/CaraJ7/CoMat.svg?style=social&label=Official)](https://github.com/CaraJ7/CoMat)  [![Website](https://img.shields.io/badge/Website-9cf)](https://caraj7.github.io/comat/)

+ [VersaT2I: Improving Text-to-Image Models with Versatile Reward](https://arxiv.org/abs/2403.18493) (2024-03-27)  


+ [Improving Text-to-Image Consistency via Automatic Prompt Optimization](https://arxiv.org/abs/2403.17804) (2024-03-26)  

+ [RL for Consistency Models: Faster Reward Guided Text-to-Image Generation](https://arxiv.org/abs/2404.03673) (2024-03-25)  
  [![Website](https://img.shields.io/badge/Website-9cf)](https://rlcm.owenoertell.com)
  [![Code](https://img.shields.io/github/stars/Owen-Oertell/rlcm.svg?style=social&label=Official)](https://github.com/Owen-Oertell/rlcm)

+ [AGFSync: Leveraging AI-Generated Feedback for Preference Optimization in Text-to-Image Generation](https://arxiv.org/abs/2403.13352) (2024-03-20)  

+ [Reward Guided Latent Consistency Distillation](https://arxiv.org/abs/2403.11027) (2024-03-16)  
  [![Code](https://img.shields.io/github/stars/Ji4chenLi/rg-lcd.svg?style=social&label=Official)](https://github.com/Ji4chenLi/rg-lcd)  [![Website](https://img.shields.io/badge/Website-9cf)](https://rg-lcd.github.io/)

+ [Universal Prompt Optimizer for Safe Text-to-Image Generation](https://arxiv.org/abs/2402.10882) (2024-02-16, NAACL 2024)  
  [![Code](https://img.shields.io/github/stars/wzongyu/POSI.svg?style=social&label=Official)](https://github.com/wzongyu/POSI)

+ [Social Reward: Evaluating and Enhancing Generative AI through Million-User Feedback from an Online Creative Community](https://arxiv.org/abs/2402.09872) (2024-02-15, ICLR 2024)
 [![Code](https://img.shields.io/github/stars/Picsart-AI-Research/Social-Reward.svg?style=social&label=Official)](https://github.com/Picsart-AI-Research/Social-Reward)

+ [A Dense Reward View on Aligning Text-to-Image Diffusion with Preference](https://arxiv.org/abs/2402.08265) (2024-02-13, ICML 2024)  
  [![Code](https://img.shields.io/github/stars/Shentao-YANG/Dense_Reward_T2I.svg?style=social&label=Official)](https://github.com/Shentao-YANG/Dense_Reward_T2I)

+ [PRDP: Proximal Reward Difference Prediction for Large-Scale Reward Finetuning of Diffusion Models](https://arxiv.org/abs/2402.08714) (2024-02-13)


+ [Human Aesthetic Preference-Based Large Text-to-Image Model Personalization: Kandinsky Generation as an Example](https://arxiv.org/abs/2402.06389) (2024-02-09)

+ [Divide and Conquer: Language Models can Plan and Self-Correct for Compositional Text-to-Image Generation](https://arxiv.org/abs/2401.15688) (2024-01-28)
[![Code](https://img.shields.io/github/stars/zhenyuw16/CompAgent_code.svg?style=social&label=Official)](https://github.com/zhenyuw16/CompAgent_code)

+ [Large-scale Reinforcement Learning for Diffusion Models](https://arxiv.org/abs/2401.12244) (2024-01-20)

+ [Parrot: Pareto-optimal Multi-Reward Reinforcement Learning Framework for Text-to-Image Generation](https://arxiv.org/abs/2401.05675) (2024-01-11)

+ [InstructVideo: Instructing Video Diffusion Models with Human Feedback](https://arxiv.org/abs/2312.12490) (2023-12-19)  
  [![Website](https://img.shields.io/badge/Website-9cf)](https://instructvideo.github.io)

+ [Rich Human Feedback for Text-to-Image Generation](https://arxiv.org/abs/2312.10240) (2023-12-15, CVPR 2024)  

+ [InstructBooth: Instruction-following Personalized Text-to-Image Generation](https://arxiv.org/abs/2312.03011) (2023-12-04)  [![Website](https://img.shields.io/badge/Website-9cf)](https://sites.google.com/view/instructbooth)

+ [DreamSync: Aligning Text-to-Image Generation with Image Understanding Feedback](https://arxiv.org/abs/2311.17946) (2023-11-29)  

+ [Enhancing Diffusion Models with Text-Encoder Reinforcement Learning](https://arxiv.org/abs/2311.15657) (2023-11-27)
[![Code](https://img.shields.io/github/stars/chaofengc/TexForce.svg?style=social&label=Official)](https://github.com/chaofengc/TexForce)

+ [AdaDiff: Adaptive Step Selection for Fast Diffusion](https://arxiv.org/abs/2311.14768) (2023-11-24) 

+ [Using Human Feedback to Fine-tune Diffusion Models without Any Reward Model](https://arxiv.org/abs/2311.13231) (2023-11-22)
[![Code](https://img.shields.io/github/stars/yk7333/d3po.svg?style=social&label=Official)](https://github.com/yk7333/d3po)

+ [Diffusion Model Alignment Using Direct Preference Optimization](https://arxiv.org/abs/2311.12908) (2023-11-21)  
  [![Code](https://img.shields.io/github/stars/SalesforceAIResearch/DiffusionDPO.svg?style=social&label=Official)](https://github.com/SalesforceAIResearch/DiffusionDPO)[![Code](https://img.shields.io/github/stars/huggingface/diffusers.svg?style=social&label=diffusers)](https://github.com/huggingface/diffusers/tree/main/examples/research_projects/diffusion_dpo) [![Website](https://img.shields.io/badge/Website-9cf)](https://blog.salesforceairesearch.com/diffusion-dpo/)

+ [BeautifulPrompt: Towards Automatic Prompt Engineering for Text-to-Image Synthesis](https://arxiv.org/abs/2311.06752) (2023-11-12) 

+ [Aligning Text-to-Image Diffusion Models with Reward Backpropagation](https://arxiv.org/abs/2310.03739) (2023-10-05)  
  [![Code](https://img.shields.io/github/stars/mihirp1998/AlignProp.svg?style=social&label=Official)](https://github.com/mihirp1998/AlignProp/)
  [![Website](https://img.shields.io/badge/Website-9cf)](https://align-prop.github.io/)

+ [Directly Fine-Tuning Diffusion Models on Differentiable Rewards](https://arxiv.org/abs/2309.17400) (2023-09-29)

+ [LayoutLLM-T2I: Eliciting Layout Guidance from LLM for Text-to-Image Generation](https://arxiv.org/abs/2308.05095) (2023-08-09, ACM MM 2023)  
  [![Code](https://img.shields.io/github/stars/LayoutLLM-T2I/LayoutLLM-T2I.svg?style=social&label=Official)](https://github.com/LayoutLLM-T2I/LayoutLLM-T2I)  [![Website](https://img.shields.io/badge/Website-9cf)](https://layoutllm-t2i.github.io/) [![Hugging Face](https://img.shields.io/badge/%F0%9F%A4%97%20Hugging%20Face-blue)](https://huggingface.co/leigangqu/LayoutLLM-T2I/tree/main)


+ [FABRIC: Personalizing Diffusion Models with Iterative Feedback](https://arxiv.org/abs/2307.10159) (2023-07-19) 
[![Code](https://img.shields.io/github/stars/sd-fabric/fabric.svg?style=social&label=Official)](https://github.com/sd-fabric/fabric) [![Website](https://sd-fabric.github.io/)


+ [Divide, Evaluate, and Refine: Evaluating and Improving Text-to-Image Alignment with Iterative VQA Feedback](https://arxiv.org/abs/2307.04749) (2023-07-10, NeurIPS 2023)  
  [![Code](https://img.shields.io/github/stars/1jsingh/Divide-Evaluate-and-Refine.svg?style=social&label=Official)](https://github.com/1jsingh/Divide-Evaluate-and-Refine) [![Website](https://img.shields.io/badge/Website-9cf)](https://1jsingh.github.io/divide-evaluate-and-refine)

+ [StyleDrop: Text-to-Image Generation in Any Style](https://arxiv.org/abs/2306.00983) (2023-06-01)
 [![Website](https://img.shields.io/badge/Website-9cf)](https://styledrop.github.io/)


+ [RealignDiff: Boosting Text-to-Image Diffusion Model with Coarse-to-fine Semantic Re-alignment](https://arxiv.org/abs/2305.19599) (2023-05-31)


+ [DPOK: Reinforcement Learning for Fine-tuning Text-to-Image Diffusion Models](https://arxiv.org/abs/2305.16381) (2023-05-25, NeurIPS 2023)  
  [![Code](https://img.shields.io/github/stars/google-research/google-research.svg?style=social&label=Official)](https://github.com/google-research/google-research/tree/master/dpok)  [![Website](https://img.shields.io/badge/Website-9cf)](https://sites.google.com/view/dpok-t2i-diffusion/home)

+ [Training Diffusion Models with Reinforcement Learning](https://arxiv.org/abs/2305.13301) (2023-05-22) 
[![Code](https://img.shields.io/github/stars/jannerm/ddpo.svg?style=social&label=Official)](https://github.com/jannerm/ddpo)
[Website](https://img.shields.io/badge/Website-9cf)](https://rl-diffusion.github.io/)

+ [ImageReward: Learning and Evaluating Human Preferences for Text-to-Image Generation](https://arxiv.org/abs/2304.05977) (2023-04-12)  
  [![Code](https://img.shields.io/github/stars/THUDM/ImageReward.svg?style=social&label=Official)](https://github.com/THUDM/ImageReward)

+ [Confidence-aware Reward Optimization for Fine-tuning Text-to-Image Models](https://arxiv.org/abs/2404.01863) (2023-04-02, ICLR 2024)  


+ [Human Preference Score: Better Aligning Text-to-Image Models with Human Preference](https://arxiv.org/abs/2303.14420) (2023-03-25)  
  [![Code](https://img.shields.io/github/stars/tgxs002/align_sd.svg?style=social&label=Official)](https://github.com/tgxs002/align_sd)
  [![Website](https://img.shields.io/badge/Website-9cf)](https://tgxs002.github.io/align_sd_web/)

+ [Aligning Text-to-Image Models using Human Feedback](https://arxiv.org/abs/2302.12192) (2023-02-23)

+ [Optimizing Prompts for Text-to-Image Generation](https://arxiv.org/abs/2212.09611) (2022-12-19, NeurIPS 2023)  
  [![Code](https://img.shields.io/github/stars/microsoft/LMOps.svg?style=social&label=Official)](https://github.com/microsoft/LMOps/tree/main/promptist)  
  [![Hugging Face](https://img.shields.io/badge/%F0%9F%A4%97%20Hugging%20Face-blue)](https://huggingface.co/spaces/microsoft/Promptist)

<!-- ## Evaluation Datasets
- UCF101
- ImageNet
- COCO -->

<a name="5."></a>
## 5. Quality Assessment for AIGC

### 5.1. Image Quality Assessment for AIGC

+ [Descriptive Image Quality Assessment in the Wild](https://arxiv.org/abs/2405.18842) (2024-05-29)   
  [![Website](https://img.shields.io/badge/Website-9cf)](https://depictqa.github.io/depictqa-wild/)

+ [Large Multi-modality Model Assisted AI-Generated Image Quality Assessment](https://arxiv.org/abs/2404.17762) (2024-04-27)  
  [![Code](https://img.shields.io/github/stars/wangpuyi/MA-AGIQA.svg?style=social&label=Official)](https://github.com/wangpuyi/MA-AGIQA)

+ [Adaptive Mixed-Scale Feature Fusion Network for Blind AI-Generated Image Quality Assessment](https://arxiv.org/abs/2404.15163) (2024-04-23)  

+ [PCQA: A Strong Baseline for AIGC Quality Assessment Based on Prompt Condition](https://arxiv.org/abs/2404.13299) (2024-04-20)  

+ [AIGIQA-20K: A Large Database for AI-Generated Image Quality Assessment](https://arxiv.org/abs/2404.03407) (2024-04-04)  
  [![Website](https://img.shields.io/badge/Website-9cf)](https://www.modelscope.cn/datasets/lcysyzxdxc/AIGCQA-30K-Image/summary)
  
+ [AIGCOIQA2024: Perceptual Quality Assessment of AI Generated Omnidirectional Images](https://arxiv.org/abs/2404.01024) (2024-04-01)

+ [Bringing Textual Prompt to AI-Generated Image Quality Assessment](https://arxiv.org/abs/2403.18714) (2024-03-27, ICME 2024)  
  [![Code](https://img.shields.io/github/stars/Coobiw/IP-IQA.svg?style=social&label=Official)](https://github.com/Coobiw/IP-IQA)

+ [TIER: Text-Image Encoder-based Regression for AIGC Image Quality Assessment](https://arxiv.org/abs/2401.03854) (2024-01-08) 
[![Code](https://img.shields.io/github/stars/jiquan123/TIER.svg?style=social&label=Official)](https://github.com/jiquan123/TIER)

+ [Exploring the Naturalness of AI-Generated Images](https://arxiv.org/abs/2312.05476) (2023-12-09)  
  [![Code](https://img.shields.io/github/stars/zijianchen98/AGIN.svg?style=social&label=Official)](https://github.com/zijianchen98/AGIN)
  
+ [PKU-I2IQA: An Image-to-Image Quality Assessment Database for AI Generated Images](https://arxiv.org/abs/2311.15556) (2023-11-27)  
  [![Code](https://img.shields.io/github/stars/jiquan123/I2IQA.svg?style=social&label=Official)](https://github.com/jiquan123/I2IQA)

+ [AIGCIQA2023: A Large-scale Image Quality Assessment Database for AI Generated Images: from the Perspectives of Quality, Authenticity and Correspondence](https://arxiv.org/abs/2307.00211) (2023-07-01)  
  
+ [AGIQA-3K: An Open Database for AI-Generated Image Quality Assessment](https://arxiv.org/abs/2306.04717) (2023-06-07)  
  [![Code](https://img.shields.io/github/stars/lcysyzxdxc/AGIQA-3k-Database.svg?style=social&label=Official)](https://github.com/lcysyzxdxc/AGIQA-3k-Database)

+ [A Perceptual Quality Assessment Exploration for AIGC Images](https://arxiv.org/abs/2303.12618) (2023-03-22)

+ [SPS: A Subjective Perception Score for Text-to-Image Synthesis](https://ieeexplore.ieee.org/abstract/document/9401705) (2021-04-27)  


+ [GIQA: Generated Image Quality Assessment](https://arxiv.org/abs/2003.08932) (2020-03-19)
[![Code](https://img.shields.io/github/stars/cientgu/GIQA.svg?style=social&label=Official)](https://github.com/cientgu/GIQA)

### 5.2. Aesthetic Predictors for Generated Images

+ [Multi-modal Learnable Queries for Image Aesthetics Assessment](https://arxiv.org/abs/2405.01326) (2024-05-02, ICME 2024)  

+ Aesthetic Scorer extension for SD Automatic WebUI (2023-01-15)  
  [![Code](https://img.shields.io/github/stars/vladmandic/sd-extension-aesthetic-scorer.svg?style=social&label=Official)](https://github.com/vladmandic/sd-extension-aesthetic-scorer)


+ Simulacra Aesthetic-Models (2022-07-09)  
  [![Code](https://img.shields.io/github/stars/crowsonkb/simulacra-aesthetic-models.svg?style=social&label=Official)](https://github.com/crowsonkb/simulacra-aesthetic-models)

+ [Rethinking Image Aesthetics Assessment: Models, Datasets and Benchmarks](https://www.researchgate.net/publication/362037160_Rethinking_Image_Aesthetics_Assessment_Models_Datasets_and_Benchmarks) (2022-07-01)
[![Code](https://img.shields.io/github/stars/woshidandan/TANet-image-aesthetics-and-quality-assessment.svg?style=social&label=Official)](https://github.com/woshidandan/TANet-image-aesthetics-and-quality-assessment)


+ LAION-Aesthetics_Predictor V2: CLIP+MLP Aesthetic Score Predictor (2022-06-26)  
  [![Code](https://img.shields.io/github/stars/christophschuhmann/improved-aesthetic-predictor.svg?style=social&label=Official)](https://github.com/christophschuhmann/improved-aesthetic-predictor)
  [![Website](https://img.shields.io/badge/Visualizer-9cf)](http://captions.christoph-schuhmann.de/aesthetic_viz_laion_sac+logos+ava1-l14-linearMSE-en-2.37B.html)
  [![Website](https://img.shields.io/badge/Website-9cf)](https://laion.ai/blog/laion-aesthetics/#laion-aesthetics-v2)


+ LAION-Aesthetics_Predictor V1 (2022-05-21)  
  [![Code](https://img.shields.io/github/stars/LAION-AI/aesthetic-predictor.svg?style=social&label=Official)](https://github.com/LAION-AI/aesthetic-predictor)
  [![Website](https://img.shields.io/badge/Website-9cf)](https://laion.ai/blog/laion-aesthetics/#laion-aesthetics-v1)


<!-- ## Video Quality Assessment for AIGC
- To be added -->

<a name="6."></a>
## 6. Study and Rethinking

### 6.1. Evaluation of Evaluations
+ [GAIA: Rethinking Action Quality Assessment for AI-Generated Videos](https://arxiv.org/abs/2406.06087) (2024-06-10)

+ [Who Evaluates the Evaluations? Objectively Scoring Text-to-Image Prompt Coherence Metrics with T2IScoreScore (TS2)](https://arxiv.org/abs/2404.04251) (2024-04-05)  
  [![Code](https://img.shields.io/github/stars/michaelsaxon/T2IScoreScore.svg?style=social&label=Official)](https://github.com/michaelsaxon/T2IScoreScore)
  [![Website](https://img.shields.io/badge/Website-9cf)](https://t2iscorescore.github.io) [![Hugging Face](https://img.shields.io/badge/%F0%9F%A4%97%20Hugging%20Face-blue)](https://huggingface.co/datasets/saxon/T2IScoreScore)



### 6.2. Survey

+ [From Sora What We Can See: A Survey of Text-to-Video Generation](https://arxiv.org/abs/2405.10674) (2024-05-17)  
  [![Code](https://img.shields.io/github/stars/soraw-ai/Awesome-Text-to-Video-Generation.svg?style=social&label=Official)](https://github.com/soraw-ai/Awesome-Text-to-Video-Generation) 
  > <i> Note: Refer to Section 3.4 for Evaluation Datasets and Metrics</i>

+ [A Survey on Personalized Content Synthesis with Diffusion Models](https://arxiv.org/abs/2405.05538) (2024-05-09) 
  > <i> Note: Refere to Section 6 for Evaluation Datasets and Metrics</i>

+ [A Survey on Long Video Generation: Challenges, Methods, and Prospects](https://arxiv.org/abs/2403.16407) (2024-03-25)
  > <i>Note: Refer to table 2 for evaluation metrics for long video generation</i>
+ [Evaluating Text-to-Image Synthesis: Survey and Taxonomy of Image Quality Metrics](https://arxiv.org/abs/2403.11821) (2024-03-18)  

+ [Sora as an AGI World Model? A Complete Survey on Text-to-Video Generation](https://arxiv.org/abs/2403.05131) (2024-03-08) 

+ [State of the Art on Diffusion Models for Visual Computing](https://arxiv.org/abs/2310.07204) (2023-10-11)  
  > <i> Note: Refer to Section 9 for Metrics</i>

+ [A Survey on Video Diffusion Models](https://arxiv.org/abs/2310.10647) (2023-10-06)  
  [![Code](https://img.shields.io/github/stars/ChenHsing/Awesome-Video-Diffusion-Models.svg?style=social&label=Official)](https://github.com/ChenHsing/Awesome-Video-Diffusion-Models)
  ><i> Note: Refer to Section 2.3 for Evaluation Datasets and Metrics</i>

+ [Text-to-image Diffusion Models in Generative AI: A Survey](https://arxiv.org/abs/2303.07909) (2023-03-14) 
  ><i> Note: Refer to Section 5 for Evaulation from Techincal and Ethical Perspective</i>

+ [Adversarial Text-to-Image Synthesis: A Review](https://arxiv.org/abs/2101.09983) (2021-01-25)  
  > <i> Note: Refer to Section 5 for Evaluation of T2I Models</i>

+ [What comprises a good talking-head video generation?: A Survey and Benchmark](https://arxiv.org/abs/2005.03201) (2020-05-07) 
[![Code](https://img.shields.io/github/stars/lelechen63/talking-head-generation-survey.svg?style=social&label=Official)](https://github.com/lelechen63/talking-head-generation-survey)

+ [A Survey and Taxonomy of Adversarial Neural Networks for Text-to-Image Synthesis](https://arxiv.org/abs/1910.09399) (2019-10-21)  
  ><i> Note: Refer to Section 5 for Benchmark and Evaluation</i>

### 6.3. Study

+ [A-Bench: Are LMMs Masters at Evaluating AI-generated Images?](https://arxiv.org/abs/2406.03070) (2024-06-05)
  [![Code](https://img.shields.io/github/stars/Q-Future/A-Bench.svg?style=social&label=Official)](https://github.com/Q-Future/A-Bench)

+ [On the Content Bias in Fréchet Video Distance](https://arxiv.org/abs/2404.12391) (2024-04-18, CVPR 2024)  
  [![Code](https://img.shields.io/github/stars/songweige/content-debiased-fvd.svg?style=social&label=Official)](https://github.com/songweige/content-debiased-fvd)
  [![Website](https://img.shields.io/badge/Website-9cf)](https://content-debiased-fvd.github.io)

+ [Text-to-Image Synthesis With Generative Models: Methods, Datasets, Performance Metrics, Challenges, and Future Direction](https://ieeexplore.ieee.org/abstract/document/10431766) (2024-02-09)

+ [On the Evaluation of Generative Models in Distributed Learning Tasks](https://arxiv.org/abs/2310.11714) (2023-10-18)

+ [Recent Advances in Text-to-Image Synthesis: Approaches, Datasets and Future Research Prospects](https://ieeexplore.ieee.org/abstract/document/10224242) (2023-08-18)

+ [Exposing flaws of generative model evaluation metrics and their unfair treatment of diffusion models](https://arxiv.org/abs/2306.04675) (2023-06-07, NeurIPS 2023)  
  [![Code](https://img.shields.io/github/stars/layer6ai-labs/dgm-eval.svg?style=social&label=Official)](https://github.com/layer6ai-labs/dgm-eval)

+ [Toward Verifiable and Reproducible Human Evaluation for Text-to-Image Generation](https://arxiv.org/abs/2304.01816) (2023-04-04, CVPR 2023)

+ [Revisiting the Evaluation of Image Synthesis with GANs](https://arxiv.org/abs/2304.01999) (2023-04-04)

+ [A Study on the Evaluation of Generative Models](https://arxiv.org/abs/2206.10935) (2022-06-22)

+ [REALY: Rethinking the Evaluation of 3D Face Reconstruction](https://arxiv.org/abs/2203.09729) (2022-03-18) 
[![Code](https://img.shields.io/github/stars/czh-98/REALY.svg?style=social&label=Official)](https://github.com/czh-98/REALY)
[![Website](https://img.shields.io/badge/Website-9cf)](https://realy3dface.com/)

+ [On Aliased Resizing and Surprising Subtleties in GAN Evaluation](https://arxiv.org/abs/2104.11222) (2021-04-22)  
  [![Code](https://img.shields.io/github/stars/GaParmar/clean-fid.svg?style=social&label=Official)](https://github.com/GaParmar/clean-fid)  
  [![Website](https://img.shields.io/badge/Website-9cf)](https://www.cs.cmu.edu/~clean-fid/)

+ [Pros and Cons of GAN Evaluation Measures: New Developments](https://arxiv.org/abs/2103.09396) (2021-03-17)  

+ [On the Robustness of Quality Measures for GANs](https://arxiv.org/abs/2201.13019) (2022-01-31, ECCV 2022)  
  [![Code](https://img.shields.io/github/stars/MotasemAlfarra/R-FID-Robustness-of-Quality-Measures-for-GANs.svg?style=social&label=Official)](https://github.com/MotasemAlfarra/R-FID-Robustness-of-Quality-Measures-for-GANs)

+ [An Analysis of Text-to-Image Synthesis](https://papers.ssrn.com/sol3/papers.cfm?abstract_id=3852950) (2021-05-25)

+ [Pros and Cons of GAN Evaluation Measures](https://arxiv.org/abs/1802.03446) (2018-02-09)  

+ [A Note on the Inception Score](https://arxiv.org/abs/1801.01973) (2018-01)

+ [An empirical study on evaluation metrics of generative adversarial networks](https://arxiv.org/abs/1806.07755) (2018-06-19)  
  [![Code](https://img.shields.io/github/stars/xuqiantong/GAN-Metrics.svg?style=social&label=Official)](https://github.com/xuqiantong/GAN-Metrics)
### 6.4. Competition
+ [NTIRE 2024 Quality Assessment of AI-Generated Content Challenge](https://arxiv.org/abs/2404.16687) (2024-04-25)

<a name="7."></a>
## 7. Other Useful Resources
 + Stanford Course: CS236 "Deep Generative Models" - Lecture 15 "Evaluation of Generative Models" [[slides]](https://deepgenerativemodels.github.io/assets/slides/lecture15.pdf)

<!-- 
Papers to read and to organize:
- Rethinking FID: Towards a Better Evaluation Metric for Image Generation 
- Wasserstein Distortion: Unifying Fidelity and Realism
-->
