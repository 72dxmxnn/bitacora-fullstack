# Bitácora Full Stack – Josué Daniel Turcios Galdámez

Repositorio de evidencias del curso Desarrollo Web [Full Stack Junior].

---

## Datos del estudiante

| Campo               | Información                              |
| ------------------- | ---------------------------------------- |
| **Nombre**          | Josué Daniel Turcios Galdámez            |
| **Usuario GitHub**  | [@72dxmxnn](https://github.com/72dxmxnn) |
| **Curso**           | Desarrollo Web Full Stack Junior         |
| **Fecha de inicio** | 13 de noviembre                          |

---

## Objetivo del repositorio

Documentar, día a día, los temas vistos en clase, las prácticas realizadas y lo que aprendí, como evidencia de mi progreso en el curso.

---

## Tabla de contenido

- [Día 1 – 13 de noviembre: Fundamentos de la web](#día-1--13-de-noviembre-fundamentos-de-la-web)
- [Esquema cliente-servidor](#esquema-cliente-servidor)
- [Dominio, hosting y servidor](#dominio-hosting-y-servidor)
- [Análisis con DevTools](#análisis-con-devtools)
- [Reflexión sobre el uso de IA](#reflexión-sobre-el-uso-de-ia)

---

## Día 1 – 13 de noviembre: Fundamentos de la web

### Esquema cliente-servidor

![Esquema cliente-servidor](esquema-cliente-servidor.png)

Recorrido paso a paso:

1. Escribo la URL en el navegador, por ejemplo `https://www.fusalmo.org`.
2. El navegador le pregunta al servidor DNS cuál es la IP de ese dominio y el DNS se la devuelve.
3. Con la IP, el navegador manda una solicitud HTTP con el método GET para pedir la página.
4. El servidor web busca el archivo y responde con el código 200 OK y el HTML.
5. El navegador lee el HTML y pide lo que falta: CSS, JavaScript e imágenes.
6. Cuando ya tiene todo, el navegador dibuja la página en la pantalla.

### Dominio, hosting y servidor

| Criterio                      | Dominio                                                                  | Hosting                                                                                             | Servidor                                                                               |
| ----------------------------- | ------------------------------------------------------------------------ | --------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------- |
| ¿Qué es?                      | El nombre del sitio, el que escribimos en el navegador. Apunta a una IP. | Un servicio que alquila espacio en un servidor para guardar los archivos del sitio.                 | La computadora que guarda los archivos y contesta cuando un navegador los pide.        |
| ¿Para qué sirve?              | Para no tener que aprenderse la IP. Es como la dirección de una casa.    | Para que el sitio esté en línea todo el día sin dejar mi computadora encendida. Es como el terreno. | Para recibir las solicitudes y mandar los archivos. Es la casa.                        |
| ¿Tiene costo? ¿Cuánto aprox.? | Sí, se paga cada año. Un .com anda entre $10 y $15 al año.               | Hay gratis para sitios sencillos (GitHub Pages, Netlify) y de pago desde $3 a $10 al mes.           | Casi siempre viene incluido en el hosting. Uno propio (VPS) sale desde unos $5 al mes. |
| Ejemplo real                  | `fusalmo.org`                                                            | GitHub Pages, Hostinger, Netlify                                                                    | Un servidor Linux con Apache o Nginx                                                   |

### Análisis con DevTools

- Sitio analizado: Aula Virtual de FUSALMO, página "Mis cursos" (https://aula-virtual.fusalmo.org/my/courses.php)
- Número de solicitudes: 31
- Método y código de estado de la primera solicitud: GET, 200 OK
- Tres tipos de archivo recibidos: JavaScript (.js), fuentes (.woff2) e imágenes (.png)
- Tiempo de carga: 0.6 segundos
- Observación: cargó muy rápido porque varios archivos ya estaban en la caché del navegador, solo se descargaron unos 20 KB. También vi que después de cargar se siguen haciendo algunas solicitudes en segundo plano, creo que son para las notificaciones.

### Reflexión sobre el uso de IA

Usé Claude. Primero le pedí que me dijera qué pedía la guía, porque yo solo tenía hecho el diagrama. Cuando lo revisó me di cuenta de que mi diagrama no tenía el servidor DNS, ni los pasos numerados, ni el GET y el 200 OK, y yo pensaba que ya estaba completo. Con eso armamos el esquema nuevo.

También me ayudó con la tabla y a sacar los datos de carga del Aula Virtual. Los datos los revisé después con F12 en la pestaña Network, y la tabla la cambié para que quedara como yo lo explicaría. Los precios los dejé como aproximados porque cada proveedor cobra distinto.

Lo que me quedó es que la IA sirve para ver lo que se me pasa, pero si no reviso lo que me da no sabría explicar el esquema en clase.

---

_Esta bitácora se actualiza al final de cada clase._
