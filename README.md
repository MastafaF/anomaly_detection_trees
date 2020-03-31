# Introduction 

The goal here is to compare Extended Isolation Forest (EIF) with Isolation Forest (iForest). EIF is 
supposed to be an improved version of iForest. They are supposed to achieve good performance
 on unsupervised anomaly detection. Hence it is worth comparing both 
models on NLP tasks in an Anomaly Detection setting. They do unsupervised anomaly detection so no labels need
 to be fed to the two models at training time. 

# Goals

1. We compare the two models between each other. 
2. We analyse the sensitivity of the models with respect to the dimension of the input space. 
3. We analyse the effect of the percentage of anomalies in the training data on overall performance => 

# Background 

They consider two assumptions:  
1. Anomalies are deviated from standard data 
2. Anomalies are few 

@TODO: write more about it. 

# Examples 

1. **SPAM Collection Dataset:**  
SPAM Collection Dataset is a monolingual dataset in English. There are approximately 87% nonSPAM data and 13% SPAM data.   
In our analysis, we leave the prior distributions as is following a uniform distribution 
for each class. However, according to the paper, EIF and iForest are sensitive to
the number of anomalies. A problem with too many anomalies can be an issue. It could be interesting
to see how they would perform when reducing the percentage of anomalies at training time. 

## Results: 
They have rather poor performance on high dimensional input data. Best performance is obtained with iForest after UMAP projection of the train and test data.  


In data folder, we add the data used in our SPAM Collection Dataset experiments. 
Embeddings are given with XLM-en with 2048 dimensions. We have used a MAX_LEN parameter
which in this case is either 20 or 40 tokens. (not sure which one was used here)  

2. Add more examples in NLP here. 
