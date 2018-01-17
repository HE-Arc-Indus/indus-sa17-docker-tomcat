# indus-sa17-docker-tomcat
simple example for docker + tomcat deployment

## Approche 1: fichier war dans le container

build docker image
```bash
docker build -t tomcatserver1 .
```

run docker container:
```bash
 docker run -it --rm -p 8080:8080 --name user-reg1 tomcatserver1
```

Tester: http://localhost:8080/user-registration-application-0.0.1-SNAPSHOT/


## Approche 2: montage du dossier dist sur le container.

build docker image
```bash
docker build -t tomcatserver2 .
```

run docker container:

On va monter le dossier `dist` sur le dossier de déploiement tomcat du container.
Remplacez le path par celui sur votre machine.

```bash
docker run -it --rm -p 9090:8080 -v C:\temp\docker\tomcat\indus-sa17-docker-tomcat\approche2\dist:/usr/local/tomcat/webapps/ --name user-reg2 tomcatserver2
```

Tester: http://localhost:9090/user-registration-application-0.0.1-SNAPSHOT/


## HelloWorld simple avec java

dossier jarhelloworld

build docker image
```bash
docker build -t javahello .
```

run
```bash
docker run javahello
```
