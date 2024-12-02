[![Zero-Shot Image Editing](https://img.shields.io/badge/zero%20shot-image%20editing-Green)]([https://github.com/topics/video-editing](https://github.com/topics/text-guided-image-editing))
[![Python](https://img.shields.io/badge/python-3.8+-blue?python-3670A0?style=for-the-badge&logo=python&logoColor=ffdd54)](https://www.python.org/downloads/release/python-38/)
![PyTorch](https://img.shields.io/badge/torch-2.0.0-red?PyTorch-%23EE4C2C.svg?style=for-the-badge&logo=PyTorch&logoColor=white)

# FlowEdit

[Project](https://matankleiner.github.io/flowedit/) | [Arxiv](https://arxiv.org/abs/) 

### Official Pytorch implementation of the paper: "FlowEdit: Inversion-Free Text-Based Editing Using Pre-Trained Flow Models"

![](imgs/teaser.png)

## Installation
1. Clone the repository

2. Install the required dependencies using `pip install torch diffusers transformers accelerate sentencepiece protobuf` <br>
	* Tested with CUDA version 12.4 and diffusers 0.31.0

## Running examples
Run editing with Stable Diffusion 3: `python run_script.py --exp_yaml SD3_exp.yaml`

Run editing with Flux: `python run_script.py --exp_yaml FLUX_exp.yaml`

## Usage - your own examples

* Upload images to `example_images` folder. 

* Create an edits file that specifies: (a) a path to the input image, (b) a source prompt, (c) target prompts, and (d) target codes. The target codes summarize the changes between the source and target prompts and will appear in the output filename. <br>
See `edits.yaml` for example.

* Create an experiment file containing the hyperparamaters needed for running FlowEdit, such as `n_max`, `n_min`. This file also includes the path to the `edits.yaml` file<br>
See `FLUX_exp.yaml` for FLUX usage example and `SD3_exp.yaml` for Stable Diffusion 3 usage example. <br>
For a detailed discussion on the impact of different hyperparameters and the values we used, please refer to our paper.

Run `python run_script.py --exp_yaml <path to your experiment yaml>`


## License
This project is licensed under the [MIT License](LICENSE).


### Citation
If you use this code for your research, please cite our paper:

```
```
