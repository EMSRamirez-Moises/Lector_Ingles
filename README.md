Lectura progresiva para aprender inglés
El Modo Guía de `lector_corregido.html` funciona en tu navegador con reglas lingüísticas y compromise.js, incluido dentro del HTML. No necesita Gemini, una clave nueva ni el servidor de guía de la versión anterior. No utiliza audio.
La selección de texto sigue utilizando tu Google Translate y el guardado de frases que ya tenía el lector. La guía visual no envía párrafos al traductor ni consume su cuota.
Cómo usarlo
Publica `lector_corregido.html` como `index.html` en tu repositorio. Inicia sesión con tu cuenta de lector de Supabase. Más abajo se explica cómo trasladar tus libros anteriores.
Abre un libro desde el estante y activa Modo guía.
Empieza con Aprendizaje · 100 y Pausar entre bloques. Puedes bajar a Muy suave · 80. El número es el ritmo base de palabras por minuto; las pausas naturales hacen que el promedio real sea menor.
Pulsa Iniciar. Verás un bloque suave y la palabra actual subrayada. Al terminar un bloque, el reloj se pausa al comienzo del siguiente. Pulsa Continuar cuando estés listo.
Usa ‹ y › para repetir o avanzar bloques; ↺ vuelve al inicio de la sección. La barra permite buscar otra posición. También puedes tocar una palabra en el libro para comenzar allí.
Abre Entender bloque cuando necesites apoyo: muestra los bloques de esa oración, expresiones del diccionario y orientación SUVO. La ayuda pausa la lectura para que puedas pensar.
Selecciona una frase en el libro cuando necesites traducirla. La lectura se detiene mientras consultas el significado. Después pulsa Continuar.
Lee el bloque como una idea y pregúntate qué aporta. Repite cuando no conectes con el sentido. El reloj es una ayuda visual: no detecta si entendiste ni mide tu nivel.
Cuando te sientas cómodo, prueba Lectura continua. Avanza dentro de la sección y abre automáticamente la siguiente al terminar. El porcentaje corresponde a la sección actual, no al libro entero.
Qué se conserva y cómo se comporta
El texto del libro, sus signos, contracciones, comillas y formato original se conservan. El resaltado utiliza rangos sobre ese texto; no lo reescribe.
Pausar y continuar conservan la posición temporal. Cambiar el ritmo mantiene la palabra y la proporción de su duración que ya recorrió el reloj.
Se añade tiempo para palabras largas, puntuación, cambios de bloque y final de párrafo.
El scroll solo acompaña cambios de bloque que salen de la zona cómoda. No se ejecuta por cada palabra. Puedes desactivarlo en la ayuda.
Mover la página manualmente o salir de la pestaña pausa la guía. El regreso no reanuda automáticamente.
Se guardan tus preferencias y la palabra de lectura mediante un CFI de EPUB. Los EPUB se guardan en Supabase y se descargan al abrirlos en otro dispositivo con la misma cuenta. La copia descargada se reutiliza.
Los controles y el resaltado respetan el movimiento reducido. En navegadores sin CSS Custom Highlights se utiliza una capa visual que permite seguir seleccionando el texto.
Tu estante en Supabase
La URL y la clave publicable de tu proyecto ya están integradas. Este es un HTML estático: las variables `NEXT_PUBLIC_...` de Vercel no se insertan automáticamente en un archivo HTML. Para esta versión no necesitas configurarlas en Vercel ni instalar un framework.
Descarga `lector_corregido.html`, renómbralo a `index.html` y reemplaza el archivo de tu repositorio `emsramirez-moises/Lector_Ingles`. Guarda el cambio. Vercel volverá a desplegar si el proyecto está conectado a ese repositorio; GitHub Pages también debe publicar la versión actualizada.
Entra al lector con el correo y la contraseña del usuario creado en Supabase > Authentication > Users. Es una cuenta del lector, distinta de tu cuenta administradora de Supabase. Si aún no existe, créala en Add user > Create new user, con Auto Confirm User.
Añade un EPUB de hasta 50 MB. Puedes leerlo mientras se sube. Antes de pasar al teléfono, espera el mensaje Estante y progreso sincronizados con tu cuenta.
Abre el lector en el iPhone e inicia sesión con la misma cuenta. Al tocar Continuar leyendo, el EPUB se descarga de tu cuenta y se recupera la posición guardada. No necesitas adjuntarlo otra vez.
Pulsa ☆ para poner nombre y guardar un marcador. Esa ventana permite volver a una posición o borrar un marcador. Las notas y los temas nocturnos tienen campos preparados en la base de datos; esta interfaz todavía no incorpora su edición.
El ritmo, el modo de avance y el seguimiento con scroll también se sincronizan. Los datos locales se guardan por cuenta; al cerrar sesión se retiran de la pantalla el libro, la biblioteca, la traducción y los marcadores anteriores.
La sincronización ocurre tras los cambios, al regresar a la página, al recuperar la conexión, al abrir un libro y con Reintentar conexión. No es una transmisión en tiempo real entre dos dispositivos leyendo simultáneamente. Si dos dispositivos guardaron posiciones diferentes a partir del mismo progreso, aparece Resolver progreso: puedes usar la posición de la nube o la de este dispositivo. Esa elección evita sobrescribir silenciosamente un avance pendiente.
Trasladar tus EPUB anteriores
Abre la versión actualizada en el mismo dominio y navegador donde tenías los archivos. Entra a tu cuenta y pulsa Traer libros de este navegador. El lector copia los EPUB válidos a tu cuenta y conserva su posición si existe en el catálogo local anterior. Los archivos originales del navegador se conservan.
Los datos de GitHub Pages y Vercel pertenecen a dominios distintos. Si tus libros estaban en `https://emsramirez-moises.github.io/Lector_Ingles/`, entra primero por esa dirección actualizada para trasladarlos; después aparecerán también desde Vercel con la misma cuenta. Si ya no existe la copia del navegador, utiliza Añadir libro con tu EPUB original.
Los datos que estaban únicamente en Firebase no se importan automáticamente. Esta versión no lee ni modifica Firestore. El guardado de frases sigue utilizando Google Sheets y su copia local; no se ha trasladado a una tabla nueva de vocabulario.
Cuando se elimina un libro, el lector elimina el EPUB de Storage y su fila de catálogo; los marcadores asociados se borran por su relación con el libro. Si la conexión falla, conserva la operación pendiente para volver a intentarlo. Si una copia descargada está dañada, intenta recuperarla de Supabase.
Alcance de la ayuda lingüística
Los bloques son aproximaciones basadas en puntuación, conectores, grupos gramaticales y expresiones conocidas. Normalmente contienen entre 3 y 8 palabras; pueden ser más cortos o largos para conservar una expresión. No se cortan simplemente cada cinco palabras.
El diccionario inicial contiene expresiones y verbos comunes como show up, give up, pick up, put off y look forward to. Muestra significados habituales y ejemplos preparados; no determina automáticamente cuál sentido eligió el autor ni reconoce todos los modismos. Algunas coincidencias pueden ser literales.
SUVO es orientativo. En estructuras simples propone el sujeto, el grupo verbal y un posible objeto o complemento. En oraciones complejas utiliza preguntas para guiarte; no presenta un análisis incierto como seguro. No genera una traducción contextual dominicana de cualquier párrafo.
El límite de 16,000 palabras diarias de Google Translate no se modifica ni se sustituye. En el HTML recibido no había una implementación de ese contador: esta edición tampoco lo añade. Si tu versión publicada lo controla en otro archivo o servidor, conserva ese mecanismo.
La guía se procesa localmente. EPUB.js, JSZip, localForage y el cliente de Supabase se cargan desde sus CDN. Abrir la página por primera vez, iniciar sesión, descargar un libro y traducir requieren conexión. Un libro descargado se puede seguir leyendo si la página y la sesión continúan abiertas; los cambios locales pendientes se enviarán al volver la conexión. No se ha añadido una aplicación PWA para cargar toda la interfaz sin conexión.
Alternativas revisadas
Alternativa	Qué aporta	Encaje con este lector
Reglas propias y `Intl.Segmenter`	Palabras, oraciones, signos y pausas; permiten un reloj visual sin un modelo de IA.	Se utilizan para conservar el texto y construir la línea temporal. Por sí solas no interpretan el significado.
compromise.js	Etiquetas gramaticales y grupos nominales/verbales mediante reglas, en navegador.	Es la elegida como apoyo lingüístico. Está incluida en el HTML, sin llamadas externas para analizar párrafos.
NLTK con gramáticas de chunks	Permite definir patrones gramaticales clásicos en Python.	Alternativa válida, pero necesita un entorno Python o servidor y cambios de arquitectura para esta aplicación.
Fuentes primarias:
compromise: conceptos, reglas y limitaciones
compromise: API y grupos de palabras
Intl.Segmenter
NLTK: gramáticas de chunks
CSS Custom Highlight API
requestAnimationFrame
Verificación realizada
Se probaron el motor y el lector en Chromium, con vistas de escritorio y móvil. Pasaron las pruebas de pausa, reanudación, velocidad, navegación, resaltado, CFI exacto, selección, ayuda, paso entre secciones y scroll en un capítulo de más de 5,000 palabras.
La integración utiliza el SDK real de Supabase 2.117.3. Se probaron dos navegadores independientes contra Auth y Storage simulados y PostgreSQL local (PGlite), ejecutando el mismo SQL y sus políticas RLS: acceso por contraseña, subida, descarga privada, reutilización y reparación de la copia local, marcadores, preferencias, progreso sin conexión, conflictos, cambio de cuenta, eliminación e importación. Google Translate y Google Sheets se simularon para no consumir cuota ni guardar frases de prueba.
En tu proyecto real solo se hicieron comprobaciones de lectura: Auth responde, el acceso por correo está habilitado, los registros públicos están deshabilitados y las tres tablas rechazan consultas sin sesión. No se ha probado una sesión autenticada real ni Safari en un iPhone físico. Esta entrega no ha modificado tu sitio publicado ni escrito datos de prueba en tu proyecto.
