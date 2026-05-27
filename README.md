# DevOps Backend Ventas - Innovatech Chile

## Descripción

Este repositorio contiene el microservicio Backend de Ventas del proyecto Innovatech Chile.

El servicio fue desarrollado con Spring Boot y Java 17. Se encuentra contenedorizado mediante Docker y se despliega en una instancia EC2 privada de AWS. Además, utiliza una base de datos MySQL ejecutada en contenedor, con persistencia mediante volúmenes Docker.

## Tecnologías utilizadas

- Java 17
- Spring Boot
- Maven
- Spring Data JPA
- MySQL
- Docker
- Docker Compose
- GitHub Actions
- Docker Hub
- AWS EC2

## Arquitectura del servicio

El microservicio de ventas se ejecuta en la instancia Backend privada. No se expone directamente a Internet.

La comunicación se realiza desde la instancia Frontend pública hacia el Backend privado mediante la red interna de AWS.

```text
EC2 Frontend pública
        |
        v
EC2 Backend privada
        |
        ├── back-ventas-app
        └── mysql-ventas
