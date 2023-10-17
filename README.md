# SLC-AS-AddAliasViaSLNet
An automation Script that helps you to add an alias that can be used to query offloaded data via GQI. 

Steps on how this Automation script can be useful. 

1. Create a protocol with a table that is offloading data via "Direct Connection", of which the implementation is explained on [a specific page on the public Dataminer Docs]([https://pages.github.com/](https://docs.dataminer.services/develop/devguide/Connector/AdvancedLoggerTablesDefiningDirectConnectionTable.html)).

   An example is shown below, where a table is offloading a type of Error-records.  



  ![ExampleTable](https://github.com/SkylineCommunications/SLC-AS-AddAliasViaSLNet/assets/121804974/f19f6df2-6fad-42af-8368-a96732b13730)

  Please note, as indicated in the documentation, that you need to set RTDisplay-tag to true in order to enable the GQI query "Get Parameter Table By Alias". 

2. Install this automation script on your Dataminer Agent. Execute the Automation Script, where the first parameter "Alias" is a text-value you can choose. The "CustomDatabaseNameInProtocol" and "OffloadedTableNameInProtocol" depend on what you implemented in your protocol.
  
  ![ExecuteAlias](https://github.com/SkylineCommunications/SLC-AS-AddAliasViaSLNet/assets/121804974/ceae1370-b9b1-4d1a-bb2f-a1bbd6312ba0)

3. Create a dashboard and load a "Get Parameter By Alias"-query. Select the "Alias"-text-value you chose in step 2. You should get the records displayed that were offloaded. 

  ![ExampleGetParameterTableByAlias](https://github.com/SkylineCommunications/SLC-AS-AddAliasViaSLNet/assets/121804974/9f98ba44-d532-4e0a-aeb3-9746d76f4e5d)

  Note that the "partitionsToKeep" attribute also has an influence. In the example below, it is mentioned that the data is only kept 3 hours, so only the records of the last 3 hours will be shown.

  ![TimeToLive](https://github.com/SkylineCommunications/SLC-AS-AddAliasViaSLNet/assets/121804974/f09fc701-7e77-43fc-b54d-eeacdef19a2a)


Here's a line for us to start with.

This line is separated from the one above by two newlines, so it will be a *separate paragraph*.

This line is also a separate paragraph, but...
This line is only separated by a single newline, so it's a separate line in the *same paragraph*.
