# Docker Commands (basics)

## Old and New Commands
There is a "new" way to writer docker commands. The old commands will still work for example: `docker ps` /n
asd

old: $ docker ps
new: $ docker container ls
    ($docker container ls -a) ect.

old: & docker run
new: & docker container run

old: & docker start <container>
new: & docker container run <container>

This cheatsheet will use the new commandstructure.


$ docker version
// shows infos about installed Docker version

$ docker infos
// shows even more infos about the installed Docker



## Running and Starting containers
$ docker container run

e.g. running a nginx container old and new way:

old:
$ docker run -p 8080:80 --name nginx -d nginx

new:
$ docker container run -p 8080:80 --name nginx -d nginx

(-p = Port Exposure, --name = Naming the Container, -d = detached)


