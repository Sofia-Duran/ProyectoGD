[![Open in MATLAB Online](https://www.mathworks.com/images/responsive/global/open-in-matlab-online.svg)](https://matlab.mathworks.com/open/github/v1?repo=Sofia-Duran/ProyectoGD)
# Proyecto Dinámica Metabólica

## Información de las estudiantes
Sofía Cristina Durán Muñoz [22211752]; l22211752@tectijuana.edu.mx
Karla Emilia Silva Pérez [22211767]; l22211767@tectijuana.edu.mx

Gemelos Digitales

Ingeniería Biomédica

## Docente
Dr. Paul Antonio Valle Trujillo; paul.valle@tectijuana.edu.mx; https://biomath.xyz/

Departamento de Ingeniería Eléctrica y Electrónica, Tecnológico Nacional de México/IT Tijuana, Blvd. Alberto Limón Padilla s/n, Tijuana, C.P. 22454, B.C., México.

## Información general

El diseño de Gemelos Digitales en la biología de sistemas representa una herramienta crucial para comprender y predecir el comportamiento dinámico de los procesos metabólicos celulares. El propósito de este proyecto consiste en diseñar, parametrizar y validar un modelo computacional de alta fidelidad capaz de replicar la evolución temporal de una cascada metabólica interactiva compuesta por tres especies esenciales: un sustrato ($x$), un intermediario ($y$) y un producto final ($z$), utilizando datos experimentales. El sistema biológico fue modelado matemáticamente mediante un conjunto de tres Ecuaciones Diferenciales Ordinarias (EDOs) de primer orden acopladas, donde destacan interacciones no lineales complejas como el estímulo del producto sobre el sustrato ($k_1 z$) y la generación sinérgica del intermediario ($k_3 x z$). Ante la ausencia de una solución analítica, las ecuaciones se integraron numéricamente mediante el Método de Heun en MATLAB y se acoplaron a un algoritmo de regresión no lineal (fitnlm) asistido por barreras matemáticas para estimar con precisión sus seis parámetros cinéticos ($k_1$ a $k_6$). Adicionalmente, se calcularon analíticamente los puntos de equilibrio numérico para evaluar la estabilidad a largo plazo y la capacidad de homeostasis del sistema frente a perturbaciones. Los resultados muestran que el Gemelo Digital optimizado logra un ajuste de alta fidelidad respecto a las curvas experimentales de concentración versus tiempo, demostrando que la arquitectura propuesta captura eficazmente los mecanismos de autorregulación celular y consolidándose como una herramienta matemática predictiva válida para futuras aplicaciones de control y optimización biotecnológica.

## Objetivo del proyecto

Desarrollar un Gemelo Digital predictivo de una cascada metabólica celular a partir de datos experimentales, utilizando un sistema de ecuaciones diferenciales ordinarias ajustado mediante regresión no lineal, para validar y simular la dinámica de autorregulación del sistema.


El sistema simula una ruta de biosíntesis donde el flujo de masa sigue una secuencia lógica (x &rarr; y &rarr; z). La característica distintiva de este modelo es su mecanismo de control por retroalimentación negativa (Feedback Inhibition). En este proceso, la acumulación del producto final (z) inhibe la velocidad de entrada del sustrato inicial mediante una cinética de Hill. Este comportamiento es fundamental para la supervivencia celular, ya que permite mantener la homeostasis y evitar el desperdicio de recursos energéticos.

#### Palabras clave: Cascada metabólica; Gemelo digital; Homeostasis; Inhibición por retroalimentación; Regresión no lineal.

## Modelos para ajustar a los datos experimentales:
 El sistema se rige por un conjunto de tres Ecuaciones Diferenciales Ordinarias (EDOs) que describen las tasas de cambio de cada componente basándose en interacciones directas:
 Dinámica del Sustrato (x): 
 
$$
\dot{x}=k\left( \beta -x\right).
$$

La tasa de cambio del sustrato depende positivamente de la presencia del producto  (catalizada por el parámetro ), enfrentando una tasa de consumo basal constante representada por .

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
