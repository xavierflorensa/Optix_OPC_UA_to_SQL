<a name="_toc157191126"></a>OPC UA to SQL with FactoryTalk Optix
# Contents
[1.	OPC UA Client](#_toc157234601)

[2.	Writing to an SQL database](#_toc157234602)

[3.	Creating a OPC UA to SQL converter](#_toc157234603)


1. # <a name="_toc157234601"></a>OPC UA Client
Let’s create a new OPC Client

<https://www.rockwellautomation.com/docs/en/factorytalk-optix/1-00/contents-ditamap/using-the-software/opc-ua/manage-the-opc-ua-client.html>


![Aspose Words 9a4ef72d-2c56-4e38-8555-c09687483f0d 001](https://github.com/xavierflorensa/Optix_OPC_UA_to_SQL/assets/55208134/5c242f15-4cf1-48c6-b3a2-ff112654de31)

Change the address and port of the OPC UA server

![Aspose Words 9a4ef72d-2c56-4e38-8555-c09687483f0d 002](https://github.com/xavierflorensa/Optix_OPC_UA_to_SQL/assets/55208134/cbe038f9-8e23-47c9-b3b3-5996ed55002c)

For instance with FT Kepserver Enterprise, port number is 49370

![Aspose Words 9a4ef72d-2c56-4e38-8555-c09687483f0d 003](https://github.com/xavierflorensa/Optix_OPC_UA_to_SQL/assets/55208134/554f2a08-e62e-4617-a1a8-42605b21ab02)

Right click to add a new OPCUA Tag Importer

Then double click on it

![Aspose Words 9a4ef72d-2c56-4e38-8555-c09687483f0d 004](https://github.com/xavierflorensa/Optix_OPC_UA_to_SQL/assets/55208134/bcc1d093-ff17-4307-b59e-65f7a26eab7b)

Click on the Button to go online with the OPC server

![Aspose Words 9a4ef72d-2c56-4e38-8555-c09687483f0d 005](https://github.com/xavierflorensa/Optix_OPC_UA_to_SQL/assets/55208134/4ac45690-9d0c-41a6-929a-2d57cf6707fc)

![Aspose Words 9a4ef72d-2c56-4e38-8555-c09687483f0d 006](https://github.com/xavierflorensa/Optix_OPC_UA_to_SQL/assets/55208134/0cbd745f-bd0d-4fa2-ac2c-58d2e2d3bb86)

Click on apply

![Aspose Words 9a4ef72d-2c56-4e38-8555-c09687483f0d 007](https://github.com/xavierflorensa/Optix_OPC_UA_to_SQL/assets/55208134/9892fa5f-8a72-44e7-91d3-f932c458fc10)

On Objects you will see this

![Aspose Words 9a4ef72d-2c56-4e38-8555-c09687483f0d 008](https://github.com/xavierflorensa/Optix_OPC_UA_to_SQL/assets/55208134/7a2b86a0-9ead-4f1a-8051-901ed86dfcea)
Now let’s create a texbox that points to the data

![Aspose Words 9a4ef72d-2c56-4e38-8555-c09687483f0d 009](https://github.com/xavierflorensa/Optix_OPC_UA_to_SQL/assets/55208134/c6a11572-7076-456c-993c-5a93fe58a6c8)

![Aspose Words 9a4ef72d-2c56-4e38-8555-c09687483f0d 010](https://github.com/xavierflorensa/Optix_OPC_UA_to_SQL/assets/55208134/6f7bfee6-0995-4731-8c24-e90d5eebb633)

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

