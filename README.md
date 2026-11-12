# app-mis-comprobantes-arca-xubiohttps:Conciliación bancaria · Santander → Xubio
App web que convierte un resumen bancario digital de Santander (PDF) en el Excel importador de Xubio para la Conciliación Bancaria Automática. Permite revisar cada movimiento, controlar los saldos del extracto y descargar el archivo listo para importar.

Versión de la app: 1.4 · Manual: 06/11/2026

Privacidad
La app es un único archivo index.html que corre completa en el navegador.
No usa servidor, no requiere Python ni instalación.
Los PDF y Excel que cargás se procesan en tu equipo y no se envían a ningún lado.
La revisión no queda guardada: descargá el Excel antes de cerrar la página.
Cómo usarla
Abrí la app desde el enlace publicado (GitHub Pages) en Edge o Chrome. También funciona abriendo index.html localmente.
Cargá el PDF del resumen digital descargado de Santander. La app trae el modelo de Xubio incluido; si necesitás otro compatible, usá Cambiar plantilla (opcional).
Pulsá Procesar PDF y modelo y esperá el progreso por página. Elegir el archivo no inicia la lectura.
Revisá los movimientos:
Elegí la cuenta y la moneda en Cuenta a preparar (pesos y dólares se descargan por separado).
Controlá fecha, concepto, tipo e importe. Los créditos y débitos van con importe positivo.
Revisá el nombre del concepto (Transf. Apellido Nombre) y la etiqueta (por ejemplo, Cobros).
Cargá los saldos inicial y final del PDF y verificá que la diferencia sea cero: saldo inicial + créditos − débitos = saldo final.
Pulsá Descargar Excel.
En Xubio: Finanzas > Conciliación Bancaria Automática, elegí la cuenta contable y el período, y en Importar adjuntá el .xlsx generado.
Si Xubio acepta solo una parte, desmarcá en la app las filas ya aceptadas y descargá únicamente las rechazadas. No importes el mismo resumen por Excel y por PDF, para evitar duplicados.

El detalle paso a paso está en el manual (también se abre desde el botón Manual (PDF) de la app).

Formato del Excel generado
Conserva las seis columnas del modelo de Xubio: Fecha, Concepto, Importe, Débito, Crédito y Etiqueta. Los importes son numéricos, con dos decimales y sin separador de miles (ej.: 909871.42).

Alcance
Admite el diseño de resumen digital de Santander usado en las pruebas. Los PDF escaneados u otros diseños de banco necesitan adaptar el lector.

Archivos del repositorio
Archivo	Descripción
index.html	La app completa (incluye las librerías necesarias).
manual-conciliacion-bancaria.pdf	Manual de uso.
modelo-xubio-conciliacion-bancaria.xlsx	Modelo del importador de Xubio (botón Descargar modelo).
licencias/	Licencias de las librerías de terceros.
README.md	Este archivo.
Publicar en GitHub Pages
Subí todos los archivos a la raíz del repositorio, respetando la carpeta licencias/.
En Settings > Pages, elegí Deploy from a branch, rama main y carpeta / (root).
La app queda disponible en https://<usuario>.github.io/<repositorio>/.
Licencias de terceros
La app incluye estas librerías, cuyas licencias están en licencias/:

PDF.js (Mozilla), para leer el PDF: Apache License 2.0. Ver licencias/PDFjs-LICENSE.txt.
JSZip, para generar el Excel: MIT o GPLv3 (doble licencia). Ver licencias/JSZip-LICENSE.txt.
Estudio Borrione & Asociados · Área Administración
