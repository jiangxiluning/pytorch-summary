# Changes

- [x] Embedding Input
- [ ] Receptive Field

## Keras style `model.summary()` in PyTorch
[![PyPI version](https://badge.fury.io/py/torchsummary.svg)](https://badge.fury.io/py/torchsummary)

Keras has a neat API to view the visualization of the model which is very helpful while debugging your network. Here is a barebone code to try and mimic the same in PyTorch. The aim is to provide information complementary to, what is not provided by `print(your_model)` in PyTorch.

### Usage

- `pip install -e .` or 

For the input is sequence, especially when the model is RNN or encoder-decoder and etc.

```python
from torchsummary import summary
from torchsummary import InputFactory

input1 = InputFactory((10,), device=model.device, is_seq=True, vocab_size=input_dim)
input2 = InputFactory((10,), device=model.device, is_seq=True, vocab_size=output_dim)

summary(model, [input1, input2])
```

## Other useage please refer to https://github.com/sksq96/pytorch-summary 
