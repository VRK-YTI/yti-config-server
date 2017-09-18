# Pull base image
FROM cls-docker-java-base:alpine

# Deploy project
ADD target/yti-config-server.jar ${deploy_dir}/yti-config-server.jar


RUN bash -c 'touch ${deploy_dir}/yti-config-server.jar'

# Port exposure
EXPOSE 8888

# Set default command on run
ENTRYPOINT ["java","-Djava.security.egd=file:/dev/./urandom","-jar","yti-config-server.jar"]
