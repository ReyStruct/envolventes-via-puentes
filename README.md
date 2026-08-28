# Análisis de Envolventes AASHTO LRFD para Puentes 🌉
Este repositorio contiene un algoritmo paramétrico desarrollado en Python para el análisis dinámico y estático de vigas continuas en superestructuras de puentes, evaluando el tránsito de cargas vehiculares móviles (HL-93).

# 📋 Descripción Técnica
El código ha sido programado para resolver la hiperestaticidad de vigas de múltiples tramos utilizando el Teorema de los Tres Momentos.

A diferencia de análisis estáticos simples, este script evalúa el paso iterativo del Camión de Diseño (HS-20) y el Tándem, combinándolos con la alternancia de la Carga de Carril distribuida para encontrar las envolventes máximas de diseño basándose en los criterios de la norma AASHTO LRFD.

# 🚀 Características Principales
Cumplimiento Normativo: Ejecuta automáticamente la combinación extrema de diseño 1.33(Camión o Tándem) + Carril evaluada sección por sección a lo largo de toda la estructura.

Data Matricial (Excel): Exporta el archivo Fuerzas Internas por Via.xlsx con la discretización exacta punto a punto (dx = 0.05m). Esta matriz cruda está lista para aplicar factores de distribución transversal en el diseño de vigas interiores y exteriores.

Planos de Diseño (PNG): Genera la gráfica estática de la envolvente gobernante (DFC y DMF), detectando y acotando de forma automática los picos máximos y mínimos locales en cada apoyo y centro de vano.

Verificación Dinámica (GIF): Renderiza una animación secuencial del barrido vehicular, permitiendo visualizar cómo las líneas de estado instantáneas tocan y forman los límites teóricos de la envolvente de diseño.

Reporte Automatizado: Despliega un resumen tabular inmediato en consola con las reacciones extremas por apoyo y los esfuerzos máximos absolutos por tramo.

# 🛠️ Requisitos
Para ejecutar este script necesitas tener instalado Python 3.x y las siguientes librerías de cálculo, manejo de datos y visualización:

* `numpy`
* `pandas`
* `matplotlib`

Puedes instalar las librerías con el siguiente comando:
```bash
pip install numpy pandas matplotlib openpyxl
