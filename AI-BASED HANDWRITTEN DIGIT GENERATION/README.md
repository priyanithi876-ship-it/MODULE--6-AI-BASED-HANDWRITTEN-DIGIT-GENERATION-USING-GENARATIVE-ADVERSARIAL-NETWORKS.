# AI-Based Handwritten Digit Generation Using Generative Adversarial Networks (GAN)

**Module:** 6 – Generative Deep Learning Applications  
**GitHub Repository:** `MODULE--6-AI-BASED-HANDWRITTEN-DIGIT-GENERATION-USING-GENERATIVE-ADVERSARIAL-NETWORK`  
**Project Folder:** `AI-BASED HANDWRITTEN DIGIT GENERATION`

## 1. Project Overview

This project generates handwritten digit images using a Generative Adversarial Network (GAN) trained on the MNIST dataset. It contains two neural networks: a Generator and a Discriminator. The Generator creates digit-like images from random noise, while the Discriminator learns to distinguish real MNIST images from generated images. Through adversarial training, both networks improve.

## 2. Project Objectives

- Load and preprocess the MNIST dataset.
- Build a Generator neural network.
- Build a Discriminator neural network.
- Train both networks using adversarial learning.
- Generate new handwritten digit images.
- Visualize training progress using loss curves.
- Inspect and compare generated images.

## 3. Dataset Details

- **Dataset:** MNIST Handwritten Digits
- **Source:** TensorFlow/Keras built-in dataset
- **Training images:** 60,000
- **Testing images:** 10,000
- **Image dimensions:** 28 × 28 pixels
- **Image type:** Grayscale
- **Classes:** Digits 0–9

The training images are converted to `float32`, normalized to `[-1, 1]`, and reshaped to `(28, 28, 1)`.

## 4. Technologies and Libraries

- Python
- TensorFlow / Keras
- NumPy
- Matplotlib
- Jupyter Notebook / Google Colab

## 5. Skill Taxonomy

- **Data Preparation:** Loading, normalization, and reshaping
- **Deep Learning:** Neural network architecture
- **Generative AI:** Generator and Discriminator
- **GAN Training:** Adversarial learning and optimization
- **Evaluation:** Generated images and loss analysis
- **Analysis:** Training behaviour and challenges
- **Reporting:** Documentation and conclusions

## 6. Project Tasks

### Task 1: Data Loading and Preprocessing
- Import the required libraries.
- Load MNIST.
- Display sample images.
- Normalize pixel values to `[-1, 1]`.
- Reshape images to `(28, 28, 1)`.
- Verify the dataset shape and data type.

### Task 2: Generator Network
- Accept a 100-dimensional random noise vector.
- Use Dense, BatchNormalization, and LeakyReLU layers.
- Use Conv2DTranspose layers to upsample feature maps.
- Generate 28 × 28 grayscale images with a Tanh output activation.

### Task 3: Discriminator Network
- Accept 28 × 28 grayscale images.
- Use Conv2D, LeakyReLU, and Dropout layers.
- Use Flatten and Dense layers.
- Produce a real/fake probability using Sigmoid activation.
- Use Binary Cross-Entropy loss and the Adam optimizer.

### Task 4: GAN Training
- Prepare a shuffled and batched TensorFlow dataset.
- Define Generator and Discriminator loss functions.
- Train both networks using gradient updates.
- Use Adam optimizers with learning rate `0.0002` and `beta_1=0.5`.
- Train for 20 epochs.
- Display generated samples during training.
- Record and plot both loss histories.

### Task 5: Image Generation and Evaluation
- Generate images from random noise using the trained Generator.
- Display a 5 × 5 grid of generated images.
- Save the generated image grid.
- Plot and save Generator and Discriminator loss curves.
- Evaluate generated images using the Discriminator.
- Compare real MNIST samples with generated samples.
- Review losses and generated image quality.

## 7. Model Architecture

### Generator
Maps a 100-dimensional noise vector to a 28 × 28 × 1 image.

Main components:
- Dense
- BatchNormalization
- LeakyReLU
- Reshape
- Conv2DTranspose
- Tanh output activation

### Discriminator
Receives a 28 × 28 × 1 image and predicts whether it is real or generated.

Main components:
- Conv2D
- LeakyReLU
- Dropout
- Flatten
- Dense output
- Sigmoid activation

## 8. Training Configuration

| Parameter | Value |
|---|---|
| Dataset | MNIST |
| Noise dimension | 100 |
| Image size | 28 × 28 × 1 |
| Batch size | 256 |
| Epochs | 20 |
| Learning rate | 0.0002 |
| Adam beta_1 | 0.5 |
| Loss function | Binary Cross-Entropy |
| Optimizer | Adam |

## 9. Evaluation Guidelines

Evaluate the project using the following:

- Inspect the generated digit image samples.
- Compare generated images with real MNIST samples.
- Review Generator and Discriminator loss graphs.
- Describe the training behaviour and generated image quality.
- Mention observed challenges and possible improvements.

Loss values alone do not establish image quality. Record conclusions based on the actual notebook outputs; do not invent metrics or results.

## 10. Project Outputs

The `GAN_Results` folder should contain:

- `generated_digits.png` — grid of generated handwritten digits
- `gan_loss_curves.png` — Generator and Discriminator loss curves

## 11. Results and Analysis

The Generator learns to create images from random noise, while the Discriminator learns to distinguish real images from generated images. Generated samples and loss curves help inspect training progress.

**Complete this section after running the notebook:** describe the generated samples, observed loss behaviour, challenges encountered, and any improvements you would try. Only report observations supported by your actual results.

## 12. Conclusion

This project demonstrates handwritten digit generation using Generative Adversarial Networks. It provides practice in image preprocessing, deep-learning architecture design, adversarial training, image generation, visualization, and evaluation.

## 13. How to Run

1. Open the notebook in Google Colab or Jupyter Notebook.
2. Install the required libraries if needed:

   ```bash
   pip install tensorflow numpy matplotlib jupyter
   ```
3. Run the notebook cells in order, from Task 1 through Task 5.
4. Allow training to complete.
5. Review generated images and loss graphs.
6. Confirm the output files are saved in `GAN_Results`.

**Note:** Run the notebook from top to bottom in the same runtime because later tasks depend on variables and models created earlier.

## 14. Project Folder Structure

```text
AI-BASED HANDWRITTEN DIGIT GENERATION/
├── GAN_Project.ipynb
├── README.md
└── GAN_Results/
    ├── generated_digits.png
    └── gan_loss_curves.png
```

Replace `GAN_Project.ipynb` with the actual notebook filename if it is different.

## 15. GitHub Deliverables

Submit the complete project through the GitHub repository. Ensure the repository contains:

- Jupyter Notebook (`.ipynb`) with code and executed outputs
- Dataset details
- GAN preprocessing
- Generator implementation
- Discriminator implementation
- Training implementation
- Generated image samples
- Generator and Discriminator loss graphs
- `README.md`

Before submitting, check that the notebook runs successfully and the generated output images are included in the repository.
