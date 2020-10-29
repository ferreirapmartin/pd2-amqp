# Programación Distribuida II - RabbitMQ

## Creando imagen y contenedores

Para crear la imagen, se debe ejecutar:

```sh
docker-compose build
```

Una vez creada la imagen de la API, para crear los contenedores (de la base de datos y de la API), es necesario ejecutar:

```sh
docker-compose up
```

## Iniciando o deteniendo los contenedores

Una vez que los contenedores están creados, se puede detener la ejecución de ambos, con:

```sh
docker-compose stop
```
Y volver a iniciarlas con

```sh
docker-compose start
```