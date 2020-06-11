This repository is a fork of [fairseq]() and contains the codes of diminishing attention and dynamic diminishing attention for BART-based summarization models and machine-translation models and Transformer-Big machine translation models. 

# dependencies: torch 1.4.0, apex
# Summarization (BART)
Please follow the intructions on the [fairseq page](https://github.com/pytorch/fairseq/tree/master/examples/bart) for downloading and pre-processing the dataset and downloading the BART-large checkpoint. 
## Train:
cd fairseq-train
<br>
pip install --editable .
<br>
bash train_summarization.sh 
<br>
(Set attention to DYDIMATTN and exp2 to 0.6 for training the dynamic diminishing attention model.) 
## Inference
cd fairseq-dec
<br>
bash infer_summarization.sh
<br>
pip install --editable .
<br>
<br>
(Please follow the instructions [here](https://github.com/pytorch/fairseq/tree/master/examples/bart) for obtaining ROUGE scores.)
# Translation
Please follow the instructions [here](https://github.com/pytorch/fairseq/blob/9f6b552d685711738aae21dbdf3868f4ca280cda/examples/scaling_nmt/README.md) for downloading the pretrained model and datasets. 
## Train
cd fairseq-train
<br>
pip install --editable .
<br>
bash train_translation.sh
<br>

(Set attention to DYDIMATTN and exp2 to 0.6 for training the dynamic diminishing attention model.)

## Inference
cd fairseq-dec
<br>
pip install --editable .
<br>
bash infer_translation.sh

## Pretrained models
* [CNN/DM DimAttn (BART)]()
* [Machine Translation En-De DimAttn]()
* [Machine Translation En-De DyDimAttn]()

