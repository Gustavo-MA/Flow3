# Flow3
Creacion de un 3er Flow que muestra el status timestamp en puerto de red
Flow2

Creacion del segundo Flow con NoteRed flow3-noteRed Agregando tercer flow con node-red al repositorio 

Introduccion

Se crea un flow quemuestra los datos de fecha y hora en el navegador cada en pantalla utilizando noteRed y dashboard

Material Necesario

En esta actividad utilizamos en siguiente material del primer flow1  y 2.

Ubuntu 20.04 NodeJS NPM NodeRed Nodos Dashboard

Instrucciones y requisitos previos (Previamente instalados)

Para que el flow arranque , se deben instalar los siguientes requisitos:

Instalación de NodeJS. Se recomienda tener instalado NodeJS en alguna versión LTS. Al momento de creación de este documento, se usó la versión 16.17.0LTS. Esta instalación debe incluir las Build-Tools para hacer uso de NPM Instalación de NodeRed. La instalación se realiza por NPM. Al momento de la creación de este contenido, se usó la versión 3.0.2

-sudo apt install curl curl -curl -fsSL https://deb.nodesource.com/setup_lts.x | sudo -E bash - sudo apt-get install -y nodejs sudo apt-get install -y bulid -esential sudo npm install -g -unsite-perm node-red node red --version
Instrucciones de preparación del entorno

Para ejecutar este flow, es necesario lo siguiente

Arrancar NodeRed con el comando node-red Clonar el flow2 anteriormente Exportar el flow2 descargar JSON Importar flow Cambiar el nombre flow2 --> flow3 (Dando doble clic en el titulo) Agregar un bloque funtion Modificar orden: time stamp --> funtion --> debug Dar doble clic en el bloque funtion poner:

// Lo que está después de “//” son comentarios // Crea un objeto Date a partir del payload enviado por timestamp var date = new Date(msg.payload); // Cambia el payload para que sea una fecha con formato msg.payload = date.toString(); // Regresa el mensaje para que se envíe al sigueinte nodo return msg; despues dar Done.
-------------------------------
Se clona el flow 2 y se cambia el nombre a flow3
Para ellos se importa y descarga flow2
Movemos el bloque debug en el nuevo flow 3
Y procedemos a instalar complementos de la paleta dashboard
Haciendo clic en el menú de hamburguesa principal de note-red
En administrador de paleta
En el buscador de la ventana emergente tecleamos note-red dashboard
E instalamos el programa
Y cerramos
Posterior mente se agregaran nuevos componentes de módulos en la paleta de common (comandos)
Arrastramos el modulo que dice text o texto
Hacemos clic en el menú DashBoard
Y en la parte de Laout agréganos un tab
Y sobre este tab otro
Haciendo clic sobre la opción (+)
Editamos los ajustes del primer tab haciendo clic sobre edit
Y cambiamos el texto de name a Fecha damos clic en update.
En el área de trabajo unimos los componentes del nuevo bloque de texto con el bloque de función
Hacemos doble clic sobre el bloque texto
Y cambiamos el texto de la etiqueta Label a: Time stamp interpretado.
Y damos clic sobre done.
Y hacemos deploy
Y nos dirigimos al dashboard en hhtp:/localhost/1808/ui
Se mostrará el resultado del flow 3 visualizando la fecha y la hora en una nueva página del navegador
-------------------------------
Por ultimo dar por ultimo hace deploy sobre los bloques timestamp y debug Y presionar (Seguir instrucciones)
Instrucciones de operación

Para observar el resutlado de este flow, sólo es necesario abrir la pestaña Debug.

Resultados

A continuación puede verse una vista previa del resultado de este flow. 

--------------------------
[
    {
        "id": "745a983bf9c9ebe4",
        "type": "ui_text",
        "z": "71be123211e38ba6",
        "group": "84e8ec8e1028a0cc",
        "order": 0,
        "width": 0,
        "height": 0,
        "name": "",
        "label": "Time Stamp interpretado",
        "format": "{{msg.payload}}",
        "layout": "row-spread",
        "className": "",
        "x": 510,
        "y": 120,
        "wires": []
    },
    {
        "id": "84e8ec8e1028a0cc",
        "type": "ui_group",
        "name": "Fecha",
        "tab": "0719df874782259d",
        "order": 1,
        "disp": true,
        "width": "6",
        "collapse": false,
        "className": ""
    },
    {
        "id": "0719df874782259d",
        "type": "ui_tab",
        "name": "Flow 3",
        "icon": "dashboard",
        "order": 1,
        "disabled": false,
        "hidden": false
    }
]
![image](https://user-images.githubusercontent.com/111370930/187046925-fb40dcc4-5eab-4121-bff0-2d264aabc3a4.png)

--------------------------

Evidencias

Repositorio github: https://github.com/Gustavo-MA/Flow3/blob/main/README.md

Créditos

Desarrollado por Gustavo Medina e-mail: gustavo.medina@uaem.edu.mx
