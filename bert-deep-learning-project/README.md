Project Theme: Deep Learning Text Classification using BERT (BERT Base Portuguese, BERT Large Portuguese, Multilingual BERT) language models, as well as derived methods (ALBERT, DISTILBERT, ROBERTA, XLM-ROBERTA, and DEBERTA), 

This project is an update of the machine learning notebooks used in developing a Django and React web application as a requirement for earning a degree in Computer Science in Universidade Paulista, Brazil, in 2022.

Keys Skills for building datasets and machine learning notebooks
along with Semantic Similarity assessment using Sentence-BERT.
Tasks: Data Extraction, Data Preprocessing and Cleaning, Text Binary Classification, Text Multilabel Classification, Semantic Similarity Assessment, Deep Learning Model Configuration and Evaluation, Comparison of Deep Learning Models.

Key Libraries used: numpy, pandas, scikit-learn, scipy, transformers.

Challenges: Implementing thorough data preprocessing steps, removing irrelevant information, transforming the data into a format suitable for machine learning models, addressing imbalanced classes in the multilabel classification task, configuring a model for multilabel classification to accurately predict multiple themes for each data point and evaluating models based on various metrics and choosing key metric to compare performance(validation loss, accuracy, precision, recall, and F1 Score).

# Abstract of the original paper

The original paper's abstract is provided below. As a summary of the project, the objective was to develop na application to be integrated in What's App via a bot and in a website, where a user could type or paste a text of a Covid-related news and get a response detailing the if the news as likely a case of disinformation or not, the top 3 possibly related themes and top 5 similar claims of news already fact-checked, with links to each and an assessment of the checked alegations.

“Fake news” is an umbrella term that is being widely discussed due to growing concerns about its impact on the formation of ideas and opinions of billions of people who use new means of communication such as social networks. In this work, Fake News is characterized as cases of disinformation. The objective of this project is to identify an efficient way to analyze a case of disinformation that is being shared on the most accessed social networks and to discern the probability of being a veridical case based on concrete data, collected using data extraction from the Internet. The defined scope for the data collection and creation of datasets was the disinformation related to the pandemic of Covid-19. After the bibliographic research and data collection, the information will be analyzed by the authors, and a web-oriented software will be developed to allow the users to research samples of text and receive an analysis via web interface or through the social networks used by them. The software will use Machine Learning techniques with Deep Learning and will be evaluated to verify its effectiveness and adherence to quality principles.

Keywords: Disinformation Detection; Deep Learning, Software Engineering.

Source: M. P. S. de Camargo, M. C. Lima, P. G. R. Sanches, R. O. Luz, and T. R. Gomes, "Verifato: Aplicação com objetivo de identificar desinformação utilizando deep learning" [Verifato: Application with the aim of identifying misinformation using deep learning], Trabalho de Conclusão de Curso, Instituto de Ciências Exatas e Tecnologia, Universidade Paulista, São José dos Campos, 2022.
Note: Paper available upon request (in Portuguese) at mpsdecamargo@gmail.com

# Authors of the original paper

The authors of the paper are:

Marcos Paulo Santos de Camargo 
LinkedIn: https://www.linkedin.com/in/mpsdecamargo/
Matheus Caldas Lima 
LinkedIn: https://www.linkedin.com/in/matheus-c-lima/
Pedro Gabriel Rodrigues Sanches 
LinkedIn: https://www.linkedin.com/in/pedro-gabriel-r-sanches-517574185/
Rafael Oliveira Luz 
LinkedIn: https://www.linkedin.com/in/rafaoluz/
Thiago Ribeiro Gomes 
LinkedIn: https://www.linkedin.com/in/thiagoribeirogomes/

# Notebooks

The notebook list includes:

