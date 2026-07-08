# OptiGIS — Sitio web

Página de presentación de **OptiGIS** (inventario y modelamiento de redes FTTH/GPON
sobre QGIS). Es un sitio estático de un solo archivo (`index.html`); no requiere
compilación ni servidor.

## Publicar en GitHub Pages

1. **Crea un repositorio** en GitHub (por ejemplo `optigis-web`).
   - Si quieres que quede en la raíz de tu usuario (`https://TUUSUARIO.github.io`),
     nombra el repo exactamente `TUUSUARIO.github.io`.
2. **Sube `index.html`** a la raíz del repositorio.
   - Vía web: botón **Add file → Upload files**, arrastra `index.html`, *Commit*.
   - Vía git:
     ```bash
     git init
     git add index.html
     git commit -m "Publica sitio OptiGIS"
     git branch -M main
     git remote add origin https://github.com/TUUSUARIO/optigis-web.git
     git push -u origin main
     ```
3. **Activa Pages:** repositorio → **Settings → Pages** → *Build and deployment* →
   Source: **Deploy from a branch** → Branch: **main** / carpeta **/(root)** → **Save**.
4. Espera ~1 minuto. Tu sitio quedará en:
   - `https://TUUSUARIO.github.io/optigis-web/`  (repo normal), o
   - `https://TUUSUARIO.github.io/`  (si el repo se llama `TUUSUARIO.github.io`).

> Dominio propio (opcional): en **Settings → Pages → Custom domain** agrega tu
> dominio y crea el registro DNS correspondiente.

## Editar antes de publicar

Reemplaza los textos entre corchetes `[ ]` en `index.html`:

- **Videos** (sección *Demos*): `[Título del video 1/2]` y `[Breve descripción…]`.
- **Canal**: `[URL del canal de YouTube]` en el botón "Ver todas las demos".
- **Documentación** y **Solicitar acceso**: cambia los `href="#"` por tus enlaces.
- **Contacto**: datos en el pie de página.

### Agregar más videos
Copia un bloque `<article class="vitem">…</article>` dentro de `<div class="vgrid">`
y cambia el ID del video en dos lugares:
`youtube-nocookie.com/embed/ID_DEL_VIDEO` (el iframe) y `youtu.be/ID_DEL_VIDEO` (el enlace).
El ID es la parte final de la URL de YouTube (p. ej. `https://youtu.be/ITusU3Ek6GY` → `ITusU3Ek6GY`).

## Notas

- Las tipografías se cargan desde Google Fonts y los videos desde YouTube, por lo
  que el sitio necesita conexión a internet (normal en un sitio web).
- Los videos usan el dominio *privacy-enhanced* `youtube-nocookie.com` y carga
  diferida (`loading="lazy"`).
