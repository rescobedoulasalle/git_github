<div align="center">
<table>
    <theader>
        <tr>
            <td><img src="https://github.com/rescobedoulasalle/git_github/blob/main/ulasalle.png?raw=true" alt="EPIS" style="width:50%; height:auto"/></td>
            <th>
                <span style="font-weight:bold;">UNIVERSIDAD LA SALLE</span><br />
                <span style="font-weight:bold;">FACULTAD DE INGENIERÍAS</span><br />
                <span style="font-weight:bold;">DEPARTAMENTO DE INGENIERÍA Y MATEMÁTICAS</span><br />
                <span style="font-weight:bold;">CARRERA PROFESIONAL DE INGENIERÍA DE SOFTWARE</span>
            </th>            
        </tr>
    </theader>
    <tbody>
        <tr>
        <td colspan="2"><span style="font-weight:bold;">Formato</span>: Guía de Práctica de Laboratorio</td>
        </tr>
    </tbody>
</table>
</div>

<div align="center">
<span style="font-weight:bold;">GUÍA DE LABORATORIO</span><br />
</div>

<table>
    <theader>
        <tr><th colspan="2">INFORMACIÓN BÁSICA</th></tr>
    </theader>
<tbody>

<tr><td>TÍTULO DE LA PRÁCTICA:</td><td>Vim - Git - GitHub</td></tr>
<tr><td colspan="2">RECURSOS A UTILIZAR:
    <ul>
        <li><a href="https://guides.github.com/">https://guides.github.com/</a></li>
        <li><a href="https://git-scm.com/book/es/v2">https://git-scm.com/book/es/v2</a></li>
    </ul>
</td>
</<tr>
<tr><td colspan="2">DOCENTES:
    <ul>
        <li>Richart Smith Escobedo Quispe (r.escobedo@ulasalle.edu.pe)</li>
    </ul>
</td>
</<tr>
</tdbody>
</table>

# Vim - Git - GitHub

[![License]][license]
[![Downloads]][downloads]
[![Last Commit][last-commit]][last-commit]

[![Debian]][Debian]
[![Git]][Git]
[![GitHub]][GitHub]
[![Vim]][Vim]
[![Java]][Java]


## OBJETIVOS TEMAS Y COMPETENCIAS

### OBJETIVOS
- Conocer el editor de texto Vim.
- Aprender a manejar el sistema de control de versiones Git y utilizar GitHub para trabajar de manera colaborativa.

### TEMAS
- Editor Vim
- Git
- GitHub

## CONTENIDO DE LA GUÍA

### MARCO CONCEPTUAL

- Editor Vim
    - Vim es un editor de texto muy completo para programadores en consola.
    
- Instalar Vim en:

    <details>
    <summary>GNU/Linux</summary>
    - Para instalar Vim en cualquier distribución GNU/Linux use sus mismos repositorios
    -   ```sh
        apt-get install vim
        ```
    </details>

	<details>
    <summary>MS Windows</summary>
    - Para descarga en sistemas MS Windows https://www.vim.org/download.php
    </details>

	<details>
    <summary>MacOS</summary>
    - Para instalar Vim en sistemas MacOS puede usar brew
    -   ```sh
        brew install macvim
        ```
    </details>

- Git
    - Git es un sistema de control de versiones creado por Linus Torvalds. Es eficiente, confiable. 

- Instalar Git

	<details>
    <summary>GNU/Linux</summary>
    - Para descarga en sistemas GNU/Linux desde https://git-scm.com/download/linux
    -   ```sh
        apt-get install git
        ```
    </details>

	<details>
    
    <summary>MS Windows</summary>
    - Para descarga en sistemas MS Windows https://git-scm.com/download/win
    </details>

	<details>
    <summary>MacOS</summary>
    - Para descarga en sistemas MacOS https://git-scm.com/download/mac
    -   ```sh
        brew install git
        ```
    </details>

- git init
    - Crea un nuevo proyecto local, se crean archivos en el directorio oculto .git
    -   ```sh
        git init
        ```

- git config
    - Establece variables de configuración. Por ejemplo para los commits se necesita los datos del desarrollador. Se puede especificar el editor y hasta el tiempo que deseas almacenar tus credenciales en la cache y otras cosas más
    -   ```sh
        git config --global user.name "Richart Smith Escobedo Quispe"
        git config --global user.email richarteq@gmail.com
        git config --list
        git config user.name
        git config --global core.editor "code --wait"
        git config --global credential.helper 'cache --timeout=3600'
        ```

