## Preguntas

### 1. Diferencia entre push y workflow

Push dispara el flujo de trabajo automáticamente cada vez que subes cambios de código (commits o etiquetas)
a una rama del repositorio. Workflow_dispatch permite ejecutarlo manualmente bajo demanda desde la interfaz
web o API de GitHub, ofreciendo la posibilidad de elegir la rama e introducir parámetros personalizados (inputs)
antes de lanzarlo.

### 2. Significado exit 1

exit 1 indica que el comando ha cometido un error.

### 3. Que he añadido en la parte 4 en la nueva rama

service: 'tasks-api'


### 4. ¿En qué se diferencia un push en tu rama de fusionar a main? ¿Por qué es mejor evitar los cambios directos en producción?

Un push sube los cambios a tu propia rama sin modificar main, mientras que un merge incorpora esos cambios a la rama principal.

Es mejor evitar cambios directos en producción porque pueden
introducir errores; las Pull Requests permiten revisar el código y ejecutar pruebas antes de integrarlo.


### 5. ¿Por qué las unitarias pueden pasar si SQL está roto?

Porque normalmente utilizan mocks que simulan el repositorio y no ejecutan las consultas SQL reales contra la base de datos.


### 6. ¿Cuándo merece la pena ejecutar un job más lento después de los tests rápidos?

Cuando necesitamos comprobar integraciones reales, como consultas SQL o conexiones a bases de datos, evitando gastar tiempo y recursos
si los tests rápidos ya han detectado errores.


