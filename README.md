### Repositorio para el Curso Profesional de Git y GitHub de Platzi

Este repositorio pretende funcionar como muestra de los conocimientos adquiridos durante el Curso Profesional de Git y GitHub de Platzi. Además de presentar un resumen de los temas trabajados y aprendidos, el mismo repositorio demuestra la práctica realizada. En el mismo, se puede observar la historia del repositorio con sus commits, branches, etc.

> Git es un sistema de control de versiones distribuido que te permite registrar los cambios que haces en tus archivos y volver a versiones anteriores si algo sale mal. Fue diseñado por Linus Torvalds para garantizar la eficiencia y confiabilidad del mantenimiento de versiones de aplicaciones que tienen un gran número de archivos de código fuente.
- Freddy Vega

------------


**Tabla de contenidos**



### Conocimientos adquiridos durante el curso
Durante el curso, se trabajaron los siguientes contenidos:

[TOCM]

##### Crear y administrar un repositorio local:
Dentro de un repositorio local, podemos realizar numerosas acciones. Muchas de estas acciones pueden realizar también en un repositorio remoto, pero algunas no pueden o no deberían hacerse en remoto.
- Crear ramas dentro del repositorio con **git branch**, añadir archivos con **git add** y realizar commits con **git commit**. También trabajamos cómo reparar un commit con **git --commit amend**
- Comprender la diferencia entre archivos locales, cambios en staging y cambios añadidos al repositorio.
- Comprender la diferencia entre los **estados** de los archivos en el respositorio: trackeados y no trackeados (tracked or untracked), staged y unstaged.
- Añadir archivos con **git add** y quitarlos con **git rm**.
- Ignorar archivos, tipos de archivos y directorios haciendo uso de .gitignore
- Realizar cambios en los tres árboles de git: *working directory*, *staging/index* y *history*.
- Poder observar los cambios con comandos como **git status**, **git diff**, **git show** y **git log**.
- Deshacer los cambios haciendo uso de los comandos **git reflog**, **git reset** y sus variantes **git reset --soft**, **git reset --hard**, **git reset --mixed** y **git reset HEAD**.
- Crear ramas y realizar merge a la rama main.
- Lidiar con los conflcitos que surgen al hacer merge.
- Guardar momentáneamente nuestros cambios en memoria con **git stash**. Este comando nos sirve para quitar los cambios que hemos hecho en nuestra sesión de trabajo, ya sea para descartarlos con **git stash drop**, para ponerlos en una rama nueva con **git stash branch** o para hacer checkout a otra rama sin realizar un commit previamente (porque todavía no estamos listos para hacerlo).
- Limpiar nuestro respositorio de archivos no deseados con **git clean** y sus variantes: **git clean -n** o **git clean --dry-run** que muestran una lista de archivos a eliminar sin eliminar realmente nada; **git clean -f** (force), que fuerza la eliminación de archivos; **git clean -i** (interactive) que realiza la limpieza solicitando confirmación antes de eliminar cada cosa.
- Buscar fragmentos de texto tanto en los archivos de todo el repositorio con **git grep** como en el registro de logs con **git log -S**.

###### Funciones que no deberían usarse en repositorios remotos:
**git cherry-pick**, **git reset** y **git rebase** son en general considerados malas prácticas ya que fundamentalmente **modifican la historia real del repositorio**, dificultando u obturando el control y seguimiento de los cambios. Podemos utilizar estos comandos en nuestros repositorios locales bajo nuestra propia responsabilidad, pero no es recomendable aplicar estas prácticas en repositorios compartidos con equipos de trabajo.

##### Crear y administrar un repositorio remoto
GitHub, además de permitirnos subir nuestro repositorio a la web para compartir el desarrollo con otros y realizar deploy llegado el momento, nos brinda funciones que exceden los límites de Git (por el carácter estrictamente local de este último).
Algunas de las funciones de GitHub trabajadas en el curso son las siguientes:
- Crear un usuario en GitHub y crear repositorios online.
- Configurar claves SSH para una comunicación más fluida y más segura entre nuestro repositorio local y el repositorio remoto.
- Clonar repositorios remotos a nuestro disco local con **git clone** y vincular nuestros repositorios locales con repositorios remotos usando **git remote add**.
- Importar y exportar cambios desde y hacia nuestro repositorio remoto con **git pull** y **git push**.
- Utilizar funcionalidades de GitHub para ver cambios en nuestro repositorio: RAW, history y blame.
- Añadir colaboradores a nuestro repositorio que tendrán permiso de realizar pull, push, revisar pull requests y autorizar su merge.

###### Buenas prácticas en GitHub
Para mejorar el funcionamiento de nuestro repositorio y la comunicación de todos los participantes o colaborades, se sugiere:
- Que el repositorio tenga un Readme.md completo que proporcione información a quienes entren a ver el proyecto.
- Que se incluya un archivo .gitignore riguroso que evite sobrecargar al repositorio remoto con archivos innecesarios (como binarios, logs, archivos duplicados, "TODO lists", etc.).


##### Colaborar con repositorios ajenos y recibir colaboraciones de 
Todo lo anterior dicho cambia drásticamente cuando no somos dueños ni colaboradores del repositorio remoto al que queremos aportar. En caso de que querramos colaborar con un proyecto ajeno (el cual debe ser público), podemos hacerlo de la siguiente manera:
- Realizando un **fork** para tener nuestra propia copia del proyecto en nuestro repositorio de GitHub.
- Clonarlo a nuestro repositorio local para poder trabajar en él.
- Realizar los cambios sugeridos.
- Realizar un **pull request** al proyecto, mediante la interfaz de GitHub.

Es importante, antes de realizar un pull request a un proyecto ajeno, asegurarnos de que nuestro repositorio esté actualizado y haya incorporado los cambios más recientes del proyecto original. Para esto, se puede asociar nuestro repostitorio local con el repositorio original mediante **git remote add** y crear lo que suele llamarse **upstream**: un pointer al repositorio original que nos permitirá hacer pull directamente para importar los cambios más recientes (sin embargo, no nos permitirá hacer push).



