Create, Build and Run docker:
------------------------------
1) Create Dockerfile
2) Add Dockerfile contents
3) docker build -t <<image_name>>
	- This command used to build image
4) docker run -dp <ip-address><Host_port>:<container_port> <image_name> 
	- This command used to run docker file in detached mode using -d
5) Access application using <<ipaddrss:port>>

Remove Container:
-----------------
1) docker ps
	- Used to get container id
2) docker stop <<container_id>>
3) docker rm <<container_id>>

Push the Image:
--------------

2) docker login -u YOUR-USER-NAME
3) docker tag getting-started YOUR-USER-NAME/getting-started
4) docker push YOUR-USER-NAME/getting-started

Create a volume:
----------------

1) docker volume create todo-db
2) docker run -dp 127.0.0.1:3000:3000 --mount type=volume,src=todo-db,target=/etc/todos getting-started
