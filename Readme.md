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

![Aspose Words 9a4ef72d-2c56-4e38-8555-c09687483f0d 011](https://github.com/xavierflorensa/Optix_OPC_UA_to_SQL/assets/55208134/c715cfd7-f367-4d58-a7e8-18748f255f53)

Let’s add a label

![Aspose Words 9a4ef72d-2c56-4e38-8555-c09687483f0d 012](https://github.com/xavierflorensa/Optix_OPC_UA_to_SQL/assets/55208134/32570b02-e218-498e-bbca-070d8ff8f24b)

1. # <a name="_toc157191127"></a><a name="_toc157234602"></a>Writing to an SQL database

Let’s write to an SQL database from Optix

First just read from a Database

<https://www.rockwellautomation.com/docs/en/factorytalk-optix/1-00/contents-ditamap/using-the-software/datastore-database.html>

Add a Database object

![Aspose Words 9a4ef72d-2c56-4e38-8555-c09687483f0d 013](https://github.com/xavierflorensa/Optix_OPC_UA_to_SQL/assets/55208134/8f294fea-3576-4411-b521-53724ac5378c)

Be sure to have an SQL working database, with user, password, access thru TCP/IP, etc.

![Aspose Words 9a4ef72d-2c56-4e38-8555-c09687483f0d 014](https://github.com/xavierflorensa/Optix_OPC_UA_to_SQL/assets/55208134/51d56bb2-fac2-4a73-a6c0-6b7c459d1453)

Complete database properties click on Table +  and Column + to match our Database

![Aspose Words 9a4ef72d-2c56-4e38-8555-c09687483f0d 015](https://github.com/xavierflorensa/Optix_OPC_UA_to_SQL/assets/55208134/775e4cc4-185f-4779-986e-afb027d15a92)

![Aspose Words 9a4ef72d-2c56-4e38-8555-c09687483f0d 016](https://github.com/xavierflorensa/Optix_OPC_UA_to_SQL/assets/55208134/22a09191-4232-4357-9882-213a59d3019d)

If you do not add a column here you will have errors when drag and drop to the Table1 to the  data grid (Unable to insert a empty table to the datagrid)

Display Database data

<https://www.rockwellautomation.com/docs/en/factorytalk-optix/1-00/contents-ditamap/using-the-software/datastore-database/display-database-table-data.html>

Just click on the + on Tables to create a new table (even thought it already exists on the MS database)

![Aspose Words 9a4ef72d-2c56-4e38-8555-c09687483f0d 017](https://github.com/xavierflorensa/Optix_OPC_UA_to_SQL/assets/55208134/109df422-e1b6-4d30-aeba-1f57227d5ab2)

Do not forget to add a column minimum

Drag and Drop

![Aspose Words 9a4ef72d-2c56-4e38-8555-c09687483f0d 018](https://github.com/xavierflorensa/Optix_OPC_UA_to_SQL/assets/55208134/9f55f04d-6337-4c68-80a2-b92a78f67fee)

It works!!

![Aspose Words 9a4ef72d-2c56-4e38-8555-c09687483f0d 019](https://github.com/xavierflorensa/Optix_OPC_UA_to_SQL/assets/55208134/71ed43ca-8ca2-478c-9a23-50d22e00cdae)

Now let’s try to write a variable on the database

Using this example

<https://www.rockwellautomation.com/docs/en/factorytalk-optix/1-00/contents-ditamap/developing-solutions/application-examples/logger-tutorial/develop-a-data-logger-with-odbc-data-store.html>

Download a sample project: [DataLoggerODBC.zip](C:\Program Files\Rockwell Automation\FactoryTalk Optix\Studio\Help\en\downloads\DataLoggerODBC.zip) 

<https://www.rockwellautomation.com/content/dam/dita/en/factorytalk-optix/1-00/downloads/DataLoggerODBC.zip>

To see how it is made.

But let’s start creating a complete new project

For instance sql\_datalogger\_optix\_v2

![Aspose Words 9a4ef72d-2c56-4e38-8555-c09687483f0d 020](https://github.com/xavierflorensa/Optix_OPC_UA_to_SQL/assets/55208134/2ee51f11-ca38-409f-9f6a-42c3e9a2a223)

But first let’s create a database without a Table (Optix and The Datalogger function will create the Table)

For instance let’s create a new database Optix2

![Aspose Words 9a4ef72d-2c56-4e38-8555-c09687483f0d 021](https://github.com/xavierflorensa/Optix_OPC_UA_to_SQL/assets/55208134/fdb2f012-adb3-4e64-abd1-dfe7b4829f4c)

Just give a name, that’s all

![Aspose Words 9a4ef72d-2c56-4e38-8555-c09687483f0d 022](https://github.com/xavierflorensa/Optix_OPC_UA_to_SQL/assets/55208134/4b6cffac-1328-4b39-bcd3-9f16050cd340)

There are no user tables

![Aspose Words 9a4ef72d-2c56-4e38-8555-c09687483f0d 023](https://github.com/xavierflorensa/Optix_OPC_UA_to_SQL/assets/55208134/f7143df8-0bf0-424b-b7cc-cfb35c3fd89f)

Now Let’s go to Optix

Add a variable to work with

![Aspose Words 9a4ef72d-2c56-4e38-8555-c09687483f0d 024](https://github.com/xavierflorensa/Optix_OPC_UA_to_SQL/assets/55208134/8f0836ad-f171-47aa-8ef8-73a4f4912fd1)

![Aspose Words 9a4ef72d-2c56-4e38-8555-c09687483f0d 025](https://github.com/xavierflorensa/Optix_OPC_UA_to_SQL/assets/55208134/8446e282-a4b0-4a0d-8842-e1eb67307990)

Add a Slider to enter values to such variable

![Aspose Words 9a4ef72d-2c56-4e38-8555-c09687483f0d 026](https://github.com/xavierflorensa/Optix_OPC_UA_to_SQL/assets/55208134/7ac72bdf-6797-471a-9f66-dcd67df6ff8c)

Next create the Database instance on Optix

![Aspose Words 9a4ef72d-2c56-4e38-8555-c09687483f0d 027](https://github.com/xavierflorensa/Optix_OPC_UA_to_SQL/assets/55208134/b720d6eb-234b-4d1f-8246-e66bce0c370e)

Point to the existing database, but do not create any Table on Optix

![Aspose Words 9a4ef72d-2c56-4e38-8555-c09687483f0d 028](https://github.com/xavierflorensa/Optix_OPC_UA_to_SQL/assets/55208134/280b4a38-2c2d-4a74-8bbf-01cd529f2403)

Then create a new DataLogger

![Aspose Words 9a4ef72d-2c56-4e38-8555-c09687483f0d 029](https://github.com/xavierflorensa/Optix_OPC_UA_to_SQL/assets/55208134/45214704-ec59-4c9e-bc00-4c133ac2b00a)

And select the variable to log and the destination, just the database

![Aspose Words 9a4ef72d-2c56-4e38-8555-c09687483f0d 030](https://github.com/xavierflorensa/Optix_OPC_UA_to_SQL/assets/55208134/7a1d663e-1cc2-49a3-b159-341ad4679925)

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

