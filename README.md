# SLC-AS-AddAliasViaSLNet
An automation Script that helps you to add an alias that can be used to query offloaded data via GQI. 

Steps on how this Automation script can be useful. 

1. Create a protocol with a table that is offloading data via "Direct Connection", of which the implementation is explained on [a specific page on the public Dataminer Docs](https://docs.dataminer.services/develop/devguide/Connector/AdvancedLoggerTablesDefiningDirectConnectionTable.html).

   An example is shown below, where a table is offloading a type of Error-records.

   ![ExampleTable](https://github.com/SkylineCommunications/SLC-AS-AddAliasViaSLNet/assets/121804974/3c5ff2f6-5cf7-47c4-a8e1-8d4dfecbd98c)
   
   Please note, as indicated in the documentation, that you need to set RTDisplay-tag to true in order to enable the GQI query "Get Parameter Table By Alias". 

3. Install this automation script on your Dataminer Agent. Execute the Automation Script, where the first parameter "Alias" is a text-value you can choose. The "CustomDatabaseNameInProtocol" and "OffloadedTableNameInProtocol" depend on what you implemented in your protocol.

   ![ExecuteAlias](https://github.com/SkylineCommunications/SLC-AS-AddAliasViaSLNet/assets/121804974/5a077cb1-dab1-425e-b62d-6f663de64395)

4. Create a dashboard and load a "Get Parameter By Alias"-query. Select the "Alias"-text-value you chose in step 2. You should get the records displayed that were offloaded.

   ![ExampleGetParameterTableByAlias](https://github.com/SkylineCommunications/SLC-AS-AddAliasViaSLNet/assets/121804974/4eaf04c1-0932-40eb-8d10-7033d5c2a236)

   Note that the "partitionsToKeep" attribute also has an influence. In the example below, it is mentioned that the data is only kept 3 hours, so only the records of the last 3 hours will be shown.

   ![TimeToLive](https://github.com/SkylineCommunications/SLC-AS-AddAliasViaSLNet/assets/121804974/b82c05ff-cc5e-40ba-b7e2-6ce28f92121d)

