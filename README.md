
## CL-SciSumm 2020: The 6th Computational Linguistics Scientific Document Summarization Shared Task
### https://ornlcda.github.io/SDProc/sharedtasks.html#clscisumm

#### This repo contains code to preprocess data that used for the CL-SciSumm2020 Shared Task. Steps of data processing are:
1. Read annotation file to get citances (citing text) and reference text. 
2. Read full-text of reference articles to get all sentences from reference articles.
3. Generate positive samples which are the pairs of citing text - reference text from the annotation file. 
4. Generate negative samples which are pairs of citing text - reference text that are not in the annotation file.
