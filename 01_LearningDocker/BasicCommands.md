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

`$ docker version`\
// shows infos about installed Docker version

`$ docker infos`\
// shows even more infos about the installed Docker



## Running and Starting containers
`$ docker container run <image>` 

e.g. running a nginx container old and new way:

`$ docker container run -p 8080:80 --name nginx -d nginx`\
*-p = Port Exposure, --name = Naming the Container, -d = detached)*


