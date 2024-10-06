# Glow-TTS

## 1. Environments we use

* Loading ..

For Mixed-precision training, we use [apex](https://github.com/NVIDIA/apex); commit: 37cdaf4


## 2. Pre-requisites

a) Download and extract the [LJ Speech dataset](https://keithito.com/LJ-Speech-Dataset/), then rename or create a link to the dataset folder: `ln -s /path/to/LJSpeech-1.1/wavs DUMMY`


b) Initialize WaveGlow submodule: `git submodule init; git submodule update`

Don't forget to download pretrained WaveGlow model and place it into the waveglow folder.

c) Build Monotonic Alignment Search Code (Cython): `cd monotonic_align; python setup.py build_ext --inplace`


## 3. Training Example


```sh
sh train_ddi.sh configs/base.json base
```

## 4. Inference Example

See [inference.ipynb](./inference.ipynb)

