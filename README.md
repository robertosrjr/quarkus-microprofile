# [Microprofile Project](https://quarkus.io/blog/quarkus-eclipse-microprofile-3-3/)

This project uses Quarkus, the Supersonic Subatomic Java Framework.

If you want to learn more about Quarkus, please visit its website: https://quarkus.io/ .

O MicroProfile é uma definição de plataforma de linha de base que otimiza Enterprise Java para uma arquitetura de microsserviços e oferece portabilidade de aplicativo em vários tempos de execução MicroProfile . ... Java EE criou um conjunto de especificações definidas primeiro pela Sun Microsystems e depois pela Oracle por meio do Java Community. (https://www.tomitribe.com/blog/what-is-eclipse-microprofile/)

## FAULT TOLERANCE
### [SMALLRYE FAULT TOLERANCE](https://quarkus.io/guides/smallrye-fault-tolerance)
- quarkus-smallrye-fault-tolerance
  - resteasy
  - smallrye-fault-tolerance
  - resteasy-jackson

## HEALTH
### [SMALLRYE HEALTH](https://quarkus.io/guides/smallrye-health)
- quarkus-smallrye-health
  - smallrye-health

## METRICS
### [MICROMETER METRICS](https://quarkus.io/guides/micrometer)
- quarkus-micrometer-registry-prometheus

### [SMALLRYE METRICS](https://quarkus.io/guides/smallrye-metrics)
- quarkus-smallrye-metrics
  - resteasy
  - smallrye-metrics

## REST CLIENT
### [REST CLIENT](https://quarkus.io/guides/rest-client)
- quarkus-rest-client
- quarkus-rest-client-jackson
  - resteasy
  - resteasy-jackson
  - rest-client
  - rest-client-jackson

Ref.:
https://quarkus.io/blog/quarkus-eclipse-microprofile-3-3/

## Running the application in dev mode

You can run your application in dev mode that enables live coding using:
```shell script
./mvnw compile quarkus:dev
```

> **_NOTE:_**  Quarkus now ships with a Dev UI, which is available in dev mode only at http://localhost:8080/q/dev/.

## Packaging and running the application

The application can be packaged using:
```shell script
./mvnw package
```
It produces the `quarkus-run.jar` file in the `target/quarkus-app/` directory.
Be aware that it’s not an _über-jar_ as the dependencies are copied into the `target/quarkus-app/lib/` directory.

If you want to build an _über-jar_, execute the following command:
```shell script
./mvnw package -Dquarkus.package.type=uber-jar
```

The application is now runnable using `java -jar target/quarkus-app/quarkus-run.jar`.

## Creating a native executable

You can create a native executable using: 
```shell script
./mvnw package -Pnative
```

Or, if you don't have GraalVM installed, you can run the native executable build in a container using: 
```shell script
./mvnw package -Pnative -Dquarkus.native.container-build=true
```

You can then execute your native executable with: `./target/microprofile-1.0.0-SNAPSHOT-runner`

If you want to learn more about building native executables, please consult https://quarkus.io/guides/maven-tooling.html.

## Provided Code

### RESTEasy JAX-RS

Easily start your RESTful Web Services

[Related guide section...](https://quarkus.io/guides/getting-started#the-jax-rs-resources)
