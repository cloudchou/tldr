# docker

> Manage Docker containers and images.

- Run web image:

`docker run -t -i --rm -p 80:80  -v (pwd):/data/work --name frontend -w /data/work  front-end:latest    /bin/bash`

- List currently running docker containers:

`docker container ls`

- List all docker containers (running and stopped):

`docker container ls -a`

- Start a container:

`docker container start {{container}}`

- Stop a container:

`docker container stop {{container}}`

- Start a container from an image and get a shell inside of it:

`docker container run -it {{image}} bash`

- Run a command inside of an already running container:

`docker container exec {{container}} {{command}}`

- Remove a stopped container:

`docker container rm {{container}}`

- Fetch and follow the logs of a container:

`docker container logs -f {{container}}`
