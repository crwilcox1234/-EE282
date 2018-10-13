# Homework #2 Answer key

## Question #1: Question #1: Write a script that makes a directory within another directory.  The first directory should be called Disneyland and the directory within Disneyland should be called StarWars (Note: you should make both directories from your home directory, do not change directories into the Disneyland directory to make the StarWars directory). After you have made both the Disneyland and the StarWars directories, change directories into the Disneyland directory and remove the StarWars directory. Your answer should include the commands you used to make the directories, enter into the Disneyland directory, and remove the StarWars directory.

Answer for Question #1: 

    mkdir -p Disneyland/StarWars
    cd Disneyland
    rmdir StarWars

## Question #2: Data frames vs matrices in R. To answer this question use the R built-in data set mtcars. Make a data frame called car_gears and a matrix called car_matrix. Using your new data frame and matrix answer the following questions.
 
**Answer:** car_gears <- as.data.frame(mtcars), car_matrix <- as.matrix(mtcars)

 * How would you determine how many gears each car has in the data set mtcars using the data frame car_gears? How would you determine this using the data matrix car_matrix?

**Answer:** car_gears['gear']
**Answer:** car_matrix[,'gear']

 * In the data frame car_gears what are 3 ways you can view the values in the gear column?

**Answer:** car_gears[,'gear'], car_gears$gear, car_gears[['gear']]

 * Make a data frame and matrix in R from the information below:

 ** horse_breeds 'Quarter horse', 'Thoroughbred', 'Haflinger'
 ** height_cm 163, 173, 150
 ** weight_kg 540, 590, 585
 ** price_dollars 4000, 90000, 5000

**Answer:** 
 horse_breeds <- c('Quarter horse', 'Thoroughbred', 'Haflinger')
 height_cm <- c(163, 173, 150)
 weight_kg <- c(540, 590, 585)
 price_dollars <- c(4000, 90000, 5000)

 horse.data <- data.frame(horse_breeds, height_cm, weight_kg, price_dollars)
 horse.matrix <- matrix(horse_breeds, height_cm, weight_kg, price_dollars)

 * Answer the following questions about the data frame you made from the info above:
 ** Do you use a different command to make a data frame from scratch vs creating a data frame using mtcars?

**Answer:** Yes, when making your own matrix or data frame from scratch you use: data.frame() or matrix(), but when using an existing data set use as.data.frame() or as.matrix()

 ** Answer the questions from the first two bullet points using the data frame and matrix above using a column of your choice.

**Answer:** horse.data['height_cm']
**Answer:** horse.matrix[,'height_cm']

**Answer:** horse.data[,'height_cm'], horse.data$height_cm, horse.data[['height_cm']]



