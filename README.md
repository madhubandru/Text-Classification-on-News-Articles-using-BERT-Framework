# Text-Classification-on-News-Articles-using-BERT-Framework

### Team Members
* Madhu Bandru - mb4236@drexel.edu
* Spandana Bendi - sb4262@drexel.edu
* Vuthej Krishna Reddy Verama Reddy - vv334@drexel.edu

### Motivation

Natural Language Processing (NLP) has many applications such as Sentiment Analysis, Text Classifications, Chatbots & Virtual Assistants, Text extractions, Text summarization and many more. Our team explored and worked on projects related to text extraction, sentiment analysis and text summarization individually. Now, for this term project we are interested to work on <b>“Intent Classification”</b> task. Intent Classification is a classification problem, which assigns a label to the given user query. This will be a multiclass-classification where the user queries will be labelled from four different categories. For example query *“Reuters - Private investment firm Carlyle Group,\which has a reputation for making well-timed and occasionally\controversial plays in the defense industry, has quietly placed\its bets on another part of the market.”* is labelled as <b>“Business”</b> while query *“AP - Kevin Hartman made seven saves for Los Angeles, and Jon Busch had two saves for Columbus as the Galaxy and Crew played to a 0-0 tie Saturday night.”* is labelled as <b>“World”</b>.  These examples are samples from “AG’s News Corpus Data”.

Intent classification plays a crucial role in business growth. Intent classifier identifies the actual intent of the customer and helps in suggesting a valuable/accurate service. Everyday there will be thousands of customer queries in different firms or applications. Manual attention for every query is a hectic task and this is where the intent classifier makes this job easy.

### Methodologies

1.	Approach-1: Baseline Model – Simple Sequential Neural Network.
2.	Approach-2: BERT Model with Keras Embeddings.
3.	Approach-3: BERT model using BERT’s default embedding technique.
4.	Approach-4: BERT model using embeddings from ELMo.

### IDE

1. Google Colab

### Packages

1. Tensorflow
2. Keras
3. Pytorch
4. Pandas
5. Numpy
6. Matplotlib

### Files included

#### Code Files

As implemented three different succesful approaches for text classification, we have maintained a single notebook for each approach. We have also included approach-4 notebook although the experiment was unsucessful.

<b>Colab Links</b>
* Approach-1: https://colab.research.google.com/drive/1n_cOeRdQVS2hQDtZA-hPL7Yt3r4GhY4w#scrollTo=fqfaav6ay9Zf
* Approach-2: https://colab.research.google.com/drive/1pGUD1AJ5gCdnUzk_gXI_s0fi4M0v--QK#scrollTo=b2XOSLa3SqBh
* Approach-3: https://colab.research.google.com/drive/1aEXyBsM7l6kCXBs6Uxyz2g1aUSu0OgLv#scrollTo=bW4GkNDLwEei
* Approach-4: https://colab.research.google.com/drive/1jsZtjhqit0PKMgM9y_UMNQgOzSr4vF3R#scrollTo=3k2gU7oU5sPL

#### Data Files

We have included the all original data csv files and also include file <b>sample.csv</b> which is a renamed version of text.csv with heading added in the top row. Same file has been used for all experiments.

##### Fields in Dataset
1. Class - Category of the news
2. Title - Heading of the news
3. Article - Content of the news

##### Field and type
1. Class - Numeric
2. Title - String
3. Article - String

#### Text Preprocessing File

We have maintained a separate py file for text cleaning for removing junk characters, special characters, extra white spaces and convert number to words. We used this <b>preprocess_data.py</b> to clean the article column from the loaded data.

### How to use files
Each approach file is independent so, there is no sequence to follow in execution of approaches.
* Step-1: Open the colab notebook of any approach.
* Step-2: Load <b>sample.csv</b> and <b>preprocess_data.py</b> files into the session.
* Step-3: Connect the session to GPU by changing in <b>runtime>>change runtime type>>select GPU>>Save</b>.
* Step-4: Run all the code cells till end.

### Challenges or Limitations

1. Due to limited (free) GPU resources by Colab, we could not perform experiments on large data set.
2. Categorical values in the dataset are starting from 1 due to which we faced error <b>CUDA runtime errors. - (Incompatible if started target class variable started off from 1)</b>. We resolved this by changing the classes to start from 0. 
3. In approach-4, we faced CUDA memory issue when passing ELMo embeddings to BERT model and it is resolved by limiting the data to 50 records. After that we faced <b>RuntimeError: CUDA error: device-side assert triggered</b> and tried to resolve it but unsuccessful. 
