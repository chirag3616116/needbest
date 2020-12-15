 Steps to Begin With Apache Spark.

Step 1: Ensure if Java is installed on your system
Before installing Spark, Java is a must-have for your system. The following command will verify the version of Java installed on your system:
Step 2:Install the IntelijIdea for the purpose of handling the spark with scala.
Step 3:Add the shortcut to the desktop .
Step 4:Open the desktop launcher of Intelijidea and make the further options so as to maintain the progress of whole criterion
Step 5:Add the sbt of required functionalities like scala,spark,delta lake,kafka and build these in build.sbt and then refresh the project so as to update the required libraries to the intelijidea.

Step 6:You can start building your project .
Software Requirements:
●Spark version: 3.0+
●Kafka Version: deployed dependencies
●Delta Lake Version: 0.7.0
●Scala version: Specific to Spark version



	                                     About Task 1:
-> I was suppose to convert csv given file to a json format .

I took csv file that was given to us as an input and then by using Sparksession firstly started the code and afterwards:
I have read the csv file and for convert csv to json file firstly i have read csv and converted to dataframe and then from 
dataframe have converted the df to json file by using .write operation in json format we can write files in different formats like.json,.csv,.parquet.


 			                                About Task 2:
(a).Apply the specified transformationsI took csv file that was given to us as an input and then by using Sparksession firstly started the code and afterwards:
(These are the transformations.):

1.Add processing_date and processing_time_utc.
2.Add ‘Xenonstack’ as company name.
3.Add ‘10min’ as data_source.
4.Set timestamp_utc as end_timestamp_utc.
5.Create start_timestamp_utc as end_timestamp_utc - 10 min.
6.Unpivot the columns other than timestamp_utc, start_timestamp_utc,
end_timestamp_utc, processing_date, processing_time_utc, turbine_id, company_name
and data_source into singal_code and signal_value.
(b).Write the Data into Open Delta lake format.
Firstly I made sure that the file in csv has to be converted into dataframe and then we can apply the changes required to the dataframes.
I got one dataframe and shown it by .show operation.
Need to add few columns for that used a code that was required to add a column in the given dataframe.
Afterwards, need to change the name of the columns given to some other that has also been done by a syntax given in spark(.withcolumnrename("",""))
It accepts 2 paremetres first is for the purpose of existing name and other one is for the purpose of new name.
Unpivot the two columns into two variables that are of columns as well, for that I have made a .selectexpr and used stack as there is no unpivot command in scala.
Furthermore i have to manage the saved file that should be saved in delta lake format for that i used .format("delta")to save that file and then.
I have a file with commit log along and with certain functionalities in my memory .
Thats all what i have done.
