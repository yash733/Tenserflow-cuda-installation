## Installation of CUDA on TensorFlow

1. Update your GeForce Experience to the latest version available.</br>
2. Install Visual Studio from [here](https://visualstudio.microsoft.com/) (not VS Code).</br>
3. To check which CUDA version is compatible with your GPU, visit [CUDA GPUs](https://developer.nvidia.com/cuda-gpus) </br>  
   ![image](https://github.com/yash733/Tenserflow-cuda-installation/assets/100533686/c4f30190-9df8-4450-b830-df58968767cb)</br>

4. Download CUDA 11 exe (local) or exe (network) and install it from [here](https://developer.nvidia.com/cuda-downloads?target_os=Windows&target_arch=x86_64&target_version=11)</br>  
   ![image](https://github.com/yash733/Tenserflow-cuda-installation/assets/100533686/1dbd1855-5aae-44c3-807d-93812cd3feee)</br>

5. Download the cuDNN version compatible with your CUDA 11 from [here](https://developer.nvidia.com/rdp/cudnn-archive) (I installed version 8.1.1 as reference).</br>  
   ![image](https://github.com/yash733/Tenserflow-cuda-installation/assets/100533686/47a567a7-9b00-4e4e-955f-22824bee07f0)</br>

6. Create a new folder in your C:/ drive (example: C:/cudnn) and extract the data into that folder.</br>
7. Set up your environment variables as follows:</br>  
   ![image](https://github.com/yash733/Tenserflow-cuda-installation/assets/100533686/e6585cd3-9c34-4269-9916-787f9246567d)</br>
   
8. Things to add: follow the paths provided below:</br>  
   9.1. `C:\Program Files\NVIDIA GPU Computing Toolkit\CUDA\"VERSION"\bin` </br>  
   9.2. `C:\Program Files\NVIDIA GPU Computing Toolkit\CUDA\"VERSION"\libnvvp` </br>  
   9.3. `C:\Program Files\NVIDIA GPU Computing Toolkit\CUDA\"VERSION"\extras\CUPTI\lib64` </br>  
   9.4. `C:\Program Files\NVIDIA GPU Computing Toolkit\CUDA\"VERSION"\extras\CUPTI\include` </br>  
   9.5. `C:\Program Files\NVIDIA GPU Computing Toolkit\CUDA\"VERSION"\include` </br>  
   9.6. `C:\"file_name where you have extracted the cudnn"\include` </br>  
   9.7. `C:\cudnn\bin` </br>  
   
   ![image](https://github.com/yash733/Tenserflow-cuda-installation/assets/100533686/fb2f0423-f695-415e-b55b-118da0125b9b)</br>  
   ![image](https://github.com/yash733/Tenserflow-cuda-installation/assets/100533686/facd0699-3c59-4191-97d7-44ef3c1f6ca9)</br>

10. Now, install TensorFlow GPU by running `pip install tensorflow-gpu==2.10.0` in your IDE (e.g., PyCharm). If it crashes in the middle, rerun the command.</br>
11. To test if everything is working:</br>  
   ```python  
   import tensorflow as tf  
   print("Num GPUs Available: ", len(tf.config.list_physical_devices('GPU')))
