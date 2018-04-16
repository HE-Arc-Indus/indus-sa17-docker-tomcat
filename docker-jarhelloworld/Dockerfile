# Pull base image
FROM openjdk:slim

# Maintainer
MAINTAINER "Ulysse Rosselet <ulysse.rosselet@he-arc.ch">

# Copy to container
ADD HelloWorld.jar /usr/local/

# Run Jar file when container launches
CMD java -jar /usr/local/HelloWorld.jar

# Running the container
# docker run javadocker