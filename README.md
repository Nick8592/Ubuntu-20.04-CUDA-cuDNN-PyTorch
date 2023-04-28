# Ubuntu-20.04-CUDA-cuDNN-PyTorch
中文版本(https://traveling-process-89d.notion.site/Ubuntu-20-04-DeepLearning-655e63dc86aa4edea87600decccb3237)

## Results
| Name | Version |
|---|---|
| Ubuntu | 20.04 |
| GPU | GTX 1080Ti |
| NVIDIA Driver | 515.65.01 |
| CUDA | 10.1 |
| cuDNN |   |
| PyTorch | 1.4 |

## Structure
- **Bottom Layer:**  
CUDA, cuDNN (cuDNN should be selected according to the CUDA version).   
- **Virtual Environments:**  
Established by Anaconda, the environment can be set according to the needs, such as the Python version, PyTorch version, but also should be selected according to the CUDA version.   

## Outline
1. NVIDIA Driver installation
2. CUDA installation
3. cuDNN installatioin
4. Anaconda3 installatioin
5. PyTorch installation

## Instruction
### 1. NVIDIA Driver installation

**Open Software & Updates Application**  
![Software & Updates app](https://github.com/nick8592/Ubuntu-20.04-CUDA-cuDNN-PyTorch/blob/main/images/software%26update.png)  

Select the Additional Drivers field, and then select the version you want (except -server). After selecting, press Apply Changes, and the new Driver will be installed.  
![NVIDIA Driver Select](https://github.com/nick8592/Ubuntu-20.04-CUDA-cuDNN-PyTorch/blob/main/images/nvidia_driver.png)  

After installation, you will be asked to restart, open terminal and type in  
```
sudo reboot
```

After restarting, open the terminal and enter the following commands to check if the Driver Version is correct. The CUDA version in the upper right corner can be ignored because we haven't installed it yet.  
```
nvidia-smi
```
![nvidia-smi](https://github.com/nick8592/Ubuntu-20.04-CUDA-cuDNN-PyTorch/blob/main/images/nvidia-smi.png)

### 2. CUDA installation 
(https://mikethreeacer.medium.com/ubuntu-18-04-安裝-cuda-cudnn-anaconda-pytorch-1f170b3326a4#1b0a)  
You can follow the above URL "2. Install CUDA 11.2.2" section to install.   

### 3. cuDNN installatioin 
(https://mikethreeacer.medium.com/ubuntu-18-04-安裝-cuda-cudnn-anaconda-pytorch-1f170b3326a4#1b0a)  
You can follow the above URL "2. Install cuDNN" section to install.   


### 4. Anaconda3 installation 
(https://www.anaconda.com/products/distribution)  
First go to Anaconda's official website to select the Linux version to download the installation file. After downloading, you will get a .sh file.   
![.sh file](https://github.com/nick8592/Ubuntu-20.04-CUDA-cuDNN-PyTorch/blob/main/images/anaconda_sh_file.png)   

Open the terminal and type in
```
sudo bash {version_name}.sh
#e.g. sudo bash Anaconda3–2022.05-Linux-x86_64.sh
```
Press enter and yes all the way to complete the installation.   


### 5. PyTorch installation
(https://pytorch.org/get-started/previous-versions/)    
The PyTorch version cannot be too new, click "install previous versions of PyTorch".   
![PyTorch install link](https://github.com/nick8592/Ubuntu-20.04-CUDA-cuDNN-PyTorch/blob/main/images/pytorch_link.png)   

Corresponding to the CUDA 10.1 version, this time I chose to install v1.4.0. You can copy the instructions under CUDA 10.1 first, we will use it later.   
```
conda install pytorch==1.4.0 torchvision==0.5.0 cudatoolkit=10.1 -c pytorch
```
![pytorch install code](https://github.com/nick8592/Ubuntu-20.04-CUDA-cuDNN-PyTorch/blob/main/images/pytorch_version.png)   

PyTorch 1.4 version requires that the python version should not be too new. If it is too new, an error will occur and PyTorch cannot be installed as shown below.  
![Error Message](https://github.com/nick8592/Ubuntu-20.04-CUDA-cuDNN-PyTorch/blob/main/images/pytorch_install_1.png)   

Create a new environment with conda on the terminal, set the python version to 3.7, and "test" can be changed to any word.   
Then enter "y" to start the installation.   
```
conda create -n {environment_name} python=3.7
#e.g. conda create -n test python=3.7
```
![create emviroment](https://github.com/nick8592/Ubuntu-20.04-CUDA-cuDNN-PyTorch/blob/main/images/conda_env.png)   

After the environment is set up, you will be instructed to enter the activate command to start the environment.   
```
conda activate {environment_name}
#e.g conda activate test
```
![activate environment](https://github.com/nick8592/Ubuntu-20.04-CUDA-cuDNN-PyTorch/blob/main/images/conda_activate.png)   


After entering the environment name, the current environment name will be displayed at the front.   
You can enter the command to check the currently installed CUDA version (V10.1).   
 ```
 nvcc -V
```
![cuda version](https://github.com/nick8592/Ubuntu-20.04-CUDA-cuDNN-PyTorch/blob/main/images/nvcc.png)   


Paste the previous instructions for copying and installing PyTorch, enter "y" to start the installation.   
```
conda install pytorch==1.4.0 torchvision==0.5.0 cudatoolkit=10.1 -c pytorch
```
![pytorch install](https://github.com/nick8592/Ubuntu-20.04-CUDA-cuDNN-PyTorch/blob/main/images/pytorch_install_1.png)  
![pytorch install](https://github.com/nick8592/Ubuntu-20.04-CUDA-cuDNN-PyTorch/blob/main/images/pytorch_install_2.png)   

Installation complete screen.   
![pytorch install complete](https://github.com/nick8592/Ubuntu-20.04-CUDA-cuDNN-PyTorch/blob/main/images/pytotrch_install_complete.png)   

Type in "python" to enter the python compilation environment, and enter the following commands in sequence.   
```
python
improt torch
torch.cuda.is_available()
```

If it's True, the installation is successful.   
![pytorch install success](https://github.com/nick8592/Ubuntu-20.04-CUDA-cuDNN-PyTorch/blob/main/images/cuda_true.png)   

Press ctrl+D or exit() to exit python.  
Then enter "conda deactivate" to exit the virtual environment.  
```
exit()
```
```
conda deactivate
```
![deactivate](https://github.com/nick8592/Ubuntu-20.04-CUDA-cuDNN-PyTorch/blob/main/images/exit.png)  
