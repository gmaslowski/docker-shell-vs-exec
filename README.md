DSVE
====

Docker image build command:
```
./gradlew clean build
cp build/libs/docker-shell-vs-exec-0.0.1-SNAPSHOT.jar docker-shell/app.jar
cp build/libs/docker-shell-vs-exec-0.0.1-SNAPSHOT.jar docker-exec/app.jar
docker build --build-arg JAR_FILE=build/libs/docker-shell-vs-exec-0.0.1-SNAPSHOT.jar docker-exec -t dsve:exec
docker build --build-arg JAR_FILE=build/libs/docker-shell-vs-exec-0.0.1-SNAPSHOT.jar docker-shell -t dsve:shell
```

Deploy:
```
docker-compose -f deployment/docker-compose.yml up -d
```
