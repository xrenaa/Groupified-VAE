# GroupifyVAE: from Group-based  Definition to VAE-based Unsupervised Representation Disentanglement

> **GroupifyVAE: from Group-based  Definition to VAE-based Unsupervised Representation Disentanglement** <br>
> Tao Yang, Xuanchi Ren, Yuwang Wang, Wenjun Zeng, Nanning Zheng and Pengju Ren <br>
> *arXiv preprint arXiv:2007.06600*<br>
> 
[[Paper]()]
[[Appendix](./GroupifyNet_ICML_2021_appendix.pdf)]
[[Demo]()]

In this repo, we propose a specific form of the **group-based definition** and prove its two equivalent conditions: **isomorphism** and ``the constancy of permutations''. And the inceptaul framework is as follows

![image](./images/theoritcal_framework.png)

We further provide an implementation of **isomorphism** based on two Group constraints: the Abel constraint for the exchangeability and Order constraint for the cyclicity. We then convert them into a **self-supervised training loss** that can be incorporated into VAE-based models to **bridge their gaps** from the Group Theory based definition. The overview of our method is as follows:

![image](./images/Overview.png)


## Qualitative evaluation
| dSprites | |
| :---: | :---: |
| BetaVAE | DCI |
| ![image](./images/beta_an.png) | ![image](./images/dci_an.png) |
| MIG | FactorVAE |
| ![image](./images/mig_an.png) | ![image](./images/factor_an.png) |

**NOTE:** Groupified VAE achieves better performance mean with lower variance.

## Latent space visualization
| dSprites AnnealVAE |  |
| :---: | :---: |
| $C_{max} = 10$, Original | $C_max = 20$, Original|
| ![image](./images/88latent.png) | ![image](./images/168latent.png) |
| $C_{max} = 10$, Groupified | $C_{max} = 20$, Groupified |
| ![image](./images/98latent.png) | ![image](./images/178latent.png) |

## Qualitative results
|Cars3d and Shapes3d | |
| :---: | :---: |
| Original | Groupified|
| ![image](./images/compare_no_group.png) | ![image](./images/compare_group.png) |


## Controllable meaningful dimensions in Groupified VAEs
| dSprites Anneal VAE | |
| :---: | :---: |
| KL divergence of dimensions | Traversal results |
| ![image](./images/253kl.png) | <img src= ./images/253traver.png width="1000px"> |

## Downstream Task Performance
![image](./images/downstream.PNG)




## BibTeX

```bibtex
@article{Tao2021groupified,
  title   = {GroupifyVAE: from Group-based  Definition to VAE-based Unsupervised Representation Disentanglement},
  author  = {Tao, Yang and Xuanchi, Ren and Yuwang, Wang and Wenjun, Zeng and Nanning, Zheng and Pengju,Ren},
  journal = {arXiv preprint arXiv:2007.06600},
  year    = {2021}
}
```
