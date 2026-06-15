# UH-GS

Official implementation of **UH-GS: Uncertainty-guided Hierarchical Gaussian Splatting for Robust Outdoor Scene Reconstruction**.

## Overview

UH-GS is a robust Gaussian Splatting framework designed for unconstrained outdoor scenes. By leveraging uncertainty estimation and hierarchical optimization, UH-GS effectively suppresses dynamic distractors and improves reconstruction quality under sparse-view and challenging real-world conditions.

<p align="center">
  <img src="assets/teaser.png" width="100%">
</p>

---

## Qualitative Results

### Dynamic Object Removal and Novel View Synthesis

<table>
<tr>
<td align="center">
<img src="assets/gifs/brandenburg.gif" width="420">
<br><b>Brandenburg Gate</b>
</td>

<td align="center">
<img src="assets/gifs/sacrecoeur.gif" width="420">
<br><b>Sacre Coeur</b>
</td>
</tr>

<tr>
<td align="center">
<img src="assets/gifs/trevi.gif" width="420">
<br><b>Trevi Fountain</b>
</td>

<td align="center">
<img src="assets/gifs/pantheon.gif" width="420">
<br><b>Pantheon Exterior</b>
</td>
</tr>
</table>

UH-GS effectively identifies unreliable observations and suppresses dynamic artifacts caused by pedestrians, vehicles, and transient occlusions, leading to cleaner geometry and higher-fidelity novel-view rendering.

---

## Installation

```bash
git clone https://github.com/haoran269/UH-GS.git
cd UH-GS

conda create -n uhgs python=3.10
conda activate uhgs

pip install -r requirements.txt
```

## Training

```bash
python train.py -s <dataset_path>
```

## Evaluation

```bash
python render.py -m <model_path>
python metrics.py -m <model_path>
```

## Dataset

We evaluate UH-GS on:

* Photo Tourism Dataset
* On-the-Go Dataset

Please follow the dataset instructions provided in the corresponding benchmark repositories.

## Citation

```bibtex
@article{gao2026uhgs,
  title={UH-GS: Uncertainty-guided Hierarchical Gaussian Splatting for Robust Outdoor Scene Reconstruction},
  author={Gao, Haoran and others},
  journal={...},
  year={2026}
}
```
