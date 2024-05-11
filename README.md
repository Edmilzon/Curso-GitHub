# Curso-GitHub

### Instalación de Git

Para instalar Git en Windows, se puede descargar desde la página oficial de [Git](https://git-scm.com/).

Verificar la instalación de Git con el siguiente comando:

```bash

git --version

```

### Configuración de Git

Para logearte y poder configurar el nombre de usuario y el correo electrónico con los siguientes comandos:

```bash

git config --global user.name 
git config --global user.email

```

### Crear un repositorio

Para crear un repositorio, se debe ir a la cuanta de git en your repositories e=en new crear con las especificaciones correspondiente 


### Estado del repositorio

Para lograr visualizar el estado del repositorio, se puede utilizar el siguiente comando:

```bash
git status
```

### Tipos de estados del repositorio

- **Modified**: Archivos que han sido modificados en el proceso.
- **Staged**: Archivos que están en el stage.
- **Committed**: Archivos que han sido guardados en el repositorio .

### Seguimiento de archivos

Para agregar un archivo modificado al stage, se puede utilizar el siguiente comando:

```bash
git add <archivo>
```

Para agregar todos los archivos modificados al stage, se puede utilizar el siguiente comando:

```bash
git add .
```

Restaurar archivos del stage:

```bash
git restore --staged <archivo>
```

Restaurar archivos del working directory:

```bash
git restore <archivo>
```

###Crear un commit

En el momento de la creacion de un commit con los archivos en el stage, se puede utilizar el siguiente comando:

```bash

git commit -m "<mensaje>"

```

### Historial de commits

Si se desea visualizar el historial de commits, se puede utilizar el siguiente comando:

```bash

git log

```

otros comandos:

```bash

git log --oneline
git log --graph
git log --oneline --graph

```

### Ramas

Una rama es una línea de desarrollo independiente que permite trabajar en una nueva funcionalidad sin afectar la rama principal.

Para crear una rama, se puede utilizar el siguiente comando:

```bash
git branch <nombre-rama>
```

Para eliminar una rama, se puede utilizar el siguiente comando:

```bash
git branch -D <nombre-rama>
```

Para eliminar ramas de mi repositorio remoto, se puede utilizar el siguiente comando:

```bash
git remote prune origin
```

Para ver las ramas, se puede utilizar el siguiente comando:

```bash
git branch
```

Para ver todas las ramas, se puede utilizar el siguiente comando:

```bash
git branch -a
```


### Importancia de generar ramas y el commit

El id del commit no cambia porque el commit es un objeto inmutable. Al crear una nueva rama, se crea un nuevo puntero que apunta al mismo commit que la rama anterior.

### Merge

Para fusionar una rama con la rama actual, se puede utilizar el siguiente comando:

```bash
git merge <nombre-rama>
```

### Merge Fast-Forward

El merge fast-forward es un tipo de merge que se realiza cuando no hay conflictos entre las ramas. Consiste en avanzar la rama actual hasta la rama que se quiere fusionar.

Para realizar un merge fast-forward, se puede utilizar el siguiente comando:

```bash
git merge <nombre-rama>  --no-ff
```

### Conflictos

Los conflictos se producen cuando se intenta fusionar dos ramas que han modificado las mismas líneas de un archivo.

- 👆 Contenido que ya existia en el archivo
- 👇 Contenido que se añade en la rama actual


Para cambiar de rama, se puede utilizar el siguiente comando:

```bash
git checkout <nombre-rama> || git switch <nombre-rama>
```

Para crear una rama y cambiar a ella, se puede utilizar el siguiente comando:

```bash
git checkout -b <nombre-rama> || git switch -c <nombre-rama>

```

### Navegando por GitHub

- Mi perfil y repositorios:
  Avatar > Your profile
- Repositorio y ramas:
  Repositorio > Branches
- Buscar perfiles, repositorios y otros:
  Search bar
- Repositorio & Pull Requests:
  Repositorio > Pull requests
- Proyectos:
  Repositorio > Projects
- Organizations:
  Avatar > Your organizations
- Repositorio & actions:
  Repositorio > Actions
- Repositorio & Projects:
  Repositorio > Projects

### Enlazar repositorio local con remoto

Para enlazar un repositorio local con un repositorio remoto, se puede utilizar el siguiente comando:

```bash
git remote add origin <url-repositorio>
```

Para subir los cambios al repositorio remoto, se puede utilizar el siguiente comando:

```bash
git push -u origin <nombre-rama>
```

Clone un repositorio remoto mediante https:

```bash
git clone <url-repositorio>
```

Clonar un repositorio remoto mediante ssh:

```bash
git clone
```

obtener claves ssh:

```bash
ssh-keygen -t rsa -b 4096 -C
```

### Git Push

Sube los cambios del repositorio local al repositorio remoto.

```bash
git push origin <nombre-rama>
```

### git push -u & git push -f

- **git push -u**: Establece la rama actual como rama por defecto.
- **git push -f**: Fuerza la subida de los cambios al repositorio remoto.

```bash
git push -u origin <nombre-rama>
```

```bash
git push -f origin <nombre-rama>
```

### eliminar rama remota

```bash
git push -d origin <nombre-rama>
```

### otros comandos relacionados

```bash
git push --all
git push --tags
```

### Git Pull

Descarga los cambios del repositorio remoto al repositorio local.

```bash
git pull origin <nombre-rama>
```

### git pull --rebase

El rebase es una técnica que permite reescribir la historia de un repositorio.

```bash
git pull --rebase origin <nombre-rama>
```

### git pull --all

Descarga todas las ramas del repositorio remoto al repositorio local.

```bash
git pull --all
```

### git pull --set-upstream

Establece la rama actual como rama por defecto.

```bash
git pull --set-upstream origin <nombre-rama>
```

### Pull Request

Un pull request es una solicitud para fusionar una rama con otra rama.

### ¿Cómo se crea un pull request?

1. La rama la subiste recientemente y te aparece la opción en GitHub.
2. Vas a la pestaña Pull requests y creas uno nuevo.

### Hacer una buena PR

- **Título descriptivo**: Indica el propósito de la PR.
- **Descripción detallada**: Explica los cambios realizados.
- **Enfocar el código en una sola cosa**: Es mucho más fácil revisar y aceptar una PR que hace solo una cosa a una que hace muchas.
- **Añadir capturas de pantalla**: Si es necesario, añadir capturas de pantalla.

### Flujos de trabajo en equipos

### Git Flow

Es un modelo de ramificación que define un flujo de trabajo para proyectos de Git. Se compone de cinco ramas:

- **Main (master)**: Contiene el código en producción.
- **Develop**: Contiene el código en desarrollo.
- **Feature**: Contiene las nuevas funcionalidades.
- **Release**: Contiene el código en preproducción.
- **Hotfix**: Contiene los parches de producción.
- **Support**: Contiene el código en mantenimiento.



### GitHub Flow

Es un modelo de ramificación que define un flujo de trabajo para proyectos de GitHub. Se compone de una rama principal:

- **Main (master)**: Contiene el código en producción.


### Trunk Based Development

Es un modelo de ramificación que define un flujo de trabajo para proyectos de Git. Se compone de una rama principal:

- **Main (master)**: Contiene el código en producción.

Es útil si contamos con un buen sistema CI/CD.


### Ship/Show/Ask

Es un modelo de ramificación que define un flujo de trabajo para proyectos de Git.

- **Ship**: Subir el código a producción.
- **Show**: Mostrar el código a los usuarios.
- **Ask**: Preguntar a los usuarios.

