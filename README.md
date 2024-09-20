# Pushing  Oracle table from On-Prem to  Snowflake using private stage (Using Python and SnowSQL) without any cloud storage

![image](https://github.com/user-attachments/assets/3a4ab2c5-27be-4234-ae0d-c9bc787d9b10)

This poc is example to copy oracle table data from onprem to SnowFlake DB using Internal stage (without azure blob)

Initially I created Oracle database in my personal machine

![image](https://github.com/user-attachments/assets/3331e393-e32a-425d-bdfe-bd2c63bd8a33)


I loaded some data in jobs table. We will load this data to SnowFlake database using private stage

![image](https://github.com/user-attachments/assets/c1e57912-a7bd-4fb0-a411-71da87168048)

created below Python file to store records from Jobs table in to a csv file

![image](https://github.com/user-attachments/assets/7cd51643-ed45-43d3-bac6-ae3957a79db3)

![image](https://github.com/user-attachments/assets/8fa4cd48-10b4-4869-8bc8-02688b8af318)

sample file created in the same folder called jobs.csv

![image](https://github.com/user-attachments/assets/af8577b6-6548-429a-8801-402f20c44078)


![image](https://github.com/user-attachments/assets/9b29df17-b141-4798-bf4d-778a60f68576)


Now we need to create internal stage in SnowFlake . I am using SnowSQL in VSCode 

![image](https://github.com/user-attachments/assets/60a52e2f-c9ec-4e87-a552-f26c6fd2c892)

Stage is created and csv file is pushed to SnowFlake internal stage in zip format . Please refer above screenshot

You can see internal stage created in SnowFlake

![image](https://github.com/user-attachments/assets/77ad2a9a-15bb-482d-8569-d267b57a9b89)


You can see data queried from Internal Stage

![image](https://github.com/user-attachments/assets/039820e8-9a60-4920-bc6f-b6a2f34421fa)


Next step is to create destination table Jobs in Snowflake

![image](https://github.com/user-attachments/assets/d0cd541e-c14b-4c15-b540-bfad6d80c2f7)

Next step is to load csv data from Internal stage to SnowFlake table


![image](https://github.com/user-attachments/assets/e922cd35-8255-419d-95ed-820578889f85)

Data is succefully loaded in SnowFlake

![image](https://github.com/user-attachments/assets/58954d93-367e-4da0-9417-996e70688ae9)






