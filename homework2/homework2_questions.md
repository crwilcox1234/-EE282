# Homework2
## hw by Christina Wilcox

1. Prompt: Ask a question that requires a student to understand navigation and manipulation of directories in a filesystem. Your question should require an answer using at least the following commands/concepts: cd, ../, mkdir, rmdir

Question #1: Write a script that makes a directory within another directory.  The first directory should be called Disneyland and the directory within Disneyland should be called StarWars (Note: you should make both directories from your home directory, do not change directories into the Disneyland directory to make the StarWars directory). After you have made both the Disneyland and the StarWars directories, change directories into the Disneyland directory and remove the StarWars directory. Your answer should include the commands you used to make the directories, enter into the Disneyland directory, and remove the StarWars directory, as well as the outputs from each command. 





2. Prompt: Ask a question that requires a student to understand the difference between accessing a column in a matrix with text indices versus accessing a column in a data frame with text indices. Your question should require an answer comparing the following: mymatrix[,'col1'] vs. mydf[,'col1'] vs. mydf['col1'] vs. mydf$col1 vs. mydf[['col1']].

Question #2: Data frames vs matrices in R. To answer this question use the R built-in data set mtcars. Make a data frame called car_gears and a matrix called car_matrix. Using your new data frame and matrix answer the following questions.  

 * How would you determine how many gears each car has in the data set mtcars using the data frame car_gears? How would you determine this using the data matrix car_matrix?

 * In the data frame car_gears what are 3 ways you can view the values in the gear column?

 * Make a data frame and matrix in R from the information below: 

   - horse_breeds 'Quarter horse', 'Thoroughbred', 'Haflinger'
   - height_cm 163, 173, 150
   - weight_kg 540, 590, 585
   - price_dollars 4000, 90000, 5000

 * Answer the following questions about the data frame you made from the info above:
   
   - Do you use a different command to make a data frame from scratch vs creating a data frame using mtcars?
   - Answer the questions from the first two bullet points using the data frame and matrix above using a column of your choise.




3. Prompt: Ask a question that requires a student to understand how to share access to a directory and a file in that directory on a Unix/Linux filesystem from their home directory with a colleague without exposing the users entire directory. Your question should require an answer using chmod {u,g,o}{+,-}{r,w,x} (not using octal permissions).
Hint 1: in order to view a file, all of its parent directories must be executable
Hint 2: in order to view a file, the file itself must be readable

Question #3: Professor Max would like to share a data file with his students from an undergraduate course he teaches. However, he does not want to share all the files in this directory because he also keeps the exam keys for the class in the same directory. This data file is called past_student_scores.txt and it is in the directory D107L_exam_scores (permissions drwx------), which is located in his home directory. How could he give access to the past_student_scores.txt file (permissions -rwx------) withought allowing students to access the other sensitive files in the D107L_exam_scores directory?

    
