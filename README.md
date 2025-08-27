<div align="center">
  <h3 align="center">Bridging Brain Signals and Language: ProphetNet Model for EEG-to-Text Decoding</h3>

  <p align="center">
    <b>Mostafa El Gedawy</b>, <b>Omnia Nabil</b>, <b>Omar Mamdouh</b>, <b>Mahmoud Nady</b>, <b>Nour Alhuda Adel</b>, <b>Ahmed Fares</b>
    <br />
  </p>
</div>

<div align="center">    

[![Paper](https://img.shields.io/badge/arXiv-2502.17465-B31B1B.svg)](https://arxiv.org/abs/2502.17465)  
[![DOI](https://img.shields.io/badge/DOI-10.48550/arXiv.2502.17465-blue.svg)](https://doi.org/10.48550/arXiv.2502.17465)

</div>


---

## Overview
This repository contains the **ProphetNet-based implementation** from our paper  
**[Bridging Brain Signals and Language: A Deep Learning Approach to EEG-to-Text Decoding](https://arxiv.org/abs/2502.17465)**.  

Our framework integrates **subject-specific representation learning** with **language models** to decode EEG into open-vocabulary text.  
This repo focuses **only on the ProphetNet model**, one of the proposed decoding architectures.

---

## Setup
### 1. Install dependencies
```bash
pip install -r requirements.txt
````

### 2. Download ZuCo datasets
* [ZuCo v1.0](https://osf.io/q3zws/files/) → place `.mat` files under
  `/dataset/ZuCo/task*/Matlab_files`
* [ZuCo v2.0](https://osf.io/2urht/files/) → place under
  `/dataset/ZuCo/task2-NR-2.0/Matlab_files`

### 3. Preprocess data
```bash
bash ./scripts/prepare_dataset_raw.sh
```

### 4. Train & Evaluate
```bash
bash ./scripts/train_decoding_raw.sh
bash ./scripts/eval_decoding_raw.sh
```

---

## Acknowledgments
This work builds on [EEG-to-Text](https://github.com/MikeWangWZHL/EEG-To-Text).
