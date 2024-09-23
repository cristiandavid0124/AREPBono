# Bono Arep

## Autor : Cristian David Naranjo Orjuela

## Instalación y Ejecución

1. Clonar el repositorio.
 ```
https://github.com/cristiandavid0124/AREPBono.git
  ```
2. Compilar usando maven
 ```
mvn clean install
  ```  

3.  ejecuta el codigo en terminales separadas 

 ```
mvn exec:java -Pserver
 ```

```
mvn exec:java -Pfachada
```

 ## Arquitectura

### CalcreflexBEFachada
Actúa como el servidor principal que escucha en el puerto 35000.
Acepta conexiones de clientes y maneja solicitudes de computación y de página HTML.
Tiene métodos para generar respuestas HTML y manejar las solicitudes recibidas.

### HttpConnection:
Es la encargada de conectar la fachada con el backend de la calculadora mediante solicitud HTTP GET al servicio en el puerto 36000.
Establece la conexión, envía la solicitud y recibe la respuesta del servidor.

### CalcreflexBEServer:
Es otro servidor que escucha en el puerto 36000 y maneja las solicitudes de computación.
Utiliza la reflexión para invocar métodos de la clase Math y ejecutar operaciones matemáticas basadas en las solicitudes.
Responde a las solicitudes con resultados en formato JSON.


## Pruebas De Funcionamiento
* bbl(19.0,7.8,10.0,11.9)

  ![image](https://github.com/user-attachments/assets/6ff3b75d-f030-4cc1-a9f5-ec3b5033c616)



* max(10.0,4.1)

![image](https://github.com/user-attachments/assets/b38f37d2-1cf1-4182-95ac-9b5fc663371d)



* sqrt(16)

  ![image](https://github.com/user-attachments/assets/e4b84a2a-fd35-44e2-938f-5c8437b00685)




