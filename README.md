# Portafolio frontend

Interfaz React + Vite del portafolio profesional.

## Desarrollo local

Requiere Node.js 20.19 o superior. Instala las dependencias e inicia Vite:

```powershell
npm ci
npm run dev
```

Abre <http://localhost:5173>. En desarrollo, las solicitudes `/api` se
redirigen a `http://127.0.0.1:3000`; inicia la API por separado para usar las
funciones conectadas al backend.

Para apuntar a una API publicada, crea un archivo `.env.local` en la raíz de
este proyecto con `VITE_API_URL` igual al origen de la API, sin `/api` al
final. No pongas secretos en variables `VITE_*`: sus valores se incluyen en
el frontend público.

## Scripts

- `npm run dev`: inicia Vite en <http://localhost:5173>.
- `npm run build`: genera el sitio estático en `dist`.
- `npm run lint`: valida el código del frontend.
- `npm run preview`: sirve localmente la compilación de producción.

## Despliegue en Vercel

- Importa este repositorio en Vercel con preset **Vite**.
- Build command: `npm run build`.
- Output directory: `dist`.
- Configura `VITE_API_URL` con el origen de la API publicada, sin `/api` al
  final.
- Configura el origen de este sitio publicado en la variable `FRONTEND_URL` de
  la API. El inicio de sesión de administración usa una cookie `HttpOnly`.
