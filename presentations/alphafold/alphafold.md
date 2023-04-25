---
marp: true
title: How AlphaFold was made possible
theme: gaia
style: |
  .small-text {
    font-size: 0.5rem;
  }
paginate: true
footer: 'Gaetan De Waele'
math: katex
---
<style>
  :root {
    --color-background: #eff1f5;
    --color-foreground: #4c4f69;
    --color-highlight: #4c4f69;
    --color-dimmed: #4c4f69;
  }
  img[alt~="center"] {
  display: block;
  margin: 0 auto;
  }
</style>

# How AlphaFold was made possible

#### Overview of talk
    
1. Protein structures
2. MSAs
3. $SE(3)$ Equivariance
4. The model
5. Future perspectives


`Exclaimer: The discussed parts of AF are extremely cherry-picked`

----

## 1. Protein structure prediction

![width:1100px center](https://wou.edu/chemistry/files/2017/05/protein-sequence.png)

![width:600px center](https://raw.githubusercontent.com/gdewael/teaching/main/presentations/alphafold/img/proteinstructure.png)

----

## 2. Using MSAs

![width:500px center](https://bioinf.comav.upv.es/courses/biotech3/_images/alig_mul_prot.png)

<p>
<center>
  <img src="https://critter.science/wp-content/uploads/2020/05/quokka1.png" width="370" />
  <img src="https://www.nature.com/scitable/content/ne0000/ne0000/ne0000/ne0000/14704938/U1CP1-2_SelectiveTransport_ksm.jpg" width="240" /> 
  <img src="https://img.thedailybeast.com/image/upload/v1679431891/230321-Thompson-Goblin-Shark-tease_zha1he.jpg" width="410" />
  </center>
</p>

----

## 2. Using MSAs

Given to model as multi-dimensional input

![width:600px center](https://raw.githubusercontent.com/gdewael/teaching/main/presentations/alphafold/img/inputs.png)

----

## 3. Grounding in 3D space

AlphaFold works by refining 3D coordinates of every amino acid

![width:700px center](https://digitalpress.fra1.cdn.digitaloceanspaces.com/iyuft7l/2021/08/AlphaFold2.jpg)



----

## 3. Grounding in 3D space

Geometric intuition:
Convolutions are **equivariant** to translations $T(2)$

![width:600px center](https://lh5.googleusercontent.com/U33fg5Nd6JDowuhXjqLveJbkG7al0zl7HId-uZ5oYk7QCrQbyW2o78GGbcpTWhIESEGMz10J-M-ZEiCtaQOwscbrodNpG6giGW702-19PDP9eLwfjKgNa-0_kZbHJjkPNWtCwk3IDGA8pmgJ31Yfdfk)

----

## 3. Grounding in 3D space

Geometric intuition:
Similarly, operations on molecules should be **equivariant** to $SE(3)$, which includes translations and rotations in 3D euclidean space.

![width:600px center](https://raw.githubusercontent.com/gdewael/teaching/main/presentations/alphafold/img/SE3_transformers.png)

Through modified self-attention (transformer)

----

## 4. Putting it together


![width:1000px center](https://i0.wp.com/www.blopig.com/blog/wp-content/uploads/2021/07/image-3.png?ssl=1)

----

## What's next

Learning interactions: Deep learning :handshake: Structural/physical models

![width:1000px center](https://www.researchgate.net/profile/Gabriele-Corso/publication/364163314/figure/fig1/AS:11431281088008531@1664947354076/Overview-of-DIFFDOCK-Left-The-model-takes-as-input-the-separate-ligand-and-protein.png)

----

## What's next

Learning interactions: Deep learning :handshake: Structural/physical models
![width:1000px center](https://www.marktechpost.com/wp-content/uploads/2022/07/Screen-Shot-2022-07-15-at-4.00.19-PM.png
)
