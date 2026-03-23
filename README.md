# WavLM-Multitask-Vietnamese-Speech-Region-and-Gender-Recognition-on-an-Expanded-Three-Region-Dataset
This repository is a substantially revised version of the conference paper “Speech Region and Gender Recognition on a Vietnamese Accent Dataset,” presented at CSoNet 2025. The present journal manuscript includes a substantially expanded dataset, a revised raw-waveform preprocessing pipeline and a new WavLM-based multitask architecture

# From Handcrafted Features to WavLM: Multitask Vietnamese Speech Region and Gender Recognition on an Expanded Three-Region Dataset

This repository contains the code, metadata, experiment settings, and result artifacts for our study on Vietnamese speech region recognition and gender recognition using an expanded three-region dataset and a multitask WavLM-based model.

## Overview

This project extends our earlier VA3R-based work in two main ways:

1. It expands the original VA3R dataset by integrating additional Vietnamese dialectal speech material derived from the ViMD resource while preserving the same three macro-region labels:
   - North
   - Central
   - South

2. It replaces the earlier handcrafted-feature + CNN2D pipeline with a raw-audio multitask framework based on a shared pretrained WavLM encoder with two classification heads:
   - region prediction head
   - gender prediction head

The project compares:
- the earlier CNN-based approach rerun on the expanded dataset
- the proposed multitask WavLM model on the same expanded dataset

## Main Results

### Speech region recognition
- Conference baseline CNN2D on original VA3R: **43.00% accuracy**
- CNN2D on expanded dataset: **53.25% to 54.37% accuracy**
- Proposed WavLM multitask model: **72.76% accuracy**, **71.70% macro-F1**

### Speech gender recognition
- Conference baseline CNN2D on original VA3R: **86.00% accuracy**
- CNN2D on expanded dataset: **90.01% to 91.90% accuracy**
- Proposed WavLM multitask model: **95.90% accuracy**, **95.43% macro-F1**

## Dataset Summary

### Original VA3R
- Total clips: **8,254**
- Region totals: **North 2,857 / Central 2,853 / South 2,540**
- Gender totals: **Male 4,761 / Female 3,489**
- The dataset is available on this Kaggle page: https://www.kaggle.com/datasets/lnt0821/vietnamese-accent-3-regions

### Expanded dataset
- Total clips: **16,156**
- Region totals: **North 5,714 / Central 5,554 / South 4,888**
- Gender totals: **Male 10,722 / Female 5,434**
- The MFCC converted version for the CNN2D baseline model was uploaded to this repository
- The raw-audio version is available in this Kaggle folder: https://www.kaggle.com/datasets/lnt0821/vietnamese-accent-3-regions?select=Expanded+dataset+for+JOCO
