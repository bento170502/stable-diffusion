Environment Setup
Create and activate the ldm environment:
```
conda env create -f environment.yaml
conda activate ldm
```

For updating an existing environment:
```
conda install pytorch torchvision -c pytorch
pip install transformers==4.19.2 diffusers invisible-watermark
pip install -e .
```

Model Weights
Download the Stable Diffusion v1 weights from the CompVis organization on Hugging Face : https://huggingface.co/CompVis/stable-diffusion-v-1-1-original

Link the weights in the specified directory:
```
mkdir -p models/ldm/stable-diffusion-v1/
ln -s <path/to/model.ckpt> models/ldm/stable-diffusion-v1/model.ckpt
```

Generating Images
Use the reference script to generate images with a custom prompt:
```
python scripts/txt2img.py --prompts "a photograph of an astronaut riding a horse" --plms
```




