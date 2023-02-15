# LSGAN (ICCV'2017)

> [Least Squares Generative Adversarial Networks](https://openaccess.thecvf.com/content_iccv_2017/html/Mao_Least_Squares_Generative_ICCV_2017_paper.html)

> **Task**: Unconditional GANs

<!-- [ALGORITHM] -->

## Abstract

<!-- [ABSTRACT] -->

Unsupervised learning with generative adversarial networks (GANs) has proven hugely successful. Regular GANs hypothesize the discriminator as a classifier with the sigmoid cross entropy loss function. However, we found that this loss function may lead to the vanishing gradients problem during the learning process. To overcome such a problem, we propose in this paper the Least Squares Generative Adversarial Networks (LSGANs) which adopt the least squares loss function for the discriminator. We show that minimizing the objective function of LSGAN yields minimizing the Pearson χ2 divergence. There are two benefits of LSGANs over regular GANs. First, LSGANs are able to generate higher quality images than regular GANs. Second, LSGANs perform more stable during the learning process. We evaluate LSGANs on five scene datasets and the experimental results show that the images generated by LSGANs are of better quality than the ones generated by regular GANs. We also conduct two comparison experiments between LSGANs and regular GANs to illustrate the stability of LSGANs.

<!-- [IMAGE] -->

<div align=center>
<img src="https://user-images.githubusercontent.com/28132635/143052264-afd97b91-5fd1-4134-ad4d-529e364fdcc8.JPG"/>
</div>

## Results and models

<div align="center">
  <b> LSGAN 64x64, CelebA-Cropped</b>
  <br/>
  <img src="https://user-images.githubusercontent.com/22982797/116498716-f4e74200-a8dc-11eb-9c28-5549d96e20a6.png" width="800"/>
</div>

|    Models     |    Dataset     |               SWD               | MS-SSIM |   FID   |                             Config                              |                             Download                              |
| :-----------: | :------------: | :-----------------------------: | :-----: | :-----: | :-------------------------------------------------------------: | :---------------------------------------------------------------: |
|  LSGAN 64x64  | CelebA-Cropped |     6.16, 6.83, 37.64/16.87     | 0.3216  | 11.9258 | [config](./lsgan_dcgan-archi_lr1e-3-1xb128-12Mimgs_celeba-cropped-64x64.py) | [model](https://download.openmmlab.com/mmediting/lsgan/lsgan_celeba-cropped_dcgan-archi_lr-1e-3_64_b128x1_12m_20210429_144001-92ca1d0d.pth)\| [log](https://download.openmmlab.com/mmediting/lsgan/lsgan_celeba-cropped_dcgan-archi_lr-1e-3_64_b128x1_12m_20210422_131925.log.json) |
|  LSGAN 64x64  |  LSUN-Bedroom  |      5.66, 9.0, 18.6/11.09      | 0.0671  | 30.7390 | [config](./lsgan_dcgan-archi_lr1e-4-1xb128-12Mimgs_lsun-bedroom-64x64.py) | [model](https://download.openmmlab.com/mmediting/lsgan/lsgan_lsun-bedroom_dcgan-archi_lr-1e-4_64_b128x1_12m_20210429_144602-ec4ec6bb.pth)\| [log](https://download.openmmlab.com/mmediting/lsgan/lsgan_lsun-bedroom_dcgan-archi_lr-1e-4_64_b128x1_12m_20210423_005020.log.json) |
| LSGAN 128x128 | CelebA-Cropped | 21.66, 9.83, 16.06, 70.76/29.58 | 0.3691  | 38.3752 | [config](./lsgan_dcgan-archi_lr1e-4-1xb64-10Mimgs_celeba-cropped-128x128.py) | [model](https://download.openmmlab.com/mmediting/lsgan/lsgan_celeba-cropped_dcgan-archi_lr-1e-4_128_b64x1_10m_20210429_144229-01ba67dc.pth)\| [log](https://download.openmmlab.com/mmediting/lsgan/lsgan_celeba-cropped_dcgan-archi_lr-1e-4_128_b64x1_10m_20210423_132126.log.json) |
| LSGAN 128x128 |  LSUN-Bedroom  |  19.52, 9.99, 7.48, 14.3/12.82  | 0.0612  | 51.5500 | [config](./lsgan_lsgan-archi_lr1e-4-1xb64-10Mimgs_lsun-bedroom-128x128.py) | [model](https://download.openmmlab.com/mmediting/lsgan/lsgan_lsun-bedroom_lsgan-archi_lr-1e-4_128_b64x1_10m_20210429_155605-cf78c0a8.pth)\| [log](https://download.openmmlab.com/mmediting/lsgan/lsgan_lsun-bedroom_lsgan-archi_lr-1e-4_128_b64x1_10m_20210429_142302.log.json) |

## Citation

```latex
@inproceedings{mao2017least,
  title={Least squares generative adversarial networks},
  author={Mao, Xudong and Li, Qing and Xie, Haoran and Lau, Raymond YK and Wang, Zhen and Paul Smolley, Stephen},
  booktitle={Proceedings of the IEEE international conference on computer vision},
  pages={2794--2802},
  year={2017},
  url={https://openaccess.thecvf.com/content_iccv_2017/html/Mao_Least_Squares_Generative_ICCV_2017_paper.html},
}
```