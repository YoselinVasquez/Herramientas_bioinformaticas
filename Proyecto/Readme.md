# Análisis génico de enterobacterias resistentes a antibióticos betalactámicos de amplio espectro y carbapenémicos aisladas de agua y fauna local de la laguna Yarinacocha, Ucayali

## Resumen 
La resistencia antimicrobiana representa una amenaza creciente para la salud pública, especialmente donde el acceso al agua es limitado. En este estudio se evaluará la presencia de genes de resistencia a antibióticos betalactámicos de amplio espectro y carbapenémicos presentes en enterobacterias aisladas en muestras de agua y fauna local de la laguna Yarinacocha, ubicada en Ucayali, Perú. Existen diferentes actividades antropogénicas como el vertimiento de aguas residuales sin tratamiento o depósito de desechos, que afectan directamente a la laguna. Se recolectarán muestras de agua en distintos puntos de la laguna, así como heces de mamíferos, aves silvestres, y superficie de peces comercializados. Las bacterias serán aisladas y evaluadas fenotípicamente en medios con antibióticos. Posteriormente, se evaluará la presencia de bacterias productoras de ß-lactamasas de espectro extendido (BLEE) y/o carbapenemasas mediante métodos fenotípicos confirmatorios. Los aislados positivos a estas enzimas, serán caracterizados mediante secuenciamiento por Nanopore para la detección de genes de resistencia. Además, se realizará un análisis metagenómico 16S rRNA del agua para identificar la diversidad microbiana. El estudio permitirá evaluar la presencia de genes de resistencia circulantes en la laguna Yarinacocha, zona contaminada por actividades humanas.

## Hipótesis
Genes de resistencia a antibióticos betalactámicos de amplio espectro y carbapenémicos están presentes en Enterobacterias aisladas de muestras de un ambiente con impacto antropogénico (laguna Yarinacocha), así como en muestras fecales de animales domésticos y silvestres que habitan en sus proximidades.

## Objetivos
### Objetivo general
Caracterizar genes de resistencia a antibióticos betalactámicos de amplio espectro y carbapenémicos procedentes en Enterobacterias aisladas de muestras de ambiente con impacto antropogénico (laguna Yarinacocha), así como de animales domésticos y silvestres que habitan en sus proximidades.

### Objetivos específicos
• Evaluar a nivel fenotípico la resistencia a antibióticos de enterobacterias resistentes a betalactámicos de amplio espectro y carbapenemicos aisladas de la laguna Yarinacocha, animales domésticos y silvestres que habitan sus proximidades.
• Caracterizar a nivel génico la resistencia a antibióticos de enterobacterias resistentes a betalactámicos de amplio espectro y carbapenemicos aisladas de la laguna Yarinacocha, animales domésticos y silvestres que habitan en sus proximidades.
• Evaluar la diversidad de bacterias en muestras de agua de la laguna Yarinacocha mediante análisis metabarcoding del gen 16S rRNA.

### Muestras
Se tomarán muestras de agua en seis puntos diferentes de la laguna Yarinacocha, tres puntos en la zona periférica del agua de la laguna, separadas por 50 m cada una, tres puntos en el centro de la laguna separadas también por 50 m cada una, y la distancia entre el punto de la orilla y el centro será de 150 metros; se tomará 1 litro de agua por punto. Se tomarán también muestras de heces frescas de mamíferos de la fauna local y aves silvestres, así mismo se tomarán muestras de la superficie de peces comercializados ubicados en el distrito de Yarinacocha, para determinar la presencia de bacterias con genes de resistencia.

### Método
Se utilizarán scripts en Bash en un entorno Linux/Ubunto para procesar y analizar las secuencias de Nanopore. Primero se inspeccionará la longitud de los reads con el programa Zcat, para evaluar si las lecturas son lo suficientemente largas, luego se verá calidad de las bases con el software Nanoplot (para evaluar si las lecturas son confiables), después se seleccionarán los reads que se conservarán, luego se filtrarán las lecturas con el programa Nanofilt, para reducir errores y aumentar la calidad del ensamblado, posteriormente se ensamblaran las lecturas con el programa Flye (ensamblado preliminar), después se se pulirán los ensamblados (Polishing), utilizando los programas Minimap2 y Racon, para corregir errores como inserciones, deleciones, sustituciones, y mejorar la calidad de la secuencia, Minimap2 mapea las lecturas originales (crudas) contra el ensamblado preliminar, y Racon usa esas alineaciones para corregir errores en el ensamblado final (secuencia final) para mejorar la presición, y posteriormente se generarán las secuencias consenso corregidas usando Medaka, luego se evaluará la calidad del ensamblado genómico final con el programa QUAST, y por último se anotará la secuencia final con el programa Prokka. Luego de este flujo de trabajo, se utilizará el programa BLAST, para confirmar y validar la identidad de los genes que se detectaron. 
Todos los genomas ensamblados serán sometidos a software bioinformáticos con el fin de obtener más información. Se listan los programas a usar para cada fin: 
-	Filogrupos: EzClermont 
-	Genes de resistencia a antibióticos: ABRicate, ResFinder Tool 4.0 y AMRFinderPlus. 
-	Plásmidos: PlasmidFinder 2.1 
-	Genes de Virulencia: VirulenceFinder 2.0 y VirulenceFactorDataBase (VFDB) 



