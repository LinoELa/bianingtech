<!-- MI DOCUMENTO "INFORMACION" DE LO QUE YO VOY HACIENDO -->
# --- DIFERENCIA ENTRE : NODO Y ELEMENTO(Element)   ---#
-->NODO : Es mas amplio he incluye : Texto, Cometario y tec...
-->ELEMENT : Solo incluye los elementos HTML

# == OBJETIVO DEL PROYECTO : USO BASICO DEL DOM == #
SELECCIONAR  <=> MODIFICAR <=>CAMBIAR ESTILO <=> MAS...

# == SHORTCOUT IMPORTANES  == #
1. Option + Shift + f => Elegir entre Beautify y Prettier => como princpales formatter

# == HTML  == #
1. Primero hemos creado  los archivos index.html style.css y app.js como principales archivos 

2. En el Index.html hemos creado la estrucutra pero en ves de bautify que ya no esta en mantenimiento pues he usado prettier

3. Hemos conectado los paginas entre si. 

4. Creamos una ->Carptea : Imagenes<- donde vamos a guardar todas las imagenes dentro 

5. Creamos o hacemos el => FAVICON

6. h1  -> dentro de un contenedor -> Div.Contenedor

7. Buscamos emojos en el artiulo del freecodecamp : https://www.freecodecamp.org/news/all-emojis-emoji-list-for-copy-and-paste/

8. Luego le ponemos el HTML junto con las clases y los Id para poder editarlo en el CSS


# == CSS == #
1. justify-content => X 
2. Align-Items => Y 
3. Backgroung : url () || no repeat center/cover => 

url('./IMG/pizza.jpg'): Especifica la ubicación de la imagen que se utilizará como fondo. En este caso, la imagen está en la carpeta "IMG" y se llama "pizza.jpg".

no-repeat: Indica que la imagen de fondo no se repetirá en ninguna dirección. En otras palabras, la imagen se mostrará solo una vez.

center: Establece la posición inicial de la imagen de fondo en el centro del elemento.

/cover: Hace que la imagen de fondo se ajuste y cubra completamente el área del elemento, incluso si esto significa recortar parte de la imagen. Esto es útil para asegurarse de que el fondo se vea bien sin importar las dimensiones del elemento.

4. flex-wrap => 
flex-wrap se utiliza en un contenedor con display: flex para controlar cómo los elementos flexibles (flex items) se deben colocar en el contenedor cuando no hay suficiente espacio en el eje principal.

Aquí hay una breve explicación de la propiedad flex-wrap:

nowrap: (valor predeterminado) Todos los elementos flexibles se ajustan en una sola línea sin envolver al siguiente renglón.

wrap: Los elementos flexibles se colocarán en varios renglones si no hay suficiente espacio en la línea principal.

wrap-reverse: Similar a wrap, pero los elementos se colocarán en renglones en sentido inverso, es decir, desde la última línea hasta la primera.


5. El min[whidth - height] es para poder crear algo como una pagina respondive

6. Antes de la clase Topping le asignamos el estilo a al etiqueta en este caso : => UL =>

# == Seleccionar Elementos en JAVASCRIPT  == #

Para tener acceso a los elementos los primero es poder selecionar el elemento primero 


=====.getElementByid() =====
const titulo = document.getElementById('titulo')
console.log(titulo.tagName)
tenemos que especificar el ID de elemento que queremos seleccionar

=>innerHTML : [inner = Interno ] nos da acceso a la estrucutra html que esta dentro del elemento elegido

=> innerText : [inner = Interno ]Retorna el titulo o el texto que esta dentro de la etiqueta.   
    -> console.log(inner.Text)


=> tagName : [tagName = Etiqueta Nombre] para tener acceso o ver una etiqueta pues se puede usar tagname 
    -> console.log(titulo.tagName)

=> SI no existe un elemento o hay un error a seleccionar un elemento, pues pondra NULL

console.log(typeof titulo)
Le podemos mirar con console.log(typeof titulo ) para saber que tipo de dado nos retorna, en caso que sea objeto como este ya lo sabemos.

=====.getElementByClassName() =====

const topping = document.getElementsByClassName('topping')
console.log(topping[0].id)

