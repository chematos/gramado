# Proyecto: Planificación Semana Santa — Gramado + Canela

## Contexto

Viaje grupal a **Gramado (RS, Brasil)** durante **Semana Santa 2026** (aprox. 31 mar – 5 abr).
Grupo: **3 familias de amigos** → 6 adultos + 6 niños (edades: 3 a 10 años).

**Objetivos del viaje:**
- Actividades "kid-friendly" sin esperas largas ni estrés logístico
- Equilibrar parques de pago con paseos gratuitos (lagos, plazas)
- Tener un plan lluvia para cada día
- Facilitar la toma de decisiones conjunta entre las 3 familias

**Idioma del proyecto:** Español (registro conversacional, orientado a familias)

---

## Páginas del proyecto

### 1. `index.html` — Criba de parques
**Scope:** Comparador interactivo de los 4 parques principales recomendados para el grupo.
Permite filtrar por nivel de colas (baja / media), tipo de espacio (interior / exterior) y búsqueda libre.
Incluye: precios, tips anti-estrés, links a entradas y videos de YouTube.

**Parques incluidos:**
- Mini Mundo (Gramado)
- Terra Mágica Florybal (Canela)
- Acquamotion (Gramado) — parque acuático cubierto
- Vila da Mônica (Gramado)

---

### 2. `gramado_lagos.html` — Lagos y paseos gratuitos
**Scope:** Guía de los lagos y paseos al aire libre gratuitos o de bajo costo. Ideal para días de transición entre parques o cuando el grupo necesita "bajar revoluciones".

**Lugares incluidos:**
- Lago Negro (paseo + pedalinho)
- Lago Joaquina Rita Bier (paseo express, fotogénico)
- Bonus: plazas, miradores, picnic

---

### 3. `itinerario_a.html` — Itinerario Opción A (5 días, 4 parques, intensivo)
**Scope:** Propuesta de itinerario día por día para los 5 días de viaje. Primera opción de varias que se van a comparar. Incluye horarios sugeridos, costos estimados por día, plan lluvia y tips por franja horaria.

**Características de esta opción:**
- 5 días (1 llegada + 4 días de actividad)
- Cubre los 4 parques principales de `index.html`
- Mezcla exterior e interior para mitigar riesgo climático
- Foco en maximizar experiencia con niños (llegar temprano, evitar picos)

---

## Design system

| Token | Valor | Uso |
|-------|-------|-----|
| `--bg` | `#0b0f14` | Fondo principal |
| `--card` | `#121823` | Fondo de tarjetas |
| `--muted` | `#9fb0c3` | Texto secundario |
| `--text` | `#e8f0fa` | Texto principal |
| `--pill` | `#1f2a3a` | Pills / tags |
| `--ok` | `#1f9d6a` | Indicador positivo (verde) |
| `--mid` | `#d7a300` | Indicador medio (dorado) |
| `--bad` | `#e05a5a` | Indicador negativo (rojo) |
| `--line` | `#243247` | Bordes y divisores |
| `--link` | `#7cc4ff` | Links |

**Tipografía:** `system-ui, -apple-system, Segoe UI, Roboto, Inter, Arial, sans-serif`
**Layout:** max-width 1100px, grid 12 columnas, gap 14px
**Breakpoint mobile:** 860px
**Border-radius:** 18px (cards), 14px (thumbs/media), 999px (pills), 12px (botones)

---

## Convenciones de contenido

- Emoji + texto para escaneo rápido
- Tono conversacional, directo, orientado a reducir estrés
- Precios en BRL (R$), estimados y con fuente indicada
- Tips siempre orientados a "3 familias + niños pequeños"
- Siempre incluir un "plan lluvia" o nota sobre clima
- Links externos siempre con `target="_blank" rel="noopener"`

---

## Próximas páginas planificadas

- `itinerario_b.html` — Opción B (variante a comparar con Opción A)
- `itinerario_c.html` — Opción C (si se crea una tercera variante)
- Posible página de **logística**: traslados, alojamiento, supermercado
