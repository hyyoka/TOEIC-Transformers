# Code for TOEIC-Transformers

*Hyowon Cho, Woojin Chung, & Sanghoun Song*: TOEIC-Transformers;Assessing the deep learning language models
with the cloze test in TOEIC (2021)

## Abstract
This study primarily focuses on measuring the linguistic ability of deep learning language models in a simple yet different way. Based on the purpose, we intend to suggest the direction of improvement of the model by analyzing the types of errors that the deep learning system misjudged and present the clue for the selected answer by attention visualization. 

Recently, deep learning models have demonstrated language proficiency that surpass humans in various benchmarks of natural language processing. However, this is difficult to fully trust for the following reasons. First, because background knowledge is structured to engage in problem-solving, it does not assess pure language proficiency. Second, the reliability of the score is low because the test dataset is not composed of uniform difficulty. Third, there is a risk of performance degradation because the dataset is not sufficiently refined. Finally, the difficulty and quality of the problems constituting the data set are not suitable for evaluating language proficiency. As an attempt to solve the problems raised to a certain extent, this study uses the TOEIC blank type problem to check the language proficiency of the deep learning model. 

In order to compare the performance difference according to the structure, three different Transformer-based language models were used (BERT, XLNet, ELECTRA). 
In addition, two methods were introduced to investigate the performance change according to the fine-tuning method. First, the language model uses a method to find the most similar correct answer candidate (distractor) after filling in the blanks. Second, the model was trained by redefining problem solving in the form of a multiple classification task and selecting the candidate with the highest probability of entering the blank. As a result of the study, the highest accuracy was achieved when the multiple classification method was applied to XLNet (92.4%).

## Experiments
### Dataset

![스크린샷 2021-08-16 오후 6.16.15](https://i.imgur.com/q3KHDBY.png)

![스크린샷 2021-08-16 오후 6.17.30](https://i.imgur.com/5SOnKX9.png)

### Models
- BERT
- AlBert
- RoBerta
- DistilBERT
- XLNET
- ELECTRA
- Longformer
- GPT2
- T5

## Usage
### Requirements
Python 3.6 or higher
Pytorch >= 1.2.0 (preferably with CUDA support)
transformers
sentencepiece

## Results
Best combination: batch:16, epoch:16, learning rate:1e-5

![스크린샷 2021-08-16 오후 6.18.08](https://i.imgur.com/ZgJseLc.png)
