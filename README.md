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

Para cambiar de rama, se puede utilizar el siguiente comando:

```bash
git checkout <nombre-rama> || git switch <nombre-rama>
```

Para crear una rama y cambiar a ella, se puede utilizar el siguiente comando:

```bash
git checkout -b <nombre-rama> || git switch -c <nombre-rama>
```
