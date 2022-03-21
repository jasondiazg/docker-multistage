# docker-multistage
A demo project to show a multistage dockerfile.

## Java App

You can see a hello world app in the folder `multistage-demo-java`. This project contains a [Dockerfile](./multistage-demo-java/Dockerfile) where you can see a multi-stage docker build.

### Local test

If you want to check the application running in your local, execute:

```bash
$ cd multistage-demo-java && mvn package clean && java -jar target/multistage-demo-java-1.0.jar
```

Notice that you need to have Maven and the JDK installed in your computer.

### Docker test

If you want to check/test the application with docker, execute:

```bash
$ cd multistage-demo-java && docker build . -t multistage-java && docker run multistage-java
```

## NodeJS App

You can see a hello world app in the folder `multistage-demo-node`. This project contains a [Dockerfile](./multistage-demo-node/Dockerfile) where you can see a multi-stage docker build.

### Local test

If you want to check the application running in your local, execute:

```bash
$ cd multistage-demo-node && npm install && npm start
```

Notice that you need to have NodeJS/npm installed in your computer.

### Docker test

If you want to check/test the application with docker, execute:

```bash
$ cd multistage-demo-node && docker build . -t multistage-node && docker run multistage-node
```