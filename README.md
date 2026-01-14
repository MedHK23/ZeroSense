# ZeroSense

## News
We now provide a pretrained  ZeroSense on Jan 9, 2026! 

## Online Demo
Click the image to have a try with ZeroSense 

<!-- Insert a pipeline of your algorithm here if got one -->
<div align="center">
    <a href="https://479d81e5a2e14b9538.gradio.live"><img width="600px" height="auto" src="https://github.com/MedHK23/ZeroSense/blob/main/Fig%201.png"></a>
</div>


## Key Features

We introduce the ZeroSense perspective to systematically remove semantic redundancy from inputs. Under low- or zero-semantic conditions, reconstruction accuracy collapses, revealing that visual tokens alone fail to carry sufficient information. In contrast, high performance on natural text mainly stems from the LLM’s ability to hallucinate plausible sequences from weak visual cues.

## Links

- [Paper](https://arxiv.org/abs/2311.01092)
- [Model](https://huggingface.co/MedHK23/ZeroSense)
- [Dataset](https://huggingface.co/datasets/MedHK23/ZeroSense)


## Dataset Links

We utilize 10 public and 6 private datasets for pre-training and provide the download via the following links:

Public dataset: 

- [MIMIC-CXR](https://physionet.org/content/mimic-cxr/2.0.0/)


## Get Started

**Main Requirements**  

- python 3.7.4
- pytorch 1.8.1
- torchvision 0.9.1
- gradio 3.34.0


**Installation**
```bash
git clone https://github.com/MedHK23/ZeroSense.git
pip install -r requirements.txt
```


**Training**
```bash
### before training, please download the pretrained models and datasets and place them in their respective folders.
bash ./run_scripts/multi_tasks/train.sh
```


**Testing**
```bash
from demo_base import init_task, ask_answer
from PIL import Image

print('Initializing Chat')
init_task()
print('Initialization Finished')

instruction = 'describe this image'
image = Image.open('test.png').convert('RGB')
report = ask_answer(image, instruction)
```


## 🛡️ License

This project is under the Apache License. See [LICENSE](LICENSE.txt) for details.

## 🙏 Acknowledgement

A lot of code is modified from [OFA](https://github.com/OFA-Sys/OFA).

## 📝 Citation

If you find this repository useful, please consider citing this paper:
```
@misc{2026,
      title={ZeroSense:How Vision matters in Long Context Compression}, 
      author={Yonghan, Zehong Chen, Jingzhi Chen,Lijian Xu,Xingyu Zeng},
      year={2026},
      eprint={2311.01092},
      archivePrefix={arXiv},
      primaryClass={cs.CV}
}
```

