# Hindi-and-Tamil-Question-Answering

This contains the code for the results obtained using mBERT, XLM-Roberta and indic-NLP on chaii dataset.

## Dataset :

The chaii-dataset was directly used for fine-tuning and besides that we used models that have been pre-trained on xQUAD, SQUAD2 and mergedQUAD. \
The chai dataset consists of : \
`id` : unique id for each input \
`context` : a paragraph based on which the question has to be answered \
`question` : the question that has to be answered \
`answer_start` : the index from which the answer starts (only train) \
`answer_text` : the answer in string format (only train)

## Models :

The models which were used are m-BERT (multilingual BERT), XLM-Roberta and indic-BERT.

## Train :

To train, run the notebooks after setting the proper address for tokenizer and model. \
The data that were used on kaggle are `huggingface-question-answering-models`, `ai4bharat-indic-bert`, `chaii-hindi-and-tamil-question-answering`.

## Test : 

For testing we have prepared the `submission.csv` file which is in the format demanded by kaggle. After running the notebook on kaggle just select the csv file from outputs and submit it.

## Results

|       Model       | no-finetuning           | finetuning (with freezing)           | finetuning (without freezing)           |  
| ------------------- | ------------- | ------------- | ------------- |
| mBERT | 0.0373        | 0.1013        | 0.2075        |
| XLM-RoBERTa | 0.2720        | 0.47679        | 0.5837        |
| indic-BERT | 0.0016        | -        | 0.0288        |
