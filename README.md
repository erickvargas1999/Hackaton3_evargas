# 🛒 Instacart Data Optimization - Hackatón III

Este repositorio contiene la arquitectura ETL y el diseño del Data Warehouse (DW) desarrollado para procesar y analizar los datos de Instacart, permitiendo una base sólida para modelos predictivos de demanda.

## 🚀 Arquitectura del Proyecto
El proyecto sigue un flujo de datos optimizado para alto volumen (32 millones de registros):
1. **Extracción:** AWS S3 (Archivos CSV).
2. **Staging:** SingleStore Cloud (Ingesta masiva).
3. **Data Warehouse:** Modelo Estrella en SingleStore con Surrogate Keys distribuidas.

## 🛠️ Stack Tecnológico
- **ETL:** Talend Open Studio 8.0.
- **Base de Datos:** SingleStore (Engine de alto rendimiento distribuido).
- **Infraestructura:** AWS (S3 para almacenamiento de fuentes).
- **Control de Versiones:** Git / GitHub.

## ⚙️ Optimizaciones Técnicas Aplicadas
- **JVM Tuning:** Configuración de `-Xmx4096M` para manejo de desbordamiento de memoria (Heap Space).
- **Parallel Loading:** Uso de `tUnite` y `Batch Size (20,000)` para acelerar la ingesta en SingleStore.
- **Performance:** Configuración de `Store on disk` en tMap para procesamiento de Lookups masivos (32M+ filas).

---
Desarrollado por: Erick Vargas
