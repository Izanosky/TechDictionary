# TechDictionary

Documentación oficial, bibliotecas de componentes y herramientas útiles, por tecnología y en un solo sitio.
Toda la web es `index.html` y todos los datos están en `data.json`.

## Añadir un enlace

Edita `data.json` y añade dentro de la sección que toque:

```json
{ "nombre": "Nombre", "url": "https://...", "desc": "Qué es, en una frase.", "tags": ["open source"] }
```

`tags` es opcional. Usa las que ya existen para que el filtro sirva: `oficial`, `español`, `open source`, `freemium`, `source-available`, `accesible`, `sin estilos`, `animación`.

Para una categoría nueva, añade otro objeto a `categorias` con `id`, `nombre` y `secciones`. Actualiza también `actualizado`.

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