Para seleccionar elementos por clases , a diferencia de el Id que es unico y solo se puede seleccionar un elemento, con las clases se puede seleccionar varios elementos.
=====.getElementByTagName() =====

const topping = document.getElementsByTagName('li')
console.log(topping)
Es para pode elegir o seleccionar a todoso los elemento por su nombre o una etiqueta. 

=====.querySelector() =====

-> const aceituna = document.querySelector('.topping.fondo-marron') /*para encontrar el primer id */
console.log(aceituna)

-> const aceituna = document.querySelector('ul li.fondo-naranja') 
console.log(aceituna)

-> const aceituna = document.querySelector('ul li:not(fondo-marron)') 
console.log(aceituna)

=> querySelector ==> Nos permite seleccionar el primer elemento que cumple este criterio 

=> querySelectorAll() ==> Nos permite seleccionar todos los elemento que cumple este criterio 

Son utilies cuando queremos un sistema de selector mas especificos
Tambien se puede selecionar el primer elemento usando:  .querySelector('.aceitunas')


=====.querySelectorAll() =====
Tambien se puede selecionar el varios elementos preciso usando:  .querySelectorAll('.aceitunas.fondo')

-> const elemento = document.querySelectorAll('.topping') 

console.log(elemento)
console.log(elemento[0])
console.log(typeof elemento)


# ==== Asignar elementos en JAVASCRIPT  ==== #
== 
Aqui lo ve que veremos es como poder asignar estilo : color, tamano , forma y mas cosas a un elemento html desde el js 

# --- VER ESTILO  ---#
const primertopping = document.querySelector('.topping')
<!-- me da una lista de las propiedades que puedo personalizar  -->
console.log(primertopping.style )
<!-- cabar el color a azul el fondo --> 
console.log(primertopping.style.backgroundColor= 'blue' ) 
<!-- cambiar el color de la letra -->
primertopping.style.color = '#6dff00';
<!-- cambiar  a mayuscula las letras -->
primertopping.style.textTransform= 'uppercase';

# --- ACCEDER A TEXTS  ---#

Es una forma de obtener el contenido interno de un elemento que contiene texto.
<!-- Acceder a al texto innerText -->
--> Inner => Interno 
--> Text ==> Texto
-- No ensena los espacios
console.log(listaDeTopppping.innerText)

-- Si que ensena los espacios : 
console.log(listaDeTopppping.textContent)

-- Nos devuelve toda la estructura del html con los espacios 
console.log(listaDeTopppping.innerHTML)

# --- MODIFICAR TEXTO  ---#
const listaDeTopppping = document.getElementById('titulo')
<!-- Obtener el texo -->
console.log(listaDeTopppping.innerText)
// cambiar o modificar el texto el texto
listaDeTopppping.innerText = 'Mis topping Favoritos';
console.log(listaDeTopppping)


# --- ATRIBUTOS CON JS  ---#
Vamos a modificar un atrbuto href
<!-- Seleccinar optener un atributo -->
const enlaces = document.getElementsByTagName('a')
console.log(enlaces[0].getAttribute('href'));
<!-- elimiar el atributo -->
console.log(enlaces[0].removeAttribute('href'));
<!-- actualizar un atributo -->
console.log(enlaces[0].setAttribute('href'));
<!-- Camabiar la direccion de la redireccion  -->
console.log(enlaces[0].setAttribute('href', 'https://www.google.com'));


# --- CLASES ---#
const primerTopping = document.querySelector('.topping')
console.log(primerTopping.classList)

<!-- Agregar una clase -->
primerTopping.classList.add('mi-clase')
console.log(primerTopping)

<!-- Verificar si una existe una clase o no  -->
// True => si exite 
console.log(primerTopping.classList.contains('fondo-marron'))

// False => Si no exite 
console.log(primerTopping.classList.contains('fondo-azul'))

<!-- Eliminar una clase  -->
lo elimina pero solo la primera clase con el valor asignado
primerTopping.classList.remove('topping')



# --- CREAR & AGREGAR & ELIMAR UN ELEMENTO DESDE 0   ---#
Vamos a ver como se puede crear  un elemento desde 0 y luego agregar el elemento al DOM de forma dinamica y es util vas a recivir informacion de un servidor o de un API, lo recibes en formato JSON y luego lo transformas en elemento HTML para que los usuarios pueda interactuar. 

