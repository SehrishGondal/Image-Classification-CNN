# Image Classification using CNN Models

## Overview
This repository contains code and resources for image classification tasks using Convolutional Neural Networks (CNNs) and other neural network architectures. It demonstrates a comprehensive comparison of different models on the MNIST dataset.

## Project Structure

- **Image_Classification(CNN).ipynb** - Jupyter notebook containing three different neural network implementations
  - Model 1: Single Hidden Layer Neural Network
  - Model 2: Multi-Layer Deep Neural Network (3 hidden layers)
  - Model 3: Convolutional Neural Network (CNN)

## Dataset

**MNIST (Modified National Institute of Standards and Technology)**
- 70,000 images of handwritten digits (0-9)
- 28×28 pixel grayscale images
- 60,000 training samples and 10,000 test samples
- Automatically downloaded from TensorFlow/Keras

## Prerequisites

Install the required libraries:
```bash
pip install tensorflow keras numpy jupyter
```

## Model Comparisons

### Model 1: Single Hidden Layer Network
- **Architecture**: 784 (input) → 128 (hidden) → 10 (output)
- **Activation**: ReLU (hidden), Softmax (output)
- **Test Accuracy**: ~57.42%
- **Training Epochs**: 50
- **Learning Rate**: 0.1

### Model 2: Multi-Layer Deep Network
- **Architecture**: 784 → 128 → 64 → 32 → 10
- **Activation**: ReLU (hidden layers), Softmax (output)
- **Test Accuracy**: ~92.05%
- **Training Epochs**: 50
- **Batch Size**: 64
- **Learning Rate**: 0.01
- **Key Feature**: Demonstrates benefits of deeper networks

### Model 3: Convolutional Neural Network (CNN)
- **Architecture**:
  - Conv2D (32 filters, 3×3) + ReLU
  - Conv2D (64 filters, 3×3) + ReLU
  - MaxPooling2D (2×2)
  - Conv2D (128 filters, 3×3) + ReLU
  - MaxPooling2D (2×2)
  - Flatten → Dense (128, ReLU) + Dropout (0.3) → Dense (64, ReLU) → Dense (10, Softmax)
- **Test Accuracy**: ~99.33%
- **Training Epochs**: 10
- **Batch Size**: 64
- **Optimizer**: Adam (learning_rate=0.001)
- **Key Feature**: Superior spatial feature extraction through convolutions

## Performance Summary

| Model | Accuracy | Speed | Architecture |
|-------|----------|-------|--------------|
| Single Hidden Layer | 57.42% | Fast | Simple |
| Deep Network (3 layers) | 92.05% | Medium | Complex |
| CNN | 99.33% | Medium | Convolutional |

## Key Learnings

1. **Depth Matters**: Adding more layers improved accuracy from 57% to 92%
2. **Convolution Power**: CNN's spatial awareness achieved 99.33% accuracy
3. **Dropout Prevention**: Dropout layer helps prevent overfitting in deeper networks
4. **Batch Processing**: Improves training stability and convergence
5. **Optimizer Selection**: Adam optimizer provides better convergence for CNN

## Usage

1. Clone the repository:
   ```bash
   git clone https://github.com/SehrishGondal/Image-Classification-CNN.git
   ```

2. Navigate to the repository:
   ```bash
   cd Image-Classification-CNN
   ```

3. Open the Jupyter notebook:
   ```bash
   jupyter notebook Image_Classification\(CNN\).ipynb
   ```

4. Run cells sequentially to:
   - Train Model 1 (Single Hidden Layer)
   - Train Model 2 (Deep Network)
   - Train Model 3 (CNN)
   - Compare results

## How CNNs Work for Image Classification

Convolutional Neural Networks are specifically designed for image processing:

- **Convolutional Layers**: Automatically learn spatial features (edges, shapes, patterns)
- **Pooling Layers**: Reduce dimensionality while preserving important features
- **Flattening**: Converts 2D feature maps to 1D vector for dense layers
- **Dense Layers**: Learn high-level patterns and make final predictions

## Results Interpretation

The CNN model achieves **99.33% accuracy** because:
- Convolutional filters capture local image features
- Multiple layers learn hierarchical representations
- Max pooling reduces noise and computational overhead
- Dropout prevents overfitting during training

## Future Improvements

- Implement data augmentation (rotation, translation, scaling)
- Test on more complex datasets (CIFAR-10, ImageNet)
- Experiment with advanced architectures (ResNet, VGG, MobileNet)
- Add visualization of learned convolutional filters
- Implement early stopping and learning rate scheduling
- Deploy model as a web service

## Technologies Used

- **Python 3.x**
- **TensorFlow/Keras** - Deep learning framework
- **NumPy** - Numerical computing
- **Jupyter Notebook** - Interactive development

## License

This project is open source and available under the MIT License.

## Author

**Sehrish Gondal**

---

**Note**: This is an educational project demonstrating the effectiveness of different neural network architectures for image classification, with emphasis on how CNNs provide superior performance for visual tasks.
