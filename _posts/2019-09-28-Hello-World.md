# ***To Trust or Not To Trust***
## Is your data trustworthy, or should it be verified and cleaned before you start working on any analysis?

![DataCleaning](https://bigdata-madesimple.com/wp-content/uploads/2018/10/Accuracy.gif "Data Accuracy")<br>
[Source](https://bigdata-madesimple.com/wp-content/uploads/2018/10/Accuracy.gif "Source")


### ***Should I clean my data?***<br>
To try to answer this question lets imagine you are a rising chef recently appointed to a big five star hotel restaurant in Vancouver!
First of all.congratulations! <br>
For a special event tonight, you are given 50 lbs. of potatoes to make your famous potato dish. You are still not so familiarized with the hotel's food quality assurance process, so you are not sure if you should trust the potatoes' quality without inspecting them? What could possibly happen if you don't wash them? What could happen if you use all of the potatoes without filtering any bad ones?<br>
As the good chef you are, you trust.but you also verify. You proceeded to wash all the ingredients and filtered 5% of the potatoes that were already rotten and as a resul: the dinner was a huge success!<br> 

If you would not have had this defensive behavior, you could have potentially ruined the taste of your dish or even made your customers sick!
<br>
As assuring your ingredients' quality is important for the quality of your dish so is assuring your data's quality for assuring your analysis's result.
 
You are probably familiar to the saying: garbage in.garbage out. Which means that it does not matter how good your algorithms are, if your ingredients (data) are not clean then your results will not be.


### ***So what is data cleaning?***

![DataCleaning](https://media.giphy.com/media/3DnDRfZe2ubQc/giphy.gif "Data Cleaning") 
<br>
[Source](https://media.giphy.com/media/3DnDRfZe2ubQc/giphy.gif "Source")

 
A more proper definition for data cleaning, would be, according to Sisense.com : "The process of preparing data for analysis by removing or modifying data that is incorrect, incomplete, irrelevant, duplicated, or improperly formatted" (From <https://www.sisense.com/glossary/data-cleaning/>) <br>
 
 In this brief introduction we will try to ***understand the main issues data could present and in a following post we will discover the main remedies for each of these issues.*** 
So lets learn by doing (or imaging doing), shall we?
 
You have been asked to analyze the results for your cohort's first lab in Communication and Argumentations in order to identify which academic background did better by comparing average scores among each.
 
You are provided with an excel sheet with the following information:

* Student Number
* Academic background
* Test Score
* Cohort

That looks like the following (All data is fictional):<br>
<img src="images/Image_1.png" width=200 align="left">

When you start viewing data you discover certain things that don't  feel right. Lets understand each of the situations you encounter and see if they relate to the issues that should be cleaned up in your data before starting any analysis.

#### **Escenario 1**


<img src="images/Image_2_duplicates.png" width=180 align="left">

In this example we can see ***Duplicates*** , which are data repetitions. In order to identify this type of anomaly, you should identify a unique key in your dataset and totalize counts per unique. Duplicates can be solved by filtering and just select a data point per unique key.
In our example the student number is the unique key.

#### **Escenario 2**
<img src="images/Image_3_standarization.png" width=200 align="left">

<br/><br/><br/><br/><br/><br/><br/><br/><br/><br/>

Here we can find two issues:

1. Missing Data <br>
Refers to missing values found in the dataset. In the picture provided we can identify 7 counts without a label and 14 counts with the "undefined" label. This data should not be excluded for analysis because, because will not add value to the question we are trying to answer.
 
2. Unstandardized data <br>
Refers to different values referring to the same event. For example we can identify that "Eengineering" and "engineering" refer both to the same value. In this case, data should be manipulated to change all unstandarized value into a single unique value.


#### **Escenario 3**
<img src="images/Image_4_cohort.png" width=200 align="left">
<br/><br/><br/><br/><br/>

In this example we can see ***irrelevant information*** to the problem trying to solve. For example information information from cohort 2018 at this time is irrelevant to want we need to answer. If working with huge data sets it can be helpful to filter just the data needed for the question trying to be answered. <br>
Anywaysm if you are in doubt if a piece of information can be helpful or not, it should be filtered and left available for further analysis.

<br>

#### **What could happen rush into conclusions without cleaning?**

Lets imagine you rush in presenting results, without cleaning your data and you just attached the following image, and accidently click "Send" to your boss:
<br/>

<img src="images/Image_5_Rushing_Conclusions.png" width=350 align="left">
<br/><br/><br/><br/><br/><br/><br/><br/><br/><br/>
What is wrong with these numbers?


You immediately get an email from you boss, saying this type of conclusions are unacceptable. Pointing out that:
+ The total number of students does not match with this year's cohort size.
+ He says grades greater than 100% are impossible!


He points out a series of cleaning actions you should do, with the following image:
<img src="images/Image_6_Identifying_Anomalities.png" width=500 align="left">
<br/><br/><br/><br/><br/><br/><br/><br/><br/><br/><br/>


You follow his recomendations and you get the new results:
<br/><br/>
<img src="images/Image_7_Result_Clean.png" width=500 align="left">
<br/><br/><br/><br/><br/><br/><br/><br/><br/><br/><br/><br/><br/><br/><br/><br/><br/><br/><br/><br/><br/><br/><br/><br/><br/><br/><br/><br/><br/>

Did you notice how results can change and also how your credibility can be kept intact with the help of data cleaning!


These are just three examples of issues we can find our data and in the following post we will earn how these can affect our result if not treated correctly.

Stay tunned!


![ObamaOut](https://media1.tenor.com/images/e7bb4a6c076fd8464b55ffec6fb03db4/tenor.gif?itemid=5658368 "Data Cleaning")<br>
[Source](https://media1.tenor.com/images/e7bb4a6c076fd8464b55ffec6fb03db4/tenor.gif?itemid=5658368 "ObamaOut")




The following sites where used as inspiration for the present post blog:

* https://elitedatascience.com/data-cleaning
* https://towardsdatascience.com/the-art-of-cleaning-your-data-b713dbd49726
