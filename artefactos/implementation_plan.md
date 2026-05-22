# Plan de Cambios - Enrutamiento y Enlaces Oficiales (Gamma Médica)

Este plan de implementación tiene como objetivo ajustar las rutas locales del proyecto para que coincidan de forma exacta con los enlaces oficiales del dominio de producción (`https://gammamedica.com.pe/`). Esto evitará fallas de redirección o errores de ruta errada (404) al navegar desde el portal de resultados de TenmaLab.

---

## 🎯 Objetivo de la Modificación

*   Cambiar la ruta `/salud_ocupacional` (con guion bajo) por `/salud-ocupacional/` (con guion medio y barra inclinada final).
*   Asegurar que la ruta `/nosotros` admita y redirija correctamente a `/nosotros/` (con barra inclinada final).
*   Actualizar todos los enlaces internos de navegación en el `Header` y otros componentes para ser consistentes con las URLs oficiales.

---

## 📋 Propuesta de Cambios

### 🛠️ Sistema de Archivos (Renombrado)

#### [NEW] [salud-ocupacional](file:///c:/Users/datho/Documents/Trabajos%202025/Gem%2014%20-%20Gamma%20Medica%20Web/src/pages/salud-ocupacional/index.astro)
*   Se renombrará el directorio de la página `src/pages/salud_ocupacional` a `src/pages/salud-ocupacional`.

#### [DELETE] [salud_ocupacional](file:///c:/Users/datho/Documents/Trabajos%202025/Gem%2014%20-%20Gamma%20Medica%20Web/src/pages/salud_ocupacional/index.astro)
*   Se eliminará el directorio antiguo para evitar rutas duplicadas.

#### [NEW] [salud-ocupacional.css](file:///c:/Users/datho/Documents/Trabajos%202025/Gem%2014%20-%20Gamma%20Medica%20Web/src/styles/salud-ocupacional.css)
*   Se renombrará el archivo de estilos `src/styles/salud_ocupacional.css` a `src/styles/salud-ocupacional.css`.

#### [DELETE] [salud_ocupacional.css](file:///c:/Users/datho/Documents/Trabajos%202025/Gem%2014%20-%20Gamma%20Medica%20Web/src/styles/salud_ocupacional.css)
*   Se eliminará el archivo antiguo de estilos.

---

### 💻 Código Fuente (Modificaciones)

#### [MODIFY] [index.astro](file:///c:/Users/datho/Documents/Trabajos%202025/Gem%2014%20-%20Gamma%20Medica%20Web/src/pages/salud-ocupacional/index.astro)
*   Se actualizará la importación de la hoja de estilos:
    ```diff
    - import "../../styles/salud_ocupacional.css";
    + import "../../styles/salud-ocupacional.css";
    ```

#### [MODIFY] [Header.astro](file:///c:/Users/datho/Documents/Trabajos%202025/Gem%2014%20-%20Gamma%20Medica%20Web/src/components/Header.astro)
*   Se actualizarán las referencias de los menús de navegación (tanto versión Escritorio como Móvil):
    ```diff
    - <a href="/nosotros">Nosotros</a>
    + <a href="/nosotros/">Nosotros</a>

    - <a href="/salud_ocupacional">🏗️ Salud Ocupacional</a>
    + <a href="/salud-ocupacional/">🏗️ Salud Ocupacional</a>
    ```

---

## 🧪 Plan de Verificación

### Pruebas Locales
1.  **Ejecución de Servidor de Desarrollo:**
    *   Ejecutar `npm run dev` para validar que el enrutamiento de Astro resuelva correctamente las URLs `/salud-ocupacional/` y `/nosotros/`.
2.  **Construcción de Producción:**
    *   Ejecutar `npm run build` para asegurar que el compilador de Astro genere la estructura estática o de servidor sin errores de importación de estilos.
3.  **Verificación de Enlaces:**
    *   Hacer clic en los menús de navegación en vista desktop y móvil para corroborar que redirijan a las nuevas rutas oficiales de forma fluida.
