# Optimización matemática con Python ([Pyomo](http://www.pyomo.org/) vs GAMS)
Ejemplos de introducción a la optimización con [Pyomo](http://www.pyomo.org/) (Python) y diapositivas presentadas por Daniel Domene y Carlos Planelles durante la PyConES 2015 celebrada en Valencia ([ver diapositivas](http://www.slideshare.net/CAChemE/optimizacion-con-python-pyomo-vs-gams-vs-ampl)).

OPEN SOURCE SOLVERS:
  Linear solvers
  Nonlinear solvers
  Constraint programming solvers
  NEOS solvers

Se pueden descargar en:
  http://ampl.com/products/solvers/open-source/

El ejecutable del solver debe añadirse al PATH ([ver documentación de Pyomo](http://www.pyomo.org/installation)).

Nota: en el problema MINLP, process synthesis, hay un fallo al aplicar big-M.

<iframe src="//www.slideshare.net/slideshow/embed_code/key/1wRhdfkPuj48Sw" width="595" height="485" frameborder="0" marginwidth="0" marginheight="0" scrolling="no" style="border:1px solid #CCC; border-width:1px; margin-bottom:5px; max-width: 100%;" allowfullscreen> </iframe> <div style="margin-bottom:5px"> <strong> <a href="//www.slideshare.net/CAChemE/optimizacion-con-python-pyomo-vs-gams-vs-ampl" title="Optimizacion con Python (Pyomo vs GAMS vs AMPL)" target="_blank">Optimizacion con Python (Pyomo vs GAMS vs AMPL)</a> </strong> from <strong><a href="//www.slideshare.net/CAChemE" target="_blank">CAChemE</a></strong> </div>

# ¿Por qué Pyomo?

La optimización o programación matemática mediante lenguajes de modelado algebraico ---comúnmente [GAMS](http://www.gams.com/), [AMPL](http://ampl.com/) y [AIMMS](http://www.aimms.com/)--- es utilizada en la industria para la resolución de diferentes problemas que van desde la selección óptima de equipos y recursos a la gestión logística de una empresa. [Pyomo](http://www.pyomo.org/) es un paquete de software de código abierto ---licenciado bajo BSD por [Sandia National Laboratories](http://www.sandia.gov/), USA--- desarrollado en Python, y que soporta un conjunto diverso de capacidades de optimización para la formulación y el análisis de modelos de optimización. En particular, Pyomo permite el modelado de problemas tipo [LP](https://en.wikipedia.org/wiki/Linear_programming), [QP](https://en.wikipedia.org/wiki/Quadratic_programming), [NP](https://en.wikipedia.org/wiki/Nonlinear_programming), MILP, MINLP, MISP entre otros y se comunica con los principales solvers comerciales, gratuitos y/o libres, así como la plataforma ofrecida por [NEOS](http://www.neos-server.org/neos/) server. La resolución mediante métodos de optimización ---comunes en un ámbito de investigación científica--- son a menudo desconocidos en la industria o bien delegados por falta de tiempo y/o recursos. Por tanto, su resolución acaba siendo mediante métodos menos eficientes que resultan en formas de trabajo con condiciones sustancialmente mejorables. Por este motivo, en esta charla, estudiantes de ingeniería química de la Universidad de Alicante realizarán una introducción visual a conceptos de optimización, presentarán Pyomo y mostrarán la resolución de casos de estudio de diferentes industrias mediante este lenguaje de modelado algebraico desarrollado en Python.

## *Resumen detallado*:
La optimización de procesos industriales ha experimentado un crecimiento considerable durante los últimos años. Las industrias modernas apuestan por ella para mejorar la producción, reducir los costes, disminuir el impacto ambiental e incrementar la seguridad. En este sentido, es sensata la introducción y formación de los nuevos ingenieros en esta rama de la ciencia. Resulta curioso pensar que en el ámbito de las ciencias de la computación, la optimización suele hacer referencia a la reducción en el tiempo de ejecución del programa. Pero la optimización matemática (también conocida como investigación de operaciones o programación matemática) no tiene nada que ver con este problema y, en muchos casos, la formación que se recibe en las universidades no pasa de explicar el algoritmo SIMPLEX para la resolución de problemas lineales con variables continuas. 

Un problema de optimización consiste, a grandes rasgos, en maximizar o minimizar una función real eligiendo sistemáticamente valores de entrada (tomados de un conjunto permitido) y calculando el valor de la función. Este problema se vuelve interesante cuando aparecen restricciones (lineales y no lineales) y variables enteras (para modelar la toma de decisiones discretas). Dos de los lenguajes de modelado comerciales más utilizados para resolver este tipo de problemas matemáticos son GAMS y AMPL. En Python existen varias bibliotecas que permiten resolver el mismo tipo de problemas como son [CVXOpt](http://cvxopt.org/), [CVXPy](http://www.cvxpy.org/en/latest/), [PulP](https://pythonhosted.org/PuLP/), [OpenOpt](http://openopt.org/Welcome), o Pyomo. Este último, Pyomo.org, resulta interesante ya que:
*  Permite la modelización matemática en Python tipo AMPL/GAMS
*  Se comunica directamente los principales solvers como GLPK, Gurobi, CPLEX, CBC y PICO
*  Es open source (licencia BSD) y está desarrollado por Sandia National Laboratories, USA.
*  Pyomo (antiguamente conocido como Coopr) es 100% gratuito, maduro y bien documentado
*  Soporta Python 3 y su instalación es sencilla
*  Se comunica con NEOS server (plataforma web que da acceso a solvers comerciales de forma gratuita)
*  Se adapta al modelado de problemas de todo tipo al estar desarrollado en Python

Por lo tanto, Pyomo proporciona una capacidad que se asocia comúnmente con lenguajes de modelado algebraico comerciales como AMPL, AIMMS y GAMS, pero los objetos de modelado de Pyomo están incrustados dentro de Python, un lenguaje de programación de alto nivel con todas las funciones con un rico conjunto bibliotecas científicas. Respecto a sus capacidades como lenguaje de modelado algebraico, Pyomo es compatible con una amplia gama de tipos de problemas de optimización, incluyendo entre otros:
*  Programación lineal
*  Programación cuadrática
*  Programación no lineal
*  Programación lineal entera mixta
*  Programación cuadrática mixta entero
*  Programación lineal entera mixta
*  Programación estocástica entera mixta
*  Programación disyuntiva generalizada
*  Ecuaciones algebraicas diferenciales

La presentación se dividió en tres partes bien diferenciadas:
1. Introducción a la optimización/programación matemática (10 min): Se realizará una introducción visual a los conceptos de optimización con restricciones (Linear Programing, Non-Linear Programing, ILP, MIP, MINLP). 
2. Introducción a la sintaxis de Pyomo y breves notas para la instalación (10 min): donde se verán ejemplos sencillos de optimización con Pyomo y se explicará de manera breve la manera de instalarlo. 
3. Serie de ejemplos de problemas de optimización en ingeniería (10 min): tomando especial atención a ejemplos resueltos de problemas de optimización reales en la industria e ingeniería química.

### ¿Quiénes somos?
[CAChemE](http://cacheme.org/) es una asociación sin ánimo de lucro formada por ingenieros químicos (profesionales, docentes y estudiantes) que pretende estimular las posibilidades de software en la ingeniería de procesos químicos. Nuestro objetivo es promover las ventajas de las nuevas herramientas de software libre disponibles y fomentar su uso tanto en la industria como en la universidad. La sede central de CAChemE se encuentra en el [Instituto Universitario de Ingeniería de Procesos Químicos](http://iipq.ua.es/) de la [Universidad de Alicante](http://www.ua.es/).
