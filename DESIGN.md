---
name: 3dF Checklist
description: Checklist de tareas de obra de 3dF Desarrollos, en negro y blanco, con sincronización a Google Drive.
colors:
  negro: "#000000"
  blanco: "#ffffff"
  gris-1: "#f3f3f3"
  gris-2: "#dcdcdc"
  gris-3: "#6b6b6b"
  gris-4: "#444444"
  marcador-rojo: "#e11d1d"
  marcador-amarillo: "#ffd400"
typography:
  display:
    fontFamily: "Archivo, -apple-system, BlinkMacSystemFont, 'Helvetica Neue', Arial, sans-serif"
    fontSize: "40px"
    fontWeight: 800
    lineHeight: 1
    fontFeature: "tnum"
  headline:
    fontFamily: "Archivo, -apple-system, BlinkMacSystemFont, 'Helvetica Neue', Arial, sans-serif"
    fontSize: "26px"
    fontWeight: 800
    lineHeight: 1.35
    letterSpacing: "0.01em"
  title:
    fontFamily: "Archivo, -apple-system, BlinkMacSystemFont, 'Helvetica Neue', Arial, sans-serif"
    fontSize: "16px"
    fontWeight: 800
    lineHeight: 1.35
  body:
    fontFamily: "Archivo, -apple-system, BlinkMacSystemFont, 'Helvetica Neue', Arial, sans-serif"
    fontSize: "15px"
    fontWeight: 400
    lineHeight: 1.35
  control:
    fontFamily: "Archivo, -apple-system, BlinkMacSystemFont, 'Helvetica Neue', Arial, sans-serif"
    fontSize: "13px"
    fontWeight: 600
    lineHeight: 1.35
  label:
    fontFamily: "Archivo, -apple-system, BlinkMacSystemFont, 'Helvetica Neue', Arial, sans-serif"
    fontSize: "11px"
    fontWeight: 800
    letterSpacing: "0.14em"
  cifra-tarjeta:
    fontFamily: "Archivo, -apple-system, BlinkMacSystemFont, 'Helvetica Neue', Arial, sans-serif"
    fontSize: "28px"
    fontWeight: 800
    lineHeight: 1
  titulo-modal:
    fontFamily: "Archivo, -apple-system, BlinkMacSystemFont, 'Helvetica Neue', Arial, sans-serif"
    fontSize: "23px"
    fontWeight: 800
  cifra-obra:
    fontFamily: "Archivo, -apple-system, BlinkMacSystemFont, 'Helvetica Neue', Arial, sans-serif"
    fontSize: "22px"
    fontWeight: 800
    fontFeature: "tnum"
  glifo-cerrar:
    fontFamily: "Archivo, -apple-system, BlinkMacSystemFont, 'Helvetica Neue', Arial, sans-serif"
    fontSize: "30px"
  glifo:
    fontFamily: "Archivo, -apple-system, BlinkMacSystemFont, 'Helvetica Neue', Arial, sans-serif"
    fontSize: "20px"
  meta:
    fontFamily: "Archivo, -apple-system, BlinkMacSystemFont, 'Helvetica Neue', Arial, sans-serif"
    fontSize: "12px"
    fontWeight: 400
  caption:
    fontFamily: "Archivo, -apple-system, BlinkMacSystemFont, 'Helvetica Neue', Arial, sans-serif"
    fontSize: "11px"
    fontWeight: 600
rounded:
  none: "0px"
spacing:
  xs: "6px"
  sm: "8px"
  md: "10px"
  lg: "14px"
  xl: "16px"
  2xl: "20px"
  3xl: "28px"
components:
  button:
    backgroundColor: "{colors.blanco}"
    textColor: "{colors.negro}"
    typography: "{typography.control}"
    rounded: "{rounded.none}"
    padding: "8px 12px"
    height: "36px"
  button-primario:
    backgroundColor: "{colors.negro}"
    textColor: "{colors.blanco}"
    typography: "{typography.control}"
    rounded: "{rounded.none}"
    padding: "8px 12px"
    height: "36px"
  button-header:
    backgroundColor: "{colors.negro}"
    textColor: "{colors.blanco}"
    rounded: "{rounded.none}"
    padding: "0 12px"
    height: "36px"
  input-campo:
    backgroundColor: "{colors.blanco}"
    textColor: "{colors.negro}"
    rounded: "{rounded.none}"
    padding: "8px 10px"
    height: "36px"
  tab:
    backgroundColor: "{colors.blanco}"
    textColor: "{colors.negro}"
    rounded: "{rounded.none}"
    height: "42px"
  tab-activa:
    backgroundColor: "{colors.negro}"
    textColor: "{colors.blanco}"
    rounded: "{rounded.none}"
    height: "42px"
  estado-no:
    backgroundColor: "{colors.blanco}"
    textColor: "{colors.negro}"
    rounded: "{rounded.none}"
    height: "32px"
  estado-si:
    backgroundColor: "{colors.negro}"
    textColor: "{colors.blanco}"
    rounded: "{rounded.none}"
    height: "32px"
  obra-item:
    backgroundColor: "{colors.blanco}"
    textColor: "{colors.negro}"
    rounded: "{rounded.none}"
    padding: "12px"
  obra-item-actual:
    backgroundColor: "{colors.negro}"
    textColor: "{colors.blanco}"
    rounded: "{rounded.none}"
    padding: "12px"
