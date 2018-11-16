# Homework #2 Answer key

## Question #1: Write a script that makes a directory within another directory.  The first directory should be called Disneyland and the directory within Disneyland should be called StarWars (Note: you should make both directories from your home directory, do not change directories into the Disneyland directory to make the StarWars directory). After you have made both the Disneyland and the StarWars directories, change directories into the Disneyland directory and remove the StarWars directory. Your answer should include the commands you used to make the directories, enter into the Disneyland directory, and remove the StarWars directory.

Answer for Question #1: 

    mkdir -p Disneyland/StarWars
    cd Disneyland
    rmdir StarWars

### Question 1 Comments:
Very well done!

## Question #2: Data frames vs matrices in R. To answer this question use the R built-in data set mtcars. Make a data frame called car_gears and a matrix called car_matrix. Using your new data frame and matrix answer the following questions.
 
**Answer:** car_gears <- as.data.frame(mtcars), car_matrix <- as.matrix(mtcars)

 * How would you determine how many gears each car has in the data set mtcars using the data frame car_gears? How would you determine this using the data matrix car_matrix?

**Answer:** car_gears['gear']
**Answer:** car_matrix[,'gear']

 * In the data frame car_gears what are 3 ways you can view the values in the gear column?

**Answer:** car_gears[,'gear'], car_gears$gear, car_gears[['gear']]

 * Make a data frame and matrix in R from the information below:

   - horse_breeds 'Quarter horse', 'Thoroughbred', 'Haflinger'
   - height_cm 163, 173, 150
   - weight_kg 540, 590, 585
   - price_dollars 4000, 90000, 5000

**Answer:** 
 horse_breeds <- c('Quarter horse', 'Thoroughbred', 'Haflinger')
 
 height_cm <- c(163, 173, 150)
 
 weight_kg <- c(540, 590, 585)
 
 price_dollars <- c(4000, 90000, 5000)

 horse.data <- data.frame(horse_breeds, height_cm, weight_kg, price_dollars)
 horse.matrix <- matrix(horse_breeds, height_cm, weight_kg, price_dollars)

 * Answer the following questions about the data frame you made from the info above:
  
   - Do you use a different command to make a data frame from scratch vs creating a data frame using mtcars?

**Answer:** Yes, when making your own matrix or data frame from scratch you use: data.frame() or matrix(), but when using an existing data set use as.data.frame() or as.matrix()

   - Answer the questions from the first two bullet points using the data frame and matrix above using a column of your choice.

**Answer:** horse.data['height_cm']

**Answer:** horse.matrix[,'height_cm']

**Answer:** horse.data[,'height_cm'], horse.data$height_cm, horse.data[['height_cm']]

### Question 2 Comments:
Well done. You can use [code blocks](https://help.github.com/articles/creating-and-highlighting-code-blocks/) a bit more liberally to make your examples easier to read, copy, and paste. You did this in #1 and #2, so no big deal.

## Question #3: Professor Max would like to share a data file with his students from an undergraduate course he teaches. However, he does not want to share all the files in this directory because he also keeps the exam keys for the class in the same directory. This data file is called past_student_scores.txt and it is in the directory D107L_exam_scores (permissions drwx------), which is located in his home directory. How could he give access to the past_student_scores.txt (permissions -rwx------) file withought allowing students to access the other sensitive files in the D107L_exam_scores directory?

**Answer:** I am going to assume the students in his undergrad class are not placed in a group, so would be considered others. In order to do the permissions properly, the directory needs to executable to other, but deny read access to the direcotry to other. The file itself also has to have read permissions for other.  By denying read access to the directory, the students would not be able to see what else was in the older.  However, this means they have to have the specific filepath for the past_student_scores.txt file beforehand.  To do permissions in this way, Professor Max would need to do the following commands: 

chmod o+x D107L_exam_scores (new permissions drwx-----x)

chmod o+r past_student_scores.txt (new permissions -rwx---r--)

### Question 3 Comments:
In this example, you are right that they would need read access to the folder, but commands to not appear to be correct. The directory itself would need to be readable by all users, or else the students will not have access to any contents inside the directory. o+x only gives execute access to the users for that directory. so you would need to do:

```
chmod +r D107L_exam_scores
cd D107L_exam_scores
chmod o-r *
chmod +r past_student_scores.txt
```

I hope this helps in the future when you need to share files with collaborators. You definetly understood what needed to be done, but unfortunatley the commands would have not been able to acheive your objective.

 
 
