FROM dpatriot/docker-awscli-java8
COPY build/libs/registration-server.jar app.jar
ADD https://raw.githubusercontent.com/vishnubob/wait-for-it/master/wait-for-it.sh wait-for-it.sh

ENTRYPOINT "echo 'Hello' && sleep 300 && echo 'World' && java -jar app.jar"
EXPOSE 8083
