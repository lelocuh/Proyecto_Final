# Sistema de gestión de biblioteca (SGB)

Proyecto de Programación de Computadores 2, Ingeniería de Software. Sistema de gestión de una biblioteca en Python para Google Colab, con arquitectura de tres capas, persistencia en archivos de texto en Google Drive e interfaz web con Gradio.

## Qué hace

- Usuarios: registro, consulta, actualización de contacto y estado, listado.
- Libros y categorías: registro, consulta por ISBN, título o categoría, listado de disponibles.
- Préstamos: préstamo con fecha límite según el tipo de usuario, validación de cupo, multas pendientes y disponibilidad, devolución, historial y vencidos.
- Reservas y multas: reserva de libros sin ejemplares atendida por orden de llegada, multa de COP 1.000 por día de retraso, pago de multas.
- Análisis de datos: libros más prestados, préstamos por categoría, morosidad por tipo de usuario, duración promedio de los préstamos y reporte de multas.

## Estructura del repositorio

```
SGB_completo.ipynb   notebook con todo el sistema
datos/               archivos .txt de prueba (campos separados por |)
diagramas/           diagramas en PNG y sus fuentes (carpeta fuentes/)
Documento_SGB.docx   documento del proyecto
```

## Cómo ejecutarlo en Google Colab

1. Abrir SGB_completo.ipynb en Colab.
2. Ir a Entorno de ejecución > Ejecutar todo y aceptar el permiso de Google Drive.
3. Los archivos se crean en MyDrive/SGB/datos/.
4. La interfaz aparece debajo de la última celda.

Para empezar con datos de ejemplo, subir el contenido de datos/ a MyDrive/SGB/datos/, o usar la pestaña Administración de la interfaz (Cargar datos de prueba), que reemplaza los archivos actuales.

## Pruebas

La celda 5.3 ejecuta las pruebas de integración sobre una carpeta temporal y no modifica los datos reales. También se pueden ejecutar desde la pestaña Administración.

## Notas

- La lógica usa solo la librería estándar de Python. Gradio forma parte de la interfaz y la lógica no lo importa.
- Las fechas se escriben como AAAA-MM-DD. Si se dejan vacías, se usa la fecha de hoy.
- Los datos de prueba son ficticios, salvo los registros tomados de los ejemplos del enunciado.