<!-- crear  y agregar un el elemento y una clase-->
// 1 Primero optenemos una referencia de donde lo queremos agregar
const listaTopping = document.getElementById('lista-toppings')
// 2 Creamos el elemento
const toppingNuevo = document.createElement('li')
// 2.1 anadimos la varias clases
toppingNuevo.classList.add('topping', 'fondo-marron')
// 2.2 le anadimos un texto
toppingNuevo.innerText = 'Queso Extra'

// 3 Especifcar donde lo queremos agragar 
listaTopping.append(toppingNuevo)

<!-- Eliminar un alemento -->
elimina todo elemento
listaTopping.remove()

# --- RECORRER EL DOM   ---#
aqui es como se puede recorrer en los elementos del DOM
Hay muchas formas el puento es 
--> verificar que el resultado no sea null

<!-- Para encontrar las propiedades de los padres -->
const listaDeToppings = document.getElementById('lista-toppings')
console.log(listaDeToppings.parentNode);
console.log(listaDeToppings.parentElement.parentElement);

<!-- Encontrar las propiedades de los hijos : Nos dara texto-->
console.log(listaDeToppings.firstChild)
// Es mejor  usar esta propiedad que es mas practica
console.log(listaDeToppings.firstElementChild)

<!-- Acceso al primer hijo y es mejor que firstChild-->
console.log(listaDeToppings.children)

<!-- para obtener el ultimo elemento-->
console.log(listaDeToppings.lastElementChildtElementChild)
console.log(listaDeToppings.lastElementChildtElementChild)

<!-- Para obtener el hermano anterior de la lista -->
--> Sibling ==>: Hermanos 
console.log(listaDeToppings.previousElementSibling)

# ==== EVENTOS DEL DOM  ==== #

# ---  EVENTO ---#
Es algo que ocurre en la web como resultado de la interraccioon con el usuario o por otra causa como cambios en el estado del dispositivo o de la ventana, ejemplosi cambiamos el tamano de la ventana
Todos esos cambios van a desencadenar eventos y eso nos permitira saber cuando ocurren estos eventos, cuando el usuarioo esta interactuando  con elemetos de la pagina y noos permite difinir como manejar estos elementos en caso que ocurra.

El mas comun es el del mouse o el punto que cualquier click que da se registrara como evento en el navegador y el navegador va a saber cual de eso elementos se ha hecho click y vamos a poder decir en caso que ocuere en  click que queremos que ocuerra. 

Otro evento comun es el de presionar una tecla en el teclaso podemos de saber y decir que pasar cuando se seleccionar una teclase, saber cual se ha selecionado y que queremos que sucesa al ser selecionada.
EJ: 
-> Un juego, las teclas 
-> Cambios de tamano 
-> Arrastrar imagenes o un archivo.
-> Tambien los gestos en un  dispositivoo toch

Los mas comunes son : 
1. Cursor
2. Teclado

Los demas eventos son iguales oparecidos.

# --- CONCEPTOS IMPORTANTES DEL LOS EVENTOS   ---#
1. Target (objetivo) : esta ingles la palabra
    Recibe la accion
2. Trigger 
    La Accion que desencadena el evento
3. Event Handler
    Funcion que maneja lo que ocurre al desencadenar el evento
4. Event Listener
    Conexion entre el evento el elemento y la funcion que lo va a manejar

# --- Target (Objetivo Blanco)   ---#
Si tenemos una pagina y hacemos click a un sitio pues este sito ya sea imagen o button , pues este elemento donde va acurir este evento (click) es a lo que nos referios como el targel element. 

Hay muchos eventos

# --- Trigger  ---#
Es la accion que va a desencadenar un evento ejemplo al hacer click.

# --- Event Handler  ---#
Estos conceptos se usan mucho en react
Es una funcion que se ejecuta cuando ocurre un evento, el esta alli pendiente esperando a que ocurra el evento

<!-- Ejemplo -->

        <li onclick="mostrarClick()" class="topping fondo-marron" id="albahaca">Albahaca</li>

