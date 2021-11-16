## Docker Compose Mongo e Mongo Express

```sh
## Criando o docker-compose.yml
version: '3.1'

services:
  mongo:
    image: mongo
    restart: always
    environment:
      MONGO_INITDB_ROOT_USERNAME: root
      MONGO_INITDB_ROOT_PASSWORD: MongoDB@2021!

  mongo-express:
    image: mongo-express
    restart: always
    ports:
      - 8081:8081
    environment:
      ME_CONFIG_MONGODB_ADMINUSERNAME: root
      ME_CONFIG_MONGODB_ADMINPASSWORD: MongoDB@2021!
      ME_CONFIG_MONGODB_URL: mongodb://root:example@mongo:27017/
```

```sh
## Comando para executar docker-compose.yml
docker-compose -f docker-compose.yml up

## Outros comandos
docker-compose help
docker-compose build
docker-compose up
```

## Mongo Express

[LocalHost:8081](http://localhost:8081)

- User: root
- Password: MongoDB@2021!
