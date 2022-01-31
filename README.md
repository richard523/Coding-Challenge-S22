# ACM Research Coding Challenge (Spring 2022)

## [](https://github.com/ACM-Research/-DRAFT-Coding-Challenge-S22#no-collaboration-policy)No Collaboration Policy

**You may not collaborate with anyone on this challenge.**  You  _are_  allowed to use Internet documentation. If you  _do_  use existing code (either from Github, Stack Overflow, or other sources),  **please cite your sources in the README**.

## [](https://github.com/ACM-Research/-DRAFT-Coding-Challenge-S22#submission-procedure)Submission Procedure

Please follow the below instructions on how to submit your answers.

1.  Create a  **public**  fork of this repo and name it  `ACM-Research-Coding-Challenge-S22`. To fork this repo, click the button on the top right and click the "Fork" button.

2.  Clone the fork of the repo to your computer using  `git clone [the URL of your clone]`. You may need to install Git for this (Google it).

3.  Complete the Challenge based on the instructions below.

4.  Submit your solution by filling out this [form](https://acmutd.typeform.com/to/uTpjeA8G).

## Assessment Criteria 

Submissions will be evaluated holistically and based on a combination of effort, validity of approach, analysis, adherence to the prompt, use of outside resources (encouraged), promptness of your submission, and other factors. Your approach and explanation (detailed below) is the most weighted criteria, and partial solutions are accepted. 

## [](https://github.com/ACM-Research/-DRAFT-Coding-Challenge-S22#question-one)Question One

[Binary classification](https://en.wikipedia.org/wiki/Binary_classification) is a type of classification task that labels elements of a set (i.e. dataset) into two different groups. An example of this type of classification would be identifying if people had a specific disease or not based on certain health characteristics. The dataset found in `mushrooms.csv` holds data (22 different characteristics, specifically) about different types of mushrooms, including a mushroom's cap shape, cap surface texture, cap color, bruising, odor, and more. Remember to split the data into test and training sets (you can choose your own percent split). Information about the meaning of the letters under each column can be found within the file `attributelegend.txt`.

**With the file `mushrooms.csv`, use an algorithm of your choice to classify whether a mushroom is poisonous or edible.**

**You may use any programming language you feel most comfortable. We recommend Python because it is the easiest to implement. You're allowed to use any library or API you want to implement this, just document which ones you used in this README file.** Try to complete this as soon as possible.

Regardless if you can or cannot answer the question, provide a short explanation of how you got your solution or how you think it can be solved in your README.md file. However, we highly recommend giving the challenge a try, you just might learn something new!


# Resources used:
 https://www.kaggle.com/jchen2186/machine-learning-with-iris-dataset/notebook
 http://www.unit-conversion.info/texttools/ascii/ (to normalize from string to numbers)
 https://colab.research.google.com/
 https://colab.research.google.com/drive/11OilxJRR-myxPzfXQwNXDnSGwtnbGt6J?usp=sharing													
													
													
https://machinelearningmastery.com/implement-backpropagation-algorithm-scratch-python/													
													
https://raw.githubusercontent.com/jbrownlee/Datasets/master/wheat-seeds.csv													
													
https://towardsdatascience.com/first-neural-network-for-beginners-explained-with-code-4cfd37e06eaf													
													
https://towardsdatascience.com/building-a-shallow-neural-network-a4e2728441e0													
													
https://github.com/MJeremy2017/deep-learning/blob/main/shallow-neural-network/one-hidden-layer-nn.ipynb													
													
https://towardsdatascience.com/logistic-regression-step-by-step-implementation-f032a89936ca													
													
https://scikit-learn.org/stable/modules/preprocessing.html													
													
https://www.kaggle.com/jchen2186/machine-learning-with-iris-dataset/notebook													
													
https://pandas.pydata.org/docs/reference/api/pandas.DataFrame.drop.html													
													
https://towardsdatascience.com/machine-learning-basics-with-the-k-nearest-neighbors-algorithm-6a6e71d01761#:~:text=KNN%20works%20by%20finding%20the,in%20the%20case%20of%20regression).													
![image](https://user-images.githubusercontent.com/60868589/151781487-3776e1ed-5506-41c8-b1a2-24dc7e552be3.png)


# Notes:
Renamed some of the columns (example: gill-attached to gill_attached)

- I added a new component called mushroom_id that indexes all mushrooms. 

- Uploaded my version of the mushrooms.csv file.

- Implemented using KNN and used previous notebook's example (for classifying iris species)

- In graphs.xlsx I took notes for each of the data. 

- Sunken cost fallacy made me normalize all the categorical data manually. By the time I discovered sklearn's normalization tools I was already 80% finished with preprocessing the data. (I might have done preprocessing part wrong.)

- I was going to try making simple neural network but ran out of time.


# Update:
- Created version two using sklearn's tools as explained in this link: https://scikit-learn.org/stable/modules/preprocessing.html

- I no longer get the warning that the graph "fails to converge" since I believe the data is now correctly preprocessed.

- Used less iterations in order to avoid overfitting


# Graph results:

(click to view)

![image](https://user-images.githubusercontent.com/60868589/151863384-c9191350-de96-496b-800e-a6b217162493.png)

![image](https://user-images.githubusercontent.com/60868589/151863397-e69768fe-233a-42fe-95a8-a5a5508ddda2.png)

# error/warning I received: 
![image](https://user-images.githubusercontent.com/60868589/151863441-c7a5dc14-d4f1-4eaf-a151-1c8034f3fd5e.png)

k vs accuracy graph is not converging on any iterations so far

![image](https://user-images.githubusercontent.com/60868589/151863534-e4f30fc9-54b9-4c11-a690-24688abb424a.png)
tried using more iterations

# After preprocessing using sklearn's chapter 6.3:
![image](https://user-images.githubusercontent.com/60868589/151863620-fcf1882c-ec15-4391-9bca-f784f4df27a1.png)




# How to create a mushroom prediction:

Just run my notebook through google colab. Example format for predictions are as follows:


knn.predict([[5.0,	3.0,	8.0,	1.0,	6.0,	1.0,	0.0,	1.0,	5.0,	0.0,	3.0,	2.0,	2.0,	8.0,	8.0,	112.0,	2.0,	1.0,	4.0,	2.0,	3.0,	5.0	]])


where each number is mapped in the chart below (needs 22 data points but may experiment with missing ones or putting values outside of boundaries?)


													

![image](https://user-images.githubusercontent.com/60868589/151779920-6b5a2489-1d03-4052-9734-1bbdaae25ba7.png)


