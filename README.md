# Improving Quality of Software Issue Report Descriptions

We labeled 1,041 software issue reports at Softtech Inc ([Softtech Inc.](https://softtech.com.tr/)) as having observed behaviour (OB), expected behaviour (EB) and steps to reproduce (S2R), and the related sentences that indicate them. The reports are written in Turkish, an agglutinative language, meaning that whole sentences can be formed by adding suffixes to roots, especially verbs. Thus, we utilize morphological analysis to extract the features. Furthermore, we extract the patterns that indicate OB, EB and S2R in these sentences. We use the Zemberek tool [1] for morhological analysis. Due to security reasons, we are not able to publish the issue reports used in the studies. However, the scripts, which we used in the experiments can be found here.

## Getting Started

The repository includes the following **Jupyter Notebook** scripts coded with **Python 3.9**: 

* single_project_qual_eval.ipynb
* cross_project_qual_eval.ipynb

Single project evaluation uses all the reports in a single project to predict on the issue reports on the same project, while cross project evaluation uses 1 out of n projects in the dataset for testing and the remaining for training. 

Before running any script, the issue reports should have been downloaded and saved as a csv file. If you have a stop-word list, assign the list to the variable "stop_word_list". 

[1] Akın A A, Akın M D (2007) Zemberek, an open source nlp framework for turkic languages. Structure, 10(2007), 1-5.
