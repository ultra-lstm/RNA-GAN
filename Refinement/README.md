# LSTM Refinement

This is the code for the refinement network. We have a training script `v2.py` and a prediction script `predict.py`.

To train the model with 1 GPU use `CUDA_VISIBLE_DEVICES=1 python my_script.py`

# Input

To use these script you have to create a sequence list. The listname is stored in the variable file_list inside both script files. The list contains a formatable expression that looks like this: `{2}/Brats17_2013_10_1_{0}.nz.{1}.png`. The placeholders have the following meanings:
-  `{0}` replaced by string input_mode
-  `{1}` is a counter
-  `{2}` is the folder with the data, stored in the variable folder-  

The counter starts at sequence_start and end at sequence_start + sequence_length. The input images should have the same format than the test output of the cGAN. After training you can predict using the `predict.py` with the same configuration parameter.

# Folder

When using both scripts you have to create 4 folders: `outv2` `o1` `o2` `o3`.

# Software Requierements

  - python 2.7
  - tensorflow 0.11
  - keras 2
