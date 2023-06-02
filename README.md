# CIFAR10-Preprocessing-Analysis

This project aims to analyze how preprocessing techniques applied to image data can affect the accuracy results. It focuses specifically on using the CIFAR-10 dataset and a CNN architecture (Convolutional Neural Network). By examining different preprocessing methods, the project seeks to understand their impact on the performance of the CNN model in classifying images.

![CIFAR10](https://github.com/kevin-wijaya/CIFAR10-Preprocessing-Analysis/blob/main/image.png)

## Dataset Information

The CIFAR-10 dataset consists of 60000 32x32 colour images in 10 classes, with 6000 images per class. There are 50000 training images and 10000 test images.

The dataset is divided into five training batches and one test batch, each with 10000 images. The test batch contains exactly 1000 randomly-selected images from each class. The training batches contain the remaining images in random order, but some training batches may contain more images from one class than another. Between them, the training batches contain exactly 5000 images from each class.

The CIFAR-10 dataset classes: [Airplane, Automobile, Bird, Cat, Deer, Dog, Frog, Horse, Ship, Truck]

## Overview

### Preprocessing Experiment
<table>
  <thead><tr>
      <th>Preprocessing</th>
      <th>Loss</th>
      <th>Accuracy</th>
  </tr></thead>
  <tbody>
      <tr>
        <td align="left"><i>Original</i></td>
          <td align="center">0.577</td>
          <td align="center">82.65%</td>
      </tr>
      <tr>
          <td align="left">Equalization</td>
          <td align="center">0.748</td>
          <td align="center">78.53%</td>
      </tr>
      <tr>
          <td align="left">Equalization + Grayscale</td>
          <td align="center">0.785</td>
          <td align="center">76.88%</td>
      </tr>
      <tr>
          <td align="left">Grayscale + Laplacian</td>
          <td align="center">0.904</td>
          <td align="center">72.25%</td>
      </tr>
      <tr>
          <td align="left">Grayscale + Sobel</td>
          <td align="center">0.852</td>
          <td align="center">75.43%</td>
      </tr>
      <tr>
          <td align="left">Equalization + Grayscale + Segmentation</td>
          <td align="center">1.148</td>
          <td align="center">62.08%</td>
      </tr>
      <tr>
          <td align="left">Equalization + Grayscale + Laplacian + Sobel + Segmentation</td>
          <td align="center">2.303</td>
          <td align="center">9.58%</td>
      </tr>
  </tbody>
</table>

### Result
The best result is obtained by using the original data without any preprocessing, followed by validation using K-Fold cross-validation with K=3.
<table>
    <tr><td><b>Accuracy</b></td><td>92.98%</td></tr>
    <tr><td><b>Loss</b></td><td>0.253</td></tr>
</table>
