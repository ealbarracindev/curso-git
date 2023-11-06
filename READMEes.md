Comandos de Git
============

## Versiones traducidas
- [Español version (original)](READMEes.md)

___

_Lista de los comandos de Git más utilizados_

*Si te interesan mis alias de Git, puedes mirar mi `.bash_profile`, lo encontrarás aquí: https://github.com/joshnh/bash_profile/blob/master/.bash_profile*

--

### Conseguir y crear proyectos

| Comando | Descripción |
| ------- | ----------- |
| `git init` | Inicializa un repositorio local de Git |
| `git clone ssh://git@github.com/[nombreDeUsuario]/[nombre-del-repo].git` | Crea una copia local de un repositorio remoto |

### Comandos globales
| Comando | Descripción |
| ------- | ----------- |
| `git config --global init.defaultBranch main` | Cambiar el nombre de la rama master por main |
| `git config --global -e` | Verificar la configuración global |
| `git config --global user.name [nombreDeUsuario]` | Establecer una configuración específica de usuario |
| `git config --global user.email [emailDeUsuario]` | Establecer una configuración específica de email |
| `git config --global --add --bool push.autoSetupRemote true` | cuando no existe seguimiento ascendente para la rama actual; esta opción surte efecto con las opciones push.default simple |

### Comandos básicos

| Comando | Descripción |
| ------- | ----------- |
| `git status` | Comprobar el status actual |
| `git add [nombre-del-archivo.txt]` | Añade un archivo a la zona de subir cambios |
| `git add -A` | Añade todos los archivos del repositorio a la zona de subir cambios |
| `git commit -m "[Mensaje del commit]"` | Crea un mensaje explicativo de los cambios |
| `git rm -r [nombre-del-archivo.txt]` | Elimina un archivo (o carpeta) |

### Ramas y fusiones

| Comando | Descripción |
| ------- | ----------- |
| `git branch` | Muestra una lista de las ramas que existen en este proyecto (el asterisco señala la rama activa) |
| `git branch -a` | Muestra una lista de todas las ramas (locales y remotas) |
| `git branch [nombre de la rama]` | Crea una nueva rama |
| `git branch -d [nombre de la rama]` | Elimina una rama local |
| `git push origin --delete [nombre de la rama]` | Elimina una rama remota |
| `git checkout -b [nombre de la rama]` | Crea una nueva rama y nos desplaza hasta ella |
| `git checkout -b [nombre de la rama] origin/[nombre de la rama]` | Clona una rama remota y nos desplaza hasta ella |
| `git branch -m [nombre de la rama antigua] [nombre de la rama nueva]` | Renombra una rama local |
| `git checkout [nombre de la rama]` | Cambia a una rama concreta |
| `git checkout -` | Cambia a la última rama activa |
| `git checkout -- [nombre-del-archivo.txt]` | Descarta cambios en un archivo |
| `git merge [nombre de la rama]` | Combina una rama concreta con la rama activa |
| `git merge [nombre de la rama de origen] [nombre de la rama de destino]` | Combina una rama concreta (rama de origen) con una rama nueva (rama de destino) |
| `git stash` | Revierte los últimos cambios y errores en el directorio actual |
| `git stash clear` | Revierte todos los cambios en el directorio actual |

### Compartir y actualizar proyectos

| Comando | Descripción |
| ------- | ----------- |
| `git push origin [nombre de la rama]` | Envía una rama local al repositorio remoto |
| `git push -u origin [nombre de la rama]` | Envía cambios al repositorio remoto (y te posiciona en la rama concreta) |
| `git push` | Envía cambios al repositorio remoto (en la rama actual) |
| `git push origin --delete [nombre de la rama]` | Elimina una rama remota |
| `git pull` | Actualiza el repositorio local al último commit enviado |
| `git pull origin [nombre de la rama]` | Trae / agarra todos los cambios de un repositorio remoto |
| `git remote add origin ssh://git@github.com/[nombreDeUsuario]/[nombre-del-repo].git` | Añade cambios a un repositorio remoto |
| `git remote set-url origin ssh://git@github.com/[nombreDeUsuario]/[nombre-del-repo].git` | Ubica la rama remota de un repositorio remoto mediante su SSH |

### Inspeccionar y comparar

| Comando | Descripción |
| ------- | ----------- |
| `git log` | Visualiza los cambios |
| `git log --summary` | Visualiza los cambios (en detalle) |
| `git log --oneline` | Visualiza los cambios (resumido)) |
| `git diff [source branch] [target branch]` | Vista previa de los cambios antes de hacer un merge |

Publicacion
------------
¿Terminaste con tu proyecto?

- Cree una rama de funciones como de costumbre.
- Actualizar el historial de versiones en el archivo README.md
- Actualice esto para que se desarrolle normalmente.

| Comando | Descripción |
| ------- | ----------- |
| `git checkout master` | Cambiarse a la rama principal |
| `git merge --no-ff develop` | Tomar los cambios de la rama develop hacia la rama master |
| `git push origin master` | Tomar los cambios de la rama develop hacia la rama master |
| `git tag v1.0.0` | Generar un tag de version de cambios de la rama master |
| `git push origin v1.0.0` | Subida de version generada master |

Reemplace 1.0.0 en el fragmento aquí con sus versiones apropiadas. Ahora tienes una etiqueta guardada.