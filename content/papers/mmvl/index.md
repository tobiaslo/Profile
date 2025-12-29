---
title: "Multi Map Visual Localization for Unmanned Aerial Vehicles" 
date: 2024-12-16
url: /paper/mmvl
aliases: 
    - /old_url.html
tags: ["UAV", "Absolute visual localization", "localization", "Monte Carlo localization", "CNN"]
author: ["Tobias Lømo", "Jim Torresen", "Mariana Kolberg", "Renan Maffei"]
description: "Paper description for search engines (less than 155 characters)" 
summary: "Absolute visual localization using ResNet, multiple sattelite images and Monte Carlo localization."
cover:
    image: "System.png"
    alt: "Figure title (preferably 1280x720 pixels)"
    relative: true
editPost:
    URL: "https://doi.org/10.1109/LRA.2024.3518071"
    Text: "IEEE RA-L"

---

---

##### Download:

- [Paper](https://ieeexplore.ieee.org/abstract/document/10803035)
- [Code and data](https://github.com/tobiaslo/MMVL)

---

##### Abstract:

Localization has long been an essential area of research within robotics. The popularity of using Unmanned Aerial Vehicles (UAVs) to solve different tasks has increased and is expected to continue. Developing a robust complementary system to the Global Navigation Satellite Systems (GNSS) used today has been researched, and visual localization using cameras and satellite images is a popular choice to use. One of the challenges with using satellite images is that different images over the same area can impact the system's performance. This article proposes a novel approach called Multi Map Visual Localization (MMVL), a method to use multiple satellite images simultaneously, which is combined using a weighted average of probability maps. The proposal uses a convolutional neural network (CNN) with a caching strategy together with Monto Carlo Localization (MCL). MMVL achieves excellent robustness compared to other approaches and manages to estimate the correct location on all test flights. At the same time, using multiple satellite images does not significantly impact accuracy and computation time.

---

##### Figure X:  Figure title

![](System.pdf)

---

##### Citation

T. Lømo, J. Torresen, M. Kolberg and R. Maffei, "Multi Map Visual Localization for Unmanned Aerial Vehicles," in IEEE Robotics and Automation Letters, vol. 10, no. 2, pp. 1353-1360, Feb. 2025, doi: 10.1109/LRA.2024.3518071.

```BibTeX
@ARTICLE{10803035,
  author={Lømo, Tobias and Torresen, Jim and Kolberg, Mariana and Maffei, Renan},
  journal={IEEE Robotics and Automation Letters}, 
  title={Multi Map Visual Localization for Unmanned Aerial Vehicles}, 
  year={2025},
  volume={10},
  number={2},
  pages={1353-1360},
  doi={10.1109/LRA.2024.3518071}}

```
