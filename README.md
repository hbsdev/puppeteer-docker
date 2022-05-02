# puppeteer-docker
Docker container to render PDF files using puppeteer

## Build the Docker image
```
docker build . -t openitcockpit/puppeteer -f Dockerfile
```

## Run Container (for developments)
```
docker run --rm -it --init -p 8084:8084 openitcockpit/puppeteer /bin/bash
```

## curl Test command
```
curl -X POST -H "Content-Type: text/plain" --data "<\!DOCTYPE html><html><head><title>PDF test</title></head><body><p>It works!</p></body></html>" http://127.0.0.1:8084/pdf --output result.pdf
```


docker run --rm -it --init -p 8084:8084 -v /opt/openitc/frontend/webroot:/opt/openitc/frontend/webroot:ro  openitcockpit/puppeteer /bin/bash


https://stackoverflow.com/questions/47587352/opening-local-html-file-using-puppeteer

