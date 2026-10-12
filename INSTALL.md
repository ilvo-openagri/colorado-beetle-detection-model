# Installation and use

This repository distributes pretrained and converted model artifacts. It does
not include a Python application, dependency manifest, or the complete training
dataset.

## Obtain the artifacts

Clone this repository:

```shell
git clone https://gitlab.ilvo.be/openagri/colorado-beetle-models.git
cd colorado-beetle-models
```

If you already have a clone and need its latest committed version:

```shell
git pull --ff-only
```

## Select a model

Choose a model directory and export format supported by your inference code and
runtime. The repository contains, among others:

- TensorFlow SavedModels and TensorFlow Lite exports (`model64/`, `model128/`,
  `model256/`, and `yolo256_saved_model/`).
- Ultralytics YOLO PyTorch weights (`.pt`), ONNX (`.onnx`), TorchScript
  (`.torchscript`), and NCNN exports.
- Hailo compiled artifacts (`.hef`) and Hailo archive files (`.har`).

These formats require different software and, for Hailo artifacts, compatible
Hailo hardware and runtime versions. Consult the documentation for the
inference framework or device runtime you plan to use. This repository does not
provide a universal inference command or install those runtimes.

## Training and conversion

The complete training dataset and model-training pipeline are not included.
Some model directories contain calibration samples or intermediate exports
needed for specific conversion workflows. Review the notes in the relevant
model directory and the upstream framework or vendor documentation before
attempting to retrain or convert a model.

## License

Review [`LICENSE`](LICENSE) and [`NOTICE`](NOTICE) before using or redistributing
the artifacts. Third-party software, vendor-specific formats, and materials
from other rightsholders may be subject to additional terms.