==>funcion que va a manejar el evento
    function mostrarclick(){
    console.log('Clic')
    }


# --- Event Listener (Escuchador de eventos) ---#
La asociacion que exite entre un evento especifico y la funcion que lo va a manejar es lo que se denomina EVENT LISTENER.
Es esta conexion  para asociar un evento en un elemento con una funcion especifico.
Nosotros mismos tenemos que crear esta asociacion. 

Al crear un event listener es decirle que escuche los eventos y al escuchar el evento asigando que realizae la tarea que le asignaremos

<!-- Ejemplo :  osociacion entre funcion y el evento que esta ya predeterminada y lista para ejecutarse al ocurrir un evento -->
==> onclick="mostrarClick()"

# --- EVENTOS html   ---#
vamos a ver como funciona.
1. usar atributos [ como : onclick ]en HTML para representar eventos es buen 
para manejar un eventos

a. li > Hemos creadoo un atributo Onclick = ''  y le hemos dado una funcion llamado -- mostrarClick()-- 


# ==> NO ES PRACTICO NI BUENO EN PRACTICA REAL <==

b. luego vamos a js y creamos la funcion antes creado.
      <h1 id="titulo">🍕<br> Toppings de Pizza</h1>
      <ul id="lista-toppings">
        <li onclick="mostrarClick('Aceitunas')" class="topping fondo-marron" id="aceitunas">Aceitunas</li>
        <li onclick="mostrarClick('Cebollas')" class="topping fondo-naranja">Cebollas</li>
        <li onclick="mostrarClick('Albahaca')" class="topping fondo-marron" id="albahaca">Albahaca</li>
        <li onclick="mostrarClick('Champinones')" class="topping fondo-naranja">Champinones</li>
      </ul>
      <a href="https://www.freecodecamp.org/espagnol/">Freecodecamp</a>
    </div>

==> function mostrarClick(topping){
        cons
        
# ==> OTRA FORMA MEJOR DE HACERLO ES : .addEventListener() <==
Esta es la aternativa que se usa en los proyecto reales 
# ---  .addEventListener() ---#
Lo antes hecho lo vamos a definir y crearlo direcrtamete directamte en JS 

<!-- Codigo 1 JS para manejo de eventListener() -->
// 1  crear la variable 
const albahaca = document.getElementById('albahaca')

// 2 la funcion
// e => Evento u objeto
/* Se puede llamr a todos los eventos que se vean en la primera console. */
function mostrarClick(e){
    console.log(e)
    console.log(e.target)
    console.log(e.target.innerText)
}
// 3 llamar a variable y llamr la funcion que queremos usar
// mostrarClick sin  ()
albahaca.addEventListener('click', mostrarClick)

<!-- Codigo 2 JS para manejo total de eventListener() -->
para poder asignar el eventListener()  a todos los elementos de la lista (topping) y poder mostrar todos los elementos correspondientes.

// 1  crear la variable 
/* Para selecionar todos los topping usamos el siguiente  evento */
const toppings = document.getElementsByClassName('topping')

// 2 la funcion
// e => Evento u objeto
function mostrarClick(e){
    console.log(e.target.innerText)
}

/* .Usamos un ciclo par aterar todo los elementos */
for (const topping of toppings)  {
    // console.log(topping)
    topping.addEventListener('click' , mostrarClick)
}

<!-- OTRA ALTERNATIVA : Que tambien se usa aveces -->
En lugar de definir una funcion aparte, la podemos difiniir dentro a la vez 
EJEMPLO:

/* Para selecionar todos los topping usamos el siguiente  evento */
const toppings = document.getElementsByClassName('topping')

// utilizariamos al funcion flecha => como segungo argumento
/* .Usamos un ciclo par aterar todo los elementos */
for (const topping of toppings)  {
    // console.log(topping)
    topping.addEventListener('click' , (e)=>{
        console.log(e.target.innerText)
    })
}

<!-- Para manejar otros eventos  -->
Para manejar otros eventos simplemento con personalizar la parte del click es suficiente, alli colocar el nombre de la funcion.
for (const topping of toppings)  {
    // console.log(topping)
    topping.addEventListener('click' , (e)=>{
        console.log(e.target.innerText)
    })
}


