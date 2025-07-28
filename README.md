# Análisis predictivo del mercado de autos usados en Europa

Este repositorio incluye dos versiones del análisis:

- `workflow_autos.ipynb`: notebook sin outputs (versión liviana para revisión o ejecución local).
- `workflow_autos_visual.html`: notebook exportado con las visualizaciones y resultados.

> El archivo `.ipynb` original con outputs completos excedía los límites de GitHub, por lo que fue exportado como `.html` para conservar los gráficos no interactivos sin afectar el rendimiento.  
> Las visualizaciones interactivas no estarán ejecutadas en el `.html`, pero están disponibles para la ejecución local en el `.ipynb`.

# Introducción y objetivos generales

Este informe tiene como objetivo el análisis de un mercado de vehículos en Europa. La base de datos utilizada está compuesta por más de 50.000 registros de una plataforma de compra y venta de vehículos con una gran cantidad de variables útiles al momento de realizar modelos predictivos y análisis gráficos y estadísticos. Se propuso un modelo donde el precio de los vehículos está en función de variables tales como la potencia del motor el kilometraje el año de fabricación el tipo de transmisión (manual o automático) y el combustible utilizado.

Este trabajo no solamente se limitó al desarrollo de un modelo predictivo, sino que recorrió todas las fases del ciclo de ciencia de datos: se limpió el dataset, se realizó una transformación de las variables, se realizó un análisis de gráficos de forma tanto técnica como de un estilo más simple para que sea posible de entender para todos los individuos que lo lean además se segmento el mercado ya que se observaron patrones claros y se aplicaron algoritmos de machine learning. Todo esto brindó una perspectiva técnica con una lectura económica orientada a la toma de decisiones útil.

En un contexto donde el análisis de datos se consolida como una herramienta estratégica para distintos actores del mercado, este trabajo demuestra el potencial de la ciencia de datos aplicada. Mediante el uso de técnicas modernas de aprendizaje supervisado, combinadas con bibliotecas especializadas de Python, se logró no solo estimar precios con un nivel de error razonable, sino también resolver los principales determinantes del valor de un automóvil usado.

# Estrategia metodológica y validación del enfoque

La metodología de trabajo se desarrolló en cuatro etapas: comenzó con limpieza de datos, luego se realizó un análisis exploratorio, se propusieron modelos predictivos, los cuales fueron evaluados y comparados con métricas claras, y por último se ofreció un ejemplo práctico en el mundo real para testear la performance del modelo.

La primera etapa que consiste en la limpieza de la base de datos eliminó registros incompletos o con valores extremos además se generaron variables nuevas a partir de las ya existentes que permitieron un análisis más riguroso. Un ejemplo es el cálculo de la antigüedad de cada vehículo, lo que nos ayudó a capturar el grado de depreciación marginal de cada automóvil.

En el análisis exploratorio se intentó comprender la dinámica del mercado automovilístico desde las relaciones entre las variables. Para ello se propusieron gráficos tanto normales como interactivos que ofrecen un grado de profundidad mayor para quien quiera adentrarse más en las visualizaciones. Aquí se detectaron patrones relevantes como por ejemplo se confirmó que los autos más potentes tienen precios más elevados y que factores como el tipo de transmisión influyen significativamente en el valor del vehículo. Además de esto se identificaron grupos claramente diferenciados estos son: económicos, de gama media y premium que tenían una distinción clara en las variables.

En el momento de construir los modelos predictivos se ofrecieron 3 alternativas que al ser comparadas se observó que el mejor desempeño lo obtuvo un modelo moderno con un nivel de precisión que devolvió un margen de error bajo y gran consistencia. Dicho modelo luego fue aplicado en un ejemplo práctico del mundo real.

# Resultados, hallazgos clave y limitaciones

Tal como venimos diciendo (y no es novedad), a lo largo del proceso de entrenamiento y validación de los modelos se comprobó claramente que ciertas características técnicas tales como la potencia, la antigüedad y el tipo de transmisión tienen alta influencia sobre el precio de venta.

El modelo final, que demostró un desempeño destacado, fue aplicado sobre un conjunto de autos reales con el objetivo de evaluar la calidad de sus estimaciones. En la mayoría de los casos, las predicciones fueron cercanas al valor de mercado, lo que validó su eficacia como modelo predictivo. Sin embargo, también se detectaron errores relevantes en ciertos segmentos, especialmente en vehículos menos comunes o con atributos que no estaban suficientemente representados en los datos originales. Se observaron, por ejemplo, casos de sobreestimación en autos de gama baja y subestimación en modelos premium o atípicos.

