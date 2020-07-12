# DL-terminology-extraction
Terminology extraction based on Bi-LSTM models and word embeddings.

The file 'Terminology_extraction_BILSTM_Glove_INSPEC.ipynb' contains the code of the implementation of a model for terminology extraction based on bidirectional LSTM with variants. 
The model is trained, tested and evaluated with INSPEC dataset, whoso documents are available in the folder 'Datasets/INSPEC'. 
Glove embeedings are used as a vector representation of the words. These representations are directly downloaded from 'http://nlp.stanford.edu/data/glove.6B.zip'. The vocabulary created with INSPEC dataset and Glove word embeddings is saved in a pickle file in the folder 'Embeddings'. It might be also created the first time that the dataset is preprocessed.
The terminology extracted from INSPEC test dataset abd COVID-19 corpus is saved as a csv file in the folder 'Terminology'.

The Colab Notebook allows to set different parameters:
* new_model: if True, the code train a new model. Once that the model is created, it can be loaded setting the parameter as False. The created model is saved as defined in 'MODEL_PATH'.
* save_term_test: it allows to save the terminology obtained from INSPEC test dataset. It is saved in the path named in 'TERM_PATH_INSPEC'.
* improved_model: if True, the model created will have a deeper structure based on two BiLSTM hidden layers. 
* predict: if True, the model is used to extract terminology from an unnanotated corpus. The corpus might be saved in the folder defined in 'CORPUS_PATH'. The terminology is saved in the path 'TERM_PATH_CORPUS'.
* only_predict: when True, the model trained is used only to predict the terminology from an unnanotated corpus.
* new_corpus: if True, the code generates the structure to use a new corpus. The documents of this new corpus should be in the folder 'CORPUS_PATH'. If False, the terminology extraction will be of the COVID-19 corpus.
