# QSS20FinalProject

This is the beginning of the QSS 20 Final Project Repository for **Akshay Kelshiker, Edgar Ozuzun, Jeremy Rodriguez, and Shawn Yoon.** 
The project hopes to investigate what factors tend to indicate a lower score on the pre-assessment exam given to Medical Students. In particular, the project seeks to analyze the statisitical significance of certain variables (race, gender), as well as the effect of answering certain pre-assessment questions correctly, on the final score for the pre-assessment. The [data](https://github.com/jrodriguez25/QSS20FinalProject/blob/main/training%20data/training_data/Med%20student%20pre%20assessment%202.8.23.csv) were provided by the Dartmouth Social Impact Practicum in coordination with the [National Center for START Services](https://centerforstartservices.org/) at the Institute on Disability at University of New Hampshire. The data linked above is a .csv file containing the questions asked in the pre-assessment and the answers of 100 medical students; however, not all responses are complete as students were given the option to opt oout and forego the rest of the assignment. The questions refer to the students' ability to give definitions of medical terms relating to disabilities, previous experience with patients with disabilities, and general outlook on medicine. 

To determine this, we plan on running an OLS regression of both bivariate and multivariate association within the given variables within the pre-assessment file. Building three main models, we first want to test only bivariate association between answering specific questions correct, our independent variable, and the final score, the ultimate dependent variable. In the second model, we want to test for possible confounding variables that influence the final score along with the specific questions, including gender, race, experience, and duration time of the test. In the last model, we plan to take the strongest confounding variable and test it alongside the independent variable of questions. By doing so it allows us to test whether the correctness of certain questions is a statistically significant means of determining final scores, and what variables may be doing a better or worse job at predicting final scores. 


**Project Milestones/Updates:**

[Milestone 1 Memo](https://www.overleaf.com/project/63e91fdcd0b1390c7f3f912b): Brainstorming a Research Question and Analyzing How to Learn From Past Projects

[Milestone 2 Issue](https://github.com/jrodriguez25/QSS20FinalProject/issues/1): Loaded and Cleaned the Data; Performed some Preliminary Analysis

**Project .ipynb Scripts:**

* [00_data_cleaning_analysis.ipynb](https://colab.research.google.com/drive/1OLy87ASGkwFgVeCIRoFAAfAPg2d2YWnk?usp=sharing)

    * **Input:** Dartmouth Medical Training Data from the START Initiative(.csv Files)
    * **Functionality:** Loads dataset, cleaning and preprocessing by dropping irrelevant rows
    * **Output** Creates a datatable that contains the percentage correct scores by each multiple choice question
