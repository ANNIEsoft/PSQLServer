# PSQLServer

To create a contianer with the web server in use:

   	  docker run --name=PSQLServer --net=host -dt anniesoft/psqlserver bash -c "su postgres -c 'postgres -D /PSQLServer'"


Note: server is blank with no users permissions or tables.

You can log into it with a local psql client, or if you do not have one you can spawn a docker container to act as your local client with

    	docker run --name=PSQLClient --net=host -it anniesoft/psqlserver bash -c " su postgres -c 'psql -h 127.0.0.1' "
      
To subsequently start or stop the psql server or client use the following commands:

      docker start PSQLServer
      docker stop PSQLServer
      
      docker start -i PSQLClient
      docker Stop PSQLClient
      
Note: if you want a one time use client and not a perminant contianer replase `--name=PSQLClient` with `--rm`
