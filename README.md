# Awesome Deep Optics/End-to-End Optical Design

This is a list of awesome deep optics papers, inspired by [awesome-computer-vision](https://github.com/jbhuang0604/awesome-computer-vision). Deep optics/end-to-end optical design is different from the traditional optical design because of:

- Differentiable optical model enables more optimization power
- End-to-end co-design of optics and image processing

Please bring these questions when you read the papers:

* What is the imaging model? A differentiable model enables end-to-end optical design with a network.
* What information is encoded? Additional information is encoded for computational imaging applications.
* How to fabricate the prototype? After designing a deep optics system, verify it with a prototype!

## News

- 01/2025: This paper list is simplified following [rules](rules.md). A full list is available in [full list](full_list.md).

## Background materials

(I am trying to start a new repo to collect papers for optical/imaging process simulation. How do you think about it?)

The following are some materials I think will help you learn the imaging process.

- [1996 Book] Introduction to Fourier Optics McGraw-Hill Series in Electrical and Computer Engineering. [link](https://books.google.com.sa/books/about/Introduction_to_Fourier_Optics.html?id=jMcsmwEACAAJ&redir_esc=y)
- [2007 Book] Modern Optical Engineering. [link](https://www.amazon.com/Modern-Optical-Engineering-4th-Ed/dp/0071476873)
- [2011 Book] Computational fourier optics : a MATLAB tutorial. [link](https://www.amazon.com/Computational-Fourier-Optics-MATLAB-Tutorial/dp/0819482048)
- [2012 Siggraph course] Computational displays: combining optical fabrication, computational processing, and perceptual tricks to build the displays of the future. [link](https://dl.acm.org/doi/abs/10.1145/2343483.2343487)
- [2019 PhD thesis] Ray-based methods for simulating aberrations and cascaded diffraction in imaging systems. [link](https://repository.tudelft.nl/islandora/object/uuid:1cc83547-4292-4420-b23f-036306eded0d?collection=research)
- [2020 Siggraph course] Deep optics: joint design of optics and image recovery algorithms for domain specific cameras. [link](https://dl.acm.org/doi/abs/10.1145/3388769.3407486)
- [2022 Siggraph course] Differentiable cameras and displays. [link](https://sites.google.com/princeton.edu/neural-optics/)

## Must-read papers

### 1. Wave propagation model

In the wave propagation model, each optical element (DOE, lens, aperture, et al.) is represented as a phase mask. This idealized optics is easy to simulate; however, it is not accurate enough and cannot model optical aberrations.

#### Single DOE or metasurface (to flat cameras)

- **2018 End-to-end optimization of optics and image processing for achromatic extended depth of field and super-resolution imaging.** [paper](https://dl.acm.org/doi/pdf/10.1145/3197517.3201333), [supp](https://dl.acm.org/doi/10.1145/3197517.3201333), [project](https://www.computationalimaging.org/publications/end-to-end-optimization-of-optics-and-image-processing-for-achromatic-extended-depth-of-field-and-super-resolution-imaging/), [code](https://github.com/vsitzmann/deepoptics)
- 2020 Learned rotationally symmetric diffractive achromat for full-spectrum computational imaging. [paper](http://www.computationalimaging.org/wp-content/uploads/2020/07/learned_DA_optica_2020.pdf), [supp](https://opticapublishing.figshare.com/articles/journal_contribution/Supplementary_document_for_Learned_Rotationally_Symmetric_Diffractive_Achromat_for_Full-Spectrum_Computational_Imaging_-_4680630_pdf/12588728), [project, video](https://www.computationalimaging.org/publications/learned-rotationally-symmetric-diffractive-achromat/)
- 2020 Spectral DiffuserCam: lensless snapshot hyperspectral imaging with a spectral filter array. [paper](https://opg.optica.org/optica/fulltext.cfm?uri=optica-7-10-1298&id=440114), [code](https://github.com/Waller-Lab/SpectralDiffuserCam)
- 2021 Learning Privacy-Preserving Optics for Human Pose Estimation. [paper](https://carloshinojosa.me/files/ICCV2021/05401.pdf), [supp](https://carloshinojosa.me/files/ICCV2021/05401-supp.pdf), [project, slides, video](https://carloshinojosa.me/project/privacy-hpe/), [code](https://github.com/carlosh93/privacy-optics-hpe)
- 2021 Single-shot Hyperspectral-Depth Imaging with Learned Diffractive Optics. [paper](https://openaccess.thecvf.com/content/ICCV2021/papers/Baek_Single-Shot_Hyperspectral-Depth_Imaging_With_Learned_Diffractive_Optics_ICCV_2021_paper.pdf), [supp](http://vclab.kaist.ac.kr/iccv2021/e2eHD_supple.pdf), [project](http://vclab.kaist.ac.kr/iccv2021/dataset.html), [video](https://www.youtube.com/watch?v=Q-9PnlkxnMs)
- **2021 Neural nano-optics for high-quality thin lens imaging.** [paper](https://light.cs.princeton.edu/wp-content/uploads/2021/11/NeuralNanoOptics.pdf), [supp](https://light.cs.princeton.edu/wp-content/uploads/2021/11/NeuralNanoOptics_Supp.pdf), [project](https://light.princeton.edu/publication/neural-nano-optics/), [project](https://light.princeton.edu/publication/neural-nano-optics/), [code](https://github.com/Ethan-Tseng/Neural_Nano-Optics)

#### DOE + non-optimizable thin lens (to hybrid optics)

- 2019 PhaseCam3D — Learning Phase Masks for Passive Single View Depth Estimation. [paper](https://ieeexplore.ieee.org/stamp/stamp.jsp?tp=&arnumber=8747330), [supp](https://drive.google.com/file/d/1ZGt0Q2B7YCV-gULAuWWXYLUyucxIz-Zy/view), [project](https://yichengwu.github.io/PhaseCam3D/), [code](https://github.com/YichengWu/PhaseCam3D)
- 2020 Learning Rank-1 Diffractive Optics for Single-shot High Dynamic Range Imaging. [paper](https://vccimaging.org/Publications/Sun2020LearningRank1HDR/Sun2020LearningRank1HDR.pdf), [supp](https://vccimaging.org/Publications/Sun2020LearningRank1HDR/Sun2020LearningRank1HDR_supp.pdf), [project](https://vccimaging.org/Publications/Sun2020LearningRank1HDR/)
- 2021 Depth from Defocus with Learned Optics for Imaging and Occlusion-aware Depth Estimation. [paper](http://www.computationalimaging.org/wp-content/uploads/2021/04/DeepDfD_ICCP2021.pdf), [supp](http://www.computationalimaging.org/wp-content/uploads/2021/04/DeepDfD_supp_ICCP2021.pdf), [project](https://www.computationalimaging.org/publications/deepopticsdfd/), [code](https://github.com/computational-imaging/DepthFromDefocusWithLearnedOptics)
- 2022 End-to-end snapshot compressed super-resolution imaging with deep optics. [paper](https://opg.optica.org/optica/fulltext.cfm?uri=optica-9-4-451&id=471410), [supp](https://opticapublishing.figshare.com/articles/journal_contribution/Supplementary_document_for_End-to-end_snapshot_compressed_super-resolution_imaging_with_deep_optics_-_5748413_pdf/19361507)
- 2022 Seeing Through Obstructions with Diffractive Cloaking. [paper](https://light.princeton.edu/wp-content/uploads/2022/07/seeing_through_obstructions_main.pdf), [project](https://light.princeton.edu/publication/seeing-through-obstructions/), [code](https://github.com/princeton-computational-imaging/SeeThroughObstructions)
- **2024 Split-aperture 2-in-1 computational cameras.** [paper](https://dl.acm.org/doi/10.1145/3658225), [supp](https://light.princeton.edu/wp-content/uploads/2024/07/DualPixel_supp.pdf), [project](https://light.princeton.edu/publication/2in1-camera/), [code](https://github.com/princeton-computational-imaging/2in1_camera)

#### DOE/Metasurface array/stack (to flat cameras)

- 2016 Encoded diffractive optics for full-spectrum computational imaging. [paper](https://www.nature.com/articles/srep33543.pdf), [supp](https://static-content.springer.com/esm/art%3A10.1038%2Fsrep33543/MediaObjects/41598_2016_BFsrep33543_MOESM1_ESM.pdf)
- 2021 Shift-variant color-coded diffractive spectral imaging system. [paper](https://opg.optica.org/optica/fulltext.cfm?uri=optica-8-11-1424&id=464500), [video](https://www.youtube.com/watch?v=KNu2ZPLnR50), [code](https://github.com/jorgebaccauis/Shift-Variant-System)
- **2024 Learned Multi-aperture Color-coded Optics for Snapshot Hyperspectral Imaging.** [paper](https://dl.acm.org/doi/abs/10.1145/3687976), [supp](https://light.princeton.edu/wp-content/uploads/2024/09/ArrayHSI_supp.pdf), [project](https://light.princeton.edu/publication/array-hsi/), [code](https://github.com/princeton-computational-imaging/Array-HSI)
- 2024 Spatially varying nanophotonic neural networks. [paper](https://www.science.org/doi/full/10.1126/sciadv.adp0391), [project](https://light.princeton.edu/publication/svn3/), [code](https://github.com/princeton-computational-imaging/SVN3)

### 2. Ray tracing model

Ray tracing is the most common technique in optical design (e.g., ZEMAX and CodeV). In the field of deep optics, people usually compute the point spread function (PSF) and convolve it with the input, or perform ray-tracing-based rendering to simulate sensor images. Most ray tracing works are incoherent, but there are also some works of coherent ray tracing.

#### Lens (to optical design)

- 2021 dO: A differentiable engine for Deep Lens design of computational imaging systems. [paper](https://ieeexplore.ieee.org/stamp/stamp.jsp?arnumber=9919421), [project](https://vccimaging.org/Publications/Wang2022DiffOptics/), [code](https://github.com/vccimaging/DiffOptics)
- 2022 Computational Optics for Mobile Terminals in Mass Production. [paper](https://ieeexplore.ieee.org/stamp/stamp.jsp?tp=&arnumber=9864277)
- 2022 The Differentiable Lens: Compound Lens Search over Glass Surfaces and Materials for Object Detection. [paper](https://arxiv.org/abs/2212.04441), [code](https://github.com/princeton-computational-imaging/joint-lens-design)
- **2023 Curriculum Learning for ab initio Deep Learned Refractive Optics.** [paper](https://arxiv.org/abs/2302.01089), [video](https://youtu.be/32XuSyM-J-8), [code](https://github.com/singer-yang/DeepLens)
- 2023 Large depth-of-field ultra-compact microscope by progressive optimization and deep learning. [paper](https://www.nature.com/articles/s41467-023-39860-0), [code](https://github.com/yuanlong-o/mobilephone_EDOF)

### 3. Network Representation

Model a group of optical systems by a network. The network takes optical parameters (e.g., curvatures) as input and outputs the PSF. We can back-propagate gradients through the network to get the gradients to update input parameters.

#### Lens (to computational photography)

- 2021 Deep learning-enabled framework for automatic lens design starting point generation. [paper](https://opg.optica.org/DirectPDFAccess/3CCFC208-3A65-4ABB-8B196EC9543FBAD5_446872/oe-29-3-3841.pdf?da=1&id=446872&seq=0&mobile=no), [project](https://lensnet.herokuapp.com/)
- **2021 Differentiable Compound Optics and Processing Pipeline Optimization for End-To-end Camera Design.** [paper](https://light.cs.princeton.edu/wp-content/uploads/2021/02/DeepCompoundOptics.pdf), [project](https://light.princeton.edu/publication/deep_compound_optics/)
- 2023 Aberration-Aware Depth-from-Focus. [paper](https://singer-yang.github.io/papers/AberAwareDfF.pdf), [supp](https://singer-yang.github.io/papers/AberAwareDfF_supp.pdf), [project](https://vccimaging.org/Publications/Yang2023AATDfF), [code](https://github.com/singer-yang/Aberration-Aware-Depth-from-Focus)

#### Lithography (to computational photolithography)

- **2023 Close the Design-to-Manufacturing Gap in Computational Optics with a 'Real2Sim' Learned Two-Photon Neural Lithography Simulator.** [paper](https://dl.acm.org/doi/pdf/10.1145/3610548.3618251), [supp](https://dl.acm.org/doi/abs/10.1145/3610548.3618251), [project](https://github.com/Neural-Litho/Neural_Lithography?tab=readme-ov-file), [code](https://github.com/Neural-Litho/Neural_Lithography)

### 4. Hybrid model

Hybrid ray tracing and wave propagation model for refractive-diffractive optical systems.

#### Lens

- 2023 Metalens enhanced ray optics: an end-to-end wave-ray co-optimization framework. [paper](https://opg.optica.org/oe/fulltext.cfm?uri=oe-31-16-26054&id=535358)
- **2024 End-to-End Hybrid Refractive-Diffractive Lens Design with Differentiable Ray-Wave Model.** [paper](https://dl.acm.org/doi/10.1145/3680528.3687640), [code](https://github.com/singer-yang/DeepLens)

## Contribution

Please feel free to open pull requests or email (xinge.yang@kaust.edu.sa) to contibute to this repo.

## Licenses

License

[![CC0](http://i.creativecommons.org/p/zero/1.0/88x31.png)](http://creativecommons.org/publicdomain/zero/1.0/)

To the extent possible under law, [Xinge Yang](https://singer-yang.github.io/) has waived all copyright and related or neighboring rights to this work.
