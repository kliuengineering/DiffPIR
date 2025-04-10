# Setup

1. Do this ```git clone https://github.com/yuanzhi-zhu/DiffPIR.git```
2. Do this ```cd DiffPIR```
3. Do this ```conda create -n diffusion python=3.9```
4. Go into the cloned directory, do this ```conda activate diffusion``` 
5. Do this ```pip install -r requirements.txt```
6. Inside ```~/DiffPIR/``` folder, do this ```git clone https://github.com/LeviBorodenko/motionblur.git```
7. Go here ```https://github.com/yuanzhi-zhu/DiffPIR/blob/main/model_zoo/README.md```
    - download both files
    - make a folder here (if not already existed)```~/DiffPIR/model_zoo/```
    - put both models into ```~/DiffPIR/model_zoo/```
8. Go to ```https://drive.google.com/drive/folders/1jElnRoFv7b31fG0v6pTSQkelbSX3xGZh?usp=drive_link```
    - download only the ```imagenet256.pt``` then put it into ```~/DiffPIR/model_zoo/```
9. Rename ```ffhq_10m.pt``` to ```diffusion_ffhq_10m.pt```
10. Try and go to this directory ```C:\Users\<username>\.cache\torch\hub\checkpoints\``` 
    - if not already existed, then make sure to create this exact path / directories
11. Download trained weights from ```https://download.pytorch.org/models/vgg16-397923af.pth```
    - put it into ```C:\Users\<username>\.cache\torch\hub\checkpoints\``` 


# Run Inference

*Note: There are 4 types of inference we can run* inside the directory ```~/DiffPIR/```

## Default Settings
1. ```python main_ddpir_deblur.py ```        -> deblur
2. ```python main_ddpir_sisr.py```           -> super-resolution
3. ```python main_ddpir_inpainting.py```     -> inpainting
4. ```python main_ddpir.py```                -> DDPIR pipeline

## YAML Settings

1. ```python main_ddpir.py --opt configs/sisr.yaml```       -> DDPIR pipeline
2. ```python main_ddpir.py --opt configs/deblur.yaml```     -> deblur
3. ```python main_ddpir.py --opt configs/inpaint.yaml```    -> inpainting


# Train Your Own Model
- To train a new diffusion model, please follow [OpenAI Guided Diffusion](https://github.com/openai/guided-diffusion)


# Reference to the Original Documentation
*Note: Start reading at [Brief Introduction](./[old]README.md) section regarding the theory portion of the original paper.*