# Checklist de Tareas - Enrutamiento y Enlaces Oficiales

- `[x]` Cambiar nombres de archivos y carpetas
  - `[x]` Renombrar la carpeta `src/pages/salud_ocupacional` a `src/pages/salud-ocupacional`
  - `[x]` Renombrar el archivo de estilos `src/styles/salud_ocupacional.css` a `src/styles/salud-ocupacional.css`
- `[x]` Actualizar importación de estilos en `src/pages/salud-ocupacional/index.astro`
- `[x]` Actualizar enlaces en `src/components/Header.astro`
  - `[x]` Cambiar `/nosotros` a `/nosotros/` en Header de escritorio
  - `[x]` Cambiar `/nosotros` a `/nosotros/` en Header de móvil
  - `[x]` Cambiar `/salud_ocupacional` a `/salud-ocupacional/` en Header de escritorio
  - `[x]` Cambiar `/salud_ocupacional` a `/salud-ocupacional/` en Header de móvil
- `[x]` Verificación y pruebas locales
  - `[x]` Validar que el servidor de desarrollo (`npm run dev`) levante sin problemas
  - `[x]` Validar el enrutamiento y la navegación entre páginas
  - `[x]` Validar que el build de producción (`npm run build`) se genere exitosamente
