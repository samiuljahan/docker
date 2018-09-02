#  Basic Docker Commands
see the ip adress of the docker machine<br>
`$ docker-machine ip`

check docker version <br >
`$ docker --version`

get more info <br >
`$ docker info`

see client and server version <br >
`$ docker version`

see list of docker images <br >
`$ docker image ls`

remove a docker image <br >
`$ docker image rm -f hellojava`<br >
here, `hellojava` is the docker image

see available commands <br >
`$ docker --help`

only see new commands <br >
`$  DOCKER_HIDE_LEGACY_COMMANDS=true docker --help`

see sub commands for a command, in this case, `image` command<br >
`$  docker image --help`

see list of images on the host<br >
`$  docker image ls`

see complete list of helps of a sub command, in this case `run` subcommand<br >
`$  docker run --help`

run a docker container<br >
`$ docker container run jboss/wildfly`

run in interactive mode, in foreground<br >
 `$ docker container run -it jboss/wildfly`

run in interactive mode, in background<br >
 `$ docker container run -d jboss/wildfly`

see the list of running containers<br >
`$  docker container ls`

stopping a container, with id<br >
`$  docker container stop f4a7682e5370`<br >
here, `f4a7682e5370` is the id

stopping a container, with name<br >
`$  docker container stop trusting_booth`<br >
here, `trusting_booth` is the name

see the list of all containers<br >
`$  docker container ls -a`

completely removing the container<br>
`$ docker container rm optimistic_galileo` 

giving a custom name to a container<br>
`$ docker container run -d --name web jboss/wildfly`<br >
here, `web` is the custom name

overriding the default command of the container<br >
`$ docker container run  -it --name web jboss/wildfly bash`<br >
here, `bash` is the command that is overrding the default command and we are running the container in interactive mode using `-it` command

see the logs of a container<br >
`$ docker container logs web`

exit from a container<br >
`$ exit`

exposing the container to a port<br >
`$ docker container run -d --name web -p jboss/wildfly`

exposing the container to a custom port<br >
`$ docker container run -d --name web -p 8080:8080 jboss/wildfly`<br >
here, `8080:8080` means, map the container `8080` port to the host `8080`

restarting the docker environment<br >
`$ docker-machine restart default`

packaging a spring boot app
1. Go to the directory where the `pom.xml` file is
2. run `$ mvn package` 

running a spring boot app<br >
`$ mvn spring-boot:run`



refresh the environment<br >
`$ docker-machine env`








