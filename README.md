# QPyTorch Inference code (ImageNet)
Reference : https://github.com/Tiiiger/QPyTorch

## Test accuracy(ResNet-50)
**Full precision**
> 76.11%

**FP8(exp=5,man=2)**
> 75.38%(Retuning)

> 75.08%(No retuning)

**FP8(exp=4,man=3)**
> 75.77%(Retuning)

> 72.14%(No retuning)

| Full precision | 76.11% | # | # | # |
| :---: | :---: | :---: | :---: | :---: |
| low precision | Retuning(no bias) | No Retuning(no bias) | Retuning(with bias) | No Retuning(with bias) |
| FP8(exp=5,man=2) | 75.38% | 75.08% | blank | blank |
| FP8(exp=4,man=3) | 75.77% | 72.14% | blank | blank |


## Usage
Arguments

```--mode : 0(full precision), 1(low precision)```

```--retuning : 0(No retuning), 1(Retuning)```

Example

```python q_infer.py --mode 1 --retuning 1```

## Requirement
QPyTorch (pip install qtorch)

torch

torchvision
