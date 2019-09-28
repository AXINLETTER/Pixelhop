Yifan Wang  
yifanwang0916@outlook.com  
last update 2019.09.25

# Pixelhop
From [arXiv:1909.08190](https://arxiv.org/abs/1909.08190). This is a well packed Pixelhop Layer with simple usage. It uses Saab ([arXiv:1810.02786](https://arxiv.org/abs/1810.02786)) inside it, part of the Saab code is modified from https://github.com/davidsonic/Interpretable_CNN. 

## Usage
Run the code in `Python3` in `./src` folder.

*`x`* -> Input, 4-D tensor `(N,H,W,D)`, the same as `channel_last` mode in Keras. 

*`dilate`* -> Controls location of chooesn neghbour pixels.   

*`pad`* -> Padding, support `none`, `reflect`, `zeros` (default: `reflect`)  

*`num_AC_kernels`* -> Number of AC components to be kept.  

*`weight_name`* -> Saab kernel file location to be saved or loaded. (default: `../weight/+weight_name`)  

*`getK`* -> If use input to compute Saab kernel. (default: `True`) 

*`useDC`* -> If add DC component. (default: `False`)  
```
x1 = PixelHop_Unit(x, dilate=1, pad='reflect', num_AC_kernels=9, weight_name='pixelhop1.pkl', getK=True, useDC=False)
```

## Example
One example is shown in `./src/example.py`. 