```
docker build -t team16-db ./db
docker build -t team16-app ./app

docker network create team16-net

docker run -d --name team16-db --network team16-net --network-alias db --hostname db -it team16-db
docker run -d --name team16-app --network team16-net -p 8080:8080 -it team16-app
```
