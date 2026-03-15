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

---

## Reglas de contenido fijas (aplicar a todos los itinerarios)

- **Parque do Caracol (Canela)** debe aparecer en todos los itinerarios. Es una cascada de 131 m en mata nativa, con sendero fácil apto para todas las edades. Entrada ~R$50 adulto / ~R$25 niño. Hay bondinho y zip line opcionales.
- **Canela** debe aparecer como destino en todos los itinerarios (Parque do Caracol y/o centro + Catedral de Pedra).
- Los itinerarios siempre comienzan el **domingo 29 de marzo al mediodía** (llegada desde Montevideo) y terminan el **viernes 3 de abril** (checkout + regreso en auto a Montevideo).

## Sistema de votos por día

Cada día de itinerario tiene una sección de "me gusta" con 6 botones personales:
- **Personas:** Nano, Ina, Martín, Caro, Emi, Chema
- Cada persona vota solo por sí misma (sin auth, basado en confianza)
- Los votos se guardan en `localStorage` con clave `v_{page_id}` (JSON)
- Los botones se colorean con el color de cada persona cuando están activos
- Se muestra quién votó con corazón rojo: "❤️ Nano, Martín, Caro"

## Páginas del proyecto (actualizadas)

### 4. `itinerario_b.html` — Itinerario Opción B (6 días, 2 parques, relajada y low-cost)
**Scope:** Alternativa más económica (~40% menos en entradas). Solo 2 parques de pago (Mini Mundo + Vila da Mônica), más actividades gratuitas o baratas.

**Días:**
- Día 1: Llegada + Lago Joaquina
- Día 2: Canela completo (Parque do Caracol + Catedral de Pedra + centro)
- Día 3: Gramado low-cost (tour de fábricas de chocolate + Lago Negro)
- Día 4: Mini Mundo + tarde libre en el centro
- Día 5: Vila da Mônica (Jueves Santo)
- Día 6: Checkout + regreso Montevideo

---

## Especificaciones de restaurantes

### Perfil del grupo
- **Tamaño:** 6 adultos + 6 niños (12 personas en total, siempre)
- **Niños:** 6, edades 3–10 años — se impacientan con demoras largas
- **Estilo:** Familias de clase media, comen bien pero sin extravagancia ni precios altos
- **Formato preferido:** Lugares cómodos, familiares, con servicio ágil (buffet o platos que salen rápido)
- **Evitar:** Restaurantes de alta cocina / fine dining, lugares con demoras largas, locales muy pequeños sin espacio para grupo grande

### Criterios de selección
- Capacidad para grupos de 12 (consultar reserva previa cuando aplique)
- Precio estimado moderado: ~R$ 40–90 por persona adulta, ~R$ 20–40 por niño
- Buena para niños: menú infantil, espacio amplio, ambiente informal
- Servicio relativamente rápido (no más de 30–40 min de espera para comer)
- Dentro o cerca de la zona de actividad del día

### Organización por zona
Los restaurantes se agrupan por la zona de actividad del día:
- **Gramado centro** — días con Lago Joaquina, Mini Mundo, chocolates, centro
- **Zona Lago Negro** — días de paseo por el lago
- **Zona Acquamotion** — día del parque acuático
- **Canela centro** — días de Caracol, Catedral, Terra Mágica
- **Opciones de noche** — cenas grupales especiales (reservar con anticipación en Semana Santa)
- **Opciones en ruta** — snacks y paradas rápidas entre actividades

### Información a mostrar por restaurante
- Nombre, especialidad, zona/dirección
- Precio estimado: por familia (2A+2N) y por grupo completo (6A+6N)
- Link web oficial + Maps
- Si requiere reserva + horarios
- Evaluación de adecuación para niños y grupos grandes

---

## Páginas del proyecto (actualizadas)

### 5. `plan_actividades.html` — Votación de actividades
**Scope:** Todas las actividades posibles del viaje como unidades votables independientes. Ranking en vivo. Alimenta el itinerario definitivo.

### 6. `restaurantes.html` — Opciones de comida por zona *(próxima)*
**Scope:** Restaurantes y opciones de comida organizados por zona de actividad. Con votos por persona, precio estimado, maps y links.

---

## Próximas páginas planificadas

- `itinerario_c.html` — Opción C (si se crea una tercera variante)
- Posible página de **logística**: traslados, alojamiento, supermercado
