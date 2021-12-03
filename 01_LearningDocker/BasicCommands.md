# Docker Commands (basics)

## Old and New Commands
There is a new way to write docker commands. The old commands will still work for example: `$ docker ps` \
old: `$ docker ps` \
new: `$ docker container ls`\

Here a few examples:
-   old: `$docker ps`\
    new: `$ docker container ls`\
        ($docker container ls -a) ect.\
-   old: `& docker run`\
    new: `& docker container run` \
-   old: `& docker start <container>`\
    new: `& docker container run <container>` \ 

In this readme i will try to stick to the new way to write docker commands but also mention the old command.

## Show infos

`$ docker version` \
// shows infos about installed Docker version

`$ docker infos` \
// shows even more infos about the installed Docker

### Only show Docker Client version number:
`$ docker -v` 

## Running and Starting containers
The difference between the run and start command:\
`$ docker container run <image>` always start a new container (if possible otherwise fails)\

`$ docker container start <container>` on the other hand restarts a already build container\

`$ docker container run <image>` will always build a new container from a image, if the image already exists on the machine it will start the container right away/
otherwise it will look for the image on DockerHub(standart if not otherwise declared)\

### A few examples to run different containers
*-p = Port Exposure, --name = Naming the Container, -d = detached)*
#### Ngnix
`$ docker container run -p 80:80 --name nginx -d nginx`
#### Apache
`$ docker container run -p 8080:80 --name apache2 -d httpd`
#### MySQL
`$ docker container run -p 3306:3306 --name mysql -d -e MYSQL_RANDOM_ROOT_PASSWORD=true mysql`

__Old Way:__
```
`$ docker run <image>`
`$ docker start <container>`
```
