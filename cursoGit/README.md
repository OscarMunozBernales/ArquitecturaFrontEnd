# Curso profesional de git y github.

Oscar Muñoz Bernales
7/10/2020

# 1. Introducción a GIT
## 1.1. ¿Qué es git?
Git es un software de control de versiones diseñado por Linus Torvalds, pensando en la eficiencia y la confiabilidad del mantenimiento de versiones de aplicaciones cuando estas tienen un gran número de archivos de código fuente. En su lugar GitHub es una forja para alojar proyectos utilizando el sistema de control de versiones Git. GitHub sería la red social de código para los programadores, tu propio curriculum vitae.

## ¿Por qué usar un sistema de control de versiones como GIT?
Un sistema de control de versiones como Git nos ayuda a guardar el historial de cambios y crecimiento de los archivos de nuestro proyecto.

En realidad, los cambios y diferencias entre las versiones de nuestros proyectos pueden tener similitudes, algunas veces los cambios pueden ser solo una palabra o una parte específica de un archivo específico. Git está optimizado para guardar todos estos cambios de forma atómica e incremental, o sea, aplicando cambios sobre los últimos cambios, estos sobre los cambios anteriores y así hasta el inicio de nuestro proyecto.
- El comando para iniciar nuestro repositorio, o sea, indicarle a Git que queremos usar su sistema de control de versiones en nuestro proyecto, es **git init**.
- El comando para que nuestro repositorio sepa de la existencia de un archivo o sus últimos cambios es **git add.** Este comando no almacena las actualizaciones de forma definitiva, solo las guarda en algo que conocemos como **“Staging Area”** (no te preocupes, lo entenderemos más adelante).
- El comando para almacenar definitivamente todos los cambios que por ahora viven en el staging area es git commit. También podemos guardar un mensaje para recordar muy bien qué cambios hicimos en este commit con el argumento **-m "Mensaje del commit"**.
- Por último, si queremos mandar nuestros commits a un servidor remoto, un lugar donde todos podamos conectar nuestros proyectos, usamos el comando **git push**.

```
git add .
git commit -m "MENSAJE"
git push

// puedes ver el estado de tu rama
git status

// puedes mostrar todos los cambios historicos.
git show
```