Feature: Classify Covid-related data into False or True.
Notebook: [Covid_related_Text_Binary_Classification_using_Transformers_library](https://github.com/mpsdecamargo/ml-data-science-portfolio/blob/main/bert-deep-learning-project/Covid_related_Text_Binary_Classification_using_Transformers_library.ipynb)
Notebook content: Import of the dataset, processing of data, configuration and training of the models for binary classification data, saving models to personal Google Drive.

Feature: Classify Covid-related data into 8 themes of 9 most recurring themes of Covid related data according to UNESCO (2020).
Notebook: [Covid_related_Text_Similar_Text_Assessment_with_Sentence_BERT](https://github.com/mpsdecamargo/ml-data-science-portfolio/blob/main/bert-deep-learning-project/Covid_related_Text_Similar_Text_Assessment_with_Sentence_BERT.ipynb)
Notebook content: Import of the dataset, processing of data, configuration and training of the models for multilabel classification data, saving models to personal Google Drive.

Feature: Provide 5 Covid-related fact-checked claims of the input data, with claim verified, similarity score, date published, link and assessment of claim.
Notebook: [Covid_related_Text_Theme_Multilabel_Classification_using_Transformers_library](https://github.com/mpsdecamargo/ml-data-science-portfolio/blob/main/bert-deep-learning-project/Covid_related_Text_Theme_Multilabel_Classification_using_Transformers_library.ipynb)
Notebook content: Import of the dataset, processing of data, embedding process and semantic similarity assessment.

Notebook: [Load_and_Predict](https://github.com/mpsdecamargo/ml-data-science-portfolio/blob/main/bert-deep-learning-project/Load_and_Predict.ipynb)
Notebook content: Loading of models and evaluation on validation loss, accuracy, precision, recall and F1 Score. Comparison between models.

Notebook: [Model_Evaluation_using_Transformers_library](https://github.com/mpsdecamargo/ml-data-science-portfolio/blob/main/bert-deep-learning-project/Model_Evaluation_using_Transformers_library.ipynb)
Notebook content: Loading of models and prediction of sample corpus. Sample of final function to save output into JSON format to be sent to the front end of the application and to the user.


# Results:

## Results for best Model on Text Binary Classification Task Ordered by Accuracy

| Model                                       | Model Type | Validation Loss | Accuracy | Precision | Recall |   F1   |
|---------------------------------------------|------------|------------------|----------|-----------|--------|--------|
| neuralmind/bert-large-portuguese-cased       | BERPTL     | 0.1959           | **96.90%**   | 95.52%    | **97.39%** | **96.96%** |
| neuralmind/bert-base-portuguese-cased        | BERTPT     | **0.1158**          | 96.05%   | 93.98%    | 98.50% | 96.11% |
| distilbert-base-multilingual-cased           | DISTILBERT  | 0.1749           | 96.05%   | 95.54%    | 96.69% | 96.15% |
| microsoft/mdeberta-v3-base                   | DEBERTA     | 0.1452           | 95.79%   | **96.73%**    | 94.89% | 95.80% |
|xlm-roberta-base                             | XLMR       | 0.1935           | 95.69%   | 95.62%    | 96.99% | 95.79% |
| dlb/electra-base-portuguese-uncased-brwac    | ELECTRA     | 0.2011           | 95.54%   | 95.32%    | 95.89% | 95.60% |
| bert-base-multilingual-cased                 | MBERT      | 0.1937           | 95.49%   | 94.17%    | 97.09% | 95.61% |
| josu/albert-pt-br                            | ALBERT     | 0.2035           | 95.29%   | 93.80%    | 97.09% | 95.42% |
| rdenadai/BR_BERTo                            | ROBERTA    | 0.2244           | 94.78%   | 95.52%    | 94.09% | 94.80% |

Note: Chosen by best validation loss outcome of 5 epochs each. BERTPTL was trained with train batch size of 4 (default is 8) due to memory restrictions and with learning rate of 2e-5 instead of the default 5e-5 for better performance. In the original paper accuracy was the metric chosen for best model training optimization and comparison. In hindsight, the models had a tendency to overfit. That is the reason eval_loss was chosen for model training optimization. However, accuracy is still an important metric, so the table was ordered as such.

## Results for best Model on Text Multilabel Classification Task Ordered by Precision

| Model                                       | Model Type | Validation Loss | Accuracy | Precision | Recall |   F1   |
|---------------------------------------------|------------|------------------|----------|-----------|--------|--------|
| neuralmind/bert-base-portuguese-cased        | BERTPT_ML     | **0.3411**          | 9.83%   | **67.33%**    | 6.47% | 11.42% |
| microsoft/mdeberta-v3-base                   | DEBERTA_ML     | 0.3754           | **18.23%**   | 65.92%    | **10.61%** | **17.10%** |

Note: Chosen by best precision outcome of 5 epochs each. After analysing the problem, precision was defined as the best metric for model evaluation, because the goal is to correctly identify a theme, avoiding false positives. Also, as the dataset is imbalanced, precision is more valuable than accuracy, besides being assessed for each theme separately.

# CONCLUSION

For the Binary Classification task, the best model is BERT Large Portuguese. However, it is the most time and resource consuming model. The BERT Base Portuguese was chosen to follow through with the Multilabel task, along with the DEBERTA model which had the best precision value.

For the Multilabel Classification task, the best overall model was DEBERTA, because the precision score difference with the Bert Base model was not as significant, and the other metrics are considerably better.


Bibliography:

M. P. S. de Camargo, M. C. Lima, P. G. R. Sanches, R. O. Luz, and T. R. Gomes, "Verifato: Aplicação com objetivo de identificar desinformação utilizando deep learning" [Verifato: Application with the aim of identifying misinformation using deep learning], Trabalho de Conclusão de Curso, Instituto de Ciências Exatas e Tecnologia, Universidade Paulista, São José dos Campos, 2022.

J. Posetti and K. Bontcheva, "Disinfodemic: Deciphering COVID-19 Disinformation," Policy brief, 1. UNESCO, 2020. [Online]. Available: https://unesdoc.unesco.org/ark:/48223/pf0000374416
