[![Open in MATLAB Online](https://www.mathworks.com/images/responsive/global/open-in-matlab-online.svg)](https://matlab.mathworks.com/open/github/v1?repo=DrPaulValle/Hidrogeles)
# Taller: Estimación de tasas de liberación de fármacos por hidrogeles
<img width="1536" height="1024" alt="ChatGPT Image May 7, 2026, 12_43_10 PM" src="https://github.com/user-attachments/assets/d2d6f71e-fe25-467d-a153-cd84d1068c9a" />

## Instructor
Dr. Paul Antonio Valle Trujillo

paul.valle@tectijuana.edu.mx

https://biomath.xyz/

Departamento de Ingeniería Eléctrica y Electrónica, Tecnológico Nacional de México/IT Tijuana, Blvd. Alberto Limón Padilla s/n, Tijuana, C.P. 22454, B.C., México.

## Información general

En el contexto de sistemas dinámicos que describen sistemas biológicos o fisiológicos, el modelizado in silico es una extensión lógica de la experimentación in vitro controlada, es el resultado natural del gran aumento de la potencia computacional disponible a un costo que disminuye continuamente, combinando las ventajas de la experimentación in vivo e in vitro, sin someterse a las consideraciones éticas y la falta de control asociadas con los experimentos in vivo. A diferencia de los experimentos in vitro, que existen de forma aislada, los modelos in silico permiten incluir un conjunto prácticamente ilimitado de variables y parámetros, lo que hace que los resultados sean más aplicables en problemas del mundo real. La experimentación in silico ha dado lugar al paradigma denominado como "gemelos digitales" (en inglés digital twins); en esencia, los gemelos digitales son una réplica o representación digital de un proceso o sistema del mundo real, donde por replica se refiere a un modelo computacional desarrollado con base en datos experimentales y características especiales que le permiten conectar lo físico con lo virtual con el propósito de mejorar el rendimiento de un sistema, detectar y prevenir fallas, y realizar predicciones sobre su respuesta ante diferentes estímulos o escenarios de operación; una definición más formal establece que: un gemelo digital es un conjunto de modelos adaptativos que emulan el comportamiento de un sistema físico en un sistema virtual obteniendo datos en tiempo real para actualizarse a lo largo de su ciclo de vida; replica al sistema físico para predecir fallas y oportunidades de cambio, prescribir acciones en tiempo real para optimizar y/o mitigar eventos inesperados observando y evaluando el perfil operativo del sistema. En el campo particular de la Biología de Sistemas, un gemelo digital se presenta como un algoritmo o conjunto de algoritmos computacionales desarrollados con base en modelos mecanicistas de un organismo vivo, esto con el objetivo de emular su fisiología para ilustrar su dinámica en el corto y en el largo plazo, así como predecir su respuesta a diferentes estímulos endógenos y exógenos.

## Objetivo del taller

Determinar la tasa de liberación del hidrogel N36-2MBA3 con base en los datos experimentales de la siguiente figura.
<img width="1387" height="535" alt="paper" src="https://github.com/user-attachments/assets/eae73151-9476-4b0b-b10d-286792700391" />

Un hidrogel es un material formado por redes tridimensionales de polímeros hidrófilos capaces de absorber y retener grandes cantidades de agua sin disolverse. Debido a su alta biocompatibilidad y similitud con tejidos biológicos, los hidrogeles son ampliamente utilizados en aplicaciones biomédicas como liberación controlada de fármacos, ingeniería de tejidos y sistemas de administración terapéutica.
La estimación de la tasa de liberación de un fármaco es importante porque permite comprender y predecir cómo el medicamento es liberado desde el hidrogel hacia el organismo a lo largo del tiempo. Esto ayuda a diseñar tratamientos más eficientes y seguros, optimizando la dosis, reduciendo efectos secundarios y garantizando concentraciones terapéuticas adecuadas durante periodos prolongados. Además, el modelado matemático de la liberación permite comparar formulaciones, ajustar parámetros cinéticos y desarrollar sistemas inteligentes de administración controlada de medicamentos.

#### Palabras clave: Bioestadística; Farmacocinética; Hidrogel; MATLAB [fitnlm]; Modelo matemático; Regresión no lineal.

## Modelos para ajustar a los datos experimentales: Farmacocinética de primer orden
Ecuación diferencial ordinaria de primer orden:

$$
\dot{x}=k\left( \beta -x\right).
$$

Función del tiempo: 

$$
x\left( t\right) =\beta \left( 1-e^{-kt}\right).
$$

## Regresión no lineal
La regresión no lineal se basa en el método de mínimos cuadrados, permite ajustar modelos complejos a conjuntos de datos experimentales con diversas variables dependientes e independientes, además de distintos parámetros que describen las relaciones entre ellas; funciona mediante un enfoque iterativo y se debe elegir una estimación inicial para el valor de cada parámetro.

$$
\sum\limits_{i=1}^{n}\left[ x_{i}-f\left( \hat{x}_{i},\mathbf{\rho }\right) \right] ^{2}.
$$

## Referencias

\[1] M. A. González‐Ayón, J.A. Sañudo‐Barajas, L.A. Picos‐Corrales, & A. Licea‐Claverie, "PNVCL‐PEGMA nanohydrogels with tailored transition temperature for controlled delivery of 5‐fluorouracil", Journal of Polymer Science Part A: Polymer Chemistry, vol. 53, issue 22, pp. 2662-2672, Aug 2015. DOI: https://doi.org/10.1002/pola.27766.

\[2] H. Motulsky, Intuitive biostatistics: a nonmathematical guide to statistical thinking. 4th ed. Oxford, New York, USA: Oxford University Press, 2014.

\[3] Slavkova, K. P., Patel, S. H., Cacini, Z., Kazerouni, A. S., Gardner, A. L., Yankeelov, T. E., & Hormuth, D. A. (2023). Mathematical modelling of the dynamics of image-informed tumor habitats in a murine model of glioma. Scientific reports, 13(1), 2916. DOI: https://doi.org/10.1038/s41598-023-30010-6.

\[4] Garfinkel, Alan, Jane Shevtsov, and Yina Guo. Modeling life: the mathematics of biological systems. Springer International Publishing AG, 2017.

\[5] Bryan, Kurt. Differential equations: A toolbox for modeling the world. Simiode, 2022. Permalink: https://www.simiode.org/resources/8307.

\[6] MathWorks. (n.d.) fitnlm Fit nonlinear regression model [Online]. Available: https://www.mathworks.com/help/stats/fitnlm.html.
