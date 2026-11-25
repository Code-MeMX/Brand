# DESIGN.md — Sistema de Diseño e Identidad de Marca CODE ME

> **Fuente única de verdad (Single Source of Truth)** para diseñadores, desarrolladores frontend, creadores de contenido e inteligencias artificiales que produzcan activos para **CODE ME**.
> Basado en la documentación oficial de [docs.code-me.club](https://docs.code-me.club) y los tokens activos en [`src/css/custom.css`](./src/css/custom.css).

---

## 1. Identidad Corporativa y Filosofía (Brand Kernel)

### Nombre y Sintaxis
- **Marca:** `CODE ME` / `Code·Me` (Pronunciación: `/koʊd miː/`).
- **Concepto dual:**
  1. **The Command (Imperativo):** *"Prográmame / Constrúyeme"* — acción de transformación y regeneración constante (versión 2.0).
  2. **The User (Identidad):** *"Code & Me"* — apropiación tecnológica; el código como extensión creativa personal.
- **Variantes sintácticas permitidas en UI/avatares/copy:** `>_ Code_Me`, `>_ Code-Me`, `>_`, `>_ code.me()`.

### Propósito y Valores
- **Misión:** *"Hackear la desigualdad"* — democratizar la educación tecnológica en México para transformar a niños y adolescentes de usuarios pasivos (NPCs) en creadores activos (Admins / Root).
- **Visión:** *"Compilar un nuevo México"* — convertir la programación en una habilidad universal y formar jóvenes resilientes que exporten código.
- **Valores (Drivers):**
  1. **Resiliencia (`MODE: AXOLOTL`):** El error (`Bug`) no es fracaso, es iteración y regeneración.
  2. **Inclusión (`MODE: OPEN_SOURCE_MINDSET`):** Cero *gatekeeping*, colaboración radical (*Pair Programming*).
  3. **Ingenio (`MODE: MAKER_MENTALITY`):** Resolver problemas reales con código; ingenio mexicano potenciado por software.
  4. **Valentía Digital (`MODE: BRAVE_HEART`):** Espacios seguros para experimentar, romper y desplegar (*BETA is beautiful*).

### Taglines
| Contexto / Audiencia | Tagline | Uso recomendado |
| :--- | :--- | :--- |
| **Principal (`main()`)** | `"REGENERA TU FUTURO."` | Manifiesto central, marca institucional, hero general. |
| **Lúdico (8–15 años / Gamers)** | `"NO SOLO JUEGUES GACHO, CRÉALO."` | YouTube, TikTok, Discord, ads para jóvenes. |
| **Emocional / Aspiracional** | `"TU SUPERPODER ES EL CÓDIGO."` | Instagram, posters de salón, kick-off de cursos. |
| **Impacto Social / PR** | `"HACKEA LA DESIGUALDAD."` | Prensa, pitch decks, RSE, conferencias. |
| **Institucional / B2B** | `"EL LENGUAJE QUE COMPILA EL NUEVO MUNDO."` | Web corporativa, firmas ejecutivas, alianzas tech. |

### Pilares Conceptuales de Diseño (*Cyberpunk-Mexa / Development-First*)
1. **Caos Ordenado (`Grid_System: "Flexible"`):** Densidad visual inspirada en mercados mexicanos y cableado cyberpunk, pero 100% regida por retícula geométrica funcional.
2. **Humanismo Aumentado (`User_Focus()`):** Nunca tecnología fría vacía; siempre humanos cálidos (estudiantes, devs) potenciados por capas tecnológicas neón.
3. **El Glitch como Metáfora de Evolución (`Bug -> Feature`):** Scanlines, aberración cromática y ruido sutil como símbolo del aprendizaje iterativo (`v1.0` → `v2.0`).

---

## 2. Sistema Cromático (Color System)

CODE ME es una marca **Dark Mode nativa** construida bajo el principio de salud visual (*Development-First*). Existen dos ambientes estrictamente separados: **RGB (Pantallas / Luz)** y **CMYK (Impresión / Tinta)**. Nunca cruces ambos perfiles en un mismo archivo de producción.

### 2.1 Paleta Digital Principal (RGB / Emisiva)

| Token CSS | Nombre | HEX | Rol | Uso Estricto |
| :--- | :--- | :--- | :--- | :--- |
| `--cm-obsidiana` | **Obsidiana Digital** | `#0F172A` | Fondo base (`bg`) | Lienzo principal web, apps, presentaciones. **Prohibido `#000000` plano** en UI. |
| `--cm-rosa-ajolote` | **Rosa Ajolote** | `#FF2A6D` | Acento primario (`CTA`) | Botones de acción críticos, alertas graves, H3, piel de Bitxo. Dosificar. |
| `--cm-cyan-electrico` | **Cyan Eléctrico** | `#00F0FF` | Acento técnico (`UI`) | Enlaces, bordes HUD, H2, estados `:hover`/`:focus-visible`, goggles de Bitxo. |
| `--cm-verde-terminal` | **Verde Terminal** | `#05FF00` | Éxito (`200 OK`) | Confirmaciones, barras de progreso, checks, H4, estado feliz de Bitxo. |
| `--cm-blanco-consola` | **Blanco Consola** | `#F8FAFC` | Tipografía base | Títulos H1/H5 y lectura principal. Blanco roto anti-halo (evita `#FFFFFF` puro en Dark Mode). |

### 2.2 Tokens Secundarios y Estados UI (Implementados en `src/css/custom.css`)

| Propósito | Valor | Uso |
| :--- | :--- | :--- |
| **Texto cuerpo Dark Mode** | `#E2E8F0` *(Slate 200)* | Párrafos largos (`--ifm-font-color-base`) con contraste WCAG óptimo. |
| **Texto secundario / Menú / Lead** | `#94A3B8` *(Slate 400)* | Descripciones, `.lead-text`, `.spec-label`, menús inactivos. |
| **Texto terciario / Metadatos** | `#64748B` *(Slate 500)* | Notas pequeñas, sufijos, labels de soporte. |
| **Fondo Showcase / Profundo** | `#020617` *(Slate 950)* | Contenedores de exhibición de logotipo. |
| **Glassmorphism BG** | `rgba(15, 23, 42, 0.8)` | Tarjetas y contenedores translúcidos con `backdrop-filter: blur(12px)`. |
| **Glassmorphism Border** | `rgba(255, 255, 255, 0.1)` | Bordes sutiles de UI (`--glass-border`; variante docs: `rgba(248, 250, 252, 0.15)`). |
| **Selección de texto (`::selection`)** | `rgba(0, 240, 255, 0.3)` | Fondo de selección con texto `--cm-blanco-consola`. |
| **Escala Rosa (Infima)** | Dark `#E61958` / Darker `#CC154E` / Darkest `#990F3B` / Light `#FF4D84` / Lighter `#FF6696` / Lightest `#FF99BA` | Estados hover/active de componentes basados en primario. |
| **Warning (Admonitions)** | `#FFB800` | Borde izquierdo de advertencias. |
| **Danger Custom** | `#FF4D4D` | Botones destructivos o de error (`.button--danger-custom`). |

### 2.3 Paleta Física / Impresión (CMYK "Hard Patch")

Los tonos neón RGB están fuera de gama (*Out of Gamut*) en impresión convencional. Para lonas, papelería, vinil y offset, usar obligatoriamente:

| Nombre | Simulación HEX | Fórmula CMYK | Tinta Directa (Pantone) | Uso Impreso |
| :--- | :--- | :--- | :--- | :--- |
| **Obsidiana Rich Black** | `#000000` | `C:80 M:70 Y:50 K:100` | `Black 6 C` | Negro profundo de alto contraste. **Nunca usar `K:100` solo**. |
| **Rosa Magenta de Proceso** | `#E6007E` | `C:0 M:100 Y:10 K:0` | `Neon Pink 021 C` | Encabezados y logos impresos (usar Pantone fluorescente en offset/serigrafía si hay presupuesto). |
| **Cyan de Proceso** | `#00AEEF` | `C:100 M:0 Y:0 K:0` | `Neon Cyan 021 C`* | Diagramas de red, flechas técnicas, líneas finas. |
| **Verde Lima Analógico** | `#80C342` | `C:50 M:0 Y:100 K:0` | `Neon Green 021 C`* | Checkmarks, badges de éxito en diplomas y sellos OK. |

> *Nota técnica:* En `docs/visual/colores/cmyk.mdx`, las etiquetas Pantone de Cyan y Verde aparecen invertidas en el JSX de las tarjetas; la correspondencia cromática correcta es Cyan → `Neon Cyan` y Verde → `Neon Green`.

#### Protocolo Eco-Friendly (`Ink_Saver_Mode = true`) / Modo Blueprint
Para manuales escolares, exámenes y documentos físicos extensos o bajo luz solar directa:
- Invertir polaridad: **Fondo Blanco / Papel Ingeniería (`#FFFFFF` o papel bond roto)** + **Texto Negro (`#000000`)**.
- Usar acentos CMYK exclusivamente en títulos, vectores, QR y llamadas críticas (estética de plano arquitectónico).

### 2.4 Matriz de Contraste, WCAG y Ergonomía Visual

| Fondo (`Capa_Cero`) | Texto / Icono (`Capa_Uno`) | Aplicación |
| :--- | :--- | :--- |
| **Obsidiana Digital** (`#0F172A`) | Blanco Consola, Cyan Eléctrico, Rosa Ajolote | Setup Dark Mode principal. Blanco/Obsidiana > **15:1** (AAA). |
| **Rosa Ajolote** (`#FF2A6D`) | **Obsidiana Digital** (preferente), Blanco | Botones CTA críticos. |
| **Cyan Eléctrico** (`#00F0FF`) | **Obsidiana Digital** | Etiquetas, hover states, navegación activa. |
| **Verde Terminal** (`#05FF00`) | **Obsidiana Digital** | Badges de éxito, indicadores online, loaders. |
| **Blanco Consola** (`#F8FAFC`) | Obsidiana Digital, Rosa | Exclusivo imprenta / modo administrativo (*Ink Mode*). |

#### Reglas Obligatorias de Salud Visual y Accesibilidad
1. **Regla de la Sangre Negra:** Todo botón sólido o badge en color neón vivo (`Rosa`, `Cyan`, `Verde`) **DEBE** llevar texto en **Obsidiana Digital (`#0F172A`)** con `font-weight: 800`.
2. **Lectura larga:** Solo `Blanco Consola` (`#F8FAFC`) o `#E2E8F0` sobre `Obsidiana Digital` (`#0F172A`). Nunca párrafos largos en Rosa, Cyan o Verde.
3. **Prevención de Efecto Halo (Astigmatismo):** Evitar `#FFFFFF` puro sobre `#000000` puro.
4. **Daltonismo:** La jerarquía visual debe depender de **luminosidad perceptual** (claro vs. oscuro), no solo del matiz de color.
5. **Teclado (`:focus-visible`):** `outline: 2px solid #00F0FF; outline-offset: 4px; border-radius: 2px;`.

#### Combinaciones Prohibidas (`Syntax Errors`)
- **Rosa (`#FF2A6D`) sobre Verde (`#05FF00`)** o viceversa: Vibración cromática / efecto Moiré psicológico (fatiga ocular inmediata). Separar siempre con padding/filetes Obsidiana.
- **Cyan (`#00F0FF`) sobre Blanco (`#FFFFFF`):** Contraste `< 3:1` (FAIL WCAG); el texto desaparece.
- **Blanco (`#F8FAFC` / `#FFFFFF`) sobre Verde Terminal (`#05FF00`):** Pérdida total de definición; usar siempre texto Obsidiana.

---

## 3. Sistema Tipográfico (Typography)

### Importación (Google Fonts)
```css
@import url('https://fonts.googleapis.com/css2?family=JetBrains+Mono:wght@400;700;800&family=Montserrat:wght@400;600;700;800&family=Saira:wght@400;600;700;800&display=swap');
```

### Familias Oficiales

| Rol | Familia | Pesos Aprobados | Características y Uso |
| :--- | :--- | :--- | :--- |
| **Principal (Display / H1)** | **Saira** *(Extra Expanded)* | `800 ExtraBold`, `900 Black` *(UI headings: 600–800)* | Presencia brutalista/industrial. `text-transform: uppercase`, `letter-spacing: -0.02em`, `line-height: 1.1–1.2`, `font-stretch: extra-expanded`. Títulos mayores, merch, slides hero. |
| **Secundaria (Body / Lectura)** | **Montserrat** | `400 Regular`, `600 SemiBold`, `700 Bold` | Voz humana, geométrica y legible. Párrafos largos, documentación, legales, PDFs B2B. `line-height: >= 1.6`, `letter-spacing: 0` a `+0.01em`. |
| **Código y Comandos (Mono)** | **JetBrains Mono** *(alt: Fira Code; fallback: Consolas, Courier New)* | `400 Regular`, `700 Bold`, `800 ExtraBold` | Esencia IDE. Ligaduras activas (`font-variant-ligatures: contextual`), `letter-spacing: normal` en código; `+0.05em` a `+0.1em` en botones CTA en `UPPERCASE`. Snippets, navegación, prompts (`>_`, `//`, `[ ]`), botones `[ /START_GAME ]`. |

### Escala Jerárquica en UI (`src/css/custom.css`)

| Elemento | Familia | Tamaño | Peso | Color | Estilo |
| :--- | :--- | :--- | :--- | :--- | :--- |
| **`H1`** | `Saira` | `2.5rem` (40px) | `800` / `900` | `#F8FAFC` (Blanco Consola) | `UPPERCASE`, `-0.02em`, `lh: 1.1–1.2` |
| **`H2`** | `Saira` | `2rem` (32px) | `700` | `#00F0FF` (Cyan Eléctrico) | `UPPERCASE`, `-0.02em`, `lh: 1.2` |
| **`H3`** | `Saira` | `1.5rem` (24px) | `600` | `#FF2A6D` (Rosa Ajolote) | `UPPERCASE`, `-0.02em`, `lh: 1.2` |
| **`H4`** | `Saira` | `1.25rem` (20px) | `600` | `#05FF00` (Verde Terminal) | `UPPERCASE`, `-0.02em`, `lh: 1.2` |
| **`H5`** | `Saira` | `1.1rem` (17.6px) | `600` | `#F8FAFC` (Blanco Consola) | `UPPERCASE`, `-0.02em`, `lh: 1.2` |
| **`H6`** | `JetBrains Mono` | `1rem` (16px) | `400` | `#FF2A6D` (Rosa Ajolote) | `UPPERCASE`, `-0.02em`, `lh: 1.2` |
| **`p` / `li`** | `Montserrat` | `1rem` (16px) | `400` (`strong`: `600`) | `#E2E8F0` / `#F8FAFC` | `lh: 1.6` mínimo en Dark Mode |
| **Lead Text** | `Montserrat` | `1.15rem` | `400` | `#94A3B8` | `lh: 1.6` |
| **Code inline** | `JetBrains Mono` | `95%` | `400` / `700` | `#00F0FF` | Ligaduras contextuales activas |
| **Botón CTA** | `JetBrains Mono` | `0.9rem–1rem` | `700` / `800` | `#0F172A` sobre neón | `UPPERCASE`, tracking `+0.05em` a `+0.1em`, estilo comando `[ EJECUTAR ]` |

### Anti-Patrones Tipográficos (Prohibidos)
1. **Máximo 2 familias por encuadre/pantalla:** Combinar `Saira + Montserrat` (general) o `Saira + JetBrains Mono` (ultra técnico). Evitar que las 3 compitan en la misma jerarquía visual.
2. **Cero fuentes Serif:** Prohibidas *Times New Roman*, *Garamond* o similares, incluso en citas formales.
3. **Cero itálicas para énfasis:** No usar `font-style: italic` para destacar ideas importantes; usar **SemiBold en Rosa Ajolote (`#FF2A6D`)** o comentarios de código `/* Highlight System */`.

---

## 4. Logotipo y Reglas de Marca

### Concepto y Assets en el Repositorio
El logotipo está inspirado en la sintaxis de programación: los corchetes `[]` representan el *scope* y orden lógico, y el guion bajo `_` representa la terminal activa.

| Variante | Archivo en el Repo | Uso |
| :--- | :--- | :--- |
| **Master Dark (Principal)** | [`static/img/logos/Master_Dark.svg`](./static/img/logos/Master_Dark.svg) | Entorno nativo Dark Mode (`#0F172A`) y fondos fotográficos oscurecidos. |
| **Navbar / Horizontal** | [`static/img/logos/logo.svg`](./static/img/logos/logo.svg) | Cabeceras web y barras de navegación. |
| **Ink Mode (Monocromático oscuro)** | [`static/img/logos/Ink Mode.svg`](./static/img/logos/Ink%20Mode.svg) | Exclusivo para fondos blancos/administrativos (facturas, documentos legales, modo impresión). |
| **Isotipo (The Token)** | [`static/img/logos/The Token.svg`](./static/img/logos/The%20Token.svg) | Espacios reducidos, avatares, íconos de app. |
| **Favicon** | [`static/img/logos/favicon.svg`](./static/img/logos/favicon.svg) | Pestañas de navegador y micro UI. |

### Zona Segura (Clear Space)
- **Unidad `X`:** Altura vertical de la letra **`O`** en la palabra `CODE` (en el SVG master `450×300`, `X = 38.7` unidades).
- **Regla estándar:** Margen mínimo libre de **`1X`** en los cuatro lados (arriba, abajo, izquierda, derecha). Ningún texto, botón ni ilustración puede invadirlo.
- **Excepción Front-End (UI reducida):** En navbars móviles, footers compactos o display ads, el padding vertical puede reducirse a **`0.5X`** manteniendo `1X` horizontal.

### Escalabilidad Mínima
| Contexto | Logo Completo | Isotipo (`The Token`) | Barra Horizontal Extensa | Densidad / Nota |
| :--- | :--- | :--- | :--- | :--- |
| **Digital** | `100px` ancho mín. | `32px` ancho mín. | `140px` ancho mín. | En micro UI/favicons usar solo Isotipo sin wordmark. |
| **Impresión** | `25mm` ancho mín. | `10mm` ancho mín. | — | Mínimo **`300 DPI`**. |

### Fondos Permitidos
1. **Preferente (Óptimo):** Obsidiana Digital (`#0F172A`) con `Master_Dark.svg`.
2. **Fotográfico (Seguro):** Fotografías oscuras o tratadas con **overlay `#0F172A` al 70% de opacidad** (evitando zonas claras o ruidosas) + `Master_Dark.svg`.
3. **Administrativo (Restringido):** Fondos blancos/claros únicamente usando **`Ink Mode.svg`** (texto cambia a Obsidiana). Nunca forzar el logo neón sobre blanco o gris plano.

### Errores Prohibidos (`Strict Boolean = true`)
- **`ERROR 400` (Bad Request):** Estirar, aplastar o distorsionar proporciones (siempre escalar proporcionalmente).
- **`ERROR 404` (Not Found):** Sustituir la tipografía del wordmark por fuentes genéricas.
- **`ERROR 500` (Low Contrast):** Colocar el logo sobre fondos vibrantes o saturados que compitan con el neón.
- **`SYNTAX ERROR` (Missing Code):** Eliminar el guion bajo `_` (p. ej., en `STUDIO_`); forma parte integral del código.
- **`GLITCH NO AUTORIZADO` (Shadow Glitch):** Aplicar sombras paralelas (*Drop Shadow*) detrás del logo; el logo es la fuente de luz.
- **`COLOR SWAP` (Hue Alteration):** Invertir o alterar los colores de los corchetes sin aprobación de Dirección.

---

## 5. Tokens CSS y Componentes UI Web

### Variables Raíz (`:root` y `[data-theme='dark']`)
```css
:root {
  /* Brand Color Tokens */
  --cm-obsidiana: #0F172A;
  --cm-blanco-consola: #F8FAFC;
  --cm-rosa-ajolote: #FF2A6D;
  --cm-cyan-electrico: #00F0FF;
  --cm-verde-terminal: #05FF00;

  /* Typography Tokens */
  --cm-font-principal: 'Saira', sans-serif;
  --cm-font-secundaria: 'Montserrat', sans-serif;
  --cm-font-mono: 'JetBrains Mono', monospace;

  /* Surfaces & UI States */
  --glass-bg: rgba(15, 23, 42, 0.8);
  --glass-border: rgba(255, 255, 255, 0.1);
  --cm-border: rgba(248, 250, 252, 0.15);
  --cm-selection: rgba(0, 240, 255, 0.3);
}
```

### Patrones de Componentes
- **Glass Container (`.custom-container`):** `padding: 1.5rem`, `background: rgba(15, 23, 42, 0.8)`, `backdrop-filter: blur(12px)`, `border: 1px solid rgba(255, 255, 255, 0.1)`, `border-radius: 1.25rem`.
- **Tarjetas (`.style-card`):** `border-radius: 1.5rem` (o `4px` en variantes técnicas/brutalistas con borde de acento), transición `all 0.3s ease`. En `:hover`: `transform: translateY(-4px)`, `border-color: #00F0FF`, `box-shadow: 0 20px 40px rgba(0, 0, 0, 0.4)`.
- **Botón Primario (`.btn-core` / CTA):** Fondo `--cm-rosa-ajolote`, texto `--cm-obsidiana`, `JetBrains Mono` Bold/ExtraBold, `UPPERCASE`, glow exterior en hover.
- **Enlaces en Contenido (`.markdown a`):** Color `#00F0FF`, subrayado `rgba(0, 240, 255, 0.3)` con `text-underline-offset: 4px`; en hover subrayado sólido `#00F0FF` y fondo `rgba(0, 240, 255, 0.1)`.
- **Admonitions / Alertas:** Fondo `rgba(15, 23, 42, 0.6)`, `backdrop-filter: blur(10px)`, borde `1px solid var(--glass-border)` y borde izquierdo `4px` (`#FFB800` warning, `#FF2A6D` danger).
- **Neon Glow Protocol (Post-procesado CSS):**
  ```css
  .asset-glow-cyan {
    filter: drop-shadow(0 0 5px #00F0FF) drop-shadow(0 0 15px #00F0FF);
  }
  .asset-glow-pink {
    filter: drop-shadow(0 0 5px #FF2A6D) drop-shadow(0 0 15px #FF2A6D);
  }
  ```

---

## 6. Arquitectura de Iconografía

Dos modos estrictamente separados. **Regla de Tolerancia Cero:** nunca mezclar íconos 8-Bit Pixel Art con íconos SVG Monoline en el mismo plano focal.

### Modo A: 8-Bit Items (Gamificación)
- **Estilo:** Pixel Art retro-moderno (RPG, Minecraft, Stardew Valley).
- **Construcción:** Outline negro sólido obligatorio (`1px–2px`), pintura plana con paleta primaria (`#FF2A6D`, `#00F0FF`, `#05FF00`). **Prohibidos los degradados suaves.**
- **Espaciado:** Requiere amplio espacio vacío alrededor (*Padding Matrix*).
- **Uso:** Insignias de logro (`Badge_Unlocked`), elementos grandes en slides/masterclasses, stickers y parches de merch.

### Modo B: Neon Syntax (Interfaz Web / UI)
- **Estilo:** Line Art geométrico estricto (`Monoline`).
- **Librerías base:** **Phosphor Icons** (`@phosphor-icons/react`) o **Remix Icon**.
- **Stroke y geometría:** Grosor espeso **`Regular 2px` a `Bold 3px`**, terminaciones rectas/cuadradas (`squarish`, estilo PCB).
- **Intervención de marca (Glitch Modification):** En assets vectoriales custom, abrir o interrumpir sutilmente 1mm en una esquina del trazo para simular un micro-glitch o circuito abierto.
- **Hover Web:** `filter: drop-shadow(0 0 10px #00F0FF)`.
- **Uso:** Navegación, botones de acción, redes sociales, bullets técnicos.

### Codificación Semántica por Color (Color Coding)
- **Cyan Eléctrico (`#00F0FF`):** Acción / Verbos / Navegación (enviar, buscar, scroll, links).
- **Rosa Ajolote (`#FF2A6D`):** Alerta / Errores fatales / Acciones destructivas (eliminar, bloqueo, error de formulario).
- **Verde Terminal (`#05FF00`):** Éxito / Logros / Confirmaciones (test aprobado, pago completo, estado online).

### Diccionario Visual de Metáforas
| Concepto | Modo A (8-Bit RPG) | Modo B (Phosphor / SVG) | Metáfora |
| :--- | :--- | :--- | :--- |
| **Aprendizaje** | Cerebro metálico brillante | `Sparkle` | Upgrade Mental System |
| **Seguridad** | Escudo de fuerza pesado | `LockKey` | Firewall / Defensa Activa |
| **Comunidad** | Dos aliens abrazados | `HandPeace` | Squad / Open Source Party |
| **Código Base** | Pergamino tecnológico | `BracketsCurly` | El Hechizo / La Sintaxis |
| **Error Fatal** | Bomba radiactiva | `Bug` | Bugs en Producción |
| **Ingenio / Idea** | Foco geométrico | `Lightbulb` | Sparking Logic |

> Evitar metáforas escolares obsoletas (ej. lupa tradicional); reemplazar por visores VR, radares o escáneres.

---

## 7. Ilustraciones y Post-Procesado

| Modalidad | Estética y Reglas | Casos de Uso | Librerías Open-Source Base |
| :--- | :--- | :--- | :--- |
| **Modo 1: Hero 3D** | Objetos tech en gravedad cero (`Y=0`), resina mate, cristal esmerilado y metal neón. Iluminación dramática lateral **Cyan + Magenta**. Exclusivo sobre **`#0F172A`** (prohibido fondo blanco/pastel). | Hero web, portadas de cursos/misiones, ads de alto impacto (IG/TikTok). | `SALY` (personajes 3D), `HANDZ` (manos 3D para señalar CTAs/mockups). |
| **Modo 2: Voxel Builder** | Bloques isométricos 8-bit con volumen, acentos saturados (`0.9`), vibra *Mexican Retro-Future*. | Roadmaps isométricos, avatares pixelados, badges 3D coleccionables. | `Kenney Assets` (tilesets/low-poly), `Game-Icons.net` (skills RPG + neon glow). |
| **Modo 3: Blueprint** | Wireframes técnicos (`stroke: 1px–2px`, `fill: none`), mallas paramétricas, etiquetas monospace. Color Blanco 80% o `#00F0FF` sobre oscuro o Papel Ingeniería. | Manuales impresos, diapositivas de lógica (`If/Else`), posters, espalda de merch, stats en redes. | `Lucide`, `Reshot` (diagramas de flujo y arquitectura). |

### Protocolo Obligatorio de Post-Procesado
Ningún asset open-source se usa crudo (*RAW*):
1. Adaptación cromática a la paleta CODE ME.
2. Inyección de **Neon Glow** (doble `drop-shadow` en Cyan o Rosa).
3. **Aberración Cromática (`RGB Split`)** sutil en bordes para piezas *Hero* y campañas pagadas.

---

## 8. Patrones y Texturas

### Patrones Oficiales
| Patrón | Nivel de Ruido | Especificaciones | Uso Aprobado |
| :--- | :--- | :--- | :--- |
| **A. Retícula Maestra (`The Grid`)** | Muy bajo (`Z-index: 0`) | Cuadrícula ultrafina `0.5px–1px`. Líneas en `#F8FAFC` o `#00F0FF` al **`5%–10%` de opacidad** sobre `#0F172A`. | Fondos base web, slides, hojas de trabajo (papel milimétrico). |
| **B. Lluvia de Sintaxis** | Medio (`Z-index: -1`) | Símbolos sueltos (`< > { } / ; * = != _`) en `JetBrains Mono`, rotación/escala leve para parallax. `#F8FAFC` y `#FF2A6D` al **`10%–20%` de opacidad** sobre `#0F172A`. | Portadas, banners sociales (FB/LinkedIn), lonas OOH. |
| **C. Textil Digital (`Pixel Weave`)** | Muy alto (Decorativo) | Grecas zapotecas/otomíes/aztecas reconstruidas en 8-bit y glitch. Paleta neón completa RGB (o simulación CMYK para tela/papel). | Mangas/viseras de merch, calcetines, divisores `<hr>` de `10px`, reverso de tarjetas. **Nunca como fondo de lectura principal.** |

### Texturas Oficiales
- **Monitor Fantasma (CRT):** Scanlines horizontales + ligero bloom + aberración cromática en bordes. Mezcla `Overlay` o `Soft Light`. Opacidad `5%` en presentaciones, `10%` en miniaturas YouTube, escaneo sobre fotos. **PROHIBIDO imprimir en medios porosos/offset/lonas** (genera moiré y plastas).
- **Ruido de Compilación (`Digital Noise`):** Grano fino monocromático para romper *banding* y dar densidad táctil a `#0F172A`. Opacidad **`3%–5%`**. En web usar **SVG data-URI inline** (cero KB de descarga). Prohibido ruido grueso encima de párrafos.
- **Papel de Ingeniería:** Textura táctil mate tipo papel bond/blueprint industrial con ligero *ink bleed* y tono blanco roto cálido (no `#FFFFFF` brillante). Exclusivo para diplomas, fichas, pases y carousels estilo "documento filtrado".

### Reglas de Uso de Patrones
1. **Regla Maestra del 10%:** Si hay texto legible encima de un patrón, la opacidad máxima del patrón es **`0.10` (`10%`)**.
2. **No mezclar frecuencias:** Nunca superponer dos patrones densos (ej. Lluvia de Sintaxis + Textil Digital) en el mismo encuadre.
3. **Glitch contenido:** Prohibido aplicar efectos Glitch sobre textos legales, fechas, precios, horarios o currículum.

---

## 9. Aplicaciones por Canal

- **Web ("La Terminal Viva"):** Dark Mode puro, micro-interacciones reactivas (`scale(1.02)`, flicker CRT sutil, glow cyberpunk en CTAs), puntero custom opcional (mira vectorial o `>_` parpadeante), *scrollytelling* con líneas de código semitransparentes en bordes.
- **Redes Sociales ("Street-Tech Visual"):** Fotografía real y cálida de adolescentes/devs con iluminación neón oscura intervenida con capas HUD (`#00F0FF` / `#FF2A6D`), stickers holográficos de Bitxo, flechas de consola (`-------->`) y humor/memes tech mexicanos.
- **Presentaciones ("Modo IDE"):** Marcos que simulan ventanas de **VS Code** o terminal Linux (controles `-`, `□`, `x`), transiciones rápidas tipo glitch horizontal o cascada Matrix (**máximo `0.3s`**), texto con efecto tecleado y **barra de progreso fija inferior en Verde Terminal (`#05FF00`)**.
- **Impresos ("Manual de Resistencia"):** Estética Blueprint con retículas visibles, papel ingeniería táctil, coordenadas `(X:12, Y:43)`, marcas de corte, sellos circulares y resaltado láser en Cyan solo para datos críticos/QR.
- **Merchandising ("Code-Wear"):** Siluetas *Techwear* oversize en Obsidiana con parches de velcro modulares. **Frente minimalista** (solo `_` o isotipo sobre el corazón); **espalda maximalista** con arte *Cyber-Mexa* (glifos prehispánicos + circuitos + bloques monospace). Etiquetas ocultas (*easter eggs*) tipo `>_ EXEC: system.reboot()` o `designed_in_mexico.sh -v2`.

---

## 10. Mascota Oficial: Bitxo (El Ajolote Cibernético)

- **Lore:** Evolucionó en *Xochimilco 3.0* al asimilar código de una tablet sumergida. Su misión es erradicar el miedo humano al error rojo en consola.
- **Simbología:**
  - *Regeneración (`ReBoot Protocol`):* Capacidad de pivotar, corregir y reconstruir tras cualquier fallo (*A Bug is just an evolution in progress*).
  - *Neotenia (`Loop State`):* Conservar la curiosidad juvenil eterna (*Forever a Junior de Corazón*).
- **Anatomía Cyber-Orgánica:**
  1. **Cuerpo Base:** Ajolote translúcido en **Rosa Neón (`#FF2A6D`)** (acabado plástico esmerilado 3D con bloom y grid/código interno fluyendo).
  2. **6 Branquias de Circuito (RGB Status LEDs):**
     - `#05FF00` (Verde Terminal): Compilado / Éxito / Feliz.
     - `#FF2A6D` (Rosa Ajolote): Standby / Esperando input / Neutral.
     - `#00F0FF` (Cyan Eléctrico): Pensando / Fetching Data / Concentrado.
  3. **Goggles AR/VR:** Lentes tácticos oscuros (`Obsidiana`) siempre puestos; proyectan metadatos y símbolos de estado.
  4. **Jetpack "Enter Key":** Propulsor en la espalda con forma de tecla `Enter` (impulsa la ejecución).
- **Estados UX:**
  - **Onboarding:** Flotando con jetpack, explicando conceptos en *data-bites* estilo *Rubber Duck*.
  - **Éxito:** Confeti Voxel + branquias `#05FF00`.
  - **Error/Alerta:** Sin taches agresivos; símbolo `!` en goggles + postura analítica + brillo `#00F0FF`.
  - **Carga (`Loading`):** Nadando en alberca holográfica en un `loop{}`.

---

## 11. Identidad Verbal (Voz y Tono)

### Matriz por Audiencia
| Audiencia | Rol de Marca | Tono | Keywords Clave |
| :--- | :--- | :--- | :--- |
| **Alumnos (Kids & Teens)** | *Partner in Crime* tecnológico | Energético, horizontal (tuteo obligatorio), sin miedo al error, gamificado (*Side Quests*, *Boss Fights*, *Skill Tree*). | `Spawnear`, `Respawn`, `Lag`, `Ping`, `Hardcore`, `Nerfear`, `Buffear`, `Loot`. |
| **Docentes (Senseis)** | *Tech Lead* / Facilitador | Respetuoso, *nerd-profesional*, empático, enfocado en enseñar a aprender (*Rubber Duck*). | `Stack`, `Roadmap`, `Peer-review`, `Refactorización`, `Escalabilidad`, `Empatía Técnica`. |
| **Padres (Clientes)** | *Arquitecto del Mañana* | Aspiracional, sereno, aterrizado económicamente, aliado estratégico. Evitar decir "clases de computación". | `Ventaja Competitiva`, `Alfabetización Digital Global`, `Resolución de Problemas Críticos`, `Pensamiento Computacional`, `Liderazgo Tecnológico`. |

### Reglas Verbales Obligatorias
1. **Spanglish técnico controlado:** Conservar anglicismos reales del código envueltos en calidez mexicana (*"Tira ese Commit"* en vez de *"Haz la confirmación en el repositorio"*).
2. **Cero formalismos con alumnos:** Prohibido tratar de "Usted" a los estudiantes; profesionalismo respetuoso con padres.
3. **Humor tech interno:** Referencias a `;` olvidados, servidores caídos, café y debugging.
4. **Optimismo tecnológico (`Future == Bright`):** Prohibidas campañas basadas en miedo (ej. *"La IA robará empleos"*). El futuro es un lienzo listo para programarse.

---

## 12. Constantes y Prompts para IA Generativa (AIO)

### Parámetros Base de Estilo Visual
```bash
--style: raw
--aesthetics: "Cyberpunk Mexico", "neon pink (#FF2A6D) and cyan (#00F0FF) glow accents"
--components: "retro-tech hardware", "blueprint diagrams and labels"
--rendering: "voxel art elements", "high contrast shadows"
--theme: "dark mode ui aesthetics (#0F172A)"
```
- **Aspect Ratios recomendados:** `--ar 16:9` (web hero / slides), `--ar 1:1` (feed Instagram), `--ar 9:16` (Reels / TikTok), `--tile` (patrones y texturas repetibles).
- **Modificadores de suavizado** (si un patrón queda muy intenso): `very subtle, low contrast, muted`.

### Biblioteca Rápida de Prompts Maestros
- **Bitxo 3D Voxel:** `3D Voxel Art Engine render, isometric high-angle view, glowing neon cyberpunk aesthetic. Radical tech mascot 'Bitxo', anthropomorphic cyberpunk Mexican axolotl, stacked 3D cubes, glowing Neon Magenta Pink (#FF2A6D) skin, glowing Cyan (#00F0FF) fiber optic gills, black VR goggles on forehead, metallic 'Enter Key' jetpack. Scene: [ACCION].`
- **Icono 8-Bit (Modo A):** `A simple pixel art icon of a [OBJETO], thick black outline, flat colors using neon pink and cyan, transparent background, retro video game style asset, 8-bit style, isolated on white --v 6.0`
- **Patrón Grid Base:** `Seamless background texture, ultra-minimalist technical blueprint style, hairline 1px grid at 5-10% opacity, Background #0F172A, Grid Line #00F0FF, 8k --tile`
- **Key Visual Fotográfico:** `Hyperrealistic cinematic photo, 35mm f/1.4 anamorphic lens, Latin teen in dark room lit by Magenta and Cyan neon LEDs, black techwear oversize hoodie coding intensely, overlaid with holographic HUD UI wireframes and green 100% progress bar 'COMPILATION SUCCESS'.`

*(Prompts completos en [`docs/ia/banco-prompts.mdx`](./docs/ia/banco-prompts.mdx), [`docs/visual/patrones/generacion-ia.mdx`](./docs/visual/patrones/generacion-ia.mdx) y [`docs/visual/texturas/generacion-ia.mdx`](./docs/visual/texturas/generacion-ia.mdx)).*

---

## 13. Checklist Rápido de QA antes de Publicar

- [ ] **Ambiente correcto:** ¿Digital en RGB (`#0F172A`, `#FF2A6D`, `#00F0FF`, `#05FF00`, `#F8FAFC`) o Impreso en CMYK (`Rich Black`, `#E6007E`, `#00AEEF`, `#80C342`)?
- [ ] **Contraste WCAG:** ¿Botones/badges neón usan texto **Obsidiana (`#0F172A`)**? ¿Cero combinaciones prohibidas (Rosa/Verde, Cyan/Blanco, Blanco/Verde)?
- [ ] **Tipografía:** ¿Máximo 2 familias en pantalla? ¿H1 en `Saira UPPERCASE`, párrafos en `Montserrat` (`line-height >= 1.6`), cero Serif, cero itálicas de énfasis?
- [ ] **Logotipo:** ¿Zona segura `1X` respetada (`0.5X` solo vertical en navbar)? ¿Ancho mínimo cumplido (`>= 100px` completo / `>= 32px` isotipo)? ¿Sin sombras paralelas ni distorsión?
- [ ] **Iconografía y Patrones:** ¿Sin mezclar 8-bit y SVG monoline? ¿Patrón bajo texto `<= 10%` opacidad? ¿Sin CRT scanlines en archivos de imprenta?
- [ ] **Prueba Ácida de Marca:** *¿Se ve como un producto tech / videojuego Sci-Fi AAA o como un folleto escolar genérico?* Si tiende al segundo, recompilar.
