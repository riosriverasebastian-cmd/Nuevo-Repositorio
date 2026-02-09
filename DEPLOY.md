# Guía de Despliegue en Vercel

Sigue estos pasos para publicar tu aplicación en internet.

## Opción Recomendada: Vía GitHub (Gratis y Automático)

Esta es la forma estándar moderna. Al conectar GitHub con Vercel, cualquier cambio que hagas en tu computador y "subas" a GitHub se actualizará automáticamente en tu web.

### 1. Preparar en GitHub
1.  Crea una cuenta en [github.com](https://github.com) si no tienes una.
2.  Crea un **Nuevo Repositorio** (botón verde "New").
    *   Nombre: `plan-maestro-2026` (o el que quieras).
    *   Público.
    *   No marques "Add a README file" (ya lo tenemos).
    *   Haz clic en "Create repository".

### 2. Subir tu código
Abre una terminal en la carpeta de tu proyecto (`.gemini/antigravity/scratch/plan-maestro-2026`) y ejecuta estos comandos (reemplaza `TU_USUARIO` con tu usuario de GitHub):

```bash
git remote add origin https://github.com/TU_USUARIO/plan-maestro-2026.git
git branch -M main
git push -u origin main
```

### 3. Conectar con Vercel
1.  Ve a [vercel.com](https://vercel.com) y regístrate (recomendado: "Continue with GitHub").
2.  En tu dashboard, haz clic en **"Add New..."** -> **"Project"**.
3.  Verás una lista de tus repositorios de GitHub. Busca `plan-maestro-2026` y haz clic en **"Import"**.
4.  En la siguiente pantalla ("Configure Project"), deja todo como está.
5.  Haz clic en **"Deploy"**.

¡Listo! En unos segundos Vercel te dará un enlace (ej: `plan-maestro-2026.vercel.app`) donde tu aplicación estará viva.

---

## Opción Alternativa: Vercel CLI (Línea de Comandos)

Si prefieres no usar GitHub y solo "subir" los archivos directamente:

1.  Instala Vercel CLI: `npm i -g vercel` (requiere Node.js).
2.  En la terminal, dentro de la carpeta del proyecto, ejecuta:
    ```bash
    vercel login
    ```
    (Sigue las instrucciones para loguearte con tu email).
3.  Una vez logueado, ejecuta:
    ```bash
    vercel
    ```
4.  Responde a las preguntas con `Enter` (acepta los valores por defecto).

## ⚠️ Nota Sobre tus Datos
Al abrir la versión web (la URL de Vercel), verás que **tus tareas y progreso aparecerán vacíos**.
Esto es normal. Los datos se guardan en el navegador. La versión web es un "sitio nuevo" para tu navegador, por lo que empieza desde cero.
