---
name: naming-creativo
description: "Lee un brief sencillo de una empresa o marca y propone nombres con personalidad, no descriptivos: de 1 a 5 candidatos en español y los mismos en inglés (2 por defecto) por cada una de 5 técnicas de naming (metáfora de otro mundo, palabra inventada por su sonido, recorte o fusión, raíz de otra lengua, error intencionado). Los presenta en una sola tabla con la idea de cada nombre y siempre guarda un fichero markdown naming-creativo_<fecha>.md con la lista. Usa esta skill siempre que el usuario pida nombres para una marca, producto o empresa, quiera ideas de naming a partir de un brief o un archivo de contexto de marca, o se queje de que los nombres que le dan son sosos, genéricos o demasiado descriptivos (tipo 'Daily Bag'). Se activa con: naming, nombres de marca, ideas de nombre, buscar nombre, propuesta de nombres, nombres creativos, nombres no descriptivos, brand naming, brand name ideas."
---

# Naming creativo

Convierte un brief sencillo de empresa en una batería de nombres con personalidad. El objetivo es evitar los nombres sosos y descriptivos ("Daily Bag", "Smart Office", "Pro Clean") y proponer nombres que se recuerden, que la marca pueda hacer suyos y que no pueda usar cualquier competidor.

La skill no elige el nombre por el usuario: le da un abanico amplio y bien explicado para que elija.

---

## Cuándo usarla

- El usuario tiene un brief, un archivo de contexto de marca o una descripción de su empresa y quiere ideas de nombre
- El usuario ha recibido nombres demasiado descriptivos o genéricos y quiere algo más original
- Se necesitan nombres tanto en español como en inglés para comparar

## Cuándo NO usarla

- El usuario quiere un proceso completo de posicionamiento y narrativa, o un cuestionario previo (usa `brand-ideation`)
- El nombre ya está decidido y se quiere logo o identidad (usa `brand-identity`)

---

## Entrada: el brief

Lee el brief que aporte el usuario: un archivo adjunto o mencionado (por ejemplo `brand-context.md`) o un texto pegado en el chat. Si no hay brief, pide en una sola pregunta una descripción breve de la empresa (qué vende, a quién, cómo quiere sonar). No hagas un cuestionario.

Extrae del brief, si están:

- **Qué es y qué hace** (categoría y producto)
- **Para quién** (público y su necesidad principal)
- **Personalidad y tono** (por ejemplo "moderna, práctica, elegante"; "cercano y desenfadado")
- **Valores y diferenciación**
- **Mercado y posición de precio**
- **Cosas pendientes o sin confirmar**

Usa el brief para dos cosas: buscar la materia prima de los nombres (las ideas, objetos, gestos y sensaciones del mundo de la marca) y comprobar que cada nombre encaja con la personalidad y el tono. Si falta algún dato, sigue con lo que hay y dilo al final.

**No prometas lo que el brief no confirma.** Si el brief marca algo como pendiente de validar (por ejemplo "impermeable" o "ligero"), no propongas nombres cuyo significado principal sea esa promesa; o, si lo haces, márcalo en la explicación ("depende de que se confirme…").

---

## Cantidad de nombres

La cantidad (N) es el número de nombres **por idioma y por técnica**. Puede ser 1, 2, 3, 4 o 5. Si el usuario dice 2, salen 2 en español y 2 en inglés en cada una de las 5 técnicas.

| N | Por técnica | Total |
|---|---|---|
| 1 | 1 ES + 1 EN | 10 |
| 2 | 2 ES + 2 EN | 20 |
| 3 | 3 ES + 3 EN | 30 |
| 4 | 4 ES + 4 EN | 40 |
| 5 | 5 ES + 5 EN | 50 |

- **Si el usuario ya ha dicho cuántos quiere, no preguntes.** Si pide más de 5, usa 5 y díselo; si pide 0 o menos de 1, usa 1.
- **Si no lo ha dicho, pregúntalo antes de generar**, junto con la descripción de la empresa si también hace falta:
  - Con una herramienta de preguntas interactivas (por ejemplo `AskUserQuestion`, que admite 4 opciones como máximo), ofrece "1", "2 (por defecto)", "3" y "5". El usuario puede escribir 4 en la opción "Otra".
  - Sin esa herramienta, pregúntalo en el chat: "¿Cuántos nombres quieres por idioma y por técnica? 1, 2, 3, 4 o 5 (por defecto, 2)."
- **Por defecto, 2.** Usa 2 si el usuario responde sin elegir un número ("los que sean", "da igual"), o si no se le puede preguntar.

---

## Las 5 técnicas

Para cada técnica, genera **N nombres en español y N en inglés** (ver "Cantidad de nombres").

| Tipo (etiqueta de la tabla) | Técnica | En qué consiste | Ejemplos conocidos |
|---|---|---|---|
| Metáfora | **Metáfora de otro mundo** | Tomar una imagen de un ámbito que no tiene nada que ver con el producto pero comparte su esencia | Apple, Amazon, Patagonia |
| Sonido | **Palabra inventada por su sonido** | Una palabra nueva cuyos sonidos transmiten la personalidad (sonidos suaves para algo cálido, consonantes duras para algo firme) | Kodak, Häagen-Dazs, Zalando |
| Recorte | **Recorte o fusión** | Cortar una palabra o unir dos en una sola | Spotify, Pinterest, Netflix |
| Raíz | **Raíz de otra lengua** | Partir de una raíz latina, griega o de otro idioma con un significado ligado a la marca | Volvo ("yo ruedo" en latín), Lego ("juega bien" en danés) |
| Error | **Error intencionado** | Una palabra conocida con una letra cambiada, quitada o duplicada para hacerla propia | Flickr, Tumblr, Google |
| SimilProducto | **Error intencionado** | Una palabra que tenga relacion con el producto, su forma particular, su esencia, junto con lo que el brief distinga como valor especial del producto de la marca | en base las características del producto detallado en el brief |

### Qué significa el idioma (ES / EN)

El idioma indica **para qué público suena natural el nombre**: ES si suena y se entiende como un nombre en español; EN si suena como un nombre en inglés. En la técnica "Raíz", la lengua de origen (latín, griego, japonés…) se dice en la explicación, no en la columna de idioma.

### Cómo aplicar cada técnica

- **Parte del mundo de la marca, no de la categoría.** Haz primero, para ti, una lista de ideas del brief: los objetos que lleva el cliente, los momentos de su día, las sensaciones que busca, los valores. Los nombres salen de ahí, no del nombre del producto.
- **Español e inglés son dos búsquedas distintas, no traducciones.** Un nombre en inglés no debe ser la traducción de uno en español de la misma técnica.
- **Pronunciable para el mercado del brief.** Si el mercado es hispanohablante, los nombres en inglés tienen que poder decirse sin dudar en español.
- **En español, el error intencionado tiene que parecer deliberado,** no una falta de ortografía (mejor una letra duplicada o una "k" que una tilde quitada).
- **Variedad dentro de cada técnica.** Los nombres de una misma técnica no deben ser variaciones de la misma idea.

---

## Filtro anti-soso

Antes de presentar los nombres, descarta y sustituye cualquier candidato que falle una de estas pruebas:

1. **Prueba "Daily Bag".** ¿Es una palabra genérica más la palabra de la categoría, o dos palabras de diccionario que describen el producto? Fuera.
2. **Prueba del competidor.** ¿Podría usarlo mañana cualquier competidor sin que nadie lo notara? ¿Es ya una marca conocida de la categoría? Fuera.
3. **Prueba del tono.** ¿Choca con la personalidad y el tono del brief (por ejemplo, demasiado infantil para una marca "elegante, sin resultar infantil")? Fuera.
4. **Prueba de asociaciones.** ¿Tiene un significado negativo, vulgar o ridículo en español o en inglés? Fuera.
5. **Prueba de repetición.** ¿Es casi igual que otro nombre de la lista, aunque sea de otra técnica? Quédate con el mejor.

No compruebes dominios ni marcas registradas: eso queda para después de elegir.

---

## Salida en el chat

Responde en el chat con esta estructura:

1. **Lo que he leído del brief:** de 2 a 4 líneas con lo que has usado (qué es, para quién, personalidad, tono) y los datos que faltaban, si los hay.
2. **Una sola tabla con todos los candidatos** (N × 2 idiomas × 5 técnicas), ordenada por tipo (Metáfora, Sonido, Recorte, Raíz, Error) y, dentro de cada tipo, primero los ES y luego los EN:

```markdown
| Nombre | Idioma | Tipo | La idea |
|---|---|---|---|
| [Nombre] | ES | Metáfora | [Una frase muy breve, máximo 12 palabras] |
| [Nombre] | EN | Metáfora | [...] |
| ... | | | |
```

3. **El enlace al fichero markdown** (ver la sección siguiente).

**No des nunca favoritos, rankings ni recomendaciones** de un nombre sobre otro, ni en el chat ni en el fichero. La elección es del usuario.

Reglas para la columna "La idea":

- Una sola frase, de 12 palabras como mucho.
- Explica de dónde sale el nombre y qué conecta con la marca, no lo describe ("Orden que viaja contigo", no "Es un nombre bonito").
- En la técnica "Raíz", di la lengua de origen y el significado ("Del latín *portare*, llevar").
- En los nombres en inglés, escribe la idea en español.

---

## Fichero markdown (siempre)

Guarda siempre el resultado en un fichero markdown, aunque el usuario no lo pida.

- **Nombre:** `naming-creativo_<fecha>.md`, donde `<fecha>` es la fecha de creación del fichero en formato DDMMAAAA (por ejemplo `naming-creativo_16112026.md`). Si ya existe un fichero con ese nombre, añade `_2`, `_3`…
- **Dónde:**
  - **Si estás trabajando en un proyecto** (una carpeta de proyecto abierta como directorio de trabajo), guárdalo en la carpeta base del proyecto.
  - **Si no hay proyecto**, guárdalo en la carpeta de trabajo y entrégaselo al usuario para descargar (con la herramienta de enviar archivos, si existe, o con un enlace al fichero).
- **Formato: lista, no tabla.** Usa esta plantilla:

```markdown
# Naming creativo: [nombre o descripción breve del proyecto]

Fecha: [DD/MM/AAAA]
Brief: [nombre o ruta del brief usado]
Cantidad: [N] por idioma y por técnica ([total] nombres)

## Lo que he leído del brief

[Las mismas 2-4 líneas del chat, incluidos los datos que faltaban.]

## Candidatos

### Metáfora

- **[Nombre]** (ES): [la idea]
- ...
- **[Nombre]** (EN): [la idea]
- ...

### Sonido

[Igual]

### Recorte

[Igual]

### Raíz

[Igual]

### Error

[Igual]

## Antes de decidir

- Comprobar dominios y marcas registradas de los nombres preferidos.
- [Cualquier dato del brief que faltaba o estaba sin confirmar y afecta a los nombres.]

## Solo los nombres

[Todos los nombres, uno por línea, en el mismo orden que arriba, dentro de un bloque de texto (```text) y sin viñetas, idioma, tipo ni explicación, para poder copiarlos y pegarlos de una vez.]
```

La sección "Solo los nombres" va siempre la última del fichero.

---

## Errores habituales

- **Colar nombres descriptivos "por si acaso".** Si el usuario quiere un nombre descriptivo, no necesita esta skill. Todos los nombres deben pasar el filtro anti-soso.
- **Traducir los nombres de un idioma al otro.** Pierde la mitad de las ideas.
- **Explicaciones largas.** La tabla tiene que poder leerse de un vistazo.
- **Partir del producto en vez del mundo de la marca.** Salen nombres como "BolsoPro" o "BagMate".
- **Ignorar el tono del brief.** Un nombre ingenioso que no encaja con la personalidad de la marca no sirve.
- **Prometer lo que no está confirmado.** Si el brief dice que algo está pendiente de validar, el nombre no debe darlo por hecho.
- **Olvidar el fichero.** El fichero markdown se genera siempre, no solo cuando se pide.
- **Dar favoritos.** Nunca destaques, ordenes por preferencia ni recomiendes nombres.
- **No respetar la cantidad.** Cada técnica lleva exactamente N nombres en español y N en inglés: ni más ni menos.
