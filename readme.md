# Sketch2Manga

[![arXiv](https://img.shields.io/badge/arXiv-2312.01943-<COLOR>)](http://arxiv.org/abs/2312.01943)

Apply screentone to line drawings or colored illustrations with diffusion models.

<p float="center">
  <img src="https://github.com/dmMaze/sketch2manga/assets/51270320/e235c6bc-b6ae-4d7f-9f73-a9aacb3a83fc" />
  <br>
    <em>Drag and drop into ComfyUI to load the workflow </em>
  <a href="https://twitter.com/ini_pmh/status/715578786830417921/photo/1">(Source @ini_pmh)</a>
</p>


## Usage

### Preperation
Install [ComfyUI](https://github.com/comfyanonymous/ComfyUI) or [stable-diffusion-webui](https://github.com/AUTOMATIC1111/stable-diffusion-webui), download a diffusion model for colorization (the demo used [meinapastel](https://civitai.com/models/11866/meinapastel) for ComfyUI, [anything-v4.5](https://huggingface.co/ckpt/anything-v4.5-vae-swapped/tree/main) for sd-webui) and [control_v11p_sd15_lineart](https://huggingface.co/lllyasviel/ControlNet-v1-1/blob/main/control_v11p_sd15_lineart.pth).
Download the finetuned [vae](https://huggingface.co/dreMaz/sketch2manga/blob/main/vae/mangatone_default.ckpt) and [diffusion model](https://huggingface.co/dreMaz/sketch2manga/blob/main/manga_34000.ckpt) for screening.

### ComfyUI
Clone this repo to the ComfyUI directory and install dependencies:
``` bash
git clone https://github.com/dmMaze/sketch2manga [ComfyUI Directory]/custom_nodes/sketch2manga
cd [ComfyUI Directory]/custom_nodes/sketch2manga 
pip install -r requirements.txt
```
Launch ComfyUI, drag and drop the figure above to load the workflow.

### Gradio Demo
Clone this repo and install dependencies, launch sd-webui with argument ```--api```, and run
```
python gradio_demo/launch.py
```

#### SD-WebUI API
There is an example ```webuiapi_demo.ipynb``` showcasing inference using SD-WebUI API, it is a bit outdated though, but the logic applied is the same.


## BibTeX