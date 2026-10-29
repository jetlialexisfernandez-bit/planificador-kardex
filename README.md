# Planificador de materiales con kardex (ET505 · Semana 9)

## Propósito
Ampliación de mi Planificador de materiales de la semana 7. Se conservan el cálculo del total, el presupuesto de S/ 180.00 y la validación del pedido, y se añade un **kardex** (control de existencias físicas) con búsqueda, cambio de nombre por id, entradas/salidas, inactivación/eliminación, persistencia en localStorage y exportación de movimientos a CSV. Todos los datos son ficticios.

## Archivos
| Archivo | Para qué sirve |
|---|---|
| `index.html` | Página única. Contiene el planificador (S7) y, debajo, la sección `#kardex` (ids `k-*`). |
| `styles.css` | Estilos del planificador y, al final, el bloque de personalización S9 (color y tamaño de etiqueta, tabla, botones). |
| `app.js` | Lógica del planificador S7 (sin cambios): `calcularTotal`, `validarPedido`, eventos. |
| `kardex.js` | Lógica del kardex: `saldoDe`, `agregarMovimiento`, `exportarCSV`, eventos y localStorage (clave `et505-s9-kardex-v1`). |
| `README.md` | Este documento. |

## Ejecutar y usar
- Local: abrir `index.html` en el navegador (o con Live Server).
- Planificador: escribir material, cantidad (1–30) y precio (0.01–50); *Comprobar pedido* o *Confirmar simulación*.
- Kardex: crear material → seleccionarlo → registrar ENTRADA/SALIDA (enteros positivos). Existencia = entradas − salidas. Una salida mayor a la existencia se rechaza. *Cambiar nombre* actúa por id. *Eliminar o inactivar*: sin movimientos se elimina (con confirmación cancelable); con movimientos se inactiva y se conserva el historial. *Exportar CSV* descarga `movimientos-materiales.csv` (separador `;`, UTF-8 con BOM, abre en Excel).

## Publicación
Repositorio: [PEGAR URL DEL REPOSITORIO]
Sitio GitHub Pages: [PEGAR URL QUE GITHUB MUESTRA]

## Aportes y ayuda recibida
Trabajo individual. Ayuda de IA (Claude, Anthropic, 29/10/2026) para integrar los fragmentos del recurso S9 y ejecutar pruebas; detalle en el PDF de entrega.

## Límites
- localStorage guarda los datos solo en este navegador y este origen: no hay base de datos compartida ni multiusuario.
- El CSV es una copia de los movimientos; no se sincroniza con Excel.
- El saldo físico del kardex (unidades) es independiente del presupuesto en dinero del planificador.
- Datos ficticios; no ingresar datos personales.
