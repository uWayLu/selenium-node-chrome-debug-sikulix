# Selenium Docker with Sikulix2

The project is made possible by volunteer contributors who have put in thousands of hours of their own time, and made the source code freely available under the [Apache License 2.0](/LICENSE.md).

## Info

The [Dockerfile](/Dockerfile) is based on [selenium/node-chrome-debug](https://github.com/SeleniumHQ/docker-selenium/tree/master/NodeChromeDebug). You may execute the container with selenuium-hub together via `docker-compose`.

You can more detail from [SeleniumHQ/docker-selenium](https://github.com/SeleniumHQ/docker-selenium)

## How to get image

+ `docker pull uwaylu/node-chrome-debug-sikulix:latest`
+ build your self via `docker build $PATH`

## Use example

```bash
# up container
c_id=$(docker run -d -p 5900:5900 uwaylu/node-chrome-debug-sikulix:latest)
# with tiger-vnc client
vncviewer 127.0.0.1:5900 &> /dev/null &
# if you need to up sikulixIDE
docker exec $c_id sikulix -v
# enter into container
docker exec -it $c_id bash
```
