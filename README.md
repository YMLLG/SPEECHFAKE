# **SpeechFake**: A Large-Scale Multilingual Speech Deepfake Dataset Incorporating Cutting-Edge Generation Methods

<p align="center">  
    <a href="https://arxiv.org/abs/">Paper</a>, 
    <a href="https://www.modelscope.cn/datasets/inclusionAI/SPEECHFAKE">Dataset</a>
</p>
<p align="center">  
    <i>ACL 2025</i>
</p>

## Introduction

**SpeechFake** is a large-scale multilingual dataset for speech deepfake detection, featuring over 3 million fake samples across 46 languages. Generated using 30 diverse open-source models spanning text-to-speech (TTS), voice conversion or clone (VC), and neural vocoder (NV) methods, it offers rich metadata and strong coverage of modern generation techniques, enabling robust and generalizable detection research.

![dataset](./figs/dataset.png)

## Dataset Download

You can download the dataset in the following ways. For details, see Download [Instructions](https://www.modelscope.cn/docs/Download%20Dataset).

Before downloading, install ModelScope first by using the following command

```bash
pip install modelscope
```

### Command Line Download

Download the full dataset repo

```bash
modelscope download --dataset inclusionAI/SPEECHFAKE
```

Download a single file to a specified local folder (using the example of downloading README.md to the "dir" directory in the current path)

```bash
modelscope download --dataset inclusionAI/SPEECHFAKE README.md --local_dir ./dir
```

For more extensive command line download options, please refer to [the specific documentation](https://www.modelscope.cn/docs/datasets/download#3-使用命令行工具下载数据集文件)

### SDK Download

```python
# Dataset Download
from modelscope.msdatasets import MsDataset
ds =  MsDataset.load('inclusionAI/SPEECHFAKE')
# You can configure subset_name and split as needed, refer to the "Quick Use" sample code
```

### Git Download

Please ensure that LFS has been installed correctly.

```bash
git lfs install
git clone https://www.modelscope.cn/datasets/inclusionAI/SPEECHFAKE.git
```

## Acknowledgement

**SpeechFake** is constructed using a combination of publicly available speech datasets and open-source speech generation methods.

### **Real Speech Datasets**

| **Dataset** | **Language(s)** | **Source**                                        |
| ----------- | --------------- | ------------------------------------------------- |
| VCTK        | English         | https://datashare.ed.ac.uk/handle/10283/3443      |
| LibriTTS    | English         | https://research.google/tools/datasets/libri-tts/ |
| AISHELL-1   | Chinese         | https://openslr.org/33                            |
| AISHELL-3   | Chinese         | https://openslr.org/93                            |
| CommonVoice | 46 Languages    | https://commonvoice.mozilla.org/en/datasets       |

### **Speech Generation Methods**

| No.  | Method           | Type   | Link                                            |
| ---- | ---------------- | ------ | ----------------------------------------------- |
| 1    | MelGAN           | NV     | https://github.com/kan-bayashi/ParallelWaveGAN  |
| 2    | WaveGlow         | NV     | https://github.com/NVIDIA/waveglow              |
| 3    | Parallel WaveGAN | NV     | https://github.com/kan-bayashi/ParallelWaveGAN  |
| 4    | HiFi-GAN         | NV     | https://github.com/kan-bayashi/ParallelWaveGAN  |
| 5    | Fullband-MelGAN  | NV     | https://github.com/kan-bayashi/ParallelWaveGAN  |
| 6    | StyleMelGAN      | NV     | https://github.com/kan-bayashi/ParallelWaveGAN  |
| 7    | FastDiff         | NV     | https://github.com/Rongjiehuang/FastDiff        |
| 8    | BigVGAN          | NV     | https://github.com/NVIDIA/BigVGAN               |
| 9    | WaveNet          | TTS    | https://github.com/r9y9/wavenet_vocoder         |
| 10   | Tactotron2       | TTS    | https://github.com/NVIDIA/tacotron2             |
| 11   | Glow-TTS         | TTS    | https://github.com/jaywalnut310/glow-tts        |
| 12   | Grad-TTS         | TTS    | https://github.com/huawei-noah/Speech-Backbones |
| 13   | FastSpeech2      | TTS    | https://github.com/ming024/FastSpeech2          |
| 14   | PortaSpeech      | TTS    | https://github.com/keonlee9420/PortaSpeech      |
| 15   | VITS             | TTS    | https://github.com/jaywalnut310/vits/tree/main  |
| 16   | StarGAN-VC       | VC     | https://github.com/yl4579/StarGANv2-VC          |
| 17   | DiffGAN-TTS      | TTS    | https://github.com/keonlee9420/DiffGAN-TTS      |
| 18   | ProDiff-TTS      | TTS    | https://github.com/Rongjiehuang/ProDiff         |
| 19   | EdgeTTS          | TTS    | https://github.com/rany2/edge-tts.git           |
| 20   | TorToiSe         | TTS    | https://github.com/neonbjb/tortoise-tts         |
| 21   | StyleTTS2        | TTS    | https://github.com/yl4579/StyleTTS2             |
| 22   | OpenVoice        | VC     | https://github.com/myshell-ai/OpenVoice         |
| 23   | GPTSoVITS        | VC     | https://github.com/RVC-Boss/GPT-SoVITS          |
| 24   | Fish Speech      | TTS/VC | https://github.com/fishaudio/fish-speech        |
| 25   | MeloTTS          | TTS    | https://github.com/myshell-ai/MeloTTS           |
| 26   | ChatTTS          | TTS    | https://github.com/2noise/ChatTTS               |
| 27   | CosyVoice        | TTS/VC | https://github.com/FunAudioLLM/CosyVoice        |
| 28   | Parler-TTS       | TTS    | https://github.com/huggingface/parler-tts       |
| 29   | FireRedTTS       | TTS    | https://github.com/FireRedTeam/FireRedTTS       |
| 30   | Seed-VC          | VC     | https://github.com/Plachtaa/seed-vc             |


## Citation

If you use this dataset in your work, please cite the following paper:

```
@inproceedings{huang2025speechfake,
title     = {SpeechFake: A Large-Scale Multilingual Speech Deepfake Dataset Incorporating Cutting-Edge Generation Methods},
author    = {Huang, Wen and Gu, Yanmei and Wang, Zhiming and Zhu, Huijia and Qian, Yanmin},
booktitle = {Proceedings of the 63rd Annual Meeting of the Association for Computational Linguistics (Volume 1: Long Papers)},
year      = {2025},
pages     = {(to appear)}
}
```



