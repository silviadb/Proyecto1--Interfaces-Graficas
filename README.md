Proyecto1-_Interfaces-Gráficas
=============================

 Editor de presentaciones HTML5
--------------------------------

Introducción
--------------

El presente trabajo tiene como objetivo es investigar e implementar  una librería que permite cargar y mostrar 
una  presentación HTML5 programando desde coffeescript y utilizando además la librería d3.js; todo esto bajo el
ambiente XUL.Nosotros Utilizaremos la librería reveal.js.
Esta tarea programada se esta realizando para el Curso: “Introducción al Diseño de
Interfaces de Usuario” .
 
 
Algunas librerías  investigadas
-------------------------------

1. Fathom.js:
-------------

   * Permite sincronizar el video de su presentación de forma rápida y sencilla.
   * Viene con el ratón ,teclado y la barra de navegación integrado.

2. Deck.js:
-----------
 
   * Permite usar themes.
   * Ofrece efectos de  transiciones.
   * Permite usar extensiones.

3. impress.js:
--------------

 *  Utiliza las últimas tecnologías soportadas por los navegadores, de modo que las presentaciones requieren ser visualizadas en las últimas versiones de los navegadores modernos, como Google Chrome, Firefox, Opera o Safari.
 *  Inspirada en Prezi pero que utiliza solamente CSS3, Javascript y HTML.

4. reveal.js:
--------------
  * Cuadros de diálogo  modales sencillos y flexibles. 
 
Contenido a Desplegar
----------------------

 Se debe crear un editor de presentaciones en html5, el
 cual debe ser capaz de cargar un archivo y visualizarlo como una presentación HTML5
 
 

Estructura de los datos
------------------------

              <presentation>
                 <slide>
                   <title titulo="Titulo de la diapositiva 1"</title>
                   <h1 info="Descripción de la diapositiva 1"></h1>
                 </slide> 
                 <slide>
                   <title titulo="Titulo de la diapositiva 2"</title>
                   <h1 info="Descripción de la diapositiva 2.1"></h1>
                   <h1 info="Descripción de la diapositiva 2.2"></h1>
                 </slide>
                 
              </presentation>
                
Forma de compilación, ejecución y utilización de la aplicación
---------------------------------------------------------------

1. Crear una carpeta llamada Proyecto1, en C:/.

2. En la carpeta Proyecto1:

   a) Crear una carpeta llamada  chrome.
   
   b) Crear una carpeta llamada default.
   
   c)Crear un archivo  llamado application.ini  con lo siguiente:
              

                        [App]
                              Vendor=Silvia
                        Name=Proyecto1
                        Version=1.0
                        BuildID=20100901
                        ID=sdelgado@itcr.ac.cr
                        
                        [Gecko]
                        MinVersion=1.8
                        MaxVersion=16.*
                        
                        
   d)Crear un archivo  chrome.manifest con lo siguiente:
   
             manifest chrome/chrome.manifest
                       
                       
 3.  En la carpeta  default :

   a)Crear una carpeta preferences  y en esta crear un archivo prefs.js con lo siguiente:
   
             pref("toolkit.defaultChromeURI", "chrome://Proyecto1/content/main.xul");
           
           
4.En la carpeta chrome:

  a)Crear  una carpeta content .
  
  b)Crear un archivo chrome.manifest con lo siguiente: 
   
             content Proyecto1 content/
                 
5. En la carpeta content:

  a) Descargar en esta carpeta la compilador de coffeescript y  la librería d3.js.
  
  b) Copiar a esta carpeta los archivos main.xul ,main.coffee y reveal.js que se adjuntan.
   Estos archivos se encuentran  en la siguiente direccion de un gist.
      
             https://gist.github.com/3828478
 

Ejemplo de Datos
------------------
  
             <presentation>
                   <slide>
                     <title titulo="Interfaces Gráficas"</title>
                     <h1 info="Curso electivo del TEC"></h1>
                   </slide> 
                   <slide>
                     <title titulo="Contenidos"</title>
                     <h1 info="Diseño de Interfaces"></h1>
                     <h1 info="Programacion en Coffeescript"></h1>
                   </slide>
                   <slide>
                     <title titulo="Evaluaciones"</title>
                     <h1 info="Examenes y Proyectos"></h1>
                   </slide>
                   <slide>
                     <title titulo="Sitio web del Curso"</title>
                     <h1 info="http://www.arcux.com/cursos/course/view.php?id=9"></h1>
                   </slide>
                </presentation>

                
                


Limitaciones:
-------------

   1.Problemas para implementar la librería desde coffeescript .
   

   
   
 by Silvia Delgado y Aaron Ruiz