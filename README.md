# charla-git
un repositorio para mostrar git en clase

Indice

+ [¿que es GIT?]([#¿que-es-GIT?)
+ [_estados_ de los archivos](#estados-de-los-archivos)
+ [Comandos Útiles I](#Comandos-Útiles-I)
    -   [clone](#clone)
    -   [status](#status)
    -   [add](#add)
    -   [commit](#commit)
    -   [push](#push)
    -   [pull](#pull)
+ [¿que son los _branchs_?](#¿que-son-los-branchs?)
+ [Comandos Útiles II](#Comandos-Útiles-II)
    -   [checkout](#checkout)
    -   [branch](#branch)
    -   [merge](#merge)
+ [GitHub](#GitHub)

# ¿que es GIT?

Git es un software de control de versiones diseñado por Linus Torvalds, pensando en la eficiencia y la confiabilidad del mantenimiento de versiones de aplicaciones cuando éstas tienen un gran número de archivos de código fuente. Su propósito es llevar registro de los cambios en archivos de computadora y coordinar el trabajo que varias personas realizan sobre archivos compartidos. [Wikipedia](https://es.wikipedia.org/wiki/Git)

La posta esta en [https://git-scm.com/](https://git-scm.com/) (sin excusas, esta disponible en español también)

Para agregar, git es una herramienta que permite gestionar distintos archivos de manera segura, distribuida y eficaz (performance). 
Funciona especialmente bien para mantener el código fuente de un programa, permitiendo, entre otras ventajas, el versionado del proyecto y control de cambios.

# _stages_ de los archivos

En git casi todo se trabaja local, y los archivos pasan por distintos "estados".

## Modificados

Cuando se trabajan los archivos en un directorio git, vamos _modificando_ los mismos por ende este seria el primer estado : **Modificado**

Básicamente, los archivos en este estado están "marcados" y listos para pasar al próximo estado : **staged**

## Staged o Staging Area

En este estado los archivos pasan a estar "_preparados_" para agregarse al próximo _commit_ (guardase localmente el cambio).

Pasar un archivo a este estado requiere una acción manual (un comando git).

## Committed

Un archivo committed es un archivo que se agrego al directorio git y sus cambios se guardaron localmente, lo próximo seria hacer _push_ para subir los cambios al repositorio principal (o remoto)

# Comandos Utiles I

Para usar nuestro repositorio git vamos a utilizar los siguientes comandos

## clone

nos permite hacer una copia local de un repositorio remoto

`git clone <direccion_del_repositorio_remoto>`

## status

Lista los archivos que fueron modificados o están en stage del repositorio local

`git status`



## add

Agrega (pasa a staged) los archivos que pasamos por parámetro (ruta)

`git add <./ruta/del/archivo>`




## commit

Confirma los cambios localmente, para poder hacer un commit necesitamos tener archivos en "_stage_" y proporcionar un _mensaje de confirmación_

`git commit` (abre el editor por default para que escribas el mensaje de confirmación, si no se cambia por lo general es *vim*)

Una forma mas utilizada y corta de hacer un _commit_ es:

`git commit -m "mensaje de confirmacion"`

de esta manera podemos hacer todo en un solo comando.

## push

Intenta subir al repositorio remoto los cambios que se _commitiaron_ localmente

`git push`

## pull

recupera los cambios del repositorio remoto

`git pull`

# ¿que son los _branchs_?

Otra gran ventaja de git es que podemos crear ramificaciones (branch) lo que nos permite "_copiar_" nuestros archivos en _otro lado_ y seguir haciendo cambios sin afectar los otros _branchs_.

Es una parte muy importante de todo el flujo de git, ya que permite que muchas personas trabajen en simultaneo en un mismo proyecto, que se pueda agregar nuevas _features_ y se pueda revisar el código generado.

# Comandos Útiles II

## checkout

permite "pararse" en un branch especifico

`git checkout <nombre_del_branch>`

## branch

permite gestionar un branch (por ejemplo crear uno)

`git branch <nombre_del_branch>`

Esto solo crea el branch, una manera mas corta seria:

`git checkout -b <nombre_del_branch>`

esto crea un branch nuevo a partir del actual y hace _checkout_ del mismo

## merge

hacer merge de dos branchs significaria "_unir_" los mismos, el producto es un branch nuevo, donde van a existir los todos los archivos del branch de _target_ con los cambios producidos en el branch _source_

Se utiliza cuando se usa un branch para desarrollar una _feature_ y luego hay que traer esa funcionalidad al branch principal.

[desde el branch _target_]
`git merge <nombre_del_source_branch>`

# GitHub

Github es un sitio web que funciona como storage masivo de repositorios git, basicamente ofrece almacenamiento gratuito para cualquier repositorio git siempre y cuando el mismo sea publico.

Tener el codigo en git significa que cualquier persona del mundo puede acceder al mismo, es uno de los pilares del open source y tambien muy util para armar un "portfolio" para cualquier desarrollador.

Tiene muchas ventajas ademas se ser un repositorio, permite integrar aplicaciones para analizar el codigo, correr tests, "_buildear_" el código fuente, gestionar el proyecto, gestionar documentación y un largo etcétera...