# Docker Command
01. docker --version : Check docker version

## Docker Images
01.  docker pull nameimage:tag : pull a image from dockerhub
02.  docker images : Show all images in docker
03.  docker run [imageName] : run a container
04.  docker rmi [imageName] : Remove a image
05.  docker rmi $(docker images -q) : Delete All images

## Docker Container
01.  docker ps : Show all container is running
02.  docker ps -a : Show all container is running and stop
03.  docker start [containerId] : Start container when it is stop
04.  docker stop [containerId] : Start container when it is start
05.  docker restart [containerId] : Restart a container
06.  docker rm [containerId] : Remove a container when it is stop
07.  docker stop $(docker ps -a -q) : Stop all container is running
08.  docker rm $(docker ps -a -q) : Delete All container
09.  docker container attach containerid : Go to terminal container is running
10.  CTRL + P + Q : Exit terminal, but container is running
11.  docker history name_or_id_of_image : The history of container or images
12.  docker diff container-name-or-id : diff
13.  docker logs -f container-name-or-id : Log container
14.  docker stats container-name-or-id : Stats
15.  docker exec -it {new_container_name} sh: Truy cập vào container đang chạy:


## Network in Docker
01. docker network ls: Show all list networks
02. docker network create --driver [driverOption] networkName : Create a network
 driverOption:
  - bridge
  - ...
03. docker network disconnect : Disconnect a container from a network
04. docker network inspect : Display detailed information on one or more networks
05. docker network prune : Remove all unused networks
06. docker network rm :	Remove one or more networks

## Sử dụng Dockerfile
Dockerfile là một file text, trong đó chứa các dòng chỉ thị để Docker đọc và chạy theo chỉ thị đó để cuối cùng bạn có một image mới theo nhu cầu. Khi đang có một Dockerfile giả sử có tên là Dockerfile để ra lệnh cho Docker chạy nó bạn có thể gõ:
```
docker build -t nameimage:version --force-rm -f Dockerfile .
```
Bạn chú ý dấu . ở cuối lệnh docker build ở trên, có nghĩa tìm file có tên Dockerfile ở thư mục hiện tại.

-t nameimage:version là đặt tên và tag được gán cho image mới tạo ra.


## Docker Compose
01. docker-compose up --build -d : run file docker-compose.yml
02. docker-compose down : Stop and delete container
