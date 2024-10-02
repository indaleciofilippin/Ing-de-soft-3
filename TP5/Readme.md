# Trabajo Práctico 5 - Despliegue de aplicaciones con Azure Devops Release Pipelines

## 1\. Crear una cuenta en Azure

## 2\. Crear un recurso Web App en Azure Portal y navegar a la url provista

![Captura](imagenes/tp5-1-1.png)
![Captura](imagenes/tp5-1-2.png)
![Captura](imagenes/tp5-1-3.png)
![Captura](imagenes/tp5-1-4.png)
![Captura](imagenes/tp5-1-5.png)
![Captura](imagenes/tp5-1-6.png)

## 3\. Actualizar Pipeline de Build para que use tareas de DotNetCoreCLI@2 como en el pipeline clásico, luego crear un Pipeline de Release en Azure DevOps con CD habilitada

![Captura](imagenes/tp5-3-1.png)
![Captura](imagenes/tp5-3-2.png)
![Captura](imagenes/tp5-3-3.png)
![Captura](imagenes/tp5-3-4.png)

## 4\. Optimizar Pipeline de Build

![Captura](imagenes/tp5-4-1.png)

## 5\. Verificar el deploy en la url de la WebApp /weatherforecast

Se modifico la version de .NET para que el deploy se realice correctamente.
![Captura](imagenes/tp5-5-1.png)
![Captura](imagenes/tp5-5-2.png)
![Captura](imagenes/tp5-5-3.png)
![Captura](imagenes/tp5-5-4.png)

## 6\. Realizar un cambio al código del controlador para que devuelva 7 pronósticos, realizar commit, evaluar ejecución de pipelines de build y release, navegar a la url de la webapp/weatherforecast y corroborar cambio

![Captura](imagenes/tp5-6-1.png)
![Captura](imagenes/tp5-6-2.png)
![Captura](imagenes/tp5-6-3.png)
![Captura](imagenes/tp5-6-4.png)
![Captura](imagenes/tp5-6-5.png)

## 7\. Clonar la Web App de QA para que contar con una WebApp de PROD a partir de un Template Deployment en Azure Portal y navegar a la url provista para la WebApp de PROD.

![Captura](imagenes/tp5-7-1.png)
![Captura](imagenes/tp5-7-2.png)
![Captura](imagenes/tp5-7-3.png)
![Captura](imagenes/tp5-7-4.png)
![Captura](imagenes/tp5-7-5.png)
![Captura](imagenes/tp5-7-6.png)
![Captura](imagenes/tp5-7-8.png)
![Captura](imagenes/tp5-7-9.png)

## 8\. Agregar una etapa de Deploy a Prod en Azure Release Pipelines

![Captura](imagenes/tp5-8-1.png)
![Captura](imagenes/tp5-8-2.png)
![Captura](imagenes/tp5-8-3.png)

## 9\.  Realizar un cambio al código del controlador para que devuelva 10 pronósticos, realizar commit, evaluar ejecución de pipelines de build y release, navegar a la url de la webapp/weatherforecast y corroborar cambio, verificar que en la url de la webapp_prod/weatherforecast se muestra lo mismo.

![Captura](imagenes/tp5-9-1.png)
![Captura](imagenes/tp5-9-2.png)
![Captura](imagenes/tp5-9-3.png)
![Captura](imagenes/tp5-9-4.png)

- QA
![Captura](imagenes/tp5-9-6.png)

- Produccion
![Captura](imagenes/tp5-9-5.png)

## 10\. Modificar pipeline de release para colocar una aprobación manual para el paso a Producción.

![Captura](imagenes/tp5-10-1.png)

## 11\. Realizar un cambio al código del controlador para que devuelva 5 pronósticos, realizar commit, evaluar ejecución de pipelines de build y release, navegar a la url de la webapp/weatherforecast y corroborar cambio, verificar que en la url de la webapp_prod/weatherforecast aun se muestra la versión anterior.

![Captura](imagenes/tp5-11-1.png)
![Captura](imagenes/tp5-11-2.png)
![Captura](imagenes/tp5-11-3.png)

- Produccion
![Captura](imagenes/tp5-11-4.png)

- QA
![Captura](imagenes/tp5-11-5.png)

## 12\. Aprobar el pase ya sea desde el release o desde el mail recibido.

![Captura](imagenes/tp5-12-1.jpg)
![Captura](imagenes/tp5-12-2.png)
![Captura](imagenes/tp5-12-3.png)

## 13\. Esperar a la finalización de la etapa de Pase a Prod y luego corroborar que en la url de la webapp_prod/weatherforecast se muestra la nueva versión coinicidente con la de QA.

Una vez aprobado y finalizado el release, vamos a la url y vemos los cambios realizados.
![Captura](imagenes/tp5-13-1.png)

## 14\. Realizar un pipeline (no release) que incluya el deploy a QA y a PROD con una aprobación manual. El pipeline debe estar construido en YAML sin utilizar el editor clásico de pipelines ni el editor clásico de pipelines de release.

![Captura](imagenes/tp5-14-1.png)
![Captura](imagenes/tp5-14-2.png)

Antes de aprovar produccion:
![Captura](imagenes/tp5-14-3.png)

Se hizo un commit en donde el programa devuelve 8 pronosticos, a continuacion se muestra que antes de aprovar la produccion solo es visible en QA.
![Captura](imagenes/tp5-14-4.png)
![Captura](imagenes/tp5-14-5.png)

Luego continuamos con la aprovacion y vemos que es visible ahora tambien en Produccion.
![Captura](imagenes/tp5-14-6.png)
![Captura](imagenes/tp5-14-7.png)
