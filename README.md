# Text-Classification-on-News-Articles-using-BERT-Framework

### Team Members
* Madhu Bandru - mb4236@drexel.edu
* Spandana Bendi - sb4262@drexel.edu
* Vuthej Krishna Reddy Verama Reddy - vv334@drexel.edu


### Files included

#### Code Files

As implemented three different succesful approaches for text classification, we have maintained a single notebook for each approach. In approach experimented is not successfully completed so, we dint include the notebook for same.

1.	Approach-1: Baseline Model – Simple Sequential Neural Network.
2.	Approach-2: BERT Model with Keras Embeddings.
3.	Approach-3: BERT model using BERT’s default embedding technique.
4.	Approach-4: BERT model using embeddings from ELMo.

<b>Colab Links</b>
* Approach-1: https://colab.research.google.com/drive/1n_cOeRdQVS2hQDtZA-hPL7Yt3r4GhY4w#scrollTo=fqfaav6ay9Zf
* Approach-2: https://colab.research.google.com/drive/1pGUD1AJ5gCdnUzk_gXI_s0fi4M0v--QK#scrollTo=b2XOSLa3SqBh
* Approach-3: https://colab.research.google.com/drive/1aEXyBsM7l6kCXBs6Uxyz2g1aUSu0OgLv#scrollTo=bW4GkNDLwEei

#### Data Files

We have included the csv files of original data set and also include csv names <b>sample.csv</b> in which added the header and used same file all experiments.

#### Text Preprocessing File

We have maintained a separate py file for text cleaning for removing junk characters, special characters, extra white spaces and convert number to words. We used this <b>preprocess_data.py</b> to clean the article column from the loaded data.

#### How to use files
Each approach file is independent so, there is no sequence to follow in execution of approaches.
* Step-1: Open the colab notebook for any approach.
* Step-2: Load <b>sample.csv</b> and <b>preprocess_data.py</b> files into the session.
* Step-3: Connect the session to GPU by changing in <b>runtime>>change runtime type>>select GPU>>Save</b>.
* Step-4: Run all the code cells till end.

#### Challenges or Limitations

1. Due to limited (free) GPU resources by Colab, we could not perform experiments on large data.
2. Categorical values in the dataset are starting from 1 due to which we faced error <b>CUDA runtime errors. - (Incompatible if started target class variable started off from 1)</b>. We resolved this by changing the class from 0. 
3. In approach-4, we faced CUDA memory issue when passing ELMo embeddings to BERT model and it is resolved by limiting the data to 50 records. After that we faced <b>RuntimeError: CUDA error: device-side assert triggered</b> and tried to resolve it but unsuccessful. 
