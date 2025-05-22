# Wave Digital Filters (WDF) – Estudio Teórico y Comparativo

Este repositorio contiene una serie de notebooks teórico-prácticos diseñados para comprender el funcionamiento de los Wave Digital Filters (WDF) y su aplicación en la simulación de circuitos analógicos con fines de procesamiento de audio digital.

El objetivo es documentar progresivamente cada etapa del pipeline, desde los conceptos fundamentales hasta implementaciones comparativas usando `pywdf`, LTSpice y JUCE (C++).

---

## 📁 Contenido del repositorio

### ✅ `01_Ports_and_Waves.ipynb`
- Introducción a los conceptos base de WDF.
- Qué es un puerto adaptado, cómo se definen las ondas `a` y `b`.
- Propagación de señales unidimensionales en puertos ideales.

---

### ✅ `02_OnePorts_Algebraicos.ipynb`
- Implementación de elementos resistivos (resistencias, cortocircuito, circuito abierto).
- Cálculo de impedancias equivalentes y ondas reflejadas.
- Evaluación del comportamiento estático de componentes no reactivos.

---

### ✅ `03_OnePorts_Reactivos.ipynb`
- Introducción de elementos dependientes del tiempo: capacitor e inductor.
- Cálculo de impedancias discretizadas dependientes del muestreo.
- Revisión del estado interno y su rol en la propagación de ondas.

---

### ✅ `04_Adaptadores.ipynb`
- Construcción de adaptadores Serie y Paralelo (`SeriesAdaptor`, `ParallelAdaptor`).
- Uso del principio de conservación de energía en la unión de dos puertos.
- Validación práctica de la propagación de ondas con topologías compuestas.

---

### ✅ `05_Arboles_y_Conexiones.ipynb`
- Estructuración jerárquica de los componentes en un árbol WDF válido.
- Conexión de adaptadores con fuentes y receptores.
- Ejemplo completo con árbol simple: resistencia y capacitor en serie.

---

### ✅ `06_RC_Filtros_RC_FirstOrder.ipynb`
- Implementación de dos filtros **RC de primer orden** en `pywdf`:
  - Filtro **LowPass**: Resistor seguido de capacitor.
  - Filtro **HighPass**: Capacitor seguido de resistor.
- Análisis detallado:
  - Respuesta en frecuencia (`.plot_freqz()`)
  - Respuesta transitoria (`.AC_transient_analysis()`)
  - Exportación de impulso como `.wav`

---

### ✅ `07_RC_Filtros_RC_FirstOrder_Comparacion_LTSpice.ipynb`
- Comparación cuantitativa entre la simulación WDF y LTSpice:
  - Análisis AC de un filtro LowPass RC de primer orden a 100 Hz.
  - Carga de archivos `.txt` de LTSpice.
  - Generación del espectro en `pywdf` por FFT y comparación de magnitud/fase.
  - Cálculo del **error cuadrático medio (MSE)** entre ambas curvas.

---

## 📦 Archivos auxiliares

- `frequency_analysis_dc_100hz_1st_order_lpf.txt`:  
  Resultado del análisis AC exportado desde LTSpice para el filtro RC LowPass.

---

## 🛠️ Próximos pasos

🔜 En desarrollo:

- Implementación de:
  - Filtros RC de segundo orden (cascada de dos etapas)
  - Filtro RC BandPass
- Comparación directa con:
  - Simulaciones en LTSpice
  - Implementaciones en C++ con JUCE (`WDFRC2LowPassCascade`, `WDFRCHighPassCascade`)
  - Prototipos VST para pruebas auditivas

---

## 📚 Requisitos

- Python 3.8+
- [`pywdf`](https://github.com/gusanthon/pywdf) – librería para simulación de filtros WDF
- Otras dependencias:
  ```bash
  pip install numpy matplotlib scipy scikit-learn
  pip install git+https://github.com/gusanthon/pywdf
