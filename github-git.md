#  Para convertir una carpeta en un nuevo proyecto Git
 ```bash
 git init
````
Algo como esto debería aparecer a continuación:

Initialized empty Git repository in /Users/username/.git

Esto significa que se creó el proyecto Git.

Para conectar el repositorio creado localmente con uno que creamos en GitHub, podemos usar el remote addcomando:

git remote add origin https://github.com/username/repo-name.git 

Para definir la rama principal, que será la rama a la que enviaremos el código . ¡Discutiremos qué ramas hay más adelante en el capítulo!

git branch -M main


04. Flujo de trabajo de Git
# Git internamente
Ahora que hemos conectado nuestros repositorios locales y remotos, aprendamos cómo mover nuestro código entre ellos.

Los dos comandos principales de Git que usarás primero: git addy git commit.

## Directorio de trabajo
¡El directorio de trabajo es donde tienes los archivos y carpetas de tu computadora en los que estás trabajando o cambiando activamente! ¡Es la carpeta donde vive tu proyecto! Para nosotros, esta es la nueva carpeta del proyecto que conectamos previamente a nuestro repositorio remoto.

## Área de preparación / Índice
El área de preparación es un estado de archivos y carpetas dentro de tu proyecto que le dice a Git: "¡Oye, me estoy preparando para conectarme!". Es un área temporal donde usted elige qué archivos desea "confirmar" o enviar al repositorio remoto.

¡Usar el git addcomando nos permite hacerlo! Aquí hay algunas variaciones del comando que quizás quieras considerar:

git add example.txtagregará el archivo único al área de preparación. Si solo desea que uno de sus archivos de trabajo aparezca en GitHub en lugar del resto de su proyecto, considere especificar un archivo específico.
git add .agregará todos los archivos modificados al área de preparación. Esto significa que se incluirá cualquier archivo nuevo agregado o modificado al directorio de trabajo.
git add *.htmlsólo preparará archivos con una extensión especificada. En este ejemplo, este comando solo agregará archivos .html .
git reset filenameelimina la preparación de un archivo específico si no era su intención prepararlo.
git resetelimina todos sus archivos y regresa al estado anterior de su directorio de trabajo.
## Archivos confirmados
¡Confirmar archivos significa que los archivos están listos para enviarse a GitHub! Puede cambiar varios archivos en una sola confirmación y puede tener varias confirmaciones listas para ser "enviadas". Las confirmaciones nos ayudan a separar diferentes acciones en nuestro código y nos permiten agregar mensajes útiles para que podamos saber y realizar un seguimiento de lo que hemos cambiado.

Así es como podrían verse algunos mensajes de confirmación para un proyecto típico:

first commit! yay- nuestro primer compromiso.
add fun pics to header- el desarrollador agregó un encabezado a su proyecto
REMOVE THIS- El desarrollador eliminó algunos archivos o códigos que. empujado accidentalmente.
fixed again fr this time!!!!!!- El desarrollador solucionó un error... o eso esperan.
Nota: Los mensajes de confirmación se vuelven tontos cuando trabajas solo por un tiempo 😛, ¡pero siempre es bueno ser claro y conciso en tus mensajes de confirmación cuando estás en un equipo! ¡Queremos que los mensajes expliquen lo que estamos haciendo con el código para que otros desarrolladores puedan saber en qué se trabajó de un vistazo!

Ahora que estamos listos para enviar sus archivos preparados, use el siguiente comando:

git commit -m 'type your commit message here' 

Bastante útil, ¿verdad? ¡Los mensajes de compromiso son vitales para el desarrollo de cualquier proyecto! Los mensajes suelen tener alrededor de 30 palabras o menos. ¡Cuanto más conciso, mejor!

¡Usar el git statuscomando te permite saber en qué punto del flujo de trabajo de Git te encuentras! Si necesita saber qué archivos están preparados o no, úselo para saber si es necesario addo commit!

# Instrucciones
Con nuestro repositorio remoto inicializado, preparemos nuestros cambios y confirmemos nuestros archivos.

Agregue sus archivos al área de preparación.
Confirme sus cambios y agregue el mensaje de confirmación "Compromiso inicial".

¡Estamos listos para hablar sobre el comando que usaremos para finalmente "impulsar" o publicar nuestro código! Este es el último paso del flujo de trabajo básico de Git.

El git pushcomando se utiliza para enviar los cambios confirmados localmente a su repositorio remoto. Verás todos los cambios que has realizado en GitHub.

La primera vez que ingresa a una rama, el comando generalmente se ve así:

git push -u origin main

Después git push, utilizará -u origin mainpara configurar y realizar un seguimiento de los cambios desde la mainrama ascendente a través del origincontrol remoto que apunta a su repositorio de GitHub.

Una vez configurado, cualquier confirmación que envíe a esta rama solo requerirá git push. Cuando haya terminado, podrá actualizar su repositorio de GitHub y ver sus cambios en línea.

# Instrucciones
GIF de Octocat de GitHub

Usando el comando de esta lección, envíe su código a GitHub. 🥳

¡Compruebe para asegurarse de que esto se haya completado correctamente actualizando la página!


![image](https://github.com/BoatCode404/Git/assets/166348131/5a600d1f-6a53-45ee-bc7f-41495838a730)

Aquí hay un resumen de todo lo que hemos aprendido en este capítulo:

- git initpara crear un nuevo repositorio local.
- git remote addpara conectar nuestros repositorios locales y remotos.
- git addpara preparar los archivos en los que hicimos cambios.
- git commit -m ''para preparar nuestros archivos para GitHub (junto con un mensaje).
- git pushpara publicar nuestros cambios de código en nuestro repositorio remoto en GitHub.
- git pull para traer los cambios del repositorio remoto a tu repositorio local:(git pull origin main)
- git push origin main despues de hacer git pull
