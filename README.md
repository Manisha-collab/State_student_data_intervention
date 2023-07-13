# State_student_data_intervention

Data Description
Imagine that a state (fictional) recently piloted an intervention that provides
additional reading material to schools in order to improve student learning
outcomes. The intervention was piloted in roughly half of the schools.
A few months later, the state conducted an assessment of all the students on three
sections: arithmetic, word reading, sentence reading and spelling. The state also
collected data on teachers on how many years of experience they have on
teaching.
The state has now shared the data with you and asked you to clean and analyze
the data. There are two tables being shared with you:
1. student_test_data.csv
● pupilid : Pupil ID
● schoolid : School ID
● district : District of school
● intervention : Whether school was given additional reading material (dummy
variable; 1 if true and 0 if false)
● girl : Pupil is female (dummy variable, 1 if female and 0 if male)
● arithmetic: score on arithmetic section of the test (maximum 24)
● word: score on word reading section of the test (maximum 24)
● sentence: score on sentence reading section of the test (maximum 40)
● spelling: score on spelling section of the test (maximum 10)
2. teacher_data.csv
● teacherid : Teacher ID within the school
● schoolid : School ID
● yrstaught: Years of teaching experience
2
#####################Exercises######################################
● Load the student test data
● Recode the arithmetic score variables as integers rather than as strings.
(“NONE” is 0.)
● The Word Reading and/or Sentence Reading scores are missing for some
pupils. Missing values have been coded as -99. Drop them from the record
● Generate a variable for the total_score (sum of reading, spelling, sentence
and arithmetic scores).
● Create another variable for letter_grades based on the total_score. Pupils
should be assigned letter grades as follows: A: if total_score is between
80–98; B: if 60–79; C: if 40–59; D: if 20–39; F: if 0–19.
● Save this updated student test data as “modified_student_test_data.csv”
#########################################################
● Load the teacher data
● If any of the values for experience are missing, the drop those records
● Compute the average years of experience of teachers by school id. Name this
variable “avg_yrstaught”
● If needed reshape the data so that observations are uniquely identified by
school
● Your data should look something like
schoolid avg_yrstaught
● Save this data as “school_avg_yrstaught.csv”
#########################################################
● Merge the “modified_student_test_data” and “school_avg_yrstaught” by
schoolid
● Save the merged data as “student_school_merged.csv”

##################################################################
Comparison Across District
Using the data visualization libraries in your preferred programming language,
create a bar chart that compares average of total score for all the districts
Comparison Across Girls and Boys
Using the data visualization libraries in your preferred programming language,
create a bar chart that compares average score of girls and boys on the four
sections of the test: arithmetic, word, sentence and spelling
Based on the two graphs, what are your observations? What can you infer
and what can you not infer from the data? (No more than 100 words)
#####################################################################
a. Regress (with OLS) the total score on the intervention dummy. Include zone
fixed effects in your specification.
Interpret the results. What is the effect of the intervention on pupil test scores?
Explain the meaning both of the point estimate and of the statistical significance.

b. Rerun the regression above and this time control for the gender of the pupil
and for the average years of experience of teachers at the pupil’s school.

