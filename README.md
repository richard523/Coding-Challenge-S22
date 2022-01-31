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
# https://www.kaggle.com/jchen2186/machine-learning-with-iris-dataset/notebook
# http://www.unit-conversion.info/texttools/ascii/ (to normalize from string to numbers)
# https://colab.research.google.com/

## Notes:
Implemented using KNN and used previous notebook's example (for classifying iris species)

In graphs.xlsx I took notes for each of the data. 

I was going to try making simple neural network but ran out of time.


# How to create a mushroom prediction:

Just run my notebook through google colab. Example format for predictions are as follows:
knn.predict([[5.0,	3.0,	8.0,	1.0,	6.0,	1.0,	0.0,	1.0,	5.0,	0.0,	3.0,	2.0,	2.0,	8.0,	8.0,	112.0,	2.0,	1.0,	4.0,	2.0,	3.0,	5.0	]])
where each number is mapped in the chart below (needs 22 data points but experiment with missing ones)

make sure to stay within the normalized values

			
cap_shape	                #1 {98.0, 99.0, 102.0, 107.0, 115.0, 120.0} maps to  ? b f s x but normalized to 0 1 2 3 4 5						b c f k s x						
cap_surface	              #2 {121.0, 115.0, 102.0, 103.0} maps to ? f g s y normalized to 0 1 2 3						f g s y						
cap_color	                #3 {98.0, 99.0, 101.0, 103.0, 110.0, 112.0, 114.0, 117.0, 119.0, 121.0} to --> 0 to 9						b c e g n p r u w y						
bruises	                  #4 true or false --> 1 or 0						f t						
odor	                    #5 {97.0, 99.0, 102.0, 108.0, 109.0, 110.0, 112.0, 115.0, 121.0} --> 0 to 8						alcyfmnps						
gill_attachment	          #6 {97.0, 102.0} --> t or f --> 0 or 1 (f is 1)						t f						
gill_spacing	            #7 {99.0, 119.0} --> 0 or 1						c d w	order matters?					
gill_size     	          #8 {98, 110} --> 0 or 1						b n	order matters?					
gill_color	              #9 {98.0, 101.0, 103.0, 104.0, 107.0, 110.0, 111.0, 112.0, 114.0, 117.0, 119.0, 121.0} --> 0 to 11						beghknopruwy						
stalk_shape	              #10 {116.0, 101.0} --> 0 or 1						e t						
stalk_root	              #11 {98.0, 99.0, 101.0, 114.0, 63.0} --> 0 to 4						b c e r u z	not all letters. only 5 		has missing values?			
stalk_surface_above_ring	#12 {107.0, 121.0, 115.0, 102.0} --> 0 to 3												
stalk_surface_below_ring	#13 {107.0, 121.0, 115.0, 102.0} --> 0 to 3												
stalk_color_above_ring	  #14 {98.0, 99.0, 101.0, 103.0, 110.0, 111.0, 112.0, 119.0, 121.0} --> 0 to 8												
stalk_color_below_ring	  #15 {98.0, 99.0, 101.0, 103.0, 110.0, 111.0, 112.0, 119.0, 121.0} --> 0 to 8												
veil_type	                #17 do we want to delete this useless piece of data? --> 112 only												
veil_color	              #18  {121.0, 111.0, 110.0, 119.0} --> 0 to 3												
ring_number	              #19 {116.0, 110.0, 111.0} order matters? none one two == 110 111 116 --> 0 to 2												
ring_typ	                #20 {101.0, 102.0, 108.0, 110.0, 112.0} --> 0 to 4												
spore_print_color	        #21 {98.0, 104.0, 107.0, 110.0, 111.0, 114.0, 117.0, 119.0, 121.0} to 0 to 8 												
population	              #22  {97.0, 99.0, 110.0, 115.0, 118.0, 121.0} --> 0 to 5												
habitat	                  #23 {100.0, 103.0, 108.0, 109.0, 112.0, 117.0, 119.0} --> 0 to 6											

![image](https://user-images.githubusercontent.com/60868589/151779920-6b5a2489-1d03-4052-9734-1bbdaae25ba7.png)


