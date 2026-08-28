# envolventes-via-puentes
Automatización del cálculo de fuerzas internas y envolventes en vías continuas de puentes según la norma AASHTO LRFD, evaluando el tránsito de cargas vehiculares móviles para generar matrices de diseño en Excel, planos de combinaciones críticas en PNG y animaciones secuenciales en GIF.
Análisis de Envolventes AASHTO LRFD para Puentes 🌉

Este repositorio contiene un algoritmo paramétrico desarrollado en Python para el análisis dinámico y estático de vigas continuas en superestructuras de puentes, evaluando el tránsito de cargas vehiculares móviles (HL-93).

📋 Descripción Técnica

El código resuelve la hiperestaticidad de vigas de múltiples tramos utilizando el Teorema de los Tres Momentos.

Evalúa el paso iterativo del Camión de Diseño (HS-20) y el Tándem, combinándolos con la alternancia de la Carga de Carril distribuida para encontrar las envolventes máximas de diseño basándose en los criterios de la norma AASHTO LRFD.

🚀 Características Principales

Cumplimiento Normativo: Ejecuta automáticamente la combinación extrema de diseño 1.33(Camión o Tándem) + Carril evaluada sección por sección a lo largo de toda la estructura.

Data Matricial (Excel): Exporta el archivo Fuerzas Internas por Via.xlsx con la discretización exacta punto a punto (dx = 0.05m). Esta matriz cruda está lista para el procesamiento de factores de distribución transversal para momento y cortante en el diseño de vigas interiores y exteriores.

Planos de Diseño (PNG): Genera la gráfica estática de la envolvente gobernante (DFC y DMF), detectando y acotando de forma automática los picos máximos y mínimos locales en cada apoyo y centro de vano.

Verificación Dinámica (GIF): Renderiza una animación secuencial del barrido vehicular. Permite visualizar cómo las líneas de estado instantáneas tocan y forman los límites teóricos de la envolvente gris de diseño.

Reporte Automatizado: Despliega un resumen tabular inmediato en consola con las reacciones extremas por apoyo y los esfuerzos máximos absolutos por tramo.

🛠️ Requisitos

Para ejecutar este script necesitas tener instalado Python 3.x y las siguientes librerías de cálculo y visualización:

numpy

pandas

matplotlib

Puedes instalarlas rápidamente ejecutando el siguiente comando en tu terminal:

Bash
pip install numpy pandas matplotlib
