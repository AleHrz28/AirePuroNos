# Cómo publicar la página Aire Puro Tren Nos en Vercel

La página es **un solo archivo**: `index.html`. Ya trae adentro todas las fotos
(incluida la del prototipo 1) y la simulación 3D. No hay que instalar ni compilar nada.

```
aire-puro-tren-nos/
├── index.html          ← la página completa (fotos y simulación 3D incluidas)
└── LEEME_PUBLICAR.md   ← este archivo
```

> No uses el código React/Vite del paquete anterior (`02_Landing/codigo`): está
> desactualizado. La versión vigente es este `index.html`.

## Opción A (recomendada): GitHub + Vercel, todo desde el navegador

1. Entra a github.com, inicia sesión y crea un repositorio nuevo
   (por ejemplo `aire-puro-tren-nos`), **público**.
2. En el repositorio, elige **Add file → Upload files** y arrastra el contenido de
   esta carpeta: `index.html` y este archivo. Haz clic en
   **Commit changes**.
3. Entra a vercel.com e inicia sesión con tu cuenta de GitHub.
4. **Add New → Project** → elige el repositorio → **Import**.
5. Configuración del proyecto:
   - **Framework Preset:** Other
   - **Build Command:** vacío
   - **Output Directory:** vacío (o `.`)
6. Haz clic en **Deploy**. Al terminar, Vercel entrega un enlace que termina en
   **.vercel.app**: ese es el enlace para entregar.

**Para actualizar después:** sube el archivo nuevo al mismo repositorio
(Add file → Upload files, reemplazando el anterior) y Vercel publica la nueva
versión solo, en menos de un minuto.

## Opción B: con la terminal (requiere Node.js)

```
cd aire-puro-tren-nos
npx vercel@latest          # la primera vez pide iniciar sesión y crea el proyecto
npx vercel@latest --prod   # publica la versión final (.vercel.app)
```

Para actualizar, se repite `npx vercel@latest --prod` en la misma carpeta.

## Si la página cambia

Cuando haya una versión nueva de `index.html`, solo hay que reemplazar el archivo:
opción A, subirlo al mismo repositorio (Add file → Upload files); opción B, repetir
`npx vercel@latest --prod`. El enlace `.vercel.app` se mantiene.

## Revisión antes de entregar el enlace

- [ ] Abre el enlace `.vercel.app` en modo incógnito o en otro equipo, sin iniciar sesión.
- [ ] Revisa que se vean las fotos y que la simulación 3D cargue (sección "3. Prototipo").
- [ ] Revisa la página en un celular.
- [ ] Entrega el enlace `.vercel.app`, no el de GitHub ni el panel de Vercel.