Con el objetivo de analizar estas desviaciones se propusieron gráficos y tablas que compararon los precios reales con las estimaciones del modelo, también se ofrecieron rankings de error por unidad y métricas clave. Este análisis facilitó identificar los patrones de error, tales como las dificultades que presenta el modelo para valorar de forma correcta vehículos con valores extremos en sus variables, por ejemplo kilometraje muy alto, motores con muy baja potencia o que presentaban combinaciones inusuales de variables. Esto igualmente es esperado cuando se tiene un dataset tan heterogéneo y con valores atípicos frecuentes.

Además de un enfoque predictivo. Se realizó una división en clusters lo que permite identificar con claridad cuatro grupos claramente separados por sus características, estos son:

- Vehículos deportivos o de alta gama: alta potencia, antigüedad y kilometraje bajos.
- Vehículos usados de gama media: antigüedad y kilometraje promedio y potencia baja.
- Vehículos con poca vida útil restante: kilometraje y antigüedad muy alta y potencia muy baja.
- Vehículos económicos nuevos: potencia media-baja y antigüedad y kilometraje muy bajos.

Cada uno de estos segmentos presenta una estructura de precios y atributos técnicos claramente diferenciados. Esta información es clave en el momento de la formulación de estrategias de segmentación de fijación de precios o de diseño de políticas comerciales.

Es importante aclarar que a pesar de que estos resultados sean significativos se identificaron limitaciones importantes. Una de las más relevantes es la ausencia de variables. Ejemplo de esto son:

- El estado general del vehículo, ya que tenemos el kilometraje, pero no sabemos el estado del automóvil.
- Su ubicación geográfica, debido a que el traslado representa un costo importante.
- La versión específica de cada auto, ya que se ofrecen marcas, pero no necesariamente el modelo específico.
- Entre otras variables importantes.

La ausencia de estas variables podría explicar la diferencia entre el precio real y el que efectivamente estimó el modelo. Es importante aclarar esto, ya que algunos errores de estimación no necesariamente reflejan fallas del modelo sino carencias de la información disponible.

Además, se observaron posibles sesgos en el dataset, tales como la presencia de marcas populares que pueden haber influido en la performance del modelo al generalizar sobre segmentos menos representados. Es importante tener en cuenta estos sesgos, ya que, si no se abordan adecuadamente, podrían generar problemas éticos, económicos y derivar en una toma de decisiones incorrecta. Respetar estos límites y tomar acción al respecto es una parte fundamental de un enfoque responsable en la ciencia de datos.

# Reflexiones finales: ética, gobernanza y proyección del trabajo

Más allá de los buenos resultados alcanzados en términos de precisión predictiva, el trabajo adoptó una mirada crítica sobre el uso de modelos de machine learning en contextos económicos reales. Se reconoció que la calidad técnica de un algoritmo no garantiza por sí sola transparencia, equidad ni legitimidad. En este sentido, se subrayó la importancia de acompañar el desarrollo de modelos con principios de gobernanza de datos que garanticen trazabilidad, documentación clara, control de versiones y validación continua de las variables y supuestos utilizados.

Se le dió atención y se denotaron los riesgos de aplicar predicciones automatizadas en decisiones económicas sensibles, como la fijación del valor de venta de un automóvil. Para mitigar estos riesgos, se enfatizó la necesidad de contar con procesos auditables y herramientas que permitan revisar, explicar y corregir errores sistemáticos. La ciencia de datos no debe convertirse en una “caja negra”, sino en una herramienta transparente y explicable, alineada con valores éticos y criterios profesionales.

Desde esa perspectiva, este trabajo no solo aportó un ejercicio técnico de modelado predictivo, sino también una reflexión sobre el rol social y económico de la ciencia de datos. Se abordó un problema relevante la estimación del precio de vehículos usados aplicando de forma sistemática todas las etapas del ciclo: desde la recolección y limpieza inicial, pasando por la exploración visual, la transformación de variables y la construcción de modelos, hasta su validación y aplicación práctica.

Los resultados validaron el enfoque elegido. El modelo XGBoost, que combinó precisión con capacidad de generalización, demostró ser una herramienta eficaz para estimar precios con un margen de error razonable. A su vez, el análisis de errores y la segmentación del mercado permitieron identificar patrones económicos subyacentes, enriqueciendo la comprensión del sector automotor con evidencia empírica.

Desde el punto de vista académico, el proyecto permitió consolidar habilidades técnicas, analíticas y críticas en un entorno realista. Y desde una perspectiva aplicada, abre múltiples posibilidades para desarrollos futuros.

