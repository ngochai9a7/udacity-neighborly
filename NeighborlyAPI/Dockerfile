# To enable ssh & remote debugging on app service change the base image to the one below
# FROM mcr.microsoft.com/azure-functions/python:3.0-python3.9-appservice
FROM mcr.microsoft.com/azure-functions/python:3.0-python3.9

ENV AzureWebJobsScriptRoot=/home/site/wwwroot \
    host:logger:consoleLoggingMode=always \
    AzureFunctionsJobHost__Logging__Console__IsEnabled=true \
    myAzureCosmosMongoDBConnectionString=mongodb://neighborlycosmosdb:4CavwWB9VDXIPgkoV42Yd1rQuFyDD4y84YSAT5giKBn2N8PFQ9u8oBbHdIZubqz077FHe5TkkU1NACDbLobKZg==@neighborlycosmosdb.mongo.cosmos.azure.com:10255/?ssl=true&replicaSet=globaldb&retrywrites=false&maxIdleTimeMS=120000&appName=@neighborlycosmosdb@

COPY requirements.txt /

EXPOSE 8080

RUN pip install -r /requirements.txt

COPY . /home/site/wwwroot