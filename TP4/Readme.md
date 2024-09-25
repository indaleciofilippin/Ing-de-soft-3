## Trabajo Práctico 4 - Azure Devops Pipelines

### 2- Agregar en pipeline YAML una tarea de Publish

Se agrega en el pipeline una tarea de publish y se hace un commit de los cambios que automáticamente corre el pipeline nuevamente.
![Captura](imagenes/tp4-2-1.png)
![Captura](imagenes/tp4-2-2.png)
![Captura](imagenes/tp4-2-3.png)

### 3- Explicar por qué es necesario contar con una tarea de Publish en un pipeline que corre en un agente de Microsoft en la nube

- En un pipeline que corre en un agente de Microsoft en la nube, es necesario incluir una tarea de Publish para:

  - Persistencia de Artefactos: Los agentes de Microsoft-hosted son efímeros, lo que significa que los archivos generados durante la ejecución se perderían si no se publican. La tarea de Publish guarda estos artefactos en Azure DevOps, asegurando su disponibilidad para etapas posteriores.

  - Despliegues y Etapas Posteriores: Los artefactos publicados son necesarios para las fases de despliegue y otros usos posteriores, garantizando que el mismo código construido se despliegue de manera consistente.

  - Acceso y Trazabilidad: Publicar artefactos permite a los equipos revisar los resultados de construcción, pruebas y asegurar la trazabilidad para auditorías o cumplimiento normativo

### 4- Descargar el resultado del pipeline y correr localmente el software compilado

![Captura](imagenes/tp4-4-1.png)

Se modificó el archivo `SimpleWebApi.runtimeconfig.json` para que soporte la versión de dotnet instalada localmente.
![Captura](imagenes/tp4-4-2.png)
![Captura](imagenes/tp4-4-3.png)

