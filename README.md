# QSS20_23WFinal_Project

This is the beginning of the QSS 20 Final Project Repository for **Akshay Kelshiker, Edgar Ozuzun, Jeremy Rodriguez, and Shawn Yoon.** 
The project hopes to investigate what factors tend to indicate a lower score on the pre-assessment exam given to Medical Students. In particular, the project seeks to analyze the statisitical significance of certain variables (race, gender), as well as the effect of answering certain pre-assessment questions correctly, on the final score for the pre-assessment. The [data](https://github.com/jrodriguez25/QSS20FinalProject/blob/main/training%20data/Med%20student%20pre%20assessment%202.8.23.csv) were provided by the Dartmouth Social Impact Practicum in coordination with the [National Center for START Services](https://centerforstartservices.org/) at the Institute on Disability at University of New Hampshire. The data linked above is a .csv file containing the questions asked in the pre-assessment and the answers of 100 medical students; however, not all responses are complete as students were given the option to opt oout and forego the rest of the assignment. The questions refer to the students' ability to give definitions of medical terms relating to disabilities, previous experience with patients with disabilities, and general outlook on medicine. 

To determine this, we plan on running an OLS regression of both bivariate and multivariate association within the given variables within the pre-assessment file. Building three main models, we first want to test only bivariate association between answering specific questions correct, our independent variable, and the final score, the ultimate dependent variable. In the second model, we want to test for possible confounding variables that influence the final score along with the specific questions, including gender, race, experience, and duration time of the test. In the last model, we plan to take the strongest confounding variable and test it alongside the independent variable of questions. By doing so it allows us to test whether the correctness of certain questions is a statistically significant means of determining final scores, and what variables may be doing a better or worse job at predicting final scores. 


**Project Milestones/Updates:**

[Milestone 1 Memo](https://www.overleaf.com/project/63e91fdcd0b1390c7f3f912b): Brainstorming a Research Question and Analyzing How to Learn From Past Projects

[Milestone 2 Issue](https://github.com/jrodriguez25/QSS20FinalProject/issues/1): Loaded and Cleaned the Data; Performed some Preliminary Analysis

[Status Update Presentation](https://github.com/jrodriguez25/QSS20FinalProject/blob/main/output/03_in_class_presentation.pdf): Brief presentation highlighting research goals and updates as of 03-06-2023. Presented to classroom and procured constructive feedback on areas of improvement

**Project .ipynb Scripts:**

* [00_data_cleaning_analysis.ipynb](https://colab.research.google.com/drive/1OLy87ASGkwFgVeCIRoFAAfAPg2d2YWnk?usp=sharing)

    * **Input:** [Dartmouth Medical Training Pre-examination Data](https://github.com/jrodriguez25/QSS20FinalProject/blob/main/training%20data/Med%20student%20pre%20assessment%202.8.23.csv) from the START Initiative.
    * **Functionality:** 
      * Loads dataset, cleaning and preprocessing by dropping irrelevant rows. 
      * Creates a table of the percentage of certain questions being answered correctly by means of preliminary data analysis. 
    * **Output:** 
      * [Cleaned Data](https://github.com/jrodriguez25/QSS20FinalProject/blob/main/output/00_precleaned_df), the cleaned dataframe
      * [Table of Selected Questions and Percentage Correct](https://github.com/jrodriguez25/QSS20FinalProject/blob/main/output/00_perc_questions_correct.png), the table of percentage of correct answers. 

* [01_regrading_and_score_production.ipynb](https://github.com/jrodriguez25/QSS20FinalProject/blob/main/code/01_regrading_and_score_production.ipynb)

    * **Input:** Precleaned data from the 00_script
    * **Functionality:**
      * Creates a dictionary that contains the Question as key (for example, question 6 is Q6) and the value(s) is/are the correct answer(s). Q6 has one correct answer, so the 'answer' value is of length one, whereas Q34 has an 'answer' value of length 3.
      * Utilizes a function, "regrading," that creates a dataframe of the point values for each student for each question by comparing the text string from the response to the dictionary of correct answers. An additional benefit is that this awards partial credit for partially correct answers, because the [Answer Key](https://github.com/jrodriguez25/QSS20FinalProject/blob/main/training%20data/Answer%20key.docx) did not specify how 'select all that apply' questions were graded. 
   * **Output:** 
      * [scores_df](https://github.com/jrodriguez25/QSS20FinalProject/blob/main/output/01_scores_df.csv), a table in which the columns specify the questions and the values represent the score. The rows correspond to the same patient as in the original data table. 
     
* [02_OLS_Regression_Visualization](https://github.com/jrodriguez25/QSS20FinalProject/blob/main/code/02_OLS_Regression_Visualization.ipynb)
    * **Input:**
      * Uses information from scores_df, from the code above.
    * **Functionality:**
      * The code runs the full regression after the other scripts provided the code to input the graded questions. It creates the dummy variables and uses them to run the OLS regression, and it visualizes three of the variables in a scatterplot.
    * **Output:** 
      * [OLS Regression of Q39](https://github.com/jrodriguez25/QSS20FinalProject/blob/main/output/02_Figure_1.png), OLS regression on Question 39 of the pre-assessment.
      * [OLS Regression of Q34](https://github.com/jrodriguez25/QSS20FinalProject/blob/main/output/02_Figure_2.png), OLS regression on Question 34 of the pre-assessment.
      * [OLS Regression of 'Previous Training' Variable on Score](https://github.com/jrodriguez25/QSS20FinalProject/blob/main/output/02_Figure_3.png), OLS regression on the Previous Training Variable on Score
      * [OLS Regression Table](https://github.com/jrodriguez25/QSS20FinalProject/blob/main/output/02_OLSRegressionTable.png), table of beta values for the three models. 
   
