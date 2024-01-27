<a name="_toc157191126"></a>OPC UA to SQL with FactoryTalk Optix
# Contents
[1.	OPC UA Client	1](#_toc157234601)

[2.	Writing to an SQL database	7](#_toc157234602)

[3.	Creating a OPC UA to SQL converter	29](#_toc157234603)


1. # <a name="_toc157234601"></a>OPC UA Client
Let’s create a new OPC Client

<https://www.rockwellautomation.com/docs/en/factorytalk-optix/1-00/contents-ditamap/using-the-software/opc-ua/manage-the-opc-ua-client.html>


![Graphical user interface, application

Description automatically generated](Aspose.Words.9a4ef72d-2c56-4e38-8555-c09687483f0d.001.png)

Change the address and port of the OPC UA server

![Graphical user interface, application

Description automatically generated](Aspose.Words.9a4ef72d-2c56-4e38-8555-c09687483f0d.002.png)

For instance with FT Kepserver Enterprise, port number is 49370

![Graphical user interface, text, application, email

Description automatically generated](Aspose.Words.9a4ef72d-2c56-4e38-8555-c09687483f0d.003.png)

Right click to add a new OPCUA Tag Importer

Then double click on it

![Graphical user interface, text, application

Description automatically generated](Aspose.Words.9a4ef72d-2c56-4e38-8555-c09687483f0d.004.png)

Click on the Button to go online with the OPC server

![Graphical user interface, text, application, Word

Description automatically generated](Aspose.Words.9a4ef72d-2c56-4e38-8555-c09687483f0d.005.png)

![Graphical user interface

Description automatically generated](Aspose.Words.9a4ef72d-2c56-4e38-8555-c09687483f0d.006.png)

Click on apply

![Graphical user interface, application

Description automatically generated](Aspose.Words.9a4ef72d-2c56-4e38-8555-c09687483f0d.007.png)

On Objects you will see this

![Text

Description automatically generated](Aspose.Words.9a4ef72d-2c56-4e38-8555-c09687483f0d.008.png)

Now let’s create a texbox that points to the data

![Graphical user interface, application

Description automatically generated](Aspose.Words.9a4ef72d-2c56-4e38-8555-c09687483f0d.009.png)

![Graphical user interface, table

Description automatically generated](Aspose.Words.9a4ef72d-2c56-4e38-8555-c09687483f0d.010.png)

That’s all

![Graphical user interface, table

Description automatically generated](Aspose.Words.9a4ef72d-2c56-4e38-8555-c09687483f0d.011.png)

Let’s add a label

![Graphical user interface, text

Description automatically generated](Aspose.Words.9a4ef72d-2c56-4e38-8555-c09687483f0d.012.png)
1. # <a name="_toc157191127"></a><a name="_toc157234602"></a>Writing to an SQL database

Let’s write to an SQL database from Optix

First just read from a Database

<https://www.rockwellautomation.com/docs/en/factorytalk-optix/1-00/contents-ditamap/using-the-software/datastore-database.html>

Add a Database object

![Graphical user interface, application

Description automatically generated](Aspose.Words.9a4ef72d-2c56-4e38-8555-c09687483f0d.013.png)

Be sure to have an SQL working database, with user, password, access thru TCP/IP, etc.

![Graphical user interface, text, application

Description automatically generated](Aspose.Words.9a4ef72d-2c56-4e38-8555-c09687483f0d.014.png)

Complete database properties click on Table +  and Column + to match our Database

![Table

Description automatically generated](Aspose.Words.9a4ef72d-2c56-4e38-8555-c09687483f0d.015.png)

![Graphical user interface, application

Description automatically generated](Aspose.Words.9a4ef72d-2c56-4e38-8555-c09687483f0d.016.png)

If you do not add a column here you will have errors when drag and drop to the Table1 to the  data grid (Unable to insert a empty table to the datagrid)

Display Database data

<https://www.rockwellautomation.com/docs/en/factorytalk-optix/1-00/contents-ditamap/using-the-software/datastore-database/display-database-table-data.html>

Just click on the + on Tables to create a new table (even thought it already exists on the MS database)

![Graphical user interface, text, application

Description automatically generated](Aspose.Words.9a4ef72d-2c56-4e38-8555-c09687483f0d.017.png)

Do not forget to add a column minimum

Drag and Drop

![Chart

Description automatically generated with medium confidence](Aspose.Words.9a4ef72d-2c56-4e38-8555-c09687483f0d.018.png)

It works!!

![Graphical user interface, text, application

Description automatically generated](Aspose.Words.9a4ef72d-2c56-4e38-8555-c09687483f0d.019.png)

Now let’s try to write a variable on the database

Using this example

<https://www.rockwellautomation.com/docs/en/factorytalk-optix/1-00/contents-ditamap/developing-solutions/application-examples/logger-tutorial/develop-a-data-logger-with-odbc-data-store.html>

Download a sample project: [DataLoggerODBC.zip](C:\Program Files\Rockwell Automation\FactoryTalk Optix\Studio\Help\en\downloads\DataLoggerODBC.zip) 

<https://www.rockwellautomation.com/content/dam/dita/en/factorytalk-optix/1-00/downloads/DataLoggerODBC.zip>

To see how it is made.

But let’s start creating a complete new project

For instance sql\_datalogger\_optix\_v2

![Graphical user interface, application

Description automatically generated](Aspose.Words.9a4ef72d-2c56-4e38-8555-c09687483f0d.020.png)

But first let’s create a database without a Table (Optix and The Datalogger function will create the Table)

For instance let’s create a new database Optix2

![Graphical user interface, text, application, email

Description automatically generated](Aspose.Words.9a4ef72d-2c56-4e38-8555-c09687483f0d.021.png)

Just give a name, that’s all

![Graphical user interface, text, application

Description automatically generated](Aspose.Words.9a4ef72d-2c56-4e38-8555-c09687483f0d.022.png)

There are no user tables

![Graphical user interface, application

Description automatically generated](Aspose.Words.9a4ef72d-2c56-4e38-8555-c09687483f0d.023.png)

Now Let’s go to Optix

Add a variable to work with

![Graphical user interface, text, application

Description automatically generated](Aspose.Words.9a4ef72d-2c56-4e38-8555-c09687483f0d.024.png)

![Graphical user interface, text, application

Description automatically generated](Aspose.Words.9a4ef72d-2c56-4e38-8555-c09687483f0d.025.png)

Add a Slider to enter values to such variable

![Graphical user interface, chart

Description automatically generated](Aspose.Words.9a4ef72d-2c56-4e38-8555-c09687483f0d.026.png)

Next create the Database instance on Optix

![Graphical user interface

Description automatically generated](Aspose.Words.9a4ef72d-2c56-4e38-8555-c09687483f0d.027.png)

Point to the existing database, but do not create any Table on Optix

![Graphical user interface, text, application

Description automatically generated](Aspose.Words.9a4ef72d-2c56-4e38-8555-c09687483f0d.028.png)

Then create a new DataLogger

![A picture containing table

Description automatically generated](Aspose.Words.9a4ef72d-2c56-4e38-8555-c09687483f0d.029.png)

And select the variable to log and the destination, just the database

![Graphical user interface, text, application, email

Description automatically generated](Aspose.Words.9a4ef72d-2c56-4e38-8555-c09687483f0d.030.png)

If we now open the ODBC object, surprise, a new Table an columns have been created for us

![Graphical user interface, text, application

Description automatically generated](Aspose.Words.9a4ef72d-2c56-4e38-8555-c09687483f0d.031.png)

If we take a look at the database:

You have to disconnect and connect again to see the changes

![Graphical user interface, text, application

Description automatically generated](Aspose.Words.9a4ef72d-2c56-4e38-8555-c09687483f0d.032.png)

![Graphical user interface, text, application, email

Description automatically generated](Aspose.Words.9a4ef72d-2c56-4e38-8555-c09687483f0d.033.png)

Still nothing

![Graphical user interface, text, application

Description automatically generated](Aspose.Words.9a4ef72d-2c56-4e38-8555-c09687483f0d.034.png)

Until you run the Optix Runtime

![Chart

Description automatically generated](Aspose.Words.9a4ef72d-2c56-4e38-8555-c09687483f0d.035.png)

Give some values to the gauge dropping the index

Then go to the Database, and …voilà

![Graphical user interface, application

Description automatically generated](Aspose.Words.9a4ef72d-2c56-4e38-8555-c09687483f0d.036.png)

Now let’s look at the data, this is working fine

![Graphical user interface, text, application

Description automatically generated](Aspose.Words.9a4ef72d-2c56-4e38-8555-c09687483f0d.037.png)

Now let’s add a Datagrid on the Optix Project

Drag and drop the table to the Datagrid

![Graphical user interface

Description automatically generated with medium confidence](Aspose.Words.9a4ef72d-2c56-4e38-8555-c09687483f0d.038.png)

![A picture containing chart

Description automatically generated](Aspose.Words.9a4ef72d-2c56-4e38-8555-c09687483f0d.039.png)

Let’s test it. It works! That’s all

![Graphical user interface

Description automatically generated](Aspose.Words.9a4ef72d-2c56-4e38-8555-c09687483f0d.040.png)






1. # <a name="_toc157191128"></a><a name="_toc157234603"></a>Creating a OPC UA to SQL converter

Take last SQL project and delete the gauge.

Then add the OPC UA client like in section 6.

![Graphical user interface, text, application, email

Description automatically generated](Aspose.Words.9a4ef72d-2c56-4e38-8555-c09687483f0d.041.png)

Now we have access to IoT\_data Tag

![Graphical user interface, application, table, Excel

Description automatically generated](Aspose.Words.9a4ef72d-2c56-4e38-8555-c09687483f0d.042.png)

First of all test that we are reading OPC UA data

Yes

![Graphical user interface, text, application

Description automatically generated](Aspose.Words.9a4ef72d-2c56-4e38-8555-c09687483f0d.043.png)

Then let’s erase the data on the database from previous chapter.

![Graphical user interface, text, application, email

Description automatically generated](Aspose.Words.9a4ef72d-2c56-4e38-8555-c09687483f0d.044.png)

Verify that the data is erased from Optix

![Graphical user interface, text, application, email

Description automatically generated](Aspose.Words.9a4ef72d-2c56-4e38-8555-c09687483f0d.045.png)

Now just change the source of data on the datalogger Object

![Graphical user interface, text, application, email

Description automatically generated](Aspose.Words.9a4ef72d-2c56-4e38-8555-c09687483f0d.046.png)

Let’s test The Optix Runtime

It takes a while until the values are logged. I have also restarted the OPC UA server.

![Graphical user interface, text, application

Description automatically generated](Aspose.Words.9a4ef72d-2c56-4e38-8555-c09687483f0d.047.png)

Clear the Table again

First time we see nothing on the  Optix runtime datagrid window

Let’s close the runtime and open it again

Now it works

![Graphical user interface, text

Description automatically generated](Aspose.Words.9a4ef72d-2c56-4e38-8555-c09687483f0d.048.png)

Let’s put an autorefresh to the datagrid and sort ascending, descending to see it live!

![Graphical user interface, text, application

Description automatically generated](Aspose.Words.9a4ef72d-2c56-4e38-8555-c09687483f0d.049.png)

![Table

Description automatically generated](Aspose.Words.9a4ef72d-2c56-4e38-8555-c09687483f0d.050.png)

As you can see on this video

<https://www.youtube.com/watch?v=irL_CHUZaHY>

![Graphical user interface, application, Excel

Description automatically generated](Aspose.Words.9a4ef72d-2c56-4e38-8555-c09687483f0d.051.png)

