<p align="center">
  <a href="http://nestjs.com/" target="blank"><img src="https://nestjs.com/img/logo-small.svg" width="200" alt="Nest Logo" /></a>
</p>

[circleci-image]: https://img.shields.io/circleci/build/github/nestjs/nest/master?token=abc123def456
[circleci-url]: https://circleci.com/gh/nestjs/nest

  <!--[![Backers on Open Collective](https://opencollective.com/nest/backers/badge.svg)](https://opencollective.com/nest#backer)
  [![Sponsors on Open Collective](https://opencollective.com/nest/sponsors/badge.svg)](https://opencollective.com/nest#sponsor)-->

# Ejecutar en desarrollo

1. Clonar el repositorio
2. Ejecutar
```
yarn install
```

3. Tener Next CLI instalado
```
npm i -g @nestjs/cli
```

4. Levantar Base de datos
```
docker-compose up -d
```

5. Clonar el archivo __.env.templete__ y renombre la copia a __.env__

6. Llenar variable de entorno definidas en el __.env__

7. Ejecutar la aplicación en dev:
```
yarn start_dev
```

8. Reconstruir la base de datos con la semilla
```
http://localhost:3000/api/v2/seed
```

# Stack Usado

1. MondoDB
2. NestJS

# Production Build

1. Crear el archivo ```.env.pro```
2. LLenar las variables de entorno
3. Crear la nueva imagen
```
docker-compose -f docker-compose.prod.yaml --env-file .env.prod up --build
```

# Nota
1. Para levantar el Contenedor nuevamente
```
docker-compose -f docker-compose.prod.yaml --env-file .env.prod up
```

2. Por defecto, docker-compose usa el archivo __.env__, por lo que si tienen el archivo __.env__ y lo configuran con sus variables de entorno de producción, bastaría con
```
docker-compose -f docker-compose.prod.yaml up --build
```