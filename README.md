how to comunicate two docker container on the same machine 

# first create network 
1. docker network create name_of_the_network_give_by_you

# for the app
1. build the image using below command 
docker build -t "my-app" .

2. run container 
docker run -p 3000:3000 --network name_of_network my-app


# for the data base 

1. create docker volume
docker volume create volume_name

2. take image from docker Engine using below command
docker run image-name(mongo)

3. run container using below command 
docker run --name name_of_the_mongo_container_you_want  --network name_of_network docker_volume:/data/db image_name(mongo) 
