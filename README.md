[![Open in MATLAB Online](https://www.mathworks.com/images/responsive/global/open-in-matlab-online.svg)](https://matlab.mathworks.com/open/github/v1?repo=Dario-Mtz/Pr-ctica3GD)
 Práctica 3: Liberación controlada de fármacos por hidrogeles

 Información del estudiante

Darío Antonio Martínez Camarena
Ingeniería Biomédica

 Asignatura

Gemelos Digitales

 Docente

Dr. Paul Antonio Valle Trujillo

 Institución

Departamento de Ingeniería Eléctrica y Electrónica
Tecnológico Nacional de México / Instituto Tecnológico de Tijuana



 Descripción de la práctica

En el campo de la ingeniería biomédica, la liberación controlada de fármacos mediante hidrogeles representa una estrategia fundamental para mejorar la eficacia terapéutica y reducir efectos secundarios. Los hidrogeles son redes poliméricas capaces de retener grandes cantidades de agua y liberar compuestos activos de manera controlada en función del tiempo.

El modelado matemático de estos sistemas permite describir y predecir el comportamiento de liberación del fármaco, lo cual es esencial para el diseño de sistemas de administración eficientes. En este contexto, la experimentación *in silico* facilita el análisis de datos experimentales mediante el ajuste de modelos matemáticos y herramientas de regresión no lineal.

Palabras clave

Liberación controlada de fármacos; Hidrogeles; Farmacocinética; Regresión no lineal; Modelado matemático; Gemelos digitales; Sistemas dinámicos; Simulación in silico


 Objetivo

Determinar la tasa de liberación del hidrogel **N36 2MBA3** con base en datos experimentales mediante el ajuste de diferentes modelos matemáticos.



Modelos matemáticos utilizados

Ecuación de Peppas

Modelo empírico utilizado para describir mecanismos de difusión en sistemas poliméricos:

x(t) = k · tⁿ

Donde:

* k: constante de liberación
* n: exponente que describe el mecanismo de transporte



Modelo farmacocinético de primer orden

x(t) = β(1 - e^(-k·t))

Donde:

* β: liberación máxima
* k: constante de velocidad



Modelo empírico tipo Eureqa

x(t) = ρ₁ + ρ₂·t - ρ₃·t²

Modelo ajustado mediante regresión simbólica.



Modelo diferencial de primer orden

dx/dt = r₁ - r₂·x

Este modelo describe la dinámica de acumulación y eliminación del fármaco.



Datos experimentales

Los datos experimentales corresponden al porcentaje de liberación acumulada del fármaco en función del tiempo para diferentes hidrogeles.

Variables analizadas:

* N45-2MBA12
* N32
* N35-VP15
* N36-2MBA3

Los datos fueron importados desde el archivo `data3.csv` y procesados en MATLAB para su análisis y visualización.



Metodología

1. Importación de datos experimentales.
2. Visualización de curvas de liberación.
3. Aplicación de regresión no lineal para cada modelo:

   * Peppas
   * Farmacocinética
   * Eureqa
   * Modelo diferencial
4. Estimación de parámetros mediante `fitnlm`.
5. Evaluación estadística de los modelos:

   * R² (coeficiente de determinación)
   * SSE (error cuadrático)
   * AIC (criterio de Akaike)
6. Comparación entre modelos para determinar el mejor ajuste.



Resultados

Los modelos fueron ajustados exitosamente a los datos experimentales, obteniendo parámetros característicos para cada hidrogel.

El modelo farmacocinético presentó los valores más altos de R², indicando un mejor ajuste a los datos experimentales, especialmente para el hidrogel N36 2MBA3.

El modelo de Peppas permitió identificar el mecanismo de liberación a través del parámetro n, sugiriendo un comportamiento de difusión no puramente Fickiano.

El modelo Eureqa proporcionó un buen ajuste matemático, aunque sin interpretación física directa.

El modelo diferencial mostró una representación adecuada de la dinámica de liberación mediante ecuaciones diferenciales.



Discusión

Los resultados indican que la liberación del fármaco desde el hidrogel presenta un comportamiento característico de saturación, lo cual es consistente con modelos farmacocinéticos de primer orden.

El modelo de Peppas es útil en etapas iniciales del proceso, donde domina la difusión, mientras que el modelo farmacocinético describe mejor la fase completa del proceso de liberación.

Aunque el modelo Eureqa presenta un ajuste adecuado, su falta de base física limita su interpretación en aplicaciones biomédicas.

El uso de modelos diferenciales permite una representación más realista del sistema, facilitando la simulación de escenarios futuros en un entorno *in silico*.



Conclusiones

Se determinó la tasa de liberación del hidrogel N36 2MBA3 mediante el ajuste de modelos matemáticos a datos experimentales.

El modelo farmacocinético de primer orden resultó ser el más adecuado para describir el comportamiento global del sistema.

El análisis comparativo permitió identificar las ventajas y limitaciones de cada modelo, destacando la importancia del modelado matemático en el diseño de sistemas de liberación controlada.

Este enfoque contribuye al desarrollo de gemelos digitales en ingeniería biomédica, permitiendo predecir el comportamiento de sistemas terapéuticos en condiciones controladas.



 Archivos incluidos

* Cuaderno computacional de MATLAB (.mlx)
* Datos experimentales (`data3.csv`)
* Gráficas de resultados (.pdf)
* Código fuente de funciones
* Imágenes de simulaciones



Referencias

[1] M. A. González-Ayón et al., *PNVCL-PEGMA nanohydrogels with tailored transition temperature for controlled delivery of 5-fluorouracil*, Journal of Polymer Science Part A, 2015.

[2] P. A. Valle, Syllabus para Gemelos Digitales, TecNM Tijuana.
