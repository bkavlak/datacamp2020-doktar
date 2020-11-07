# Agricultural Boundary Delineation <a href='https://www.doktar.com/'><img src='../../images/doktarhex2.png' align="right" height="139" /></a>

This repository consists of materials that are used
in [Datacamp 2020](http://datacamp.boun.edu.tr/) workshop
 at [Bogazici University](http://www.boun.edu.tr/en-US/Index).


## Requirements

- [Google Earth Engine Registration](https://code.earthengine.google.com/)

## Agricultural Boundary Delineation

We will hopefully extract boundaries of agricultural fields
with image processing techniques on GEE. We will try to translate
the processes of a paper about boundary delineation.

At first, we will try to understand convolutions and their use basically.

### Convolution arithmetic

The images and explanations are copied from this file & repository to illustrate
how convolutions behave:

* \[1\] Vincent Dumoulin, Francesco Visin - [A guide to convolution arithmetic
  for deep learning](https://arxiv.org/abs/1603.07285)
  ([BibTeX](https://gist.github.com/fvisin/165ca9935392fa9600a6c94664a01214))
  
* \[2\] Vincent Dumoulin, Francesco Visin - [Github Repository](https://github.com/vdumoulin/conv_arithmetic)

#### Convolution animations

_N.B.: Blue maps are inputs, and cyan maps are outputs._

<table style="width:100%; table-layout:fixed;">
  <tr>
    <td><img width="150px" src="gif/no_padding_no_strides.gif"></td>
    <td><img width="150px" src="gif/arbitrary_padding_no_strides.gif"></td>
    <td><img width="150px" src="gif/same_padding_no_strides.gif"></td>
    <td><img width="150px" src="gif/full_padding_no_strides.gif"></td>
  </tr>
  <tr>
    <td>No padding, no strides</td>
    <td>Arbitrary padding, no strides</td>
    <td>Half padding, no strides</td>
    <td>Full padding, no strides</td>
  </tr>
  <tr>
    <td><img width="150px" src="gif/no_padding_strides.gif"></td>
    <td><img width="150px" src="gif/padding_strides.gif"></td>
    <td><img width="150px" src="gif/padding_strides_odd.gif"></td>
    <td></td>
  </tr>
  <tr>
    <td>No padding, strides</td>
    <td>Padding, strides</td>
    <td>Padding, strides (odd)</td>
    <td></td>
  </tr>
</table>

#### Transposed convolution animations

_N.B.: Blue maps are inputs, and cyan maps are outputs._

<table style="width:100%; table-layout:fixed;">
  <tr>
    <td><img width="150px" src="gif/no_padding_no_strides_transposed.gif"></td>
    <td><img width="150px" src="gif/arbitrary_padding_no_strides_transposed.gif"></td>
    <td><img width="150px" src="gif/same_padding_no_strides_transposed.gif"></td>
    <td><img width="150px" src="gif/full_padding_no_strides_transposed.gif"></td>
  </tr>
  <tr>
    <td>No padding, no strides, transposed</td>
    <td>Arbitrary padding, no strides, transposed</td>
    <td>Half padding, no strides, transposed</td>
    <td>Full padding, no strides, transposed</td>
  </tr>
  <tr>
    <td><img width="150px" src="gif/no_padding_strides_transposed.gif"></td>
    <td><img width="150px" src="gif/padding_strides_transposed.gif"></td>
    <td><img width="150px" src="gif/padding_strides_odd_transposed.gif"></td>
    <td></td>
  </tr>
  <tr>
    <td>No padding, strides, transposed</td>
    <td>Padding, strides, transposed</td>
    <td>Padding, strides, transposed (odd)</td>
    <td></td>
  </tr>
</table>

#### Dilated convolution animations

_N.B.: Blue maps are inputs, and cyan maps are outputs._

<table style="width:25%"; table-layout:fixed;>
  <tr>
    <td><img width="150px" src="gif/dilation.gif"></td>
  </tr>
  <tr>
    <td>No padding, no stride, dilation</td>
  </tr>
</table>
