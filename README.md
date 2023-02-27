# QSS20FinalProject

This is the beginning of the QSS 20 Final Project Repository for **Akshay Kelshiker, Edgar Ozuzun, Jeremy Rodriguez, and Shawn Yoon.** The project hopes to investigate which questions in the pre-assessment indicate a lower score in the final assessment. We want to determine if performance on certain questions has a strong influence on how high or low an individual would score on the total assessment.

To determine this, we plan on running an OLS regression of both bivariate and multivariate association within the given variables within the pre-assessment CSV file titled "Med student pre assessment 2.8.23." These data were collected by the Social Impact Practicum, given to medical students from various different schools undergoing a six-hour training session. The data sample size was 99 individuals, but not all responses are complete as students were given the option to opt out and forego the rest of the assessment. The questions refer to the individuals' ability to give definitions of medical terms relating to disabilities, previous experience and comfort with the material covered in training, and agreement with certain statements. The students' responses were then used to calculate a certain score. 

Building three main models, we first want to test only bivariate association between answering specific questions correct, our independent variable, and the final score, the ultimate dependent variable. In the second model, we want to test for possible confounding variables that influence the final score along with the specific questions, including gender, race, experience, and duration time of the test. In the last model, we plan to take the strongest confounding variable and test it alongside the independent variable of questions. By doing so it allows us to test whether the correctness of certain questions is a statistically significant means of determining final scores, and what variables may be doing a better or worse job at predicting final scores. 


**Project Milestones/Updates:**

[Milestone 1 Memo](https://www.overleaf.com/project/63e91fdcd0b1390c7f3f912b): Brainstorming a Research Question and Analyzing How to Learn From Past Projects
Milestone 2 Issue

**Project .ipynb Scripts:**

* [QSS20_Project.ipynb](https://colab.research.google.com/drive/1OLy87ASGkwFgVeCIRoFAAfAPg2d2YWnk?usp=sharing)

    * **Input:** Dartmouth Medical Training Data from the START Initiative(.csv Files)
    * **Functionality:**
    * **Output**
