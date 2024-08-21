# Trabajo Practico 1 - git Basico

## 2- Crear un repositorio local y agregar archivos

#### - Crear un repositorio local en un nuevo directorio

#### - Agregar un archivo Readme.md, agregar algunas líneas con texto a dicho archivo

![Captura](imagenes/ej-2-1.png)

![Captura](imagenes/ej-2-2.png)

#### - Crear un commit y proveer un mensaje descriptivo

![Captura](imagenes/ej-2-3.png)

## 4- Creación de Repos 01 -> Crearlo en GitHub, clonarlo localmente y subir cambios

#### - Crear un nuevo repositorio en dicha página con el Readme.md por defecto

![Captura](imagenes/ej-4-1.png)

#### - Clonar el repo remoto en un nuevo directorio local

#### - Editar archivo Readme.md agregando algunas lineas de texto

![Captura](imagenes/ej-4-2.png)
![Captura](imagenes/ej-4-3.png)
![Captura](imagenes/ej-4-4.png)

#### - Editar (o crear si no existe) el archivo .gitignore agregando los archivos *.bak

![Captura](imagenes/ej-4-5.png)

#### - Crear un commit y porveer un mensaje descriptivo

#### - Intentar un push al repo remoto

#### - En caso de ser necesario configurar las claves SSH requeridas y reintentar el push

![Captura](imagenes/ej-4-6.png)

## 5- Creación de Repos 02-> Crearlo localmente y subirlo a GitHub

#### - Crear un repo local

#### - Agregar archivo Readme.md con algunas lineas de texto

![Captura](imagenes/ej-5-2.png)

#### - Crear repo remoto en GitHub

![Captura](imagenes/ej-5-1.png)

#### - Asociar repo local con remoto

![Captura](imagenes/ej-5-3.png)

#### - Crear archivo .gitignore

#### - Crear un commit y proveer un mensaje descriptivo

#### - Subir cambios

![Captura](imagenes/ej-5-4.png)

![Captura](imagenes/ej-5-5.png)

## 6- Ramas

#### - Crear una nueva rama

#### - Cambiarse a esa rama

![Captura](imagenes/ej-6-1.png)

#### - Hacer un cambio en el archivo Readme.md y hacer commit

![Captura](imagenes/ej-6-2.png)

#### - Revisar la diferencia entre ramas

![Captura](imagenes/ej-6-3.png)

## 7- Merges

#### - Hacer un merge FF

![Captura](imagenes/ej-7-1.png)

#### - Borrar la rama creada

#### - Ver el log de commits

![Captura](imagenes/ej-7-2.png)

#### - Repetir el ejercicio 6 para poder hacer un merge con No-FF

- Me confundi, asi que hice merge con la main, es lo mismo el ejercicio. 

![Captura](imagenes/ej-7-7.png)

## 8- Resolución de Conflictos

#### - Crear una nueva rama conflictBranch

#### - Realizar una modificación en la linea 1 del Readme

#### - En la conflictBranch modificar la misma línea del Readme.md y commitear

![Captura](imagenes/ej-8-3.png)

#### - Ver las diferencias con git difftool main conflictBranch

![Captura](imagenes/ej-8-1.png)

#### - Cambiarse a la rama main e intentar mergear con la rama conflictBranch

#### - Resolver el conflicto con git mergetool

- Elegi quedarme con el cambio actual

![Captura](imagenes/ej-8-2.png)

#### - Agregar .orig al .gitignore

#### - Hacer commit y push

![Captura](imagenes/ej-8-4.png)

## 9- Familiarizarse con el concepto de Pull Request

#### - Explicar que es un pull request

- Un pull request es una solicitud que un desarrollador hace para que los cambios que ha hecho en su rama de trabajo (generalmente en un repositorio de Git) sean revisados e integrados en la rama principal (o cualquier otra rama).

#### - Crear un branch local y agregar cambios a dicho branch

![Captura](imagenes/ej-9-1.png)
![Captura](imagenes/ej-9-3.png)

#### - Subir el cambio a dicho branch y crear un pull request

![Captura](imagenes/ej-9-2.png)

#### - Completar el proceso de revisión en github y mergear el PR al branch master

![Captura](imagenes/ej-9-4.png)

![Captura](imagenes/ej-9-7.png)

![Captura](imagenes/ej-9-5.png)

![Captura](imagenes/ej-9-6.png)
