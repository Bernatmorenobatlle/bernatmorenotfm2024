# DESIGN AND IMPLEMENTATION OF A BIOINFORMATICS PIPELINE FOR GENOMIC ANALYSIS AT THE VACTERL ASSOCIATION

## Creación de Tablas Interactivas

En este proyecto, hemos implementado la capacidad de generar dos tablas interactivas que contienen información esencial sobre las variantes. 

### Primera Tabla: Impacto Funcional de las Variantes

La primera tabla está compuesta por datos relacionados con el impacto funcional de las variantes en comparación con el gen original y la región específica afectada. Las columnas de esta tabla incluyen:

- **GeneName:** Nombre del gen.
- **GeneId:** Identificador único del gen.
- **TranscriptId:** Identificador único del transcrito asociado al gen.
- **BioType:** Tipo biológico o funcional del transcrito (por ejemplo, "rRNA" para ácido ribonucleico ribosomal o "protein_coding" para genes que codifican proteínas).
- **HIGH, LOW, MODERATE, MODIFIER:** Categorías que indican el impacto o gravedad de las variantes, clasificadas desde "HIGH" (alto) hasta "MODIFIER" (modificador).
- **EXON, INTRON, UPSTREAM, DOWNSTREAM, UTR_3_PRIME, UTR_5_PRIME:** Columnas que representan diferentes regiones del genoma donde se han identificado o anotado las variantes. Cada número en estas columnas indica la cantidad de variantes encontradas en una región específica del gen o transcrito, como exones, intrones, regiones aguas arriba (UPSTREAM) o aguas abajo (DOWNSTREAM) del gen, y regiones no traducidas en el ARN mensajero (UTR_3_PRIME y UTR_5_PRIME).

### Filtros Interactivos

Esta tabla está diseñada con filtros que permiten acotar la búsqueda a los genes de interés:

- **Buscador:** Permite seleccionar por el nombre del gen, la información asociada y todas sus variantes.
- **Tipo Biológico o Funcional:** Posibilidad de filtrar por el tipo biológico o funcional del transcrito, como "protein_coding".
- **Grado de Impacto:** Filtrado por el grado de impacto o gravedad de las variantes (HIGH, LOW, MODERATE o MODIFIER), mostrando solo las variantes que coincidan con el grado seleccionado.


![image](https://github.com/polmoreno/test-streamlit-b/assets/62899431/6721f35e-ae8d-4eac-bd88-d35f9fce42aa)

### Segunda Tabla: Métricas del Archivo VCF

En la segunda tabla, presentamos información esencial del archivo VCF, que contiene diversas métricas para cada variante. Las columnas de esta tabla incluyen:

- **#CHROM:** Nombre del cromosoma (1 al 22 para autosomas, 'X' e 'Y' para cromosomas sexuales).
- **POS:** Posición exacta de la variante en el cromosoma.
- **REF:** Secuencia de referencia en esa posición.
- **ALT:** Secuencia alternativa encontrada en esa posición.
- **QUAL:** Calidad de la llamada de variante, indicando su confiabilidad.
- **DP:** Profundidad de cobertura, muestra cuántas veces se leyó esa posición.
- **AC:** Número de copias del alelo alternativo observado.
- **AF:** Frecuencia del alelo alternativo en relación con el total de copias de alelos observados.
- **AO:** Número de observaciones que contienen alelos alternativos.
- **MQM:** Calidad promedio de las bases que mapean en esa posición.
- **TYPE:** Tipo de variante, como deleción ("del") o polimorfismo de nucleótido único ("snp").
- **ANN:** Información detallada sobre la anotación de la variante, incluyendo el gen afectado, tipo de transcrito, impacto de la variante (MODIFIER, LOW, etc.), posición específica en el transcrito y naturaleza de la variante.

En esta tabla, la información detallada proporciona una visión completa de las variantes, desde su ubicación en el cromosoma hasta la calidad de la llamada de la variante y su impacto potencial en los genes asociados. La incorporación de enlaces, en las dos tablas, a la base de datos ENSEMBL permite una exploración más profunda del gen y de la región, enriqueciendo así la comprensión de las variantes y su contexto genómico.

![image](https://github.com/polmoreno/test-streamlit-b/assets/62899431/e970a3a6-7ffa-49e1-852a-2bf63cddbbbc)

