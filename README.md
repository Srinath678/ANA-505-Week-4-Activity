# ANA-505-Week-4-Activity
ANA 505 Week 4 Activity Dplyr

#Week 4: dplyr package



data_color <- data.frame(HairEyeColor)



head(data_color,10)



install.packages("dplyr")
library(dplyr)



select(data_color, Hair, Sex)



data_new <- select(data_color, Hair = Hair, Sex = Sex)



data_new <- select(data_new, -Sex)



rename(data_color, Gender = Sex)



data_color[,"Gender"] <- NA
data_color



data_maleonly <- filter(data_color, Sex == "Male")
data_maleonly <- select(data_maleonly, Sex)
data_maleonly



group_by(data_color, Sex)

#After you run it, write the total here:592

total=mutate(data_color, total=cumsum(Freq))
total



data_femaleonly <- filter(data_color, Sex == "Female")
data_femaleonly <- select(data_femaleonly, Sex)
data_femaleonly



bind_rows(data_maleonly,data_femaleonly)


#Here we are using 'group_by' function to arrange a dataframe with 'Eye' Column

group_data_by_Eye<- group_by(data_color, Eye)
group_data_by_Eye
