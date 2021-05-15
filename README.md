# SNN-Distill
CS242 Final Course Project GitHub Repository for Hamza Chaudhry & Joshua Benjamin III.

## Set Up
with anaconda :
```setup
git clone https://github.com/hamzatc/snn_distill
cd snn_distill
conda env create -f snn_distill.yaml
conda activate snn_distill
```

## Training

To train the model, run `main.py`. Default values of each arguments are specified in `main.py`. Run `python main.py --help` for an explanation of each parameter.

For example, to train a spiking neural network on MNIST, run following command:  

```train
python main.py --task mnist --tag <model name>
```

The tag will be the name of the directory where the model's training/evaluation information is saved

## Evaluation

To evaluate a trained model on the test dataset, run the following code:

```eval
python main.py --eval-mode --gpu --tag <name of model to evaluate>
```

## Distillation
```eval
python main.py --task mnist --gpu --distill-mode --tag <model name>
```

This repository builds upon theory and code for SNN backpropagation defined in this paper: [Unifying Activation- and Timing-based Learning Rules for Spiking Neural Networks](https://papers.nips.cc/paper/2020/file/e2e5096d574976e8f115a8f1e0ffb52b-Paper.pdf) (NeurIPS 2020)
