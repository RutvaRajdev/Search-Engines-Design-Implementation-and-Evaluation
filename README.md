# Search-Engines-Design-Implementation-and-Evaluation
Design, Implementation and Evaluation of various Search Engines

INSTALLATION -Python
For Windows

There are various dependencies. 
You need to have Python 3.x installed.

Also It uses build-in libraries like operator, math , os and re
Also Install NLTK and Numpy and BeautifulSoup and urllib3
example to install
c:>pip install regex
c:>pip install beautifulsoup4 
c:>pip install numpy
c:>pip install nltk 
c:>pip install urllib3

by above commands

Results for each of the following codes are there in Results folder Phase and Task wise
How are we submitting the codes and the required outputs:

Implementation phase-1:

Task-1:
Codes: 
Lucene: ‘TextFileIndexer.java’ (how to run written at end of document)
Bm25, tf-idf, Smoothed Query: ‘Results/Phase-1-Task-1/3runswithoutstopping.py’
Results: 
Lucene: Folder ‘Results/Phase-1-Task-1/Lucene_BaseLine_Results’
Bm25: Folder ‘Results/Phase-1-Task-1/BM25_BaseLine_Results’
Tf-idf: Folder ‘Results/Phase-1-Task-1/TF-IDF_BaseLine_Results’
Smoothed Query: ‘Results/Phase-1-Task-1/SMQ_BaseLine_Results’

Task-2:
Code: ‘PRF.py’
Results: Folder ‘Results/Phase-1-Task-2/PRF_Results’

Task-3:
A. Code: ‘3runswithstopping.py’
	Results: 
Bm25: Folder ‘Results/Phase-1-Task-3/BM25_WithStopping_Results’
Tf-idf: Folder ‘Results/Phase-1-Task-3/TF-IDF_WithStopping_Results’
Smoothed Query: Folder ‘Results/Phase-1-Task-3/SMQ_WithStopping_Results’
     B.	Code: ‘3runswithstemming.py’
Results:
Bm25: Folder ‘Results/Phase-1-Task-3/BM25_WithStemming_Results’
Tf-idf: Folder ‘Results/Phase-1-Task-3/TF-IDF_WithStemming_Results’
Smoothed Query: Folder ‘Results/Phase-1-Task-3/SMQ_WithStemming_Results’ 

Implementation phase-2:

Code: ‘SnippetGeneration.py’
Results: Folder ‘Results/Phase-2-Snippets/BM25_Snippets_Results’

Implementation phase-3:

Code: ‘Evaluation.py’ for MAP , Precision and Recall, Precision At 5 And 20
Code: 'MRR.py' for MRR
Results:
MAP: Folder ‘Results/Phase-3-Evaluation/MAP’
MRR: Folder ‘Results/Phase-3-Evaluation/MRR’
P@K: Folder ‘Results/Phase-3-Evaluation/Precision At 5 And 20’
Precision: Folder ‘Results/Phase-3-Evaluation/Precision_Table’ 
Recall: Folder ‘Results/Phase-3-Evaluation/Recall_Table’

Extra credit:

Codes:
Without stopping: ‘Proximity_WithoutStopping.py’
With stopping: ‘Proximity_WithStopping.py’
Results:
Without stopping: Folder ‘Results/ExtraCredit/Results_withoutstop_proxi’
With stopping: Folder ‘Results/ExtraCredit/Results_withstop_proxi’
Evaluation:
MAP: Folder ‘Results/ExtraCredit/Map for no stopping.txt’
		          Folder ‘Results/ExtraCredit/Map for stopping.txt’
MRR: Folder ‘Results/ExtraCredit/Mrr for no stopping.txt’
		          Folder ‘Results/ExtraCredit/Mrr for stopping.txt’
Precision and recall tables: 
Folder ‘Results/ExtraCredit/precision and recall no stopping.txt’
		Folder ‘Results/ExtraCredit/precision and recall with stopping.txt’

Setup, compile  and run instructions

python Tokenizer.py : This shall create a folder(named SP) for all the parsed(i.e. Space separated) CACM files. This uses CACM folder which contains the given html files. The code and the CACM file should be in the same folder. 
python Indexer.py : for making the unigram indexer from the generated corpus. (select the option for unigram from given options). Input is taken from the SP folder which contains the space separated files. 
python 3runswithoutstopping.py : When this is run, it would provide options of the system for which you want the results. Namely,
BM25
Tf-Idf
Smoothed query
TextFileIndexer.java : run for lucene scoring system
python PRF.py : pseudo relevance feedback 
python 3runswithstemming.py : for generating results for the 3 runs with stemming. The corpus with stemming is already prepared by parsing the given stemmed documents. 
python SnippetGeneration.py : run to generate the snippets
python Evaluation.py : run on your choice of system to get the evaluation of the system you want. Precision, Recall, MAP(separate file for MRR)
python MRR.py : calculates the MRR of the system
python Proximity_WithoutStopping.py for Proximity without stopping
python Proximity_WithStopping.py for Proximity with stopping

There are some other helper python files too which need to be in the main folder, in the same way as submitted by us.

LUCENE
java
The documentation of lucene had the code in java which is used

The java program can be compiled as

javac -cp ".;<PATH>\lib\lucene-analyzers-common-4.7.2.jar;<PATH>\lib\lucene-core-4.7.2.jar;<PATH>\lib\lucene-queryparser-4.7.2.jar" *.java

Run using
java -cp ".;<PATH>\lib\lucene-analyzers-common-4.7.2.jar;<PATH>\lib\lucene-core-4.7.2.jar;<PATH>\lib\lucene-queryparser-4.7.2.jar" TextFileIndexer
Where the PATH in the above is the path of the dir where this Folder is saved 
Please Enter the Entire Path

Command line arguments can be entered using the instructions after running the code

Once  the index is created in a folder before re running the program delete the old index created

While Using the raw text or document use the path of the "\SP" Folder given in this file
The output are just printed and not written to the file
