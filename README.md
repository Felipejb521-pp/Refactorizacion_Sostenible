Este trabajo hace un estudio exhaustivo para la refactorización de la pagina web de la copisteria FyC https://fycprint.com/
### Fase 1: Inventario y Dimensión Ambiental (A)
Mediante el uso de Lighthouse vemos que la pagina web tiene una accesibilidad casi inmejorable
![ligthhouse accesibility](/images/Captura%20de%20pantalla%202026-05-12%20112146.png)
además de que para cargarla emitimos muy poco dioxido de carbono , ya que está muy optimizada
![WAVE](/images/Captura%20de%20pantalla%202026-05-12%20114041.png)

### Usando las herramientas de desarrolladores :
En la pagina incial :
![Pagina inicio](/images/Captura%20de%20pantalla%202026-05-12%20113335.png)

En el apartado "Gran formato":
![Apartado "Gran formato"](/images/Captura%20de%20pantalla%202026-05-12%20113400.png)

En el apartado "Pequeño formato":
![Apartado "Gran formato"](/images/Captura%20de%20pantalla%202026-05-12%20113413.png)
### Fase 2: Dimensión Social y Equidad (S)
Contraste de color bajo en la pagina de inicial:
![Contraste color bajo ](/images/Captura%20de%20pantalla%202026-05-19%20111553.png)
![Contraste color bajo ](/images/Captura%20de%20pantalla%202026-05-19%20111439.png)
### Fase 3: Dimensión de Gobernanza y Ética (G)
Al acceder a la pagina web no aparece la ventanita para rechazar o aceptar las cookies.
![Herramientas desa Storage Cookies](/images/Captura%20de%20pantalla%202026-05-12%20115421.png)
Al acceder a herramientas de desarrollador , averiguamos que la pagina no tiene cookies.

La web no nos pide informacion de registro ni formulario para acceder a ella sino que entramos directamente a la pagina de la copisteria.
### Fase 4: Propuesta de Refactorización (Green Coding)

Optimización de activos

En vez de utilizar png o svg utilizaria AVIF o WebP que son muchos mas ligeros.
Aparte, utilizar loading = "lazy" es fundamental para el impacto sostenible, mejoprando el importe cargado.
 
![Formato imagenes](/images/Captura%20de%20pantalla%202026-05-19%20113448.png)

**Reducción de peticiones**
Tiene un script <script src="/js/wave.min.js?v=3.3.0.4"></script>. ES una liberia que actualmente depende de toda pagina.
