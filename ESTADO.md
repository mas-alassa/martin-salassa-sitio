# Sitio personal — Martín Salassa
## Estado del proyecto para retomar contexto

---

## Stack
- **Un solo archivo**: `index.html` (HTML + CSS + JS vanilla, sin frameworks)
- **Fuentes**: Archivo (headings, Google Fonts) + Space Grotesk (body)
- **Deploy**: Netlify → dominio `martinsalassa.com`
- **Repo**: `github.com/mas-alassa/martin-salassa-sitio` (privado → luego público)
- **Workflow**: editar `index.html` → `git push` → Netlify despliega automático (~30s)

---

## Posicionamiento (rediseño junio 2026)
Según `Nuevo Brief_MAS.txt`: el sitio pasó de "estoy buscando un nuevo trabajo" a una
propuesta de valor directa: **"Hago que tu empresa venda más y gaste menos."**
Los números/resultados son protagonistas; menos secciones, copy más corto.

---

## Diseño
- **Referencia visual**: Showcasy (showcasy.framer.website) — tipográfico, blanco/negro, bold
- **Paleta**: `--black: #0A0A0A` / `--white: #FAFAFA` / grises intermedios
- **Estilo secciones**: alternan fondo claro (`var(--gray-50)`) y blanco; "Mis últimos resultados" en negro
- **Tags de sección**: gris claro en fondos claros; **blanco** en secciones de fondo oscuro (decisión del brief, adaptada)
- **Cursor custom**: dot + ring con lerp, se vuelve blanco sobre fondos oscuros (detección por luminancia)
- **Animaciones**: fade-up on scroll (IntersectionObserver), ticker animado

---

## Estructura de secciones (en orden)
1. **Header** — sticky, blur on scroll, pill button "Hablemos" (→ WhatsApp); menú hamburguesa: Quién soy · Qué hago · Mis resultados · Hablemos (WhatsApp)
2. **Hero** — H1 "Hago que tu empresa venda más y gaste menos." + subtítulo (15 años…) + CTA "Tomemos un café". En mobile, gráfico wireframe `hero-graphic.png` **en flujo normal** arriba del titular (antes era absolute y se superponía con el H1 largo)
3. **Ticker** — banda negra animada: Ventas · Crecimiento · Operaciones · Estrategia de negocio · Equipos · Mendoza · LATAM · Startups y pymes
4. **Mis últimos resultados** (`#mis-resultados`) — fondo negro, tag blanco, sin H2. 4 ítems (`.result-item`): línea grande bold + contexto gris. Sin KPI counters (se eliminó ese JS)
5. **Qué hago** (`#que-hago`) — una sola frase como big-statement: "Me dedico a acelerar las ventas de las empresas con las que trabajo."
6. **Quién soy** (`#quien-soy`) — grid 58/42, texto nuevo (integra el reconocimiento del CEM) + foto `Foto4-transparent.png`
7. **CTA final** (`#hablemos`) — "Si te interesa, hablemos y veamos si tiene sentido hacer algo juntos." + CTA "Tomemos un café"
8. **Footer** — "Gracias." / email grande / nav (4 links) / LinkedIn + Instagram / teléfono / copyright

### Secciones eliminadas en el rediseño
"Lo que cambia cuando estoy" (acordeón), "Dónde puedo sumar" (5 áreas),
"Lo que hice" (timeline con KPI counters), "Reconocimiento" (integrado en Quién soy).
Se limpió el CSS y JS huérfano (service-*, accordion-*, award-*, metric*, counters).

---

## CTAs y links
- **Botones "Tomemos un café" / "Hablemos"** → `https://wa.me/5492615981450` (WhatsApp, `target="_blank"`)
- **Email footer** → `mailto:hola@martinsalassa.com` (único link a mail)
- **LinkedIn** → `https://www.linkedin.com/in/martinsalassa`
- **Instagram** → `https://www.instagram.com/martin.salassa`

---

## Imágenes en el repo
| Archivo | Uso |
|---------|-----|
| `Foto1.png` | Ceremonia reconocimiento (no usada actualmente) |
| `Foto2.png` | Foto con camiseta #5 en estadio (no usada) |
| `Foto3.png` | Foto con camiseta #5 interior (no usada) |
| `Foto4.png` | Foto original con fondo blanco (no usada) |
| `Foto4-transparent.png` | ✅ Usada en "Quién soy" — fondo removido con Python/PIL |
| `hero-graphic.png` | ✅ Gráfico wireframe hero mobile + imagen OG |
| `Prueba-cuerpo-entero.png` | Foto cuerpo entero alternativa (no usada) |

---

## Decisiones técnicas tomadas
- **Foto sin fondo**: procesada con Python/PIL (no remove.bg) — guardada como `Foto4-transparent.png`
- **Figura en Quién soy**: `width: 90%; height: auto` (no height fijo) para que llene la columna proporcionalmente
- **No se usó sticky/parallax** para la figura — intentado 3 veces, descartado por complejidad
- **Mobile**: figura centrada 240px max-width, sin columnas; gráfico hero en flujo (no absolute)
- **Meta tags / OG**: description actualizado al nuevo posicionamiento
- **Git config**: usuario `mas-alassa`, email `martinsalassa@gmail.com`

---

## Pendientes / ideas anotadas
- [ ] Actualizar la landing `/tech` al nuevo posicionamiento (hoy sigue con el copy viejo)
- [ ] Foto de Martín: considerar una toma más profesional cuando esté disponible
- [ ] Potencial: animación de entrada al hero (texto que aparece letra a letra o por palabras)

---

## Cómo retomar
```
"Seguimos con mi sitio en C:\Proyectos\MAS. 
Repo: github.com/mas-alassa/martin-salassa-sitio
Lee el ESTADO.md y el index.html para ponerte al día."
```
