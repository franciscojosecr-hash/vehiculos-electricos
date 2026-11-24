# Fase II — Engineering Mathematics | Automotive and Smart Mobility

Estudio académico **exclusivamente simulado** que continúa un trabajo sobre vehículo eléctrico hipotético (1.800 kg, batería 75 kWh). No hay observaciones reales de conductores ni baterías.

## Archivos
- `analisis_vehiculos_electricos.ipynb`: carga, limpieza, funciones, P4, P5, M2, cinco gráficas y discusión de límites.
- `datos/demanda_simulada.csv`: 300 días simulados, 60 de cada año 1–5.
- `datos/bateria_modelo.csv`: nueve estimaciones deterministas de t=0 a 8.
- `datos/resumen_anual.csv`: estadísticas descriptivas.
- `graficas/`: imágenes reproducibles.
- `paper_fase_II_borrador.docx` y `.pdf`: borrador académico para revisar y adaptar.

## Reproducir
1. En Google Colab, sube el notebook y las carpetas `datos/` y `graficas/` respetando las rutas, o ejecuta localmente desde la raíz del repositorio.
2. Instala, si hace falta: `pip install numpy pandas scipy matplotlib jupyter`.
3. Ejecuta todas las celdas desde arriba hacia abajo.
4. Compara la tabla resumen con `datos/resumen_anual.csv` y verifica que se regeneren cinco imágenes en `graficas/`.

## Supuestos
Generación determinista con `np.random.default_rng(4002)` y 60 días por año. Temperatura uniforme entre 10 °C y 30 °C. Demanda en kWh/día: 240+12(año-1)+0,6(temperatura-20)+ruido N(0,10). Eventos de carga por día Poisson(0,8). Degradación de batería: H(t)=100(0,975)^t. Todo es **hipotético**. La tasa 2,5 % no fue medida y no garantiza durabilidad. La correlación temperatura-demanda se construyó deliberadamente, así que no prueba causalidad.

## Revisión antes de entregar
- Revisar redacción propia, verificar manualmente al menos un cálculo de cada método.
- Registrar una interacción real con IA y auditar su respuesta.
- Subir los archivos a un repositorio GitHub propio y añadir la URL real al PDF.
- Comprobar instrucciones finales del docente y plazos de entrega.
