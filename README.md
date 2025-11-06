## Installation

### System Requirements
- Recommended: Ubuntu 20.04
- CUDA: 11.7

### Environment Setup
1. Install Anaconda as your package manager.
2. Create a dedicated virtual environment with Python 3.8.19:
   ```
   conda create -n your_env_name python=3.8.19
   conda activate your_env_name
   ```
3. Install PyTorch 1.13.1 and its related components. For CUDA 11.7 support, use:
   ```
   pip install torch==1.13.1+cu117 torchvision==0.14.1+cu117 torchaudio==0.13.1 --extra-index-url https://download.pytorch.org/whl/cu117
   ```
4. Install Ultralytics:
   ```
   pip install ultralytics
   ```
5. Install additional required packages:
   ```
   pip install timm==1.0.7 thop efficientnet_pytorch==0.7.1 einops grad-cam==1.5.4 dill==0.3.8 albumentations==1.4.11 pytorch_wavelets==1.3.0 tidecv PyWavelets opencv-python prettytable -i https://pypi.tuna.tsinghua.edu.cn/simple
   ```

## Usage

This repository includes several scripts for training, evaluating, and analyzing models.

- **train.py**: Script for training the model. Specify the YAML file for the model configuration and the YAML file containing the dataset paths.


- **val.py**: Script for evaluating metrics on a trained model. Specify the weights file generated from training to test detection accuracy.


- **get_FPS.py**: Script for calculating model storage size, inference time, and FPS.


- **heatmap.py**: Script for generating heatmaps.
