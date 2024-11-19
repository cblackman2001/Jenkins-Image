FROM jenkins/jenkins:lts

USER root
RUN apt-get update && apt-get install -Y git curl sudo
USER jenkins
RUN jenkins-plugins-cli --plugins "blueocean workflow-aggregator"