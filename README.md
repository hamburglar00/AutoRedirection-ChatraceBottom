# AutoRedirection-ChatraceBottom

Link para usar en **tarjetas de Chatrace**. Redirección automática a un número de WhatsApp activo por agencia.

- **Con agency en la URL** (`/a/8` o `/?agency=8`): se muestra "Redireccionando a WhatsApp activo..." y se redirige a WhatsApp con un número obtenido de la API.
- **Sin agency**: se muestra un mensaje de error pidiendo usar un link tipo `/a/123`.
- **Si la API no devuelve número**: se muestra "No hay número disponible para esta agencia en este momento."

## Estructura

- **`index.html`** – Página mínima: lee `agency` de la URL, llama a la API y redirige a WhatsApp (o muestra error). Sin imágenes ni diseño.
- **`api/get-random-phone.js`** – Misma lógica que antes: número aleatorio por agencia (api.asesadmin.com), retry y cache.
- **`vercel.json`** – Rewrite `/a/:agencyId` → `/index.html?agency=:agencyId`.

No se usan `styles.css` ni la carpeta `imagenes/`; se pueden eliminar si no los necesitás.

## Repo original

[https://github.com/hamburglar00/AutoRedirection-ChatraceBottom](https://github.com/hamburglar00/AutoRedirection-ChatraceBottom)
