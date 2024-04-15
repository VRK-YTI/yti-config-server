# Pull base image
FROM yti-docker-java11-base:alpine

# Deploy project
ADD target/yti-config-server.jar ${deploy_dir}/yti-config-server.jar

RUN bash -c 'touch ${deploy_dir}/yti-config-server.jar'

# Port exposure
EXPOSE 8888

# Set default command on run
ENTRYPOINT ["/bootstrap.sh", "yti-config-server.jar"]
