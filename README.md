# Actividad final trimestre 1:

```
git clone --recursive git@github.com:jkutkutorg/Cloud_Computing-Docker.git
```

## Contenedor en DockerHub:
El contenedor subido ha sido creado mediante la lógica que hay en [Docker4Java](./Docker4Java/)

### Funcionamiento:
Para ejecutar el contenedor se debe ejecutar el siguiente comando:
```bash
./Docke4Java/run.sh
```

Este se encargará de ejecutar la imagen (y descargarla si no está disponible).


Este contenedor permite ejecutar el proyecto [Java-Text_Analyzer](./Cloud_Computing-Docker/Docker4Java/Java-Text_Analyzer). Este te pedirá el nombre de un archivo en tu directorio actual y te lo analizará.

### Explicación de la lógica:
Una vez definida las características de nuestro proyecto Java (la versión, la lógica y el código), se puede crear un contenedor Docker que lo ejecute. Creamos un Dockerfile con nuestra versión de Java y los Jar necesarios para ejecutarlos. Una vez hecho, la ejecución consiste en ejecutar los jar con el comando `java`.

En el caso concreto del proyecto [Java-Text_Analyzer](./Docker4Java/Java-Text_Analyzer), a este programa se le añaden dos argumentos extra:
- El nombre del comando que ejecuta el programa (en el caso de docker, `java`)
- La ubicación del jar que ejecuta como hijo (parte de los requerimientos del proyecto).

De esta manera, desde cualquier dispositivo con Docker instalado podemos ejecutar esta versión concreta de Java y nuestro proyecto.

### Ejemplo de ejecución:
```bash
./Docker4Java/run.sh
```
```
Please, fill the data:
- File to analyze: README.md

Vocales: 52
Consonantes: 66
Letras: 118
Números: 3
```

## Contenedores apache:
Toda la documentación se encuentra [aquí](./parte2/parteII.pdf)