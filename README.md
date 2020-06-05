# Federated Triplet Loss

Paper: _Augenstein, Sean, H. Brendan McMahan, Daniel Ramage, Swaroop Ramaswamy, Peter Kairouz, Mingqing Chen, Rajiv Mathews, and Blaise Aguera y Arcas_. 2019. [“Generative Models for Effective ML on Private, Decentralized Datasets”](https://arxiv.org/abs/1911.06679)

## Demos

### Ablation for differentially private federated GAN

![Ablation results](./docs/ablation_results.gif)

- [`./demos/federated-gan-training-loop.ipynb`](./demos/federated-gan-training-loop.ipynb): training a federated GAN on Colab
- [`./demos/ablation-results.ipynb`](./demos/ablation-results.ipynb): visualizing the runs

#### Examples of successful convergence after 1000 rounds

- `dp_l2_norm_clip`: **0.1**, `dp_noise_multiplier`: **0.01**

  - **Sample**:

    ![](./docs/0.1_0.01.png)

  - **Log**:

    ![](docs/0.1_0.01_tensorboard.png)

- `dp_l2_norm_clip`: **0.08036**, `dp_noise_multiplier`: **0.00555**

  - **Sample**:

    ![](./docs/0.08035796650374172_0.00555296000118007.png)

  - **Log**:

    ![](docs/0.08035796650374172_0.00555296000118007_tensorboard.png)

- `dp_l2_norm_clip`: **0.105667**, `dp_noise_multiplier`: **0.001130**

  - **Sample**

    ![](./docs/0.10566677867136223_0.0011304778440122771.png)

  - **Log**

    ![](./docs/0.10566677867136223_0.0011304778440122771_tensorboard.png)

#### Examples of unsuccessful convergence after 1000 rounds

- `dp_l2_norm_clip`: **0.119396**, `dp_noise_multiplier`: **0.064232**

  - **Sample**

    ![](./docs/0.1193956099396842_0.06423220094293745.png)

  - **Log**

    ![](./docs/0.1193956099396842_0.06423220094293745_tensorboard.png)

- `dp_l2_norm_clip`: **2.408976**, `dp_noise_multiplier`: **0.386463**

  - **Sample**

    ![](./docs/2.408975881783719_0.3864631885252761.png)

    The model diverged early in the process:

    - Round 120

      ![](./docs/2.408975881783719_0.3864631885252761_00120.png)

    - Round 130

      ![](./docs/2.408975881783719_0.3864631885252761_00130.png)

  - **Log**

    ![](./docs/2.408975881783719_0.3864631885252761_tensorboard.png)
