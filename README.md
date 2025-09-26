# API Testing - Librería de recetas

En este repositorio se encuentran los archivos necesarios para ejecutar una batería de pruebas funcionales que tienen como fin validar los endpoints de la API que desarrollé: [Librería de recetas](https://github.com/Pablomartin20/recipelibrary).

## Contenido

- 'RecipesAPI.postman_collection.json' → Colección de requests y tests automatizados.
- 'RecipesAPIEnvironment.postman_environment.json' → Variables de entorno requeridas.

## Requisitos para la ejecución de las pruebas

- El proyecto de la API instalado y el servidor en ejecución.
- [Node.js](https://nodejs.org/) instalado, en caso de que necesites instalar Newman y el Reporter.
- [Newman](https://www.npmjs.com/package/newman) instalado globalmente:
  
    ```bash
    npm install -g newman
    
- (Opcional) Reporter HTML Extra para generar reportes en HTML:
  
    ```bash
    npm install -g newman-reporter-htmlextra

## Ejecución

### Sin reporte HTML

    newman run RecipesAPI.postman_collection.json -e RecipesAPIEnvironment.postman_environment.json

### Con reporte HTML

    newman run RecipesAPI.postman_collection.json -e RecipesAPIEnvironment.postman_environment.json -r htmlextra --reporter-htmlextra-export reports/report.html