- git status
    - Permite verificar el estado de los archivos
    -   ```sh
        git status
        ```
- git add
    - Añade archivos al staging area. El punto "." agrega todos
    -   ```sh
        git add HolaMundo.java
        git add .
        ```

- git commit
    - Sube los archivos al área de staging, en la máquina local. La opción -m permite escribir el mensaje en línea
    -   ```sh
        git commit -m "Probando el Hola Mundo"    
        ```

- git clone
    - Clona un repositorio remoto como un repositorio local, en el cual se puede hacer push
    -   ```sh
        git clone <remote repo>
        ```

- git remote
    - Persigue un repositorio remoto para hacer push.
    -   ```sh
        git remote add origin <remote repo>
        ```

- git push
    - Permite subir archivos al repositorio remoto
    -   ```sh
        git push -u origin main    
        ```

- git show
    - Muestra detalles del commit actual
    -   ```sh
        git show
        ```

-   git log
    - Permite ver un resumen de los commit realizados
    -   ```sh
        git log
        git log --pretty=oneline
        git log --graph --pretty=oneline --abbrev-commit --all
        git log --pretty=format:"%h - %an, %ar : %s"
        git log -p -2
        ```
    -   <pre>
        6bb6b6e - Richart Escobedo Quispe, hace 3 minutos : Git - GitHub
        6bb6b6e - Richart Escobedo Quispe, hace 12 minutos : Git - GitHub
        b36a9fd - Richart Escobedo Quispe, hace 14 minutos : Git - GitHub
        e86aac8 - Richart Escobedo Quispe, hace 22 minutos : Git - GitHub
        e58f653 - Richart Escobedo Quispe, hace 31 minutos : first commit
        5747062 - Richart Escobedo Quispe, hace 35 minutos : first commit
        </pre>

- git diff
    - Permite comparar los cambios en los archivos
    -   ```sh
        git diff 6bb6b6e 6bb6b6e
        ```

- git branch
    - Permite ver las ramas existentes o crea una rama alternativa al proyecto principal git branch -a
    -   ```sh
        git branch prueba1
        git branch
        ```
    -   <pre>
        * main
        prueba1
        </pre>

- git checkout
    - Permite regresar a versiones anteriores o saltar a otra rama
    -   ```sh
        git checkout prueba1
        git branch
        ```
    -   <pre>
        main
        * prueba1
        </pre>


- git pull
    - Permite descargar los cambios del repositorio remoto al directorio local
    -   ```sh
        git pull
        ```
    -   ```sh
        git checkout nueva_rama
        git pull <remote repo>
        ```
    -   ```sh
        git checkout main
        git pull --rebase origin
        ```



## EJERCICIO RESUELTO POR EL DOCENTE
Primer repositorio en GitHub
- Creamos un nuevo proyecto en GitHub
    - ![Nuevo Proyecto GitHub](github_proyecto_programacion.png)

- Crearemos un repositorio local usando git init
    -   ```sh
        pwd
        /home/richart/gits/proyecto
        git init
        ```

- Crearemos un archivo Readme.md con contenido Markup
    -   ```sh
        echo "# Mi proyecto Git" > README.md
        ```

- Agregaremos este archivo al staging area usando git add .
    -   ```sh
        git status
        ```
    -   <pre>
        En la rama main

        No hay commits todavía

        Archivos sin seguimiento:
        (usa "git add <archivo>..." para incluirlo a lo que se será confirmado)
        README.md
        no hay nada agregado al commit pero hay archivos sin seguimiento presentes (usa "git add" para hacerles seguimiento)
        </pre>
    -   ```sh
        git add README.md
        ```

- Hacemos un primer commit en nuestro repositorio local 
    -   ```sh
        git commit -m "Mi primer proyecto en github"
        ```
- Asociamos el repositorio local con el repositorio remoto 
    -   ```sh
        git remote add origin <remote repo>
        ```

- Actualizamos el repositorio remoto
    -   ```sh
        git push -u origin main
        ```

- Ahora podemos verificar en GitHub que nuestro repositorio se actualizó con el proyecto local
    - ![Readme.md](Readme.md.png)

