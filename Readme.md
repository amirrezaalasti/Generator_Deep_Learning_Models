# Deep Learning Foundations Project

This repository contains solutions for the "Deep Learning Foundations" course project, focusing on implementing and training Deep Convolutional Generative Adversarial Networks (DCGANs) and Variational Autoencoders (VAEs) for image synthesis tasks. The project is structured as follows:

## Repository Structure

- `DC_GAN.ipynb`: Jupyter Notebook implementing the DCGAN architecture, training process, and evaluation on the Fashion-MNIST dataset.
- `VAE.ipynb`: Jupyter Notebook implementing the VAE architecture, training process, and evaluation on the CIFAR-10 dataset.
- `tensorboard.sh`: Shell script to launch TensorBoard for monitoring training progress.
- `images/DC-GAN-LOSS.png`, `images/GAN.png`, `images/VAE-loss-function.png`: Images depicting loss functions and model architectures used in the project.
- `data/`: Directory containing datasets used for training and evaluation.
- `runs/`: Directory storing TensorBoard logs for training visualization.

## Project Tasks

### 1. Deep Convolutional Generative Adversarial Network (DCGAN)

- **Data Loading and Preprocessing**:
  - Utilized the Fashion-MNIST dataset, a collection of Zalando’s article images.
  - Implemented a data loading pipeline for DCGAN training, including normalization and preparation steps.
  - Visualized samples from different classes to understand data format and dimensions.

- **DCGAN Architecture**:
  - Designed and implemented the generator and discriminator architectures for image synthesis.
  - Discussed design choices, including layer configurations and activation functions.

- **Training**:
  - Experimented with different weight initialization methods to assess their impact on training.
  - Implemented the training loop for DCGAN and trained the model.
  - Explained the adversarial loss function used for GAN training.
  - Monitored training progress using TensorBoard:
    - Plotted generator and discriminator losses over training iterations.
    - Visualized generator outputs on a fixed noise batch for each epoch.

- **Evaluation**:
  - Qualitatively evaluated the generative performance by visualizing newly generated samples.
  - Addressed challenges encountered during training, such as mode collapse and training instability.

### 2. Variational Autoencoder (VAE)

- **Data Loading and Visualization**:
  - Loaded the CIFAR-10 dataset, comprising 32x32 color images across 10 classes.
  - Displayed sample images to understand data characteristics.

- **VAE Architecture**:
  - Implemented encoder and decoder networks to form the VAE, adapting architectures to accommodate CIFAR-10's image size and color channels.
  - Selected an appropriate number of latent dimensions and justified design choices.

- **Loss Function**:
  - Explained the combined reconstruction and KL divergence loss function used for VAE training.

- **Training and Evaluation**:
  - Trained the VAE over multiple epochs.
  - Compared input and reconstructed images after each epoch to assess model performance.

### 3. Pen & Paper Exercises

- **Reparameterization Trick**:
  - Explained the reparameterization trick and its role in enabling gradient-based optimization in VAEs.

- **Challenges in GAN Optimization**:
  - Discussed difficulties in GAN training, such as convergence issues and mode collapse.
  - Explored common techniques to improve training stability, including learning rate adjustments and architectural modifications.

- **Comparison of GANs and VAEs**:
  - Compared the strengths and weaknesses of GANs and VAEs.
  - Discussed scenarios where one model may be preferred over the other.

## Requirements

- Python 3.x
- PyTorch
- torchvision
- TensorBoard
- Jupyter Notebook

## Usage

1. **Clone the Repository**:

   ```bash
   git clone https://github.com/DevNerds2020/Generator_Deep_Learning_Models.git
   cd Generator_Deep_Learning_Models
   ```

2. **Set Up the Environment**:

   Ensure all required packages are installed:

   ```bash
   pip install torch torchvision tensorboard jupyter
   ```

3. **Run Jupyter Notebooks**:

   Launch Jupyter Notebook:

   ```bash
   jupyter notebook
   ```

   Open and execute the `DC_GAN.ipynb` and `VAE.ipynb` notebooks to explore the implementations.

4. **Monitor Training with TensorBoard**:

   Start TensorBoard to visualize training progress:

   ```bash
   ./tensorboard.sh
   ```

   Access TensorBoard at `http://localhost:6006/`.

*Winter Semester 2024/25*

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details. 