# FlowBender

Official implementation of **FlowBender: Feedback-Aware Training for Self-Correcting Conditional Flows** (Gilo et al., 2026).

- 🌐 Project page: https://flow-bender.github.io/
- 📄 Paper: https://arxiv.org/pdf/2606.20404

FlowBender is a feedback-aware training method for conditional generation with flow matching models: the model is trained to correct its own errors along the sampling trajectory. This self-correction capability improves sample quality and adherence to the provided condition across different conditional generation tasks, such as depth-to-RGB, edge-to-RGB, image super-resolution, JPEG restoration, and 3D mesh texturing.

This repository hosts the code for the two experiment tracks presented in the paper, each maintained as an independent, stand-alone submodule:

| Submodule | Description |
|---|---|
| [`image-to-image`](image-to-image) | Image-to-image experiments, built on top of ControlNet with SD3.5 ([FlowBender-I2I](https://github.com/selflein/FlowBender-I2I)). |
| [`3d-texturing`](3d-texturing) | 3D mesh texturing experiments, built on top of [TRELLIS.2](https://github.com/DanielGilo/flowbender-texturing-trellis2). |

Each submodule is self-contained and includes its own setup, training, and evaluation instructions — see the README inside each one.

## Getting the code

Clone with submodules:

```bash
git clone --recurse-submodules https://github.com/DanielGilo/FlowBender.git
```

If you've already cloned the repo without submodules, fetch them with:

```bash
git submodule update --init --recursive
```

## Citation

If you find this work useful, please cite:

```bibtex
@misc{gilo2026flowbenderfeedbackawaretrainingselfcorrecting,
  title         = {FlowBender: Feedback-Aware Training for Self-Correcting Conditional Flows},
  author        = {Daniel Gilo and Sven Elflein and Ido Sobol and Or Litany},
  year          = {2026},
  eprint        = {2606.20404},
  archivePrefix = {arXiv},
  primaryClass  = {cs.CV},
  url           = {https://arxiv.org/abs/2606.20404},
}
```
