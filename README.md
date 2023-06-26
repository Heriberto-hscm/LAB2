En esta práctica diseñamos un página de lista de tareas cuyo propocito es enlistar una serie de tareas a través de una barra que nos permita agregar y genarar las tareas de manera dinámica en formas de caja, a su vez podamos irlas descartando por medio de un boton de eliminar presente en cada una de las cajas.

HTML

La estructura básica del html consta de una serie de etiquetas como:

    !DOCTYPE html: Esta línea declara el tipo de documento como HTML5.

    html: Este elemento marca el inicio del documento HTML.

    head: Aquí comienza la sección del encabezado del documento, donde se definen 
    metaetiquetas, enlaces a archivos externos y otros elementos relacionados con la configuración 
    de la página.
    title Lista de Tareas: Esta etiqueta establece el título de la página, que se mostrará en la pestaña del navegador.

    link rel="stylesheet" type="text/css" href="estilos.css": Este enlace vincula un archivo CSS externo llamado "estilos.css" para aplicar estilos a la página. 

    head: Aquí termina la sección del encabezado.

    body: Aquí comienza la sección del cuerpo del documento, que contiene el contenido visible de la página.

    h1 Lista de Tareas: Este encabezado de nivel 1 (<h1>) muestra el título principal de la página, que es "Lista de Tareas".

    div id="task-container": Este elemento de división (<div>) se utiliza como contenedor para el campo de entrada de tarea y el botón de agregar.

    input type="text" id="task-input" placeholder="Agregar nueva tarea": Esta etiqueta de 
    entrada (<input>) crea un campo de texto donde puedes ingresar nuevas tareas. 

    button id="add-task-btn" Agregar: Este elemento de botón (<button>) muestra 
    un botón con el texto "Agregar". 

    ul id="task-list": Este elemento de lista desordenada (<ul>) se utiliza para mostrar la lista de tareas.

    script src="app.js: Se utiliza para especificar la ruta del archivo JS.

CSS

Aquí se definen los diferentes estilos de los caracteres de la estructura de estructura html de forma general mediante el body y paticularmente en acada una de las diferentes etiquetas, ademas definen las animaciones que se generan a partir de la asiganición de tareas y eliminación de las mismas.

    .body: Esto establece los estilos para el elemento body, que representa el cuerpo de la página. 

    h1: Esto establece los estilos para los encabezados de nivel 1 (<h1>) en la página. 

    #task-container: Esto establece los estilos para el contenedor de tareas identificado con el ID task-container. 

    #task-input: Esto establece los estilos para el campo de entrada de tareas identificado con el ID task-input. 

    #add-task-btn: Esto establece los estilos para el botón de agregar tareas identificado con el ID add-task-btn. 

    #task-list: Esto establece los estilos para la lista de tareas identificada con el ID task-list. 

    .task-item: Esto establece los estilos para cada elemento de tarea en la lista.

    .task-item span: Esto establece los estilos para los elementos <span> dentro de los elementos de tarea. 

    .fade-in: Esto establece los estilos para la clase .fade-in. 

    @keyframes fade-in: Esto define la animación fade-in utilizando la regla @keyframes. La animación tiene dos puntos clave (from y to) que definen cómo se verá el elemento al principio y al final de la animación. En este caso, la animación hace que el elemento pase de una opacidad de 0 a una opacidad de 1 y se desplace hacia abajo (-10 píxeles a 0 píxeles) para crear un efecto de aparición 
    gradual.

JS

En el archivo js se definen una serie de códigos que permiten adjuntar las tareas  de forma dinámica a través de una serie de funciones como: addTask() una función que se ejecuta cuando se quiere agregar una nueva tarea. Dentro de la función, se obtiene el texto de la tarea del campo de entrada (taskInput.value). Si el texto no está vacío después de eliminar los espacios en blanco, se crea un nuevo elemento de lista (li) utilizando document.createElement('li'). Se le asigna la clase "task-item" para aplicar los estilos CSS correspondientes. Luego, se establece el contenido HTML del elemento de lista utilizando taskItem.innerHTML, que incluye el texto de la tarea y un botón "Eliminar". El elemento de lista se agrega a la lista de tareas utilizando taskList.appendChild(taskItem). Por último, se restablece el valor del campo de entrada a vacío y se aplica una animación de desvanecimiento al elemento de lista 
recién agregado.