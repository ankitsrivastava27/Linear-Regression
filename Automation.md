   __*Creating Batch file of our R script*__

         start "" "C:\Program Files\Microsoft\R Open\R-3.4.2\bin\x64\R.exe" CMD BATCH C:\Users\Ankit\Desktop\schedulingpo\test.R

   __Then follow *windows task schedular* to automate it__.

   __save to sql server__

         tosql <- as.data.frame(target)

   __to drop the table__

         sqlQuery(dbhandle,"drop table Dealer_Data")

   __save the ouptput of model in sql__

         sqlSave(dbhandle,tosql,tablename = "Dealer_Data",rownames = F,
         colnames = F,safer = F,fast = T)
         
   _it will truncate the output in same table._
              
              append = TRUE(IN SQLSAVE)

   #### Requirements :

         1.	R studio 
         2.	Internet connectivity
         3.	A user is required on server with Local admin access and SQL Server database access with db_owner permission. 
         4.	Windows Server 2012R2 Standard
         5.	Database Server network connectivity
         6.	open R
         7.	Power BI





