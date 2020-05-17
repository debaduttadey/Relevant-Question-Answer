# Finding top 5 relevant question and answer based on User Input
Verdict top 5 relevant questions and answers based on user input

## Business Objective
In any website or in ecommerce business there are very few FAQ or limited user review. All the questions cannot be shown in website as website will look clumsy. Due to limited exposure of the questions, there is a possibility that user might not find question and the answer He/ She is searching for or the question is not present or never have been asked.
Considering different scenarios, we are proposing a model which will take user question and will bring out relevant top five question and answer from Question Bank.  
Our model ensures that:
- User will get relevant answer for the question he/ she is searching for 
- All the process is happening at server side and only top 5 result is achieved, website will not be clumsy.

## Problem statment
An e-commerce company wants to build an algorithm to retrieve top 5 Question and answers based on the user given Keyword.

## Data
Data was provided in NDJson format. Data had some issues when directly inserted into R. Hence data was converted into csv in python. All other steps has been performed in R.

## Project Architecture

![picture alt](Images/ProjectArchitecture.jpeg)

###	Input Layer
User Question and Question bank both are considered as input. 
-	User question/Keywords is the text or question that user will provide as an input. 
-	Question bank means the existing question and answer set that is already present. Later User question will be compared with this question bank to find relevant Question and answer.

###	 Preprocessing 
Before considering to take text as input, text needs to be cleaned. Process of cleaning text includes:
-	Removal of Stop words (common words occur in a sentence)
-	Elimination of URLs (with https or ftp [absolute URLs] and broken URLs (without https or ftp]).
-	Exclusion of emails.
-	Deletion unwanted words
-	Word spell check and correction
-	Word stemming

###	Model
Model is a function “QuestionSearch” which computes cosine similarity between user Questions/Keywords and each Question bank to find the similar questions. 

###	Final Output
Final Output is the relevant question and answer shown based on the user input/keywords. Top five results will be shown with decreasing order of cosine similarity. 



