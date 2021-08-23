# Youtube-captions-summarizer
**Objective** <br />Used advanced NLP techniques to summarize the video by extracting captions
*****
**Requirement** <br />
Nowadays, Videos which are too long on youtube are really hectic to watch. We watch a hour long video and try to grab the important ideas from it. What if we can let a system do it. With this GUI, you can select any video on youtube and summarize it. The summary contains all the useful ideas. 
*****

**Approach**:

1. Extracted captions of video using youtube_dl, read them using webvtt python module and cleaned the collected data by removing timestamps<br />
2. Used 3 NLP text summarization techniques - TfIdf-Based, Frequency-Based and Gensim-Based<br />
3. Used Spacy NLP library to process this large volume of data <br />
4. Built a GUI using tkinter library of python which saves summarized data at a particular location<br />
*****
**Python Library Requirements**:<br />
webvtt-py==0.4.5<br />
youtube_dl==2020.3.24<br />
pandas>=1.0.1<br />
gensim==3.8.1<br />
scikit-learn==0.22.2.post1<br />
spacy==2.2.4<br />
*****
**NLP Techniques detail**:
1. **Tf-Idf based** <br />TF-IDF is a statistical measure that evaluates how relevant a word is to a document in a collection of documents. This is done by multiplying two metrics: how many times a word appears in a document, and the inverse document frequency of the word across a set of documents.
TF — Term Frequency: This is the number of times the word appears in the document<br />
TF = ( Number of times a word appears in a document ) / ( Number of words in the document)<br />
IDF- Inverse Document Frequency: This downscales the word which appear frequently across the documents.<br />
IDF = log_e(Number of documents/ Number of documents in which the term appears)<br />
Basically TF-IDF increases the value of the words or token which are important for the document.<br />

2. **Frequency-Based/Count-based** It is used to transform a given text into a vector on the basis of the frequency (count) of each word that occurs in the entire text. This is helpful when we have multiple such texts, and we wish to convert each word in each text into vectors (for using in further text analysis). CountVectorizer creates a matrix in which each unique word is represented by a column of the matrix, and each text sample from the document is a row in the matrix. The value of each cell is nothing but the count of the word in that particular text sample. 
3. **Gensim-Based** Compute TF-IDF by multiplying a local component (term frequency) with a global component (inverse document frequency), and normalizing the resulting documents to unit length. Formula for non-normalized weight of term i in document j in a corpus of D documents

weight_{i,j} = frequency_{i,j} * log_2 \frac{D}{document\_freq_{i}}

*****
**Future Work**:
1. Can be used in summarizing foreign languages videos<br />
2. Can be used to summarize long educational videos on platforms like Udemy, Udacity<br />
3. Can be used to summarize a long speech or a self help video on youtube<br />
