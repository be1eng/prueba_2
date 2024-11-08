FROM mcr.microsoft.com/mssql/server:2020-latest

ENV ACCEPT_EULA=Y \
    MSSQL_SA_PASSWORD=DockerCon!!!

WORKDIR /init
COPY init-db.* ./

RUN chmod +x ./init-db.sh

CMD /bin/bash -c "/opt/mssql/bin/sqlservr & sleep 30 && ./init-db.sh"
