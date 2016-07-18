Install Docker:

$ sudo apt-get install docker.io

Adjust group for current user:

$ sudo usermod -a -G docker <username>

Logout and login to update group information.

Build docker container:

$ docker build [--no-cache=true] -t "contiki:dockerfile" .

Start docker container:

$ docker run -p 60001:60001 -ti --rm -e DISPLAY=$DISPLAY -v /tmp/.X11-unix:/tmp/.X11-unix dockerfile
