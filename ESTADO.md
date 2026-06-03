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

## Diseño
- **Referencia visual**: Showcasy (showcasy.framer.website) — tipográfico, blanco/negro, bold
- **Paleta**: `--black: #0A0A0A` / `--white: #FAFAFA` / grises intermedios
- **Estilo secciones**: alternan fondo claro (`var(--gray-50)`) y blanco
- **Cursor custom**: dot + ring con lerp, se vuelve blanco sobre fondos oscuros (detección por luminancia)
- **Animaciones**: fade-up on scroll (IntersectionObserver), ticker animado, KPI counters

---

## Estructura de secciones (en orden)
1. **Header** — sticky, blur on scroll, pill button "Hablemos" (→ WhatsApp)
2. **Hero** — "Hola." / "Estoy buscando un nuevo trabajo." / CTA
3. **Ticker** — banda negra animada: "Mendoza, Argentina · 15 años de experiencia · Operaciones · Estrategia de negocio · Equipos y liderazgo · Startups y pymes"
4. **Quién soy** — grid 58/42, texto izq + foto `Foto4-transparent.png` der, `mix-blend-mode` removido (PNG ya tiene alpha transparente procesado con PIL)
5. **Qué hago** — "Lo que cambia cuando estoy."
6. **Dónde puedo sumar** — 5 items con categoría (Administración/Finanzas/Ventas/Tecnología/Equipo), layout de filas con borde izquierdo en hover
7. **Lo que hice** — fondo negro, 3 casos con KPI counters animados (Global Fan / Cárbula / Antes de todo eso)
8. **Reconocimiento** — card simple, texto del Consejo Empresario Mendocino 2021
9. **Cierre** — "Estoy buscando mi próximo desafío."
10. **Footer** — "Gracias." / email grande / nav / LinkedIn + Instagram / teléfono / copyright

---

## CTAs y links
- **Botones "Hablemos"** → `https://wa.me/5492615981450` (WhatsApp, `target="_blank"`)
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
| `Prueba-cuerpo-entero.png` | Foto cuerpo entero alternativa (no usada) |

---

## Decisiones técnicas tomadas
- **Foto sin fondo**: procesada con Python/PIL (no remove.bg) — guardada como `Foto4-transparent.png`
- **Figura en Quién soy**: `width: 90%; height: auto` (no height fijo) para que llene la columna proporcionalmente
- **No se usó sticky/parallax** para la figura — intentado 3 veces, descartado por complejidad
- **Mobile**: figura centrada 240px max-width, sin columnas
- **Git config**: usuario `mas-alassa`, email `martinsalassa@gmail.com`

---

## Pendientes / ideas anotadas
- [ ] Foto de Martín: considerar una toma más profesional cuando esté disponible
- [ ] Sección "Quién soy": frase protagonista definitiva aún por pulir
- [ ] Sección "Lo que hice": frase protagonista ("Resultados que hablan por sí solos" fue descartada, pendiente definitiva)
- [ ] Potencial: agregar animación de entrada al hero (texto que aparece letra a letra o por palabras)

---

## Cómo retomar
```
"Seguimos con mi sitio en C:\Proyectos\MAS. 
Repo: github.com/mas-alassa/martin-salassa-sitio
Lee el ESTADO.md y el index.html para ponerte al día."
```
