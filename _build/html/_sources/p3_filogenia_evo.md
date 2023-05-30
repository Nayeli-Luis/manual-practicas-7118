# Filogenia y evolución

## Características generales

1. <font color="red">Esta práctica es para **todos/as/es**.</font>

2. Práctica que se entrega con su equipo de proyecto.

3. Entregables: 
  * Un archivo PDF con lo que se solicita durante el desarrollo de la práctica.

* Aunque la pregunta no solicite que pongan una cita, si se revisó algún artículo, libro, etc. para contestar alguna pregunta, DEBE ser citado apropiadamente. Recuerden que cuando consultamos algo, no lo traducimos literalmente, el ejercicio es comprenderlo y después poder explicarlo con nuestras palabras en un lenguaje apropiado. 
* El archivo PDF debe contener los nombres de TODOS los integrantes del equipo. 
* La entrega por Classroom es INDIVIDUAL. 


## Descubriendo un nuevo virus

En 2019 surgió un nuevo virus que conmocionó a la humanidad. Sin embargo, gracias a las tecnologías de secuenciación se logró obtener el genoma completo de este nuevo virus rápidamente. 

En aquel momento, era urgente saber todo lo que se pudiera del nuevo virus, incluyendo su origen. Si se conocía esta información, entonces iba a ser posible dar recomendaciones sobre tratamientos, valorar la agresividad del virus, la tasa de infección e incluso una posible vacuna.

Al tener una nueva secuencia, lo primero que viene a la mente es compararla con lo que ya existe en las bases de datos. 

1. Descarga el genoma completo del nuevo virus el cual se encuentra [aquí](https://www.ncbi.nlm.nih.gov/nuccore/NC_045512.2?report=fasta). 

a) ¿Cuál es el tamaño del genoma de este virus? ¿Cómo lograste saberlo?
b) ¿La secuencia fue publicada en algún artículo? Si es así, coloca la referencia en el formato que prefieras.
c) Si la secuencia tienen un artículo científico publicado, lee el resumen del artículo y explica con tus palabras en qué consistió la investigación. 

## Alineando secuencias

Cuando comparamos secuencias, lo primero que debemos hacer es alinear. El *National Center of Biotechnology Information* posee una herramienta llamada BLAST (*Basic Local Alignment Search Tool*). 

2. Ingresa a [la página web de BLAST](https://blast.ncbi.nlm.nih.gov/Blast.cgi) y da clic en "Nucleotide BLAST". Te va a aparecer una serie de secciones que hay que llenar. 

En la sección  <font color="#33B2FF">"Enter Query Sequence"</font> sube el arhivo FASTA que descargaste en la sección anterior o copia y pega la secuencia en el recuadro. 

En la siguiente sección <font color="#33B2FF">"Choose Search Set"</font> en <font color="#33B2FF">*Database*</font> selecciona <font color="#33B2FF">*Standard databases (nr etc):*</font> . Luego, en la sección de <font color="#33B2FF">*Organism*</font>  en el menú desplegable selecciona <font color="#33B2FF">*Nucleotide collection (nr/nt)*</font>  y en la seguiente linea, da click en <font color="#33B2FF">*exclude*</font>  e ingresa en el recuadro balnco  <font color="#33B2FF">*SARS-CoV-2 (taxid:2697049)*</font> . 

Y por último, en la sección <font color="#33B2FF">*Program Selection*</font> selecciona la opción <font color="#33B2FF">*Highly similar sequences (megablast)*</font> y luego clic en el botón  <font color="#33B2FF">*BLAST*</font> . De cualquier forma, a continuación una imagen por si tienes duda de como llenar esta sección. 

```{figure} images/blast.png
:height: 600px
:name: Blast-filled

Parámetros de BLAST.
```

Una vez que termina el "blasteo" (término acuñada por biólogos), el programa arroja una serie de registros. Estos registros son secuencias que han sido previamente descritas y se encuentran en el NCBI. Además, los registros arrojados son las secuencias que más se parecen a nuestra secuencia problema. 

a)  Según BLAST, ¿De dónde podría prevenir el virus? <font color="gray">*Checa la columna de description de los 100 registros que te arroja*</font>.
b) Investiga, ¿Qué significa "Per. ident" y "Query cover"?. No olvides colocar la referencia. 

Cuando "googleas" BLAST, el primer artículo que sale es de la bella Wikipedia y dice algo como:

> Es importante mencionar que BLAST usa un algoritmo heurístico por lo que no nos puede garantizar que ha encontrado la solución correcta. 

Y luego: 

