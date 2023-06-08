## These lines of code represent the image we're going to use along with copying the contents of the current directory into the container.
FROM nginx:alpine
COPY . /usr/share/nginx/html

## Build the Docker Image for the HTML Server
docker build -t html-server-image:v1

docker run -d -p 80:80 html-server-image:v1