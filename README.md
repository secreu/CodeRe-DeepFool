# DeepFool
DeepFool is a simple algorithm to find the minimum adversarial perturbations in deep networks

### pip list
Package         Version
--------------- -------
cycler          0.11.0
future          0.18.3
kiwisolver      1.3.1
matplotlib      3.3.4
numpy           1.19.5
Pillow          8.4.0
pip             21.3.1
pyparsing       3.1.0
python-dateutil 2.8.2
setuptools      59.6.0
six             1.16.0
torch           1.6.0
torchvision     0.7.0
wheel           0.37.1

### deepfool.py

This function implements the algorithm proposed in [[1]](http://arxiv.org/pdf/1511.04599) using PyTorch to find adversarial perturbations.

__Note__: The final softmax (loss) layer should be removed in order to prevent numerical instabilities.

The parameters of the function are:

- `image`: Image of size `HxWx3d`
- `net`: neural network (input: images, output: values of activation **BEFORE** softmax).
- `num_classes`: limits the number of classes to test against, by default = 10.
- `max_iter`: max number of iterations, by default = 50.

### test_deepfool.py

A simple demo which computes the adversarial perturbation for a test image from ImageNet dataset.

## Reference
[1] S. Moosavi-Dezfooli, A. Fawzi, P. Frossard:
*DeepFool: a simple and accurate method to fool deep neural networks*.  In Computer Vision and Pattern Recognition (CVPR ’16), IEEE, 2016.