> BLAST usa el algoritmo Smith-Waterman para realizar sus alineamientos. 

c) Imagina que eres el computólogo a cargo de un equipo, y que un biólogo/médico/químico te pregunta:¿Qué es un algoritmo heurístico y por qué eso implica que la solución  no es correcta?  ¿En qué consiste el algoritmo Smith-Waterman? 

Trata de explicarlo en los términos más simples que puedas (recuerda quien es tu público).

3. En un estudio de este tipo, probablemente no sea buena idea llevar a cabo una comparación por pares. Ya que podríamos llegar a una conclusión errónea, como que el SARS-COVID-2 fue creado en un laboratorio, ¿Te suena esa teoría?. Ahora, llevaremos a cabo un alineamiento múltiple (*Multiple Sequence Alignment* o abreviado MSA). 

En la parte superior de la última columna <font color="#33B2FF">*Accesion*</font>, hay una opción que dice <font color="#33B2FF">*MSA Viewer*</font>, da clic ahí.  Aquí aparece una representación de los alineamientos y cada línea roja vertical significa que hay una posición que es diferente a la secuencia problema. La siguiente imagen explica cada región de esta ventana.

Revisa "a ojo" qué tan diferente es nuestra secuencia con la de cualquiera que diga *synthetic construct*. Ahora haz la comparación con alguna secuencia que diga *Bat coronavirus* y finalmente, con cualquiera que diga *Pangolin coronavirus*.

a) Si tenemos 40 secuencias problema, ¿Qué es preferible, un alineamiento por pares o un alineamiento múltple? ¿Por qué?

b) Indaga un poco más, ¿En qué consisten las secuencias que dicen "synthetic construct"? ¿Tendría sentido que el coronovarius haya sido creado en un laboratorio? ¿Qué opinas?

Vuelve a la página anterior y selecciona únicamente aquellas secuencias que corresponden a murciélago (*Bat coronavirus* o *Bat SARS-like coronavirus*) y a pangolín (*Pangolín coronavirus*). Vuelve a dar clic en el botón *MSA viewer*. 

d) ¿Son muy diferentes las secuencias entre el pangolín y murciélago?

e) En un alineamiento, ¿Por qué puede haber espacios en blanco? 

## Infiriendo el origen 

4. Como te habrás dado cuenta, saber si algo es muy diferente o no "a ojo" es bastante complicado, para eso existen los árboles filogenéticos. Vuelve a la ventana anterior y a la izquierda de <font color="#33B2FF">*MSA viewer*</font> hay una opción que dice <font color="#33B2FF">*Distance tree of results*</font>, da clic en esta opción. Se ha creado un árbol filogenético a través del método de evolución mínima; sin embargo, es importante considerar que los árboles generados por BLAST se basan en comparaciones entre pares y no en un alineamiento múltiple.

a) Adjunta una captura de pantalla del árbol que obtuviste. 

b) ¿Es importante primero alinear antes de construir un árbol filogenético? ¿Por qué?

c) ¿Podemos confiar en el árbol que ha generado BLAST? ¿Por qué?

d) ¿Por qué BLAST no genera árboles mediante alineamientos múltiples?

e) En función de lo que observas en el árbol filogenético, ¿Qué podrías decir sobre el origen del SARS-CoV-2? 

## Sacando conclusiones

Por último, en **al menos**  400 palabras contesta la siguiente pregunta:

¿Es mejor crear un árbol tomando en cuenta todo el genoma o es suficiente con algunos genes? 

*No hay una respuesta correcta o incorrecta, solo justifica tu respuesta. Explica todo lo que consideres que debe ser explicado, cita todo aquello que hayas consultado para responder a esta pregunta y, si lo deseas, toma un caso de estudio para poder ejemplificar.*


## Referencias
Andersen, K.G., Rambaut, A., Lipkin, W.I. et al. The proximal origin of SARS-CoV-2. *Nat Med* 26, 450–452 (2020). https://doi.org/10.1038/s41591-020-0820-9

Huang, Y., Yang, C., Xu, Xf. et al. Structural and functional properties of SARS-CoV-2 spike protein: potential antivirus drug development for COVID-19. *Acta Pharmacol Sin 41*, 1141–1149 (2020). https://doi.org/10.1038/s41401-020-0485-4

McGinnis S, Madden TL. BLAST: at the core of a powerful and diverse set of sequence analysis tools. *Nucleic Acids Res*. 2004 Jul 1;32(Web Server issue):W20-5. doi: 10.1093/nar/gkh435. PMID: 15215342; PMCID: PMC441573.