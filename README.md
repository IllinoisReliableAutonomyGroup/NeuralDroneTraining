# NeuralDroneTraining
NeRF and Gaussian Splat environments for Training Quadrotor

## Installation
### Prerequisites
Ensure you have the following installed:
- Python >= 3.8
- PyTorch 2.1.2 with CUDA 11.8
- NVIDIA CUDA Toolkit (for GPU acceleration)
- AirSim (for drone simulation)
- NeRF & Gaussian Splatting dependencies

### Create Environment
```bash
conda create --name nerfstudio -y python=3.8
conda activate nerfstudio
python -m pip install --upgrade pip
```

### Dependencies
#### PyTorch
If a PyTorch version prior to 2.0.1 is installed, uninstall previous versions:
```bash
pip uninstall torch torchvision functorch tinycudann
```

#### Recommended: PyTorch 2.1.2 with CUDA 11.8
```bash
pip install torch==2.1.2+cu118 torchvision==0.16.2+cu118 --extra-index-url https://download.pytorch.org/whl/cu118
```

To build necessary CUDA extensions, install cuda-toolkit with conda:
```bash
conda install -c "nvidia/label/cuda-11.8.0" cuda-toolkit
```

#### Alternative: PyTorch 2.0.1 with CUDA 11.7 and tiny-cuda-nn
##### Linux:
```bash
pip install ninja git+https://github.com/NVlabs/tiny-cuda-nn/#subdirectory=bindings/torch
```

##### Windows:
Follow similar steps as above with Windows-compatible paths.

### Installing Nerfstudio
#### From pip:
```bash
pip install nerfstudio
```

#### From Source (Latest Development Version):
```bash
git clone https://github.com/nerfstudio-project/nerfstudio.git
cd nerfstudio
pip install --upgrade pip setuptools
pip install -e .
```


