# Machine learning models for severity classification and length-of-stay forecasting in emergency units

Length-of-stay prediction and severity classification for patients of emergency units in a clinic or hospital are crucial problems for public and private health networks.  An accurate estimation of these parameters is essential for the better planning of resources, which are usually scarce. Although it is possible to find several works that propose traditional ML to face these challenges, few works have used recent advances in natural language processing (NLP) on raw-text vector representations to improve these predictions. This article assesses the positive impact of incorporating word embeddings, which are functions with which words can be mapped into an n-dimensional vector space, to develop vector transformations of text information for inclusion in traditional machine learning models.  Moreover, we apply a strategy, which is based on Shapley Additive explanations (SHAP) values, to provide explanations for these predictions.  The results of our case study demonstrate an increase in the accuracy of the predictions using raw text with a minimum preprocessing of up to six percentage points for the classification of patients according to their level of severity. It increased by an average of two percent the accuracy obtained in the classification of
the patient’s post-care destination and by up to five percentage points for the prediction of the length of
stay in the hospital. In practical terms, if an emergency unit were to make use of these techniques, it could anticipate a patient’s need for hospitalization at the earliest stage of the care process. 

#Conclusion
After the experiments performed and the result obtained, we can conclude that the contribution of including free-text as training data for prediction and classification models, when available, is an extra effort considering classical ML methodologies. However, when datasets present missing or minor information, each valid data becomes crucial for obtaining good quality predictions and classifications. In the experiments developed, the vectorized text proved to contribute enough information for the prediction, improving the results or even being sufficient, on its own, to determine the severity category of patients at an acceptable level.
The results can certainly be better. There were free text variables in the original data set, which we did not consider in the research because they were very technical text, had acronyms, or were incomplete. The use of such sets would have been a significant contribution considering how valuable the event description set became, which, although more general and less technical, contributed significantly to improving the performance of the trained ML models.

Another relevant aspect is the importance of interpretability in ML. Although the models implemented in this research are not the most complex in this field of study, it is difficult to understand how they work and why the training data allowed us to obtain results such as those described. That is why explainability techniques provide transparency to the results, enable researchers to have more confidence in their results, and allow physicians or end-users to understand the behavior of relevant data in treating a patient. 
Finally, it is essential to mention the importance of recording health information. Hospitals are a large and endless source of information that must be analyzed. Contributions related to data analysis and ML techniques are immensely beneficial and undoubtedly open doors toward more expeditious and efficient management of patient treatment.
