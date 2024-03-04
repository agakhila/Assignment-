# Assignment


# Import the dataset

Student_assignment_6 <- read.table("<FileName>.txt", header = TRUE)



# Calculate the mean grade by sex

StudentAverage <- ddply(Student_assignment_6, "Sex", summarise, Grade_Average = mean(Grade))



# Write the output to a file

write.table(StudentAverage, "Student_Average_Grades.txt", sep = ",", row.names = FALSE)

# Filter the dataset for names containing 'i'

i_students <- student_data[grep("i", student_data$Name, ignore.case = TRUE), ]



# Write the filtered names to a CSV file

write.csv(i_students$Name, file = "i_students_names.csv", row.names = FALSE)

# Choose the file location interactively
file_location <- file.choose()

# Write the filtered dataset to a CSV file
write.csv(i_students, file = file_location, row.names = FALSE)

> reticulate::repl_python()
Sex,Grade
Female,87.31579
Male,80.33333

"Name"
"Lauri"
"Sherlyn"
"Mikaela"
"Deloris"
"Shemika"
"Delfina"
"Ernestina"
"Milo"

"Name","Age","Sex","Grade"
"Lauri",21,"Female",90
"Sherlyn",22,"Female",85
"Mikaela",20,"Female",69
"Deloris",21,"Female",67
"Shemika",23,"Female",97
"Delfina",19,"Female",93
"Ernestina",19,"Female",93
"Milo",19,"Male",67
