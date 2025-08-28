# Welcome to the Cobol App Repository

### Build the image:
``` bash
docker build -t <image_name> /path/to/directory/dockerfile
docker build -t cobol-app .
```

### Run the image in container:
``` bash
docker run -d --name <container name> -p <host_port>:<docker_port> <image_name>
docker run -d --name cobol-container -p 8000:8000 -e COBOL_ARGS="--apply-interest" cobol-app
```

### Access the container's shell:
``` bash
docker exec -it <container-name or id> sh
docker exec -it cobol-container sh
```

### Run the main cobol program with flags:
``` bash
cobc -x -o main main.cob
./main --apply-interest
```

