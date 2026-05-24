# Bolsillo · Finanzas

App de finanzas personales para iPhone (PWA). Tus datos viven solo en tu dispositivo.

## Cómo instalarla en tu iPhone

Para que funcione como app real (icono en pantalla de inicio, pantalla completa, offline), necesitas servirla desde internet. Tienes tres opciones:

### Opción 1: GitHub Pages (gratis, recomendada)

1. Crea una cuenta en [github.com](https://github.com) si no tienes
2. Crea un repositorio nuevo llamado `bolsillo` (puede ser público)
3. Sube los 5 archivos: `index.html`, `manifest.json`, `sw.js`, `icon-192.png`, `icon-512.png`
4. Ve a **Settings → Pages → Source: main branch / root**
5. Espera 1-2 minutos. Tu app estará en: `https://TUUSUARIO.github.io/bolsillo/`

### Opción 2: Netlify Drop (gratis, sin cuenta)

1. Ve a [app.netlify.com/drop](https://app.netlify.com/drop)
2. Arrastra la carpeta completa
3. Te da una URL al instante (tipo `https://nombre-aleatorio.netlify.app`)

### Opción 3: Probar local sin servidor

Abre `index.html` directamente en Safari del iPhone (subiéndolo a iCloud Drive o enviándotelo por AirDrop). Funciona pero algunas features (service worker, notificaciones) requieren HTTPS.

## Instalarla en pantalla de inicio (iPhone)

1. Abre la URL en **Safari** (no Chrome — Safari es el único que permite instalar PWAs en iOS)
2. Toca el botón **Compartir** (cuadrado con flecha hacia arriba) en la barra inferior
3. Desliza y toca **"Agregar a pantalla de inicio"**
4. Confirma el nombre y toca **Agregar**

Listo. Ya tienes Bolsillo como app en tu pantalla de inicio. Se abre en pantalla completa, sin barra de Safari.

## Funcionalidades

- ✅ Registrar ingresos y gastos con monto, descripción y categoría
- ✅ Categorías predefinidas (comida, salidas, ropa, transporte, etc.)
- ✅ Balance mensual automático
- ✅ Metas de ahorro tipo "bolsillos NU" con barra de progreso
- ✅ Aportes manuales a cada meta
- ✅ Reportes: gastos por categoría, tasa de ahorro, totales
- ✅ Recordatorios diarios (notificaciones)
- ✅ Exportar/importar respaldos en JSON
- ✅ Funciona 100% offline después de la primera carga
- ✅ Todos los datos guardados localmente (privado)

## Respaldos

Tus datos viven en `localStorage` del navegador. Si borras los datos de Safari o desinstalas la app, se pierden. **Exporta un respaldo periódicamente** desde Ajustes → Exportar datos.

## Personalización

Todo el código está en un solo archivo: `index.html`. Edítalo libremente:

- **Colores**: variables CSS al inicio (`--bg`, `--accent`, etc.)
- **Categorías**: array `CATEGORIES` en el script
- **Emojis de metas**: array `EMOJIS`
- **Moneda**: cambia `'es-CO'` y `'COP'` en las funciones de formato

## Próximas mejoras posibles

- Filtrar movimientos por mes/categoría
- Gráficos visuales (chart.js)
- Presupuesto mensual por categoría con alertas
- Movimientos recurrentes (sueldo, suscripciones)
- Múltiples cuentas (efectivo, banco, NU)
- Aportes automáticos a metas al recibir un ingreso

Cuando quieras agregar alguna, dime y la integramos.
