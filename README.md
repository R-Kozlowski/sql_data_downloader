# sql_data_downloader
A program to retrieve data from various TMS databases


This Python program is designed to retrieve data from an Oracle SQL database at one time to eliminate the need to log into each environment separately. Each environment has specific parameters, which are then passed to the function. 
The library "cx_Oracle" is used to create a connection to the database and pass the SQL query. To get the correct result of a given query, replace the values placed in apostrophes with a value like :1, :2, etc., and then pass the value in the line "cur.execute(query, 'first value','second value',)". The "pandas" library is used to concatenate the results into a single table and save it to an excel file in a given location. The "os" library is used to recognize the path where the program was opened. 
Such a program can be compiled into an .exe program (by the pyinstaller library), and then run at regular intervals through the Windows "task scheduler".
