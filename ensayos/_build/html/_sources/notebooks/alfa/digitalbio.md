# Elementos de biología digital

<br>
<p align="right"> 
—We actually made a map of the country, on the scale of a mile to the mile!
<br>
—Have you used it much? —I enquired.
<br>
—It has never been spread out.
<br>
<i>
Sylvie and Bruno Concluded, Chapter XI.
</i>
</p>
<br>

<p align="center"> <b>
§
</b>
</p>

**Las rulíadas**

Acabo de escuchar a Stephen Wolfram [improvisar](https://youtu.be/cPfbGA_hNVo?t=2331) una versión computacional del cuento *Del rigor en la ciencia*: si en una «rulíada» (*ruliad* en inglés, es decir, el entrelazamiento de todo lo que es computacionalmente posible, el resultado de seguir todas las reglas computacionales posibles de todas las formas posibles) existe un agente sin límites computacionales (*computationally unbounded*), entonces ese agente es la rulíada misma. En otras palabras: para que un agente tenga identidad e inteligibilidad, este debe ser computacionalmente limitado. O en otras: un agente computacionalmente infinito se confunde[^1] con aquello mismo que computa. Dicho de otra forma: 
<br>

> «Los Colegios de Cartógrafos levantaron un Mapa del Imperio, que tenía el tamaño del Imperio y coincidía puntualmente con él. Las Generaciones Siguientes entendieron que ese dilatado Mapa era Inútil».

<p align="center"> <b>
§
</b>
</p>

**Computationally bounded agents**

Para seguir con la idea de que somos agentes computacionalmente limitados, hablemos de algunas comparativas interesantes:

$1$. **Aprendizaje**. La [retropropagación](https://dantenoguez.github.io/notebooks/alfa/redes.html#la-regla-de-la-cadena-propagacion-hacia-atras) es un algoritmo de aprendizaje mucho más eficiente que el que sea que utilice el cerebro humano. Un modelo GPT-4 tiene alrededor de un billón de parámetros[^2], mientras que en el cerebro humano hay alrededor de [100 billones de sinapsis](https://medicine.yale.edu/lab/colon_ramos/overview/)[^3] y, aun así, GPT-4 sabe muchísimo más que un humano. Incluso si nos limitáramos a las áreas de Brodmann exclusivamente vinculadas al lenguaje, las cuales son 3 (las de Broca y la de Wernicke, o sea, el 14 % de todas las áreas), entonces estaríamos hablando de ~14 billones de sinapsis.

$2$. **FLOPS**. La [energía necesaria](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC5337805/) para activar una neurona con trifosfato de adenosina es de $2.468 \times 10^{-7} J$. El cuerpo completo de un humano promedio utiliza alrededor de 100 Watts estando en reposo[^4], y la tasa metábolica del cerebro representa el [20 %](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC2980962/) de esa cifra. De ahí, parece que tan solo [el 5 %](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC4418791/) es actividad neuronal. En suma, un solo Watt es dedicado a la actividad neuronal, de manera que el humano puede generar hasta $\frac{1}{2.468 \times 10^{−7}}J \approx 4$ millones de activaciones neuronales por segundo. Asumiendo que cada neurona tiene 1,000 sinapsis (o sea, 1,000 MAC —operaciones Multiply-Accumulate—), eso nos da un total de 2,000 FLOPS —operaciones de coma flotante por segundo; en este caso, una suma y una multiplicación— por neurona. En conjunto, los 4 millones de neuronas son apenas capaces de 8 GFLOPS. Incluso si concediéramos que el cerebro humano usa el 1 % de sus neuronas en un determinado momento, tendríamos 1 billón de sinapsis, es decir, 1 TFLOPS. En cualquier caso, una GPU 3090 del 2020 tiene una capacidad de 35.6 TFLOPS[^5], es decir, 30 veces mayor a ese generoso hipotético.

$3$. **Overhead**. Aquí la analogía ya es más complicada, pero parece que en el cerebro —o al menos en el mío— hay una sobrecarga (*overhead*) computacional significativa y un bajo ancho de banda (o alto coste por transferencia de datos). Cuando estoy concentrado y alguien me interrumpe para hablarme, me toma demasiado tiempo —y fastidio— poder responder, como si tuviera que detener la ejecución del programa, remover gran parte de lo que estaba usando de la memoria RAM, cargar los datos del nuevo tema que me plantearon desde el disco duro, preparar las nuevas instrucciones y, finalmente, computar la respuesta. El tiempo para completar ese tipo de operación está fundamentalmente determinado por todos esos preparativos, no por la computación misma. Lo peor es tener que volver a hacer lo mismo y por un costo todavía más alto cuando se quiere volver al mismo nivel de concentración previo.

$4$. **OK LLM**. No aprendiste algo nuevo, solo comprimiste la [distribución probabilística](https://raysolomonoff.com/publications/86.pdf) de un fenómeno. No es que no sepas qué decir, solamente alcanzaste tu límite máximo de *tokens*. No intentaste recordar algo, solamente computaste una búsqueda de similitud vectorial. Tus padres no te educan, solo están haciendo *prompt engineering*. No sigues el ejemplo de los demás, solo empleas el aprendizaje *few-shot*. No tienes déficit de atención, solo tienes una *context window* limitada. No tuviste una crisis existencial, más bien cambiaste la función de pérdida para optimizar tu felicidad. Y, finalmente, para despejar las telarañas mentales de quienes personifican a estos modelos: no es que estén mintiendo o «alucinen», simplemente recibieron un *input* fuera de la distribución.

<p align="center"> <b>
§
</b>
</p>

**Hutter Prize**

La idea de Hutter tiene sentido en esa misma línea: la compresión de datos es la mejor manera posible de que un agente computacionalmente limitado interactúe con una rulíada. Las leyes científicas son las reglas computacionales que [mejor comprimen](https://arxiv.org/abs/0812.4360) (*i. e.*, que describen la mayor cantidad de fenómenos con el menor volumen y la menor pérdida de información posible) una cantidad significativa de [fenómenos en el universo](https://people.idsia.ch/~juergen/digitalphysics.html).


[^1]: «por el hecho de que el poema es inagotable / y se confunde con la suma de las criaturas». 
[^2]: En realidad, se trata de un estimado; de cualquier forma, GPT-4 es significativamente superior a un humano. GPT-3 tiene 175 mil millones (alrededor de mil veces menos «sinapsis» que en un humano) de parámetros y también sabe mucho más que cualquier humano.
[^3]: Ojo: los gringos y nosotros medimos los billones, trillones, etc. de manera distinta. 100 *trillions* es 100 billones.
[^4]: Siendo más realistas, pero sesgándonos hacia la cola de la distribución: un consumo de 3,000 calorías en un día equivale a ~12,600 joules. Si el cerebro utiliza el 20 % de esa energía, tenemos 2,520 J diarios (602 calorías). En el caso de un jugador de ajedrez clase A tenemos, [como máximo](https://www.researchgate.net/publication/23455094_The_stress_of_chess_players_as_a_model_to_study_the_effects_of_psychological_stimuli_on_physiological_responses_An_example_of_substrate_oxidation_and_heart_rate_variability_in_man), ~1.7 calorías por minuto durante 9 horas (918 calorías), es decir, ~7.1 joules por minuto, o sea, 3,834 J en 9 horas y 0.11 J por segundo. $\frac{0.11}{2.468 \times 10^{−7}}J/s \approx 445,705$ activaciones neuronales por segundo. A 2,000 FLOPS por neurona, eso es 891 MFLOPS (!).
[^5]: Incluso George Hotz [sobreestima estas cifras](https://geohot.github.io/blog/jekyll/update/2022/02/17/brain-flops.html) y parece confundirse al hablar de una actividad neuronal del 1 %. La capacidad total del cerebro (100 billones de sinapsis) es de 100 TFLOPS, es decir, el 1 % debe calcularse con respecto a esos 100 billones.