---

# Design System: 3dF Checklist

## Overview

**Creative North Star: "La planilla de obra"**

La app se lee como una planilla en papel que se lleva a la obra: negro sobre blanco, todo a la vista, sin adornos. Cada caja tiene un borde firme de 2px y cada esquina es recta. La jerarquía sale del peso de la letra (Archivo 800 frente a 600 y 400) y de la inversión negro/blanco, no del color, la sombra ni el volumen.

La densidad es de herramienta de trabajo. En la compu, una tabla ancha con columnas fijas que se escanea como una hoja de Excel. En el celular, la misma fila se vuelve una tarjeta con borde, con campos de 16px y blancos de toque de 44px. Los controles son sobrios y precisos: hacen una sola cosa, se ven igual en todas las pantallas y muestran su estado invirtiéndose a negro.

Lo que no va: neumorfismo, sombras difusas, esquinas redondeadas, degradés y el branding de otros proyectos (constructora-demo, Teskel).

**Key Characteristics:**
- Monocromo puro (#000 / #fff) con cuatro grises funcionales.
- Bordes de 2px negros en todo contenedor y control; radio 0 en todos lados.
- Estado activo = invertido (fondo negro, texto blanco).
- Una sola familia: Archivo 400/500/600/800, con números tabulares en los contadores.
- Encabezado negro de borde a borde con el logo 3dF.

## Colors

Monocromo estricto: el negro y el blanco hacen todo el trabajo y los grises solo jerarquizan texto y separan filas.

### Primary
- **Negro tinta** (negro): texto, todos los bordes, encabezado, cabecera de la tabla, botón primario, pestaña activa, obra actual, estado "SI", barras de avance y scrollbar.

### Neutral
- **Blanco hoja** (blanco): fondo de la página, de las cajas y de los controles en reposo; texto sobre negro.
- **Gris renglón** (gris-1): filas pares de la tabla y pista del scrollbar.
- **Gris trazo** (gris-2): separadores entre filas, borde de campos al pasar el mouse y texto secundario sobre el encabezado negro.
- **Gris lápiz** (gris-3): placeholders, tareas tachadas, botón borrar en reposo, etiquetas de las tarjetas en celular y pie de página. Da 5,3:1 sobre blanco y 4,8:1 sobre gris renglón, así que sirve como texto.
- **Gris grafito** (gris-4): texto secundario sobre blanco (notas, metadatos, títulos de grupo) y línea inferior de los campos del encabezado.

### Tertiary
- **Marcador rojo** (marcador-rojo) y **marcador amarillo** (marcador-amarillo): solo como colores de lápiz en el editor de fotos, para marcar sobre la imagen. Nunca en la interfaz.

### Named Rules
**La regla de la tinta única.** La interfaz usa negro, blanco y grises. Un color nuevo solo entra si representa un dato, y pasa primero por DESIGN.md.

**La regla del 4,5.** Todo gris que se use como texto tiene que dar al menos 4,5:1 sobre el fondo donde aparece, incluido el gris renglón de las filas pares. Gris trazo (gris-2) es solo para bordes y para texto sobre negro.

**La regla del invertido.** Seleccionado, activo, actual o hecho se marca invirtiendo a fondo negro con texto blanco. No hay un color de acento para eso.

## Typography

**Display Font:** Archivo (con -apple-system, Helvetica Neue, Arial)
**Body Font:** Archivo
**Label/Mono Font:** Archivo; los números usan `font-variant-numeric: tabular-nums`.

**Character:** Una grotesca de trabajo con un 800 pesado para títulos y cifras y un 600 firme para los controles. Se lee como el rotulado de un plano.

### Hierarchy
- **Display** (800, 40px, 1): cifras del resumen (total, hechas, pendientes); tabulares. En el dashboard, las cifras de las tarjetas van en 28px.
- **Headline** (800, 26px; 22px en celular): "CHECKLIST TAREAS" en el encabezado, en mayúsculas.
- **Title** (800, 16px): títulos de paneles ("Obras", avisos). Los modales usan 23px.
- **Body** (400, 15px, 1.35): texto base. Las celdas de la tabla van en 13px y suben a 16px en celular para evitar el zoom de iOS.
- **Control** (600, 13px; 12px dentro de grupos y en el encabezado): botones, pestañas, selects.
- **Label** (800, 11px, 0.14em, MAYÚSCULAS): títulos de grupo de controles. Las etiquetas de campo en tarjetas van en 11px, gris lápiz.
- **Meta** (400, 12px) y **Caption** (600, 11px): metadatos, notas, nombres de foto y estado de Drive. Nada funcional va por debajo de 11px.
- **Tamaños de cifra y modal:** 28px (cifras del dashboard), 23px (título de modal), 22px (porcentaje de cada obra), 20px (glifos ★ y ×) y 30px (× de cerrar en el panel de Drive).

### Named Rules
**La regla del peso.** La jerarquía se arma con peso y tamaño: 800 para lo que se cuenta o se nombra, 600 para lo que se toca, 400 para lo que se lee.

**La regla de los 16px.** En celular, todo campo editable va en 16px como mínimo.

## Layout

Una sola columna fluida, sin contenedor máximo (`main` ocupa todo el ancho, con 16px de margen respetando el safe area). Arriba, una grilla de dos columnas: a la izquierda pestañas, resumen y controles; a la derecha el panel "Obras" (240–300px), que se estira a la altura de la columna izquierda y scrollea por dentro.

La tabla tiene `table-layout: fixed`, un ancho mínimo de 1180px y columnas de ancho fijo (fecha 124, piso 48, unidad 56, estado 86, fotos 140…). La columna Tarea toma el resto, y la tabla scrollea en horizontal dentro de su caja.

Puntos de corte:
- **≤980px:** los controles pasan a una columna.
- **≤820px:** el panel Obras baja debajo (máx. 360px de alto). La tabla se vuelve tarjetas: cada fila es una caja con borde de 2px en una grilla de dos columnas, y Tarea, Fotos y Acciones ocupan todo el ancho. Las etiquetas salen de `data-l`.
- **≤820px:** además, todo control tocable (botones, filtros, SI/NO, Cámara/Galería, estrella, borrar, pestañas, desplegables y campos) mide al menos 44px de alto.
- **≤520px:** el bloque de sincronización del encabezado pasa a ocupar todo el ancho. Logo de 44px.

El ritmo de espaciado es 6 / 8 / 10 / 14 / 16 / 20, con un salto a 28px entre las cifras del resumen. Los gaps son chicos y los bordes hacen la separación.

## Elevation & Depth

Plano por completo. No hay `box-shadow` decorativas: la profundidad sale del borde de 2px y de la inversión negro/blanco. Las capas superpuestas (modales, visor de fotos, editor) se separan con un velo negro (72% en modales y confirmaciones, 94% en el visor, sólido en el editor), nunca con sombra.

El único `box-shadow` del sistema es estructural: una barra interna de 4px a la izquierda (`inset 4px 0 0 #000`) que marca pestañas y filas **importantes**.

### Named Rules
**La regla del papel plano.** Nada flota. Si algo tiene que destacarse, se invierte o se le engrosa el borde; no se le pone sombra.

## Shapes

Esquinas rectas en todo (radio 0, declarado explícitamente en inputs y botones para anular los estilos del sistema). Los bordes son de 2px sólidos y negros. Hay 1px solo para separar filas de la tabla y en la línea inferior de los campos del encabezado.

Dos excepciones con sentido:
- **Borde punteado** (2px dashed): el botón "+ Foto", porque es un lugar donde cargar algo.
- **Círculo**: las muestras de color del editor de fotos.

Las pestañas no tienen borde inferior y se apoyan sobre una línea negra de 2px, como fichas de un bibliorato.

## Components

### Buttons
Sobrios y precisos: una caja con borde, el texto en 600 y nada más.
- **Shape:** rectos (0px), borde negro de 2px, alto mínimo de 36px (44px en celular).
- **Default:** fondo blanco y texto negro.
- **Primario:** invertido, fondo negro y texto blanco.
- **En el encabezado:** fondo transparente sobre negro, con borde y texto blancos.
- **Active:** baja 1px (`translateY(1px)`). **Disabled:** 55% de opacidad.
- **Focus:** contorno de 2px con 2px de separación, negro (blanco dentro del encabezado).

### Segmented control
- Grupo de botones unidos por un borde de 2px y divididos por líneas de 2px. El elegido (`aria-pressed`) se invierte a negro.

### Tabs
- Fichas rectas con borde de 2px y sin borde inferior, apoyadas sobre la línea negra de la barra.
- **Activa:** invertida; el nombre se edita en el lugar en 800/16px, con subrayado al enfocar.
- **Importante:** barra interna de 4px a la izquierda y texto en 800.
- "Ocultar" va como texto subrayado de 11px, no como botón.

### Inputs / Fields
- **Sueltos (búsqueda, selects, modales):** borde negro de 2px, fondo blanco, rectos, 36–44px de alto.
- **Dentro de la tabla:** sin borde visible en reposo; gris trazo al pasar el mouse; negro con fondo blanco al enfocar. En celular el borde gris queda siempre visible.
- **En el encabezado:** solo una línea inferior de 1px, sobre negro.
- **Checkbox:** nativo de 18px con `accent-color` negro, dentro de un área de toque de 36px.

### Estado (SI / NO)
Componente propio del sistema: un botón que ocupa todo el ancho de la celda y alterna entre NO (blanco con borde) y SI (invertido). Usa 800, 11px, con tracking de 0.04em, y en celular sube a 44px de alto y 13px. Una tarea hecha además se tacha en gris lápiz.

### Cards / Containers
- **Paneles** (obras, grupos de controles, avisos, dashboard): fondo blanco, borde negro de 2px, rectos, padding de 10–14px (24px en el dashboard).
- **Obra:** caja con borde; la obra actual se invierte y su barra de avance también (blanco sobre negro). Adentro, un `<button>` es el control para abrirla y el desplegable de pisos va como hermano, nunca dentro del botón. El foco se marca en toda la caja.
- **Filas como tarjeta** (celular): caja con borde de 2px y 8px de padding, sin franjas; las importantes llevan borde izquierdo de 4px.

### Barra de avance
- Caja de 12px de alto (10px por piso) con borde de 2px y relleno negro sólido. Se anima con `width .35s ease`, sin animación si el usuario pidió reducir el movimiento.

### Navigation (encabezado)
- Banda negra a todo el ancho, con el logo 3dF de 52px (44px en celular), el título en 800 y los datos de la obra en campos con línea inferior. El bloque de sincronización es una grilla de botones de 36px con el estado de Drive debajo, en 11px gris trazo.
- La insignia de versión ("Viendo: Oficial") es una caja con borde blanco de 1px, en 700/12px.

### Modales
- Todo panel superpuesto (Drive, confirmar foto, visor, editor de fotos) es `role="dialog"` con `aria-modal`: al abrir lleva el foco adentro, Tab no sale, Escape cierra y el foco vuelve al control que lo abrió. El dashboard usa `<dialog>` nativo.
- Velo negro al 72%. Caja blanca con borde de 2px, recta y sin sombra, de hasta 460px de ancho (1050px el dashboard). La X para cerrar tiene un área de toque de 44px.

## Do's and Don'ts

### Do:
- **Do** usar solo los tokens de negro, blanco y grises en la interfaz. Los marcadores rojo y amarillo quedan dentro del editor de fotos.
- **Do** cerrar cada control y contenedor con un borde negro de 2px y radio 0.
- **Do** marcar lo activo o elegido invirtiendo a negro con texto blanco.
- **Do** usar Archivo 800 con `tabular-nums` para toda cifra que se compare (totales, %, avance por obra o piso).
- **Do** subir los campos a 16px y los blancos de toque a 44px por debajo de 820px. En el celular, la regla tiene que ser al menos tan específica como la de compu que pisa.
- **Do** mantener el contorno de foco de 2px con separación de 2px, blanco dentro del encabezado.

### Don't:
- **Don't** usar neumorfismo, sombras difusas, esquinas redondeadas ni degradés.
- **Don't** usar el branding, los colores ni la tipografía de constructora-demo o Teskel.
- **Don't** agregar un color de acento para estados; el invertido es el acento.
- **Don't** reemplazar Archivo ni sumar una segunda familia tipográfica.
- **Don't** usar `box-shadow` salvo la barra interna de 4px que marca lo importante.
