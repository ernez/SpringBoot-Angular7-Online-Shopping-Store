docker run --name=my_postgres -d postgres:9.4.5
docker run --rm --name=my_postgres -p 5432:5432 -d postgres:9.4.5

docker exec -it my_postgres psql -U postgres


postgres-# \list -> list all databases

SELECT                                                                                                                           
datname                                                                                                                                     
FROM                                                                                                                                        
pg_database;
  datname  
-----------
 template1
 template0
 postgres
(3 rows)

\q  --> to quit


