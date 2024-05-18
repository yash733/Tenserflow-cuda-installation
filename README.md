## Inistruction for intallation of CUDA on Tenserflow -
1. Update your Gforce experiance to the latest version available
2. Install Visual studio https://visualstudio.microsoft.com/ (not the vs code)
3. To check which if cuda is compatible with your GPU check https://developer.nvidia.com/cuda-gpus
   ![image](https://github.com/yash733/Tenserflow-cuda-installation/assets/100533686/c4f30190-9df8-4450-b830-df58968767cb)

4. Now download CUDA 11 exe(local) or exe(network) and install it https://developer.nvidia.com/cuda-downloads?target_os=Windows&target_arch=x86_64&target_version=11
   ![image](https://github.com/yash733/Tenserflow-cuda-installation/assets/100533686/1dbd1855-5aae-44c3-807d-93812cd3feee)

5. Now download the cudnn version compatible with your cuda 11 from https://developer.nvidia.com/rdp/cudnn-archive (referance I installed 8.1.1)
   ![image](https://github.com/yash733/Tenserflow-cuda-installation/assets/100533686/47a567a7-9b00-4e4e-955f-22824bee07f0)
 
6. Create a new folder in your C:/ drive (example: C:/cudnn) and extract the data in the folder
7. Now set up our environment variables ->
   ![image](https://github.com/yash733/Tenserflow-cuda-installation/assets/100533686/e6585cd3-9c34-4269-9916-787f9246567d)
   things to add, follow the path provided -
   7.1. C:\Program Files\NVIDIA GPU Computing Toolkit\CUDA\"VERSION"\bin
   7.2. C:\Program Files\NVIDIA GPU Computing Toolkit\CUDA\"VERSION"\libnvvp
   7.3. C:\Program Files\NVIDIA GPU Computing Toolkit\CUDA\"VERSION"\extras\CUPTI\lib64
   7.4. C:\Program Files\NVIDIA GPU Computing Toolkit\CUDA\"VERSION"\extras\CUPTI\include
   7.5. C:\Program Files\NVIDIA GPU Computing Toolkit\CUDA\"VERSION"\include
   7.6. C:\"file_name where you have extracted the cudnn"\include
   7.7. C:\cudnn\bin
   ![image](https://github.com/yash733/Tenserflow-cuda-installation/assets/100533686/fb2f0423-f695-415e-b55b-118da0125b9b)
   ![image](https://github.com/yash733/Tenserflow-cuda-installation/assets/100533686/facd0699-3c59-4191-97d7-44ef3c1f6ca9)

8. Now pip install tensorflow-gpu==2.10.0 in your code ide (pycharm), if crashes in the middle rerun the code
9. To test - 
   import tensorflow as tf
   print("Num GPUs Available: ", len(tf.config.list_physical_devices('GPU')))
   
   ![image](https://github.com/yash733/Tenserflow-cuda-installation/assets/100533686/72a5fc9d-465b-402a-926d-09040311b4f1)

