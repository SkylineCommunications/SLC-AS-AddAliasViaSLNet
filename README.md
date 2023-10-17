# SLC-AS-AddAliasViaSLNet
An automation Script that helps you to add an alias that can be used to query offloaded data via GQI. 

Steps on how this Automation script can be useful. 

1. Create a protocol with a table that is offloading data via "Direct Connection", of which the implementation is explained in https://docs.dataminer.services/develop/devguide/Connector/AdvancedLoggerTablesDefiningDirectConnectionTable.html .

An example is shown below, where a table is offloading a type of Error-records. 

Please note, as indicated in the documentation, that you need to set RTDisplay-tag to true in order to enable the GQI query "Get Parameter Table By Alias". 

2. Install this automation script on your Dataminer Agent. Execute the Automation Script, where the first parameter "Alias" is a text-value you can choose. The "CustomDatabaseNameInProtocol" and "OffloadedTableNameInProtocol" depend on what you implemented in your protocol.

3. Create a dashboard and load a "Get Parameter By Alias"-query. Select the "Alias"-text-value you chose in step 2. You should get the records displayed that were offloaded. Note that the "partitionsToKeep" attribute also has an influence. In the example below, it is mentioned that the data is only kept 3 hours, so only the records of the last 3 hours will be shown.

4. 



