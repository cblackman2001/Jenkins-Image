FROM jenkins/jenkins:lts

USER root
RUN apt-get update && apt-get install -y git curl sudo
USER jenkins
RUN jenkins-plugin-cli --plugins "blueocean workflow-aggregator"