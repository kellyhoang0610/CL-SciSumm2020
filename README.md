
## CL-SciSumm 2020: The 6th Computational Linguistics Scientific Document Summarization Shared Task
### https://ornlcda.github.io/SDProc/sharedtasks.html#clscisumm

#### This repo contains code to preprocess data that used for the CL-SciSumm2020 Shared Task. Steps of data processing are:
1. Read annotation file to get citances (citing text) and reference text:
2. Read full-text of reference articles to get all sentences from reference articles.
3. Generate positive samples which are the pairs of citing text - reference text from the annotation file. 
4. Generate negative samples which are pairs of citing text - reference text that are not in the annotation file.

#### In particular:
Step 1: Run the notebook "CLSciSumm_DataPreprocessing_ReadAnnotationFile" which contain the following functions:
  + A function to read all of the annotation text file in the two folders: 
      /efs/CL-SciSumm/scisumm-corpus/data/Training-Set-2019/Task1/From-Training-Set-2018
      /efs/CL-SciSumm/scisumm-corpus/data/Training-Set-2019/Task1/From-ScisummNet-2019
  + Output of the function is an csv file (all_training_2018.csv) that contains the following columns: 'citance_number','reference_article', 'citing_article','citance_text','reference_text','discourse_facet','annotator'.
  + A function to analyze DISCOURSE FACET and Number of sentences in citances & reference text (For analysis purpose only). 
  
 Step 2: Get full-text of reference articles (Shinka's code here)
 
 Step 3: Run the notebook "CLSciSumm_DataPreprocessing_SplitSentences" which contain the following functions:
  + A function to read the "all_training_2018.csv" file and split reference text sentence by sentence. Output of the function is a splited data file that contain citances from the original annotation file and reference text which were broken down into sentences. These would be positive samples of our data
  + Note: some data need manually check. 
  
  Step 4: Run the notebook "CLSciSumm_Preprocess_NegativeSamples" which contain the following functions
