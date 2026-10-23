# 🦁 Museo del Emprendimiento: el Safari

Museo virtual interactivo para recorrer, en primera persona (3D) o desde arriba (2D), los conceptos clave del emprendimiento a través de la metáfora del **safari emprendedor**. Incluye 16 obras con información investigada, una sala de casos reales de empresas colombianas y un quiz integrado.

> Proyecto de la exposición del **Grupo 5**, Universidad EAN (Bogotá, Colombia).

**Demo:** 

---

## 🎯 ¿Qué se aprende en el museo?

El museo tiene una entrada y 4 salas temáticas:

| Sala | Contenido |
|---|---|
| **Entrada** | Bienvenida, origen del safari (Birch y Kantis) y la sala de juegos con el quiz |
| **Sala 1 · Dinámicos** | Qué es un emprendimiento dinámico; ratones, elefantes, gacelas, canguros, delfines y unicornios |
| **Sala 2 · Oportunidad vs. necesidad** | Definiciones del GEM, fuerzas *push* y *pull*, emprendimiento procíclico y contracíclico |
| **Sala 3 · Colombia en datos** | La TEA, motivaciones para emprender y comparación con otros países de la región |
| **Sala 4 · Casos reales** | Tienda de barrio (ratón), Ecopetrol (elefante), Bold (gacela), Rappi y Habi (unicornios) |

Al acercarte a cada obra se abre un panel con su descripción. Al final puedes poner a prueba lo aprendido con el **quiz de 10 preguntas**, con explicación de cada respuesta y puntaje final.

---

## 🕹️ Controles

### Versión 3D

| Acción | Computador | Celular |
|---|---|---|
| Avanzar / retroceder | `W` / `S` o flechas ↑ ↓ | Joystick virtual (abajo a la izquierda) |
| Moverse de lado | `A` / `D` | Joystick |
| Girar | `←` / `→` o arrastrar el mouse | Arrastrar con el otro dedo |
| Mirar arriba/abajo | Arrastrar el mouse | Arrastrar con el dedo |

Incluye minimapa, barra de progreso de obras vistas y colisiones con las paredes.

### Versión 2D

Vista desde arriba. Muévete con `WASD` o las flechas (en celular, toca y mantén). 

---

## 🛠️ Tecnologías

- **HTML, CSS y JavaScript** puros, sin proceso de compilación.
- **[Three.js r128](https://threejs.org/)** para el museo 3D (se carga desde cdnjs).
- **Canvas 2D** para las ilustraciones de las obras y la versión 2D.
- Las imágenes de las obras se generan en el navegador (degradados y emojis), sin archivos externos.

---

## 📁 Estructura del repositorio

```
.
├── index.html          # Museo 3D (versión principal)
├── museo-2d.html       # Versión 2D vista desde arriba
└── README.md
```

> Si tus archivos tienen otros nombres, ajusta esta sección.

---

## 🚀 Cómo ejecutarlo

1. Clona el repositorio:
   ```bash
   git clone https://github.com/<tu-usuario>/<tu-repositorio>.git
   ```
2. Abre `index.html` en tu navegador (Chrome, Edge, Firefox o Safari recientes).
3. No requiere instalar nada. La versión 3D necesita conexión a internet para descargar Three.js.

### Publicarlo con GitHub Pages

1. Ve a **Settings → Pages**.
2. En *Source* elige la rama `main` y la carpeta `/ (root)`.
3. Guarda. En unos minutos tendrás el museo en `https://<tu-usuario>.github.io/<tu-repositorio>/`.

---

## ✏️ Cómo editar el contenido

Todo el contenido está en el arreglo `S` del archivo HTML. Cada obra es un objeto:

```js
{
  r: "Sala 1 · Emprendimientos dinámicos", // sala
  t: "Título de la obra",
  d: "Descripción que aparece en el panel.",
  c: ["#2fa36b", "#0e5c4a"],               // colores del degradado
  e: "🦌📈🚀💡"                            // emojis de la ilustración
}
```

El quiz está en el arreglo `Q`, con el formato `[pregunta, [opciones], índiceCorrecto, explicación]`.

---

## 📚 Fuentes principales

- Global Entrepreneurship Monitor (GEM) Colombia. (2024). *Dinámica de la actividad empresarial en Colombia 2023-2024: Enfrentando desafíos*. https://gemconsortium.org/report/reporte-gem-colombia-2023-2024
- Goyeneche, J. J. (2022, 7 de julio). Un safari de emprendimientos en Colombia. *Asuntos Legales*. https://www.asuntoslegales.com.co/analisis/juan-jose-goyeneche-2581234/un-safari-de-emprendimientos-en-colombia-3397991
- Forbes Colombia. (2026, 7 de abril). *Seis colombianas figuran entre las compañías de mayor crecimiento de Endeavor a nivel mundial*. https://forbes.co/2026/04/07/emprendedores/seis-colombianas-figuran-entre-las-companias-de-mayor-crecimiento-de-endeavor-a-nivel-mundial/
- Valora Analitik. (2021, 5 de mayo). Colombia tiene la cuarta mejor actividad emprendedora en el mundo. https://www.valoraanalitik.com/colombia-tiene-la-cuarta-mejor-actividad-emprendedora-en-el-mundo/

Las cifras provienen de informes de distintos años y se indican como tal dentro del museo.

---

## ⚠️ Limitaciones conocidas

- La versión 3D necesita internet para cargar Three.js. La versión 2D funciona sin conexión.
- Las ilustraciones son procedurales (degradados y emojis), no imágenes reales.
- La distribución exacta de motivaciones para emprender en Colombia no está con cifras; consulta el informe GEM Colombia completo.
- En computadores de bajo rendimiento el modo 3D puede ir menos fluido.
