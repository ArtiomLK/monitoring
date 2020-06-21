## Available Scripts

In the project directory, you can run:

### Docker:

#### Create a docker image

`docker build -t {DOCKER_IMAGE_NAME}:{TAG} -f {FILE_NAME} .`

For example:

`docker build -t monitoring:dev -f dev.dockerfile .`
`docker build -t monitoring:prod -f prod.dockerfile .`

#### Run our image

`docker run -itd --rm -v ${PWD}:/app -v /app/node_modules -p 3001:3000 -e CHOKIDAR_USEPOLLING=true {DOCKER_IMAGE_NAME}:{TAG}`

For example:

`docker run -itd --rm -v ${PWD}:/app -v /app/node_modules -p 3001:3000 -e CHOKIDAR_USEPOLLING=true monitoring:dev`

`docker run -itd -p 1337:80 --rm monitoring:prod`

## Learn More

[Common Docker Commands](https://github.com/ArtiomLK/kubernetes/blob/master/Docker.md)

[Common Kubernetes Commands](https://github.com/ArtiomLK/kubernetes)
