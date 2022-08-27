# Ubuntu-20.04-DeepLearning-Environments-Setting
中文版本(https://traveling-process-89d.notion.site/Ubuntu-20-04-DeepLearning-655e63dc86aa4edea87600decccb3237)

## Results
| Name | Version |
|---|---|
| Ubuntu | 20.04 |
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
![Software & Updates app](https://s3.us-west-2.amazonaws.com/secure.notion-static.com/abc13826-15c9-42a2-b0e0-409e4bb9d595/Untitled.png?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Content-Sha256=UNSIGNED-PAYLOAD&X-Amz-Credential=AKIAT73L2G45EIPT3X45%2F20220827%2Fus-west-2%2Fs3%2Faws4_request&X-Amz-Date=20220827T153401Z&X-Amz-Expires=86400&X-Amz-Signature=9d555d81011329dfa274d29379490af2aad1566cfcf23886093672ce6001730f&X-Amz-SignedHeaders=host&response-content-disposition=filename%20%3D%22Untitled.png%22&x-id=GetObject)  

Select the Additional Drivers field, and then select the version you want (except -server). After selecting, press Apply Changes, and the new Driver will be installed.  
![NVIDIA Driver Select](https://s3.us-west-2.amazonaws.com/secure.notion-static.com/e782704f-cd4f-474d-9d8d-a67c526105d1/Untitled.png?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Content-Sha256=UNSIGNED-PAYLOAD&X-Amz-Credential=AKIAT73L2G45EIPT3X45%2F20220827%2Fus-west-2%2Fs3%2Faws4_request&X-Amz-Date=20220827T153231Z&X-Amz-Expires=86400&X-Amz-Signature=b91afa0a2a155b89c82913921ed82a9d3f0925597e20658f055c581870c261c0&X-Amz-SignedHeaders=host&response-content-disposition=filename%20%3D%22Untitled.png%22&x-id=GetObject)  

After installation, you will be asked to restart, open terminal and type in  
```
sudo reboot
```

After restarting, open the terminal and enter the following commands to check if the Driver Version is correct. The CUDA version in the upper right corner can be ignored because we haven't installed it yet.  
```
nvidia-smi
```
![nvidia-smi](https://s3.us-west-2.amazonaws.com/secure.notion-static.com/1b45c64d-a0ae-4a24-bd72-2b89eb85842f/Untitled.png?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Content-Sha256=UNSIGNED-PAYLOAD&X-Amz-Credential=AKIAT73L2G45EIPT3X45%2F20220827%2Fus-west-2%2Fs3%2Faws4_request&X-Amz-Date=20220827T155040Z&X-Amz-Expires=86400&X-Amz-Signature=2ef94e39a9467342b524461f2d127f6929b1ec4838488ef9656fa5e95d67110d&X-Amz-SignedHeaders=host&response-content-disposition=filename%20%3D%22Untitled.png%22&x-id=GetObject)

### 2. CUDA installation 
(https://mikethreeacer.medium.com/ubuntu-18-04-安裝-cuda-cudnn-anaconda-pytorch-1f170b3326a4#1b0a)  
You can follow the above URL "2. Install CUDA 11.2.2" section to install.   

### 3. cuDNN installatioin 
(https://mikethreeacer.medium.com/ubuntu-18-04-安裝-cuda-cudnn-anaconda-pytorch-1f170b3326a4#1b0a)  
You can follow the above URL "2. Install cuDNN" section to install.   


### 4. Anaconda3 installation 
(https://www.anaconda.com/products/distribution)  
First go to Anaconda's official website to select the Linux version to download the installation file. After downloading, you will get a .sh file.   
![.sh file](https://s3.us-west-2.amazonaws.com/secure.notion-static.com/17ae7e22-268d-4044-be14-900f7d1a3337/Untitled.png?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Content-Sha256=UNSIGNED-PAYLOAD&X-Amz-Credential=AKIAT73L2G45EIPT3X45%2F20220827%2Fus-west-2%2Fs3%2Faws4_request&X-Amz-Date=20220827T160339Z&X-Amz-Expires=86400&X-Amz-Signature=1ad2533f6da8ea849da85561f136e0097e9961d22d5b1a9c1e2bfd6bc85bf932&X-Amz-SignedHeaders=host&response-content-disposition=filename%20%3D%22Untitled.png%22&x-id=GetObject)   

Open the terminal and type in
```
sudo bash {version_name}.sh
#e.g. sudo bash Anaconda3–2022.05-Linux-x86_64.sh
```
Press enter and yes all the way to complete the installation.   


### 5. PyTorch installation
(https://pytorch.org/get-started/previous-versions/)    
The PyTorch version cannot be too new, click "install previous versions of PyTorch".   
![PyTorch install link](https://s3.us-west-2.amazonaws.com/secure.notion-static.com/8d402422-199c-409f-92c8-acf50d3d134e/Untitled.png?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Content-Sha256=UNSIGNED-PAYLOAD&X-Amz-Credential=AKIAT73L2G45EIPT3X45%2F20220827%2Fus-west-2%2Fs3%2Faws4_request&X-Amz-Date=20220827T161601Z&X-Amz-Expires=86400&X-Amz-Signature=f58dbc24dcf41919a3e56ba630e77601e8471f83d2192c5afd5bb05ffb15d640&X-Amz-SignedHeaders=host&response-content-disposition=filename%20%3D%22Untitled.png%22&x-id=GetObject)   

Corresponding to the CUDA 10.1 version, this time I chose to install v1.4.0. You can copy the instructions under CUDA 10.1 first, we will use it later.   
```
conda install pytorch==1.4.0 torchvision==0.5.0 cudatoolkit=10.1 -c pytorch
```
![pytorch install code](https://s3.us-west-2.amazonaws.com/secure.notion-static.com/975790e3-9f64-47f2-9c38-f5dbc114c613/Untitled.png?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Content-Sha256=UNSIGNED-PAYLOAD&X-Amz-Credential=AKIAT73L2G45EIPT3X45%2F20220827%2Fus-west-2%2Fs3%2Faws4_request&X-Amz-Date=20220827T161803Z&X-Amz-Expires=86400&X-Amz-Signature=1cd98bad97b00a229fd400d3be142a1d0831f0ad9a84eaa10f23d76853f06e17&X-Amz-SignedHeaders=host&response-content-disposition=filename%20%3D%22Untitled.png%22&x-id=GetObject)   


PyTorch 1.4 version requires that the python version should not be too new. If it is too new, an error will occur and PyTorch cannot be installed as shown below.  
![Error Message](https://s3.us-west-2.amazonaws.com/secure.notion-static.com/7d589ec1-4ab9-4e37-81f2-247058668c40/Untitled.png?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Content-Sha256=UNSIGNED-PAYLOAD&X-Amz-Credential=AKIAT73L2G45EIPT3X45%2F20220827%2Fus-west-2%2Fs3%2Faws4_request&X-Amz-Date=20220827T161952Z&X-Amz-Expires=86400&X-Amz-Signature=a6b7417139c55843b21edd791ebb3f0026c8d3bdd08605f98050859dbf9d8cda&X-Amz-SignedHeaders=host&response-content-disposition=filename%20%3D%22Untitled.png%22&x-id=GetObject)   

Create a new environment with conda on the terminal, set the python version to 3.7, and "test" can be changed to any word.   
Then enter "y" to start the installation.   
```
conda create -n {environment_name} python=3.7
#e.g. conda create -n test python=3.7
```
![create emviroment](https://s3.us-west-2.amazonaws.com/secure.notion-static.com/088a3725-9e3c-4330-8d30-c04ee16b8296/Untitled.png?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Content-Sha256=UNSIGNED-PAYLOAD&X-Amz-Credential=AKIAT73L2G45EIPT3X45%2F20220827%2Fus-west-2%2Fs3%2Faws4_request&X-Amz-Date=20220827T162316Z&X-Amz-Expires=86400&X-Amz-Signature=4b6c933b1f9c5ab867ea67d753a3e03e6aea3213932ebdbc6a7b840037ec960b&X-Amz-SignedHeaders=host&response-content-disposition=filename%20%3D%22Untitled.png%22&x-id=GetObject)   

After the environment is set up, you will be instructed to enter the activate command to start the environment.   
```
conda activate {environment_name}
#e.g conda activate test
```
![activate environment](https://s3.us-west-2.amazonaws.com/secure.notion-static.com/ff891a85-fb5a-4a7f-807f-c32d8baaf7e9/Untitled.png?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Content-Sha256=UNSIGNED-PAYLOAD&X-Amz-Credential=AKIAT73L2G45EIPT3X45%2F20220827%2Fus-west-2%2Fs3%2Faws4_request&X-Amz-Date=20220827T162706Z&X-Amz-Expires=86400&X-Amz-Signature=974cfba13200e6b5b7945f84dd0d025c24179f2be3db9d07a9f3571fe6bb5c0a&X-Amz-SignedHeaders=host&response-content-disposition=filename%20%3D%22Untitled.png%22&x-id=GetObject)   


After entering the environment name, the current environment name will be displayed at the front.   
You can enter the command to check the currently installed CUDA version (V10.1).   
 ```
 nvcc -V
```
![cuda version](https://s3.us-west-2.amazonaws.com/secure.notion-static.com/6ad659e0-3a5b-40cb-be26-f2c198285eda/Untitled.png?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Content-Sha256=UNSIGNED-PAYLOAD&X-Amz-Credential=AKIAT73L2G45EIPT3X45%2F20220827%2Fus-west-2%2Fs3%2Faws4_request&X-Amz-Date=20220827T162929Z&X-Amz-Expires=86400&X-Amz-Signature=12df68edc92f973fc9ee4949d5ed2ab381deea08ce0758ed7e7b86082f839282&X-Amz-SignedHeaders=host&response-content-disposition=filename%20%3D%22Untitled.png%22&x-id=GetObject)   


Paste the previous instructions for copying and installing PyTorch, enter "y" to start the installation.   
```
conda install pytorch==1.4.0 torchvision==0.5.0 cudatoolkit=10.1 -c pytorch
```
![pytorch install](https://s3.us-west-2.amazonaws.com/secure.notion-static.com/b93af7eb-5df5-4f81-8410-9db484d9395b/Untitled.png?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Content-Sha256=UNSIGNED-PAYLOAD&X-Amz-Credential=AKIAT73L2G45EIPT3X45%2F20220827%2Fus-west-2%2Fs3%2Faws4_request&X-Amz-Date=20220827T163122Z&X-Amz-Expires=86400&X-Amz-Signature=a4ba1568026df4224b9181acc67d4d67816dcbad2a8239abfb38e1ffa0785052&X-Amz-SignedHeaders=host&response-content-disposition=filename%20%3D%22Untitled.png%22&x-id=GetObject)  
![pytorch install](https://s3.us-west-2.amazonaws.com/secure.notion-static.com/4f284149-194b-453d-8234-fc8c1333fb6f/Untitled.png?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Content-Sha256=UNSIGNED-PAYLOAD&X-Amz-Credential=AKIAT73L2G45EIPT3X45%2F20220827%2Fus-west-2%2Fs3%2Faws4_request&X-Amz-Date=20220827T163206Z&X-Amz-Expires=86400&X-Amz-Signature=3eaa7de6496949f3973b8f2bfa16cd76c72d5c92c411a46f31c903612364be52&X-Amz-SignedHeaders=host&response-content-disposition=filename%20%3D%22Untitled.png%22&x-id=GetObject)   

Installation complete screen.   
![pytorch install complete](https://s3.us-west-2.amazonaws.com/secure.notion-static.com/1f184d0c-1917-40a7-9bcb-179ea7b343a2/Untitled.png?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Content-Sha256=UNSIGNED-PAYLOAD&X-Amz-Credential=AKIAT73L2G45EIPT3X45%2F20220827%2Fus-west-2%2Fs3%2Faws4_request&X-Amz-Date=20220827T163258Z&X-Amz-Expires=86400&X-Amz-Signature=e1798c9c2394b4469ffd47c8580b261e08dcc1c2c1451d5f172471e0199d4132&X-Amz-SignedHeaders=host&response-content-disposition=filename%20%3D%22Untitled.png%22&x-id=GetObject)   

Type in "python" to enter the python compilation environment, and enter the following commands in sequence.   
```
python
improt torch
torch.cuda.is_available()
```

If it's True, the installation is successful.   
![pytorch install success](https://s3.us-west-2.amazonaws.com/secure.notion-static.com/55d240d0-9577-4787-8ffd-24006bfe6105/Untitled.png?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Content-Sha256=UNSIGNED-PAYLOAD&X-Amz-Credential=AKIAT73L2G45EIPT3X45%2F20220827%2Fus-west-2%2Fs3%2Faws4_request&X-Amz-Date=20220827T163534Z&X-Amz-Expires=86400&X-Amz-Signature=493facaba89f413f5c6b3d7ca9a6e6222fabe8faea224b0f3327c0c86b75aa92&X-Amz-SignedHeaders=host&response-content-disposition=filename%20%3D%22Untitled.png%22&x-id=GetObject)   

Press ctrl+D or exit() to exit python.  
Then enter "conda deactivate" to exit the virtual environment.  
```
exit()
```
```
conda deactivate
```
![deactivate](https://s3.us-west-2.amazonaws.com/secure.notion-static.com/c59d486a-ee11-4914-88c1-f8cc1f845ddd/Untitled.png?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Content-Sha256=UNSIGNED-PAYLOAD&X-Amz-Credential=AKIAT73L2G45EIPT3X45%2F20220827%2Fus-west-2%2Fs3%2Faws4_request&X-Amz-Date=20220827T163729Z&X-Amz-Expires=86400&X-Amz-Signature=4f879e29fb8532a4d193f91b53f45ec25792e037194944b9355a024fcbc97e88&X-Amz-SignedHeaders=host&response-content-disposition=filename%20%3D%22Untitled.png%22&x-id=GetObject)  
