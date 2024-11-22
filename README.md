# Jenkins-Image

Docker-compose up --build -d
-----------

docker exec jenkins-custom cat /var/jenkins_home/secrets/initialAdminPassword

-----------

curl -O http://localhost:8080/jnlpJars/jenkins-cli.jar
java -jar jenkins-cli.jar -s http://localhost:8080/ who-am-i
java -jar jenkins-cli.jar -s http://localhost:8080/ get-agent-secret <AGENT_NAME>
docker exec -it jenkins-agent java -jar /usr/share/jenkins/agent.jar \
    -jnlpUrl http://jenkins-master:8080/computer/<AGENT_NAME>/jenkins-agent.jnlp \
    -secret <AGENT_SECRET>
------------

docker-compose down -v