Ingresando en [localhost:5000/weatherforecast](http://localhost:5000/weatherforecast) desde el dipositivo, se puede ver el resultado
![Captura](imagenes/tp4-4-4.png)

### 5- Habilitar el editor clásico de pipelines. Explicar las diferencias claves entre este tipo de editor y el editor YAML

![Captura](imagenes/tp4-5-1.png)

Habilito el editor clasico que estaba desabilitado.
![Captura](imagenes/tp4-5-2.png)

#### Diferencias entre editor clásico y YAML:

##### Editor Clásico:

- Es una interfaz gráfica basada en un asistente que permite a los usuarios configurar pipelines sin necesidad de escribir código.
- Ideal para usuarios que prefieren una experiencia de configuración más visual o que son nuevos en la integración y entrega continua.
- Permite crear y gestionar tareas y fases mediante una serie de menús desplegables y formularios.
- Aunque es más accesible para principiantes, puede ser menos flexible y más difícil de versionar y mantener en comparación con YAML.

##### Pipelines basados en YAML:

- Utilizan archivos YAML (YAML Ain't Markup Language) para definir los pipelines como código. Estos archivos se incluyen en el repositorio de código fuente, lo que facilita la gestión de versiones y la revisión de cambios.
- Ofrecen mayor flexibilidad y personalización, permitiendo a los usuarios definir pipelines complejos con condicionales, plantillas reutilizables y variables.
- Requieren conocimientos básicos de YAML y programación, pero proporcionan una mayor consistencia y transparencia en los procesos de CI/CD.
- Son la opción recomendada para proyectos con pipelines complejos o para equipos que siguen prácticas de DevOps maduras.

### 6- Crear un nuevo pipeline con el editor clásico. Descargar el resultado del pipeline y correr localmente el software compilado

![Captura](imagenes/tp4-6-1.png)

![Captura](imagenes/tp4-6-2.png)

![Captura](imagenes/tp4-6-3.png)

![Captura](imagenes/tp4-6-4.png)

![Captura](imagenes/tp4-6-5.png)

![Captura](imagenes/tp4-6-6.png)

![Captura](imagenes/tp4-6-7.png)

![Captura](imagenes/tp4-6-8.png)

### 7- Configurar CI en ambos pipelines (YAML y Classic Editor). Mostrar resultados de la ejecución automática de ambos pipelines al hacer un commit en la rama main

YALM:
![Captura](imagenes/tp4-7-1.png)

Classic:
![Captura](imagenes/tp4-7-2.png)

Modifico el Readme
![Captura](imagenes/tp4-7-3.png)

Hago el commit de los cambios
![Captura](imagenes/tp4-7-4.png)

Verifico que ambos pipelines se esten ejecutando
![Captura](imagenes/tp4-7-5.png)

### 8- Explicar la diferencia entre un agente MS y un agente Self-Hosted. Qué ventajas y desventajas hay entre ambos? Cuándo es conveniente y/o necesario usar un Self-Hosted Agent?

#### Diferencia entre un Agente MS y un Agente Self-Hosted:

##### Agente MS (Microsoft-hosted):

- Es un agente gestionado por Microsoft en la nube de Azure. Está preconfigurado con un entorno estándar, y se utiliza por demanda. Es efímero, es decir, se crea para cada ejecución del pipeline y se elimina al finalizar.

##### Agente Self-Hosted:

- Es un agente configurado y mantenido por el usuario en su infraestructura local o en la nube. El usuario tiene control total sobre el entorno y los recursos del agente.

#### Ventajas y Desventajas:

##### Agente MS:

- Ventajas: Fácil de usar, no requiere configuración ni mantenimiento por parte del usuario, ideal para proyectos estándar.
- Desventajas: Menos control sobre el entorno, limitado a las configuraciones y herramientas preinstaladas, costos por tiempo de uso.

##### Agente Self-Hosted:

- Ventajas: Control total sobre el entorno y las herramientas, no tiene costos por tiempo de uso, ideal para necesidades específicas o software propietario.
- Desventajas: Requiere configuración, mantenimiento y administración del usuario, necesita recursos propios de infraestructura.

##### Cuándo usar un Agente Self-Hosted:

Es conveniente usar un Agente Self-Hosted cuando necesitas configuraciones personalizadas, acceso a recursos locales, usar software propietario o específico, o cuando se requiere un mayor control y optimización del entorno de ejecución.

### 9- Crear un Pool de Agentes y un Agente Self-Hosted

![Captura](imagenes/tp4-9-1.png)
![Captura](imagenes/tp4-9-2.png)
![Captura](imagenes/tp4-9-3.png)

### 10- Instalar y correr un agente en nuestra máquina local

![Captura](imagenes/tp4-10-1.png)
![Captura](imagenes/tp4-10-2.png)
![Captura](imagenes/tp4-10-3.png)
![Captura](imagenes/tp4-10-4.png)
![Captura](imagenes/tp4-10-5.png)
![Captura](imagenes/tp4-10-6.png)
![Captura](imagenes/tp4-10-7.png)

### 11- Crear un pipeline que use el agente Self-Hosted alojado en nuestra máquina local

![Captura](imagenes/tp4-11-1.png)
![Captura](imagenes/tp4-11-2.png)
![Captura](imagenes/tp4-11-3.png)
![Captura](imagenes/tp4-11-4.png)
![Captura](imagenes/tp4-11-5.png)

### 12- Buscar el resultado del pipeline y correr localmente el software compilado

![Captura](imagenes/tp4-12-1.png)
![Captura](imagenes/tp4-12-2.png)

### 13- Crear un nuevo proyecto en ADO clonado desde un repo que contenga una aplicación en Angular como por ejemplo <https://github.com/ingsoft3ucc/angular-demo-project.git>

![Captura](imagenes/tp4-13-1.png)
![Captura](imagenes/tp4-13-2.png)
![Captura](imagenes/tp4-13-3.png)

### 14- Configurar un pipeline de build para un proyecto de tipo Angular como el clonado

![Captura](imagenes/tp4-14-1.png)
![Captura](imagenes/tp4-14-2.png)
![Captura](imagenes/tp4-14-3.png)
![Captura](imagenes/tp4-14-4.png)

### 15- Habilitar CI para el pipeline

Ya se encuentra habilitado por defecto
![Captura](imagenes/tp4-15-1.png)

### 16- Hacer un cambio a un archivo del proyecto (algún cambio en el HTML que se renderiza por ejemplo) y verificar que se ejecute automáticamente el pipeline

Verifico que no haya ningun pipeline corriendo
![Captura](imagenes/tp4-16-1.png)

Relaizo un cambio en el footer de la pagina
![Captura](imagenes/tp4-16-2.png)
![Captura](imagenes/tp4-16-3.png)

Verifico que el pipeline este corriendo
![Captura](imagenes/tp4-16-4.png)

### 17- Descargar el resultado del pipeline y correr en un servidor web local el sitio construido

Descargo los Artifacts del primer pipeline y el del pipeline con CI.
![Captura](imagenes/tp4-17-1.png)

### 18- Mostrar el antes y el después del cambio

Primero del pipeline sin modificar
![Captura](imagenes/tp-18-1.png)
![Captura](imagenes/tp-18-2.png)

Aqui deberia estar la modificacion en el otro pipeline
![Captura](imagenes/tp-18-3.png)

Ahora el pipeline con la modificacion
![Captura](imagenes/tp-18-4.png)
![Captura](imagenes/tp-18-5.png)

Aqui esta la modificacion
![Captura](imagenes/tp-18-6.png)
