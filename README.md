***Este trabajo hace un estudio exhaustivo para la refactorización de la pagina web de la copisteria FyC https://fycprint.com/ , el grupo está formado por Felipe Jimenez y Joaquin Torrubia***
# Fase 1: Inventario y Dimensión Ambiental (A) 
Mediante el uso de Lighthouse vemos que la pagina web tiene una accesibilidad casi inmejorable.
![ligthhouse accesibility](/images/Captura%20de%20pantalla%202026-05-12%20112146.png)

Además de que para cargarla emitimos muy poco dioxido de carbono , ya que está muy optimizada
![WAVE](/images/Captura%20de%20pantalla%202026-05-12%20114041.png)

### Usando las herramientas de desarrolladores :
En la pagina incial :
![Pagina inicio](/images/Captura%20de%20pantalla%202026-05-12%20113335.png)

En el apartado "Gran formato":
![Apartado "Gran formato"](/images/Captura%20de%20pantalla%202026-05-12%20113400.png)

En el apartado "Pequeño formato":
![Apartado "Gran formato"](/images/Captura%20de%20pantalla%202026-05-12%20113413.png)
# Fase 2: Dimensión Social y Equidad (S)
Contraste de color bajo en la pagina de inicial:
![Contraste color bajo ](/images/Captura%20de%20pantalla%202026-05-19%20111553.png)
![Contraste color bajo ](/images/Captura%20de%20pantalla%202026-05-19%20111439.png)

Son errores sobre todo del encabezado no tiene nada. Errores de constraste muy altos y muy bajos.

# Fase 3: Dimensión de Gobernanza y Ética (G)
Al acceder a la pagina web no aparece la ventanita para rechazar o aceptar las cookies.
Al acceder a herramientas de desarrollador , averiguamos que la pagina no tiene cookies.

![Herramientas desa Storage Cookies](/images/Captura%20de%20pantalla%202026-05-12%20115421.png)

La web no nos pide informacion de registro ni formulario para acceder a ella sino que entramos directamente a la pagina de la copisteria.
# Fase 4: Propuesta de Refactorización (Green Coding)

**Optimización de activos**

En vez de utilizar png o svg utilizaria AVIF o WebP que son muchos mas ligeros.
Aparte, utilizar loading = "lazy" es fundamental para el impacto sostenible, mejoprando el importe cargado.
En la pagina encotramos dos errores, ya que en el encabezado no tiene contenido y mas de 50 alertas por texto pequeño, alternativo...
 
![Formato imagenes](/images/Captura%20de%20pantalla%202026-05-19%20113448.png)

**Reducción de peticiones**
Tiene un script <script src="/js/wave.min.js?v=3.3.0.4"></script>. ES una liberia que actualmente depende de toda pagina.

**Reflexión sobre la Paradoja de Jevons**
Utilizaria exactamente lo que he mencionado antes en la otras preguntas. EL loading lazy es muy importante para la carga diferida y los formatos de las imagenes AVIF

**Librerias mas prescindibles :**
*JQuery Migrate 3.4.1*
Es una libreria de compatibilidad hacia atras solo sirve para que codigo obsoleto siga funcionando sin errores.El codigo fuente tiene carencia sin resolver.
*Jquery 3.7.1* 
En 2026, jQuery es ampliamente reemplazable con JavaScript nativo moderno (querySelector, fetch, classList, etc.). Sin embargo, otras librerías de la lista dependen de ella.

![Imagen librerias js](/images/Captura%20de%20pantalla%202026-05-26%20090728.png)

**Posibles mejoras sociales**
El uso de una semántica es imprescindible. En el código encontramos el uso de Head, Header, Main. Aunque el código se pasa utilizando “div". Podría utilizar más article, section y footer. Hay demasiados “div” que empeoran la semántica del codigo.

**Posibles mejoras de gobernanza**
La página web no contiene cookies .
Debería poner las cookies y si lo pusiera. Estaría bien colocar un pequeño enlace fijo en el pie de página "Configurar cookies" para que el usuario pueda cambiar de opinión y retirar su consentimiento.

**Posibles mejoras ambientales**
A esta página se le puede introducir  cosas para mejorar ambientalmente. Entre ellas el uso del loading lazy para la carga diferida. Para no cargar imágenes pesadas y ahorrar datos y conseguir fluidez en la navegación.
Eliminar enlaces HTTP para una carga más limpia y ecológica, ya que con esto los enlaces no paran de viajar de un sitio a otro en los servidores.



