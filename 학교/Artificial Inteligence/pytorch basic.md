# Pytorch Basic
> This page is for pytorch basic functions
---
### How to initialize tensors?

- `torch.empty()`
	This method make **uninitialized** tensor which has input shape.
	`torch.empty(5, 3)` will make uninitalized 5 by 3 tensor
- `torch.rand()`
	This method make **random** value tensor which has input shape
- `torch.zeros()`
- `torch.tensor()`
	Construct a tensor directly from data
- `torch.randn_like(x, dtype=)`
	Construct a tensor which *has same size with x*

### Operations for tensor

- `torch.add(x, y, out= )`
	Could assign output tensor with `out=` parameter

- `y.add_(x)`
	in-place add operator

### Things to watch out for when slicing a tensor

> The dimension of sliced tensor could change depending on the slicing method
> - `x[:, 1]` will return **1-dimension tensor**
> - `x[:, 1:2]` will return **2-dimension tensor**

### How to reshape tensor

- 'tensor.view()'
	```
	x = torch.randn(4, 4)
	print(x.view(16)) # 1-dimension tensor
	print(x.view(-1, 8)) # 2-dimension 2by8 tensor
	```
