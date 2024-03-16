### How to launch docker compose file correctly

docker compose up -d

docker run -it -d --name mongo-container -p 27017:27017 --network mydockernetwork --restart always -v "$(pwd)/mongodb_data:/data/db" mongo:latest

docker run -d --name sql-container --network mydockernetwork --restart always -e 'ACCEPT_EULA=Y' -e 'SA_PASSWORD=password123' -e 'MSSQL_PID=Express' -p 1433:1433 mcr.microsoft.com/mssql/server:2017-latest-ubuntu
