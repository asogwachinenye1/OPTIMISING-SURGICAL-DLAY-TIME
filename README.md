### OPTIMISING-SURGICAL-DLAY-TIME

# Health care daily log analysis

# introduction!
The cedercrest hospital is experiencing a lot of surgical delay in carrying out surgical activities.so they want to optimize the surgical delay time in their hospital.

#Success Achievement!
1.Delay time
2.Average delay time
3.Min and max delay time
4.common delay reason

# TOOL USED FOR EXPLORATORY DATA ANALYSIS,VISSUALIZATION AND REPORT
*POWER BI
# Executive summary
1.3 Missing surgeons in 3 procedures
2.4 common reasons out of 140 reasons
3.94 scrub nurse in 49 procedures
4.112 anesthetics in 70 procedures
5.5 Procedure not scheduled out of 288 procedures from 432 patients
6.Max delay time is 864 in minutes
7.Min delay time is 0 in minutes
8.Average delay time is 67.10 in minutes
9.Total delay time is 28,988 in minutes

# EXPLORATORY DATA ANALYSIS(EDA)
## DATA CLAEANING
For the delay_time analysis,we are expected to use scheduled time and time in column to know the exact time a surgery was delayed.

# column supervsion

so as i proceede with the analysis ,i noticed that the schedule column was having three categories of information like :
# time, 
# nil and 
# not scheduled
for a proper delay time calcuation to be done i have replace the nil and not scheduled to null to identify that those sections are empty.

![image](https://github.com/user-attachments/assets/33467574-4709-4776-8ab5-5541761e43a2)

![image](https://github.com/user-attachments/assets/0fd31b56-3a88-4a31-87db-825d8d1d5dca)



# Time column format
on the columns that contain time like scheduled_time and time_in,i noticed there a time format challange so i have to cerrect them by identifying the time format error and corrected them.

# TIME FORMAT ERROR CORRECTION PICS

![image](https://github.com/user-attachments/assets/131d409b-5582-435f-8aa2-3a4fae93f23d)

![image](https://github.com/user-attachments/assets/48ac122a-4727-4424-9a98-b2724690c40e)

![image](https://github.com/user-attachments/assets/37fb7b8f-e1bb-4e55-911a-e74b6fd73fd8)

![image](https://github.com/user-attachments/assets/5232d7c4-0da2-45ce-8918-919f27bfa562)

![image](https://github.com/user-attachments/assets/69607075-aa48-4c54-9ad2-129996516d91)

![image](https://github.com/user-attachments/assets/14f80b92-24a0-4725-872c-6c1aef0640da)

# CALCULATION OF DELAY TIME IN SURGERY
Because i usd power query for the cleaning process,it wa a bit hard to calculate the delayed time beacuse i was having an empty or blank row in the dataset,
so i have to deloy the knoweledge of custom coulmn and DAX writing to enable me achieve the result i want to achieve.

# DELAY_TIME_CALCULATION
TIME_IN_SCHEDULED TIME

![image](https://github.com/user-attachments/assets/24ce921c-578f-4868-9d05-7247f6ed0fc8)

In the above picture,what i did was to return null in the new column(calculated column called delaye_time) if i have null in the schduled time to aviod having error in the new column.

# DELAYTIME COLUMN EXPLANATION AND TRANSFORMATION
# EXPLANATION
the values contining negative means that there was no delay, the surgery started before the scheduled time while the positive values means that there was a delay afer the scheduled time.

![image](https://github.com/user-attachments/assets/4ec14e33-8336-48ec-8301-7c2bd3039eca)


# TRANSFORMATION
I have to extract out th minutes and hours from the delaytine column so i can know the total minutes that a surery was delayed 
and also the average minuted a surgery was delayed to enable me know the most delayed factor based on delay time.

![image](https://github.com/user-attachments/assets/c7111ec5-9eb7-4d4c-b6c5-cf6984b29546)
From the above picutre,i was having error due to the negative symbol attached to the values which doesn't correspond to the whole number format datatype format.




