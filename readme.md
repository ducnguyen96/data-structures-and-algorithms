# *DocFace*: Matching ID Document Photos to Selfies

By Yichun Shi and Anil K. Jain

<img src="https://raw.githubusercontent.com/seasonSH/DocFace/master/figs/docface.png" width="600px">

## Contents
0. [Introduction](#introduction)
0. [Requirements](#requirements)
0. [Usage](#usage)

## Introduction

This repository is a implementation of [DocFace](https://arxiv.org/abs/1805.02283) which is a system proposed for matching ID photos. 

DocFace is shown to significantly outperform general face matchers on the ID-Selfie matching problem.

To align the face images we're using [MTCNN](https://github.com/kpzhang93/MTCNN_face_detection_alignment)

## Requirements
1. Requirements for `Python3`
2. Requirements for `Tensorflow`
3. Requirements for `scipy numpy Pillow`
4. Requirements for `mxnet` for MTCNN face alignment.

## Usage
This repository is an API run on cloud sever by Flask to compare faces in two pictures.

Assume that we are in idSelfieMatching fordel.

Run `python3 run.py` to run the api on your sever.

The api request a dictionary contrains 2 URLs:

```python
face_url = request.form.get("face_image", "")
id_url = request.form.get("id_image", "")
```
