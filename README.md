A simple todo list manager:
The app contains a simple the package.json and two subdirectories (src and spec).

# dockerized-app-tests
A GitHub project involving a dockerized application with Kubernetes and automation tests.

The Dockerfile will build the container image for the application.

Commands:
# docker version
# docker images
# docker run -d -p 80:80 docker/getting-started
# docker build -t getting-started - docker build command

Starting the App Container:
# docker run -dp 3000:3000 getting-started

You'll notice a few flags being used. Here's some more info on them:

-d - run the container in detached mode (in the background)
-p 80:80 - map port 80 of the host to port 80 in the container
docker/getting-started - the image to use

The docker dashboard gives access to container logs, lets us get a shell inside the container and allows us to easily manage container lifecycle (stop, remove, etc.).

A container is another process on your machine that has been isolated from all other processes on the host machine.

It uses an isolated filesystem. This custom filesystem is provided by a container image. Since the image contains the container's filesystem, it must include everything needed to run the application - all dependencies, configuration, scripts, binaries, etc.

A Dockerfile is simply a text-based script of instructions that is used to create a container image.

Finally, the -t flag tags our image. Think of this simply as a human-readable name for the final image. Since we named the image getting-started, we can refer to that image when we run a container.

The . at the end of the docker build command tells that Docker should look for the Dockerfile in the current directory.

comments:
We'll dive deeper into images later on, covering topics such as layering, best practices, and more.