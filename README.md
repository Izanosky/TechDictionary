# TechDictionary

Recursos para programar, revisados a mano y ordenados por lo que quieres hacer.
Toda la web es `index.html` y todos los datos están en `data.json`.

## Cómo está ordenado

`grupos` (lo que quieres hacer: Programar, Hacer webs y apps…) → `categorias` (cada una con `grupo`, `desc` corta y `nota` opcional) → `secciones` (cada una con `desc`: para qué sirve) → `enlaces`. El `tono` de cada grupo es el matiz OKLCH de su color.

## Añadir un enlace

Edita `data.json` y añade dentro de la sección que toque:

```json
{ "nombre": "Nombre", "url": "https://...", "desc": "Qué es, en una frase.", "tags": ["open source"] }
```

`tags` es opcional. Usa las que ya existen para que el filtro sirva: `oficial`, `español`, `open source`, `freemium`, `source-available`, `accesible`, `sin estilos`, `animación`. La web las muestra con nombre y explicación (`ETIQUETAS` en `index.html`): `freemium` sale como "Plan gratis", `source-available` como "Código visible".

Una sección nueva necesita `nombre`, `desc` (para qué sirve, en una frase) y `enlaces`. Una categoría nueva, `id`, `grupo` (uno de `grupos`), `nombre`, `desc` y `secciones`. Actualiza también `actualizado`.

Cada cambio en `data.json` y cada lunes, una GitHub Action comprueba que el JSON es válido y que no hay enlaces rotos.

Solo entra lo que se haya revisado: enlace a la fuente real (no al tuit), gratis o con plan gratis útil, y nada de propaganda.

## Ver en local

`fetch` no funciona abriendo el archivo directamente; hace falta un servidor:

```sh
python -m http.server
```

y abre http://localhost:8000.

## Desplegar

GitHub → Settings → Pages → *Deploy from a branch* → `main` / `(root)`.
