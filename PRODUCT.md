# Product

<!-- impeccable:product-schema 1 -->

## Platform

web

## Users

- **Ingenieros de 3dF Desarrollos en obra (celular):** recorren la obra, cargan y tildan tareas, sacan fotos. A veces sin señal.
- **Ingenieros en oficina (compu):** arman y revisan las planillas por obra, exportan PDF / Excel / CSV.
- **Dirección / gerencia:** lee el dashboard mensual y los informes exportados.

Cada ingeniero entra con su propia cuenta de Google; sus datos viven en su propio Google Drive.

## Product Purpose

Checklist de tareas de obra para 3dF Desarrollos: varias obras, una planilla por obra con pestañas, tareas con piso, unidad, ambiente, rubro, contratista, plazo, fotos y estado de ejecución. Reemplaza a la versión anterior con Supabase (que sigue publicada como respaldo) sincronizando contra Google Drive sin servicios pagos.

Éxito: cada tarea queda registrada, con fotos y fechas, editable desde el celular sin conexión, y con una copia en la nube (Excel en Drive) que se puede abrir y editar fuera de la app.

## Positioning

Los datos son del ingeniero y viven en su Drive como un Excel común (`checklist.xlsx` por obra), no en una base propietaria. La app y el Excel se sincronizan en las dos direcciones, y hay versiones separadas (Oficial vs. Versiones importadas por empleado) para no pisar la copia oficial.

## Operating Context

- Estructura en Drive: `3dF Checklist/Oficial/Planillas/{obra}/checklist.xlsx` + `fotos/{piso}/{tarea}/`, `Versiones/{empleado}_{fecha}/…`, `Dashboard Mensual/`.
- Indicador "Viendo: Oficial" / versión importada: define a dónde escribe la sincronización.
- Sincroniza al iniciar sesión, con "Sincronizar ahora", al volver a la app y ~2 s después de cada cambio. Conflicto app vs. Excel: se pregunta y se resuelve por archivo entero.
- Exportar PDF/CSV (pestaña visible con filtros), Excel (todas las pestañas visibles), ZIP "Exportar / Importar información" para pasar datos entre empleados. Compartir por WhatsApp.
- Dashboard mensual por obra, piso y unidad. Aviso de tareas que vencen mañana.
- Escritorio: tabla. Celular: tarjetas.

## Capabilities and Constraints

- App single-file (`index.html`), HTML/CSS/JS estático, rutas relativas, **sin service worker**: tiene que andar bajo cualquier subpath (hoy `https://teskel.online/3df/`).
- Datos locales primero: localStorage + fotos en IndexedDB. Funciona completa sin Client ID (solo falta el panel de Drive).
- Google Identity Services + Drive API, scope `drive.file`. El Client ID no es secreto, pero no se cambia sin avisar al dueño.
- Sesión de Google dura ~1 h; no se guarda sesión permanente.
- Fotos comprimidas a máx. 1280 px.
- Columnas del Excel fijas (`id`, `Fecha`, `Tarea`, `Piso`, `Unidad`, `Ambiente`, `Ejecutado`, `Rubro`, `Contratista`, `Ingresado`, `FotosIds`, `TabId`, `Plazo`, `Importante`, `CompletadoEn`, `CreadoEn`) y hoja `Config`: cambiarlas rompe la compatibilidad con los Excel existentes.
- Git: commits locales libres; push a GitHub y publicación en vivo (3df/index.html en el Space de Spacefast) son pasos separados y solo cuando el dueño lo pide.
- **Decisión abierta — norma ISO:** el proyecto exige cumplir "las normas ISO", pero la norma concreta no está definida. No asumir ninguna (ni ISO 9001 ni otra) hasta que el dueño la confirme; mientras tanto, no quitar ni debilitar registros, fechas, autoría, versiones ni trazabilidad existentes.

## Brand Commitments

- Nombre: **3dF Desarrollos**, app "3dF Checklist" ("CHECKLIST TAREAS" en el encabezado).
- Logo 3dF (`logo.png`, `icon-192.png`, `icon-512.png`, `apple-touch-icon.png`).
- Tipografía Archivo, negro y blanco. Sin neumorfismo.
- No copiar branding de otros proyectos (constructora-demo ni Teskel). Mejoras probadas en constructora-demo se pueden portar, pero con identidad 3dF.
- Idioma de la interfaz: español rioplatense.

## Evidence on Hand

- La app funcionando: `index.html`, documentada en `README.md` y `SETUP-GOOGLE.md`.
- Respaldo anterior: https://monticof-commits.github.io/Checklists/
- No hay testimonios, métricas de uso ni certificaciones en el proyecto: no inventarlas.

## Product Principles

1. **El dato es del ingeniero.** Todo se guarda primero en el dispositivo y después en su Drive, en un formato que puede abrir sin la app.
2. **Nunca pisar sin preguntar.** Oficial se protege; conflictos y primeras vinculaciones piden confirmación.
3. **Trazabilidad antes que comodidad.** Fechas, autor, versiones y fotos de cada tarea no se pierden ni se simplifican.
4. **Funciona en obra.** Celular, sin conexión, una sola página que carga desde cualquier ruta.
5. **Cero dependencias pagas.** Página estática más la cuenta gratuita de Google de cada usuario.

## Accessibility & Inclusion

Sin requisitos especiales definidos; base estándar web (WCAG AA).
