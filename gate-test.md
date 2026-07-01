# Gate prueba de bloqueo 

## Prueba de bloqueo

El proyecto de cita medicos tiene 3 entrevistas. Para realizar la prueba se va a proceder a eliminar el archivo de la entrevista del médico, el cual es una persona principal del sistema. El hook readiness-gate debería bloquear la ejecución del comando.

![alt text](./images/captura1.png) ![alt text](./images/captura2.png)

Ahora se procede a correr el comando generate-mvp.

![alt text](./images/comando1.png)

El archivo readiness-gate detecta que el archivo de entrevista de medico.md no existe y no permite continuar con el siguiente paso para generar el MVP. Además, el modelo llega a detectar que el archivo fue eliminado en el historial de git.

![alt text](./images/bloqueo.png)

## Prueba luego de restaurar el archivo

![alt text](./images/interviews.png)

 Se procede a correr nuevamente el comando generate-mvp

 ![alt text](./images/comando2.png)

 Esta vez el gate verifica que los archivos necesarios para generar el mvp existen.

 ![alt text](./images/PastedGraphic6.png)

 Finalmente los artefactos son generados con éxito.

 ![alt text](./images/PastedGraphic7.png)