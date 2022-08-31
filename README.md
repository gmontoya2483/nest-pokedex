<p align="center">
  <a href="http://nestjs.com/" target="blank"><img src="https://nestjs.com/img/logo-small.svg" width="200" alt="Nest Logo" /></a>
</p>

# Pokedex

## Ejecutar en desarrollo

1. Clonar el repositorio
2. Ejecutar
    ```
    yarn install
    ```
    ó
    ```
    npm install
    ```
3. Tener Nest CLI instalado
    ```
    npm i -g @nestjs/cli
    ```
4. Levantar base de datos
    ```
    docker-compose up -d
    ```

5. Clonar el archivo __.env.template__ y renombrar la copia a __.env__
6. Llenar las variables de entorno definidas en __.env__
7. Ejecutat la aplicacion en dev:
    ```
    yarn start:dev
    ```
8. Reconstruir la base de datos ocn la semilla
    ```
    http://localhost:3000/api/v2/seed
    ```

## Stack usado
* MongoDB
* Nest
* Express


## Production Build
1. crear el archivo ```.env.prod```
2. llenar las variables de entorno para producción
3. Crear la nueva imagen

   ```
   docker-compose -f docker-compose.prod.yaml --env-file .env.prod up --build
   ```

## Ejecutar Prod:
   ```
   docker-compose -f docker-compose.prod.yaml --env-file .env.prod up
   ```


## Notas
Heroku redeploy sin cambios:
```
git commit --allow-empty -m "Trigger Heroku deploy"
git push heroku <main | main>
```
