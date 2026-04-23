[![Open in MATLAB Online](https://www.mathworks.com/images/responsive/global/open-in-matlab-online.svg)](https://matlab.mathworks.com/open/github/v1?repo=carlosazaelr/Practica3GD)

# Práctica 3: Liberación controlada de fármacos por hidrogeles

## Información de la estudiante
Carlos A. Ramirez \[22212267]; L22212267@tectijuana.edu.mx

Gemelos Digitales

Ingeniería Biomédica

## Docente
Dr. Paul Antonio Valle Trujillo; paul.valle@tectijuana.edu.mx

Departamento de Ingeniería Eléctrica y Electrónica, Tecnológico Nacional de México/IT Tijuana, Blvd. Alberto Limón Padilla s/n, Tijuana, C.P. 22454, B.C., México.

## Descripción de la asignatura
La asignatura de Gemelos Digitales forma parte del plan de estudios de la carrera en Ingeniería Biomédica con la siguiente competencia general del curso: Formula el gemelo digital a través de datos experimentales para el desarrollo estrategias de control mediante teorías de sistemas dinámicos no lineales y la experimentación in silico. Esta asignatura pretende aportar al perfil del Ingeniero Biomédico la capacidad de realizar investigación científica en el área de Biología de Sistemas con la finalidad de dirigir y participar en equipos de trabajo interdisciplinarios en contextos nacionales e internacionales, así como de proporcionar soluciones informáticas para resolver problemas en el campo de la Ingeniería Biomédica con ética profesional.

En el contexto de sistemas dinámicos que describen sistemas biológicos o fisiológicos, el modelizado in silico es una extensión lógica de la experimentación in vitro controlada, es el resultado natural del gran aumento de la potencia computacional disponible a un costo que disminuye continuamente, combinando las ventajas de la experimentación in vivo e in vitro, sin someterse a las consideraciones éticas y la falta de control asociadas con los experimentos in vivo. A diferencia de los experimentos in vitro, que existen de forma aislada, los modelos in silico permiten incluir un conjunto prácticamente ilimitado de variables y parámetros, lo que hace que los resultados sean más aplicables en problemas del mundo real. La experimentación in silico ha dado lugar al paradigma denominado como "gemelos digitales" (en inglés digital twins); en esencia, los gemelos digitales son una réplica o representación digital de un proceso o sistema del mundo real, donde por replica se refiere a un modelo computacional desarrollado con base en datos experimentales y características especiales que le permiten conectar lo físico con lo virtual con el propósito de mejorar el rendimiento de un sistema, detectar y prevenir fallas, y realizar predicciones sobre su respuesta ante diferentes estímulos o escenarios de operación; una definición más formal establece que: un gemelo digital es un conjunto de modelos adaptativos que emulan el comportamiento de un sistema físico en un sistema virtual obteniendo datos en tiempo real para actualizarse a lo largo de su ciclo de vida; replica al sistema físico para predecir fallas y oportunidades de cambio, prescribir acciones en tiempo real para optimizar y/o mitigar eventos inesperados observando y evaluando el perfil operativo del sistema. En el campo particular de la Biología de Sistemas, un gemelo digital se presenta como un algoritmo o conjunto de algoritmos computacionales desarrollados con base en modelos mecanicistas de un organismo vivo, esto con el objetivo de emular su fisiología para ilustrar su dinámica en el corto y en el largo plazo, así como predecir su respuesta a diferentes estímulos endógenos y exógenos.

## Objetivo y descripción del sistema

El objetivo principal es determinar la tasa de liberación del hidrogel N36-2MBA3 con base en los datos experimentales de liberación acumulada. Para comprender la cinética de liberación controlada de este sistema de nanohidrogeles, se ajustarán cuatro modelos matemáticos distintos a los datos experimentales obtenidos a lo largo del tiempo. Los modelos propuestos se describen mediante las siguientes ecuaciones:

        x(t) = k*t^n                               (1)
        x(t) = beta*(1 - exp(-k*t))                (2)
        x(t) = (p1*t) / (p2 + t)                   (3)
        dx/dt = p1 - p2*x                          (4)

Donde $x(t)$ representa el porcentaje de liberación acumulada del fármaco en el tiempo $t$. La descripción de cada modelo del sistema se realiza a continuación. Primero, la Ecuación (1) corresponde a la ecuación de Korsmeyer-Peppas, un modelo utilizado empíricamente donde $k$ es una constante que incorpora características estructurales y geométricas de la matriz del hidrogel, y $n$ es el exponente de liberación que define el mecanismo de transporte del fármaco. La Ecuación (2) representa un modelo farmacocinético de primer orden, indicando que la tasa de liberación depende de la concentración, donde $\beta$ indica el porcentaje máximo de liberación y $k$ es la constante de la tasa de liberación.

Por otro lado, los modelos descritos en las Ecuaciones (3) y (4) son enfoques propuestos mediante herramientas de regresión simbólica (algoritmo Eureqa). La Ecuación (3) es una función explícita en el tiempo en forma de fracción racional, dependiente de los parámetros de ajuste $p_1$ y $p_2$. Finalmente, la Ecuación (4) plantea la dinámica de liberación estructurada como una Ecuación Diferencial Ordinaria (EDO) de primer orden, la cual indica que la tasa de cambio de la liberación del fármaco ($\dot{x}$) está gobernada por una relación lineal descendente dictada por $p_1$ y $p_2$.

Palabras clave: Hidrogeles; Liberación controlada; Modelado matemático; Regresión no lineal; Bioestadística.

## Actividades a realizar
1. Visualización de datos experimentales: Importar y graficar los datos experimentales de liberación acumulada del fármaco para los diferentes tipos de nanohidrogeles utilizando MATLAB.

2. Ajuste de modelos matemáticos: Aplicar técnicas de regresión no lineal (utilizando funciones como fitnlm) para ajustar distintos modelos cinéticos (ecuación de Korsmeyer-Peppas, farmacocinética de primer orden y funciones Eureqa) a los datos de la muestra.

3. Simulación de sistemas dinámicos (in silico): Resolver modelos estructurados como Ecuaciones Diferenciales Ordinarias (EDOs) mediante métodos numéricos (como ode45) para simular la trayectoria de liberación en el tiempo.

4. Análisis bioestadístico: Evaluar la bondad de ajuste de cada modelo calculando métricas estadísticas clave, incluyendo la R-cuadrada ordinaria, la Suma Residual de Cuadrados (SSE), el Criterio de Información de Akaike (AICc), el margen de error y los intervalos de confianza.

5. Generación de resultados gráficos: Crear y exportar figuras comparativas (en formato de subgráficas vectoriales) que contrasten visualmente los datos experimentales discretos contra las curvas predictivas continuas generadas por los modelos.
...

## Lista de archivos incluidos en el repositorio
1. Cuaderno computacional de MATLAB [.mlx].
2. Imágenes de las simulaciones [.pdf].
3. Análisis matemático [.pdf].
4. Diagrama biológico del sistema [.png].

## Referencias
\[1] P. A. Valle, Syllabus para Gemelos Digitales, Tecnológico Nacional de México / Instituto Tecnológico de Tijuana, Tijuana, B.C., México, 2025. Permalink: https://biomath.xyz/course/

\[2] M. A. González-Ayón, J.A. Sañudo-Barajas, L.A. Picos-Corrales, & A. Licea-Claverie, "PNVCL-PEGMA nanohydrogels with tailored transition temperature for controlled delivery of 5-fluorouracil", *Journal of Polymer Science Part A: Polymer Chemistry*, vol. 53, issue 22, pp. 2662-2672, Aug 2015. DOI: https://doi.org/10.1002/pola.27766

