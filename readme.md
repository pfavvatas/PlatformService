commands:

**Docker:**

1. `docker build -t pfavvatas/platformservice .`
2. `docker run -p 8888:80 --name platformservice-container -d pfavvatas/platformservice`
3. `docker ps`
   CONTAINER ID IMAGE COMMAND CREATED STATUS PORTS NAMES

   93c11c33c0ae pfavvatas/platformservice "dotnet PlatformServ…" Less than a second ago Up 30 seconds 0.0.0.0:8080->80/tcp dreamy_euclid

4. `docker stop "CONTAINER ID"` example `docker stop 93c11c33c0ae`
5. `docker start "CONTAINER ID"` example `docker start 93c11c33c0ae`
6. `docker push pfavvatas/platformservice`

test results `http://localhost:8888/api/platforms`

ping docker
`docker ps`
`docker exec <container_id_or_name> curl localhost:<port>` example `docker exec 498d4756156b curl localhost:4444`
`docker inspect 7fcdfef283a8 | grep IP`

`docker exec -it platformservice-container bash`

`docker logs platformservice-container`
