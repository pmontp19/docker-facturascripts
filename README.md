# docker-facturascripts
FacturaScripts unofficial Docker image. Forked the original FacturaScripts to work with ARMv7 architecture (aka Raspberry Pi). It uses a fork of Mariadb and entrypoint script is also adapted. I also changed exposed port to 8001 for my purposes. Target FS version is 2020.61, upgrade it in the Dockerfile.

## Run
Run the container.
```
$ docker run -d --name facturascripts -p 8001:80 facturascripts:latest
```

Run the FS container with database.
```
$ docker-compose up -d
```

## Build the image
You can get the source file and build the image.
```
$ git clone https://github.com/pmontp19/docker-facturascripts.git
$ cd docker-facturascripts
$ docker build -t facturascripts:latest .
```
