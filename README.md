## Installation of CUDA on TensorFlow

1. Update your GeForce Experience to the latest version available.</br>
2. Install Visual Studio from [here](https://visualstudio.microsoft.com/) (not VS Code).</br>
3. To check which CUDA version is compatible with your GPU, visit [CUDA GPUs](https://developer.nvidia.com/cuda-gpus) </br>  
   ![image](https://github.com/yash733/Tenserflow-cuda-installation/assets/100533686/c4f30190-9df8-4450-b830-df58968767cb)</br>

4. Download CUDA - 11{means windows version} exe (local) or exe (network) and install it from [here](https://developer.nvidia.com/cuda-downloads?target_os=Windows&target_arch=x86_64&target_version=11)</br>  
   ![image](https://github.com/yash733/Tenserflow-cuda-installation/assets/100533686/1dbd1855-5aae-44c3-807d-93812cd3feee)</br>

5. Download the cuDNN version compatible with your CUDA 12.4 from [here](https://developer.nvidia.com/rdp/cudnn-archive) (I installed version 8.9.7 for reference).</br>  
   ![image](https://github.com/yash733/Tenserflow-cuda-installation/assets/100533686/47a567a7-9b00-4e4e-955f-22824bee07f0)</br>

6. Install CUDA 12.4 package</br>
---
7. Set up your environment variables Should Look Like this: </br>
   ![image](https://github.com/user-attachments/assets/385f0dd9-a522-4581-a8ff-f1394ac62c55)

### If not then try reinstalling the package
---
8. Extract CUDnn file downloaded</br>
9. copy file data in Cudnn bin, lib\x64 and include to Nvidia GPU toolkit bin, lib\x64 and include respectively</br>

   ![image](https://github.com/user-attachments/assets/7fdc9536-7641-410f-add9-e7944e6f1869)
### --- Similarly for other 2 files also

10. Now, install TensorFlow Version, which is comaptible with CUDA for referance `pip install tensorflow==2.16.0` in your IDE (e.g., PyCharm). If it crashes in the middle, re'run the command.</br>
11. To test if everything is working:</br>  
   ```python  
   import tensorflow as tf  
   print("Num GPUs Available: ", len(tf.config.list_physical_devices('GPU')))
```
![image](https://github.com/user-attachments/assets/30fdc341-3d46-4bed-b34f-b63738a85d4c)

