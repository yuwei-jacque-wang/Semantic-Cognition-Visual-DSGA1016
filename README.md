# Semantic-Cognition-Visual-DSGA1016
This is a project for semantic cognition with neural network with incorporation of visual similarity. Submitted for DS-GA 1016 Computational Cognitive Modeling at New York University.

```
Semantics Cognition Neural Network Model with Existing Knowledge from Visual Similarity
Yuwei Wang, Hengjiali Xu, Yang Gao, Siyu Shen
```
In addition to collaborators, we would like to sincerely thank our professor [Brendan Lake](https://cims.nyu.edu/~brenden/) and [Todd Gureckis](http://gureckislab.org) for valuable advice and guidance.

The complete project report can be found [here](https://github.com/yuwei-jacque-wang/Semantic-Cognition-Visual-DSGA1016/blob/main/Project%20Report.pdf)

### Requirement
- Python 3
- PyTorch
- We highly recommend running the scripts on Google Colab. The current scripts include pipeline for connecting Colab.

### Data
The data set used for this project is Chinese Conceptual Semantic Feature Dataset (CCFD) [paper link](https://pubmed.ncbi.nlm.nih.gov/33532892/). We saved a copy of full data set in data folder. For our experiments we used the following processed data sets:
- [filtered.csv](https://github.com/yuwei-jacque-wang/Semantic-Cognition-Visual-DSGA1016/blob/main/data/filtered.csv): contains items of all categories filtered by certain frequency, used for original model training
- [animal_only.csv](https://github.com/yuwei-jacque-wang/Semantic-Cognition-Visual-DSGA1016/blob/main/data/animal_only.csv): contains only animals, used for extended model with image similarity experiment

Data needs to be processed for entering model. For sample input of a prototype data set, check [here](https://github.com/yuwei-jacque-wang/Semantic-Cognition-Visual-DSGA1016/tree/main/data/sample%20input)

### Coding Scripts
- [data cleaning](https://github.com/yuwei-jacque-wang/Semantic-Cognition-Visual-DSGA1016/blob/main/code/data_cleaning.ipynb): This is to tranform the original tabular data format into one-hot encoding vectors. Outputs are in txt files of concepts (items), relations and attributes, respectively, as well as complete data set in combination of the three.
- [original NN](https://github.com/yuwei-jacque-wang/Semantic-Cognition-Visual-DSGA1016/blob/main/code/run_neural_net.ipynb): Implementation of the original neural network model, including input -> representation layer, relation layer, one hidden layer and output layer of attributes.
- [extended NN](https://github.com/yuwei-jacque-wang/Semantic-Cognition-Visual-DSGA1016/blob/main/code/run_neural_net%20extension.ipynb): Implementation of extended nerual network model by incorporating visual similarity layer. The construction of categorical visual similarities is also explained in a seperate [script](https://github.com/yuwei-jacque-wang/Semantic-Cognition-Visual-DSGA1016/blob/main/code/Image_vector.ipynb) for detailed reference.
- [performance evaluation](https://github.com/yuwei-jacque-wang/Semantic-Cognition-Visual-DSGA1016/blob/main/code/draw_graph.ipynb): Convert the learnt representation layer into 2-D vectors by PCA and plot as graph for performance visualization. 

### Reference
Parts of codes of neural network implementations are from homework of DS-GA 1016 Spring 2021. For more information of the course, check class repository [here](https://brendenlake.github.io/CCM-site/)