- Cree una clase Java HolaMundo.java que imprima un saludo, compílelo, ignore archivos binarios, agregue archivo al stating area, haga commit y súbalo al repositorio GitHub.
    -   ```sh
        vim HolaMundo.java
        ```
    -   <pre>
        public class HolaMundo
        {
            public static void main(String args[]) {
            
                /** */
                System.out.println ("¡Hola mundo!");

            }
        }
        </pre>
    -   ```sh    
        java -version
        ```
    -   <pre>
        openjdk version "11.0.14" 2022-01-18
        </pre>
    -   ```sh
        javac HolaMundo.java
        java HolaMundo
        ```
    -   <pre>
        ¡Hola mundo!
        </pre>
    -   ```sh
        vim .gitignore
        ```
    -   <pre>
        *.class
        .gitignore
        </pre>
    -   ```sh
        git add HolaMundo.java
        git commit -m "Hola Mundo"
        git push -u origin main
        ```
    
## EJERCICIOS PROPUESTOS
- Cree una cuenta de usuario en GitHub usando su correo institucional.
- [opcional por ahora] Configure su cuenta de estudiante (https://education.github.com/pack).
- Cree un nuevo proyecto personal y desarrolle el ejercicio resuelto en clase. Haga 3 commits como mínimo y muéstrelos. Commit para "¡Hola mundo!", otro para "Bienvenida al curso" y otro para imprimir su nombre.
- Cree un proyecto grupal para resolver el siguiente problema: Se desea crear una clase Calculator en Java, que tenga las siguientes operaciones: add, sub, mul, div, mod; estas operaciones recibirán dos enteros y devolverán un entero. (Forme grupos de 3 a 5 personas). Cree ramas para cada integrante y cada cierto tiempo una las ramas al main. No elimine nada para evidenciar ramas, main y commits.
- Debería haber minimo 7 commits:
    - 1er commit - Creación de la plantilla "Calculator.java"
    - 2do commit - Uniendo rama "ramma-add" al "main" para obtener metodo add().
    - 3er commit - Uniendo rama "ramma-sub" al "main" para obtener metodo sub().
    - 4to commit - Uniendo rama "ramma-mul" al "main" para obtener metodo mul().
    - 5to commit - Uniendo rama "ramma-div" al "main" para obtener metodo div().
    - 6to commit - Uniendo rama "ramma-mod" al "main" para obtener metodo mod().

## CUESTIONARIO
- ¿Por qué Git es una herramienta importante en el curso?
- ¿Qué conductas éticas debe promocionarse cuando se usa un Sistema de Control de Versiones?
- ¿Qué son los entándares de codificación?

## REFERENCIAS Y BIBLIOGRÁFIA RECOMENDADAS
- https://guides.github.com/
- https://git-scm.com/book/es/v2

- Nano vs. Emacs vs. Vim (Editor Wars!) - https://www.linuxtrainingacademy.com/nano-emacs-vim/
- Emacs vs Vim - https://www.linuxteaching.com/article/emacs_vs_vim
- Vim or Emacs? The Debate is over… - https://cmd.com/blog/vim-or-emacs-the-debate-is-over/
- Por qué un editor de texto de hace 40 años machaca al "todopoderoso" Atom - https://www.xataka.com/aplicaciones/por-que-un-editor-de-texto-de-hace-40-anos-le-da-sopas-con-ondas-al-todopoderoso-atom

- Tutorial de Vim - http://www.truth.sk/vim/vimbook-OPL.pdf
- Teclado en Vim - http://www.viemu.com/vi-vim-cheat-sheet.gif
- Cómo Configurar VIM como VS Code - https://www.youtube.com/watch?v=XgQFzi3VkC8

[license]: https://img.shields.io/github/license/rescobedoulasalle/git_github?label=rescobedoulasalle
[license-file]: https://github.com/rescobedoulasalle/git_github/blob/main/LICENSE

[downloads]: https://img.shields.io/github/downloads/rescobedoulasalle/git_github/total?label=Downloads

[last-commit]: https://img.shields.io/github/last-commit/rescobedoulasalle/git_github?label=Last%20Commit

[Debian]: https://img.shields.io/badge/Debian-D70A53?style=for-the-badge&logo=debian&logoColor=white
[Git]: https://img.shields.io/badge/git-%23F05033.svg?style=for-the-badge&logo=git&logoColor=white
[GitHub]: https://img.shields.io/badge/github-%23121011.svg?style=for-the-badge&logo=github&logoColor=white

[Vim]: https://img.shields.io/badge/VIM-%2311AB00.svg?style=for-the-badge&logo=vim&logoColor=white
[Java]: https://img.shields.io/badge/java-%23ED8B00.svg?style=for-the-badge&logo=java&logoColor=white