# Información original

[Will AI take my job?](https://amoyag.github.io/GNN/Will_AI_take_my_job)

[Graph Neural Networks: Understanding Network Data with Deep Learning](https://amoyag.github.io/GNN/gnn)

[Graph Neural Networks: Understanding Network Data with Deep Learning (audio overview)](https://amoyag.github.io/GNN/Graph_Neural_Networks_SystemsBiology.mp3?raw=true)

[GNN code](https://github.com/amoyag/GNN/blob/main/GNN_BS.ipynb)


## Documentos del Repositorio

### 0. **`GNN_tnbc_genes.ipynb`** 
Este notebook es la razón del análisis en este repositorio. Contiene un flujo de trabajo completo que toma los 20 genes de interés relacionados con el TNBC y los expande a través de proteínas mediante el algoritmo de Kneiborgh utilizando la base de datos STRING. Esta expansión incluye las relaciones proteicas basadas en la expresión genética.

Una vez obtenida esta red ampliada, se aplica una red neuronal gráfica (GNN) para predecir genes relacionados con el cáncer. Este análisis es clave para identificar nuevos posibles genes involucrados en el TNBC, proporcionando así una herramienta poderosa para el descubrimiento de biomarcadores.

### 1. `top_tnbc-genes.txt`
Este archivo contiene un listado de 20 genes altamente relacionados con el cáncer de mama triple negativo (TNBC). Estos genes han sido seleccionados por su relevancia en estudios previos y se utilizarán como punto de partida para el análisis con redes neuronales gráficas (GNN).

### 2. `GNN_BS.ipynb`
Este notebook de Jupyter incluye código de referencia y ejemplos sobre la creación y entrenamiento de una red neuronal gráfica (GNN). Es un recurso útil para comprender los fundamentos de cómo las GNN pueden ser aplicadas a datos biológicos, como redes de interacción proteica o redes de regulación génica.

### 3. Artículos Científicos de Referencia
- **Greener_2022_Nature Reviews Molecular Cell Biology_A guide to machine learning for biologists.pdf**  
  Un artículo de revisión que ofrece una guía clara para biólogos sobre cómo aplicar técnicas de machine learning en estudios biológicos. Es un excelente recurso para quienes están empezando en el campo.
  
- **LeCun_2015_Nature_Deep learning.pdf**  
  Este artículo presenta los fundamentos del deep learning, escrito por pioneros del campo como Yann LeCun, y es esencial para comprender las bases de las redes neuronales profundas, incluyendo las GNNs.
  
- **Muzio_2020_Briefings in Bioinformatics_Biological network analysis with deep learning.pdf**  
  Este artículo revisa cómo las redes biológicas pueden ser analizadas usando deep learning, específicamente aplicando GNNs a problemas biológicos complejos, como la predicción de interacciones proteicas y la identificación de genes relacionados con enfermedades.

# Teoría sobre Redes Neuronales de Grafos (GNN):

## De Aprendizaje Profundo a Redes Neuronales de Grafos
El aprendizaje profundo ha revolucionado el análisis de datos complejos mediante redes neuronales artificiales con múltiples capas. Aunque arquitecturas como las Redes Neuronales Convolucionales (CNNs) son excelentes para datos estructurados (como imágenes), muchos sistemas del mundo real, especialmente en biología, se representan mejor como redes o grafos. 

Por ejemplo, las redes de interacción de proteínas o las redes metabólicas no siguen patrones regulares como las imágenes, lo que ha llevado al desarrollo de las GNN, modelos diseñados específicamente para trabajar con datos estructurados en forma de redes.

## Importancia de las Redes en Biología
Los sistemas biológicos están interconectados por naturaleza, desde interacciones moleculares hasta vías celulares. Estas redes biológicas incluyen:

- Redes de Interacción Proteína-Proteína (PPI)
- Redes Metabólicas
- Redes Reguladoras de Genes
- Redes de Interacción Fármaco-Fármaco

La estructura de estas redes contiene información valiosa: proteínas que interactúan suelen tener funciones relacionadas, genes cercanos en redes reguladoras tienden a participar en procesos biológicos similares. Por ello, las redes no solo son visualizaciones, sino también fuentes de conocimientos biológicos importantes.

## Redes Neuronales de Grafos: Aprendizaje Basado en Estructuras de Redes
Las GNN adaptan los principios del aprendizaje profundo para trabajar con datos en forma de redes. A diferencia de las redes neuronales tradicionales, las GNN pueden aprender tanto de las características de los nodos individuales (como las propiedades de una proteína) como de las relaciones entre ellos (como las interacciones proteicas).

Una de las innovaciones clave de las GNN es la capacidad de generar *embeddings*, que son representaciones aprendidas de los nodos que capturan tanto sus características individuales como su contexto en la red. Esto es crucial para tareas como la predicción de funciones de proteínas.

## El Proceso de Aprendizaje en las GNNs
En las GNNs, el aprendizaje se basa en la "propagación de mensajes", donde los nodos intercambian información con sus vecinos a través de las conexiones de la red. Este proceso iterativo permite a cada nodo aprender de su entorno local y global, logrando representaciones ricas que capturan tanto las características del nodo como la estructura de la red.

## Aplicaciones de las GNN en Biología de Sistemas
Las GNNs han demostrado ser eficaces en varias aplicaciones biológicas, como:

- Predicción de funciones de proteínas en redes PPI
- Descubrimiento de fármacos, como la predicción de interacciones fármaco-objetivo
- Análisis de enfermedades, incluyendo clasificación de subtipos de cáncer y predicción de asociaciones gen-enfermedad

El éxito de las GNN en estos campos resalta el poder de aprovechar la estructura de red para obtener información biológica significativa.

## Consideraciones Técnicas
Al aplicar GNNs a problemas biológicos, es importante tener en cuenta la selección de características, la construcción de redes de calidad, y la arquitectura del modelo, que puede variar según las necesidades específicas del problema.

## Direcciones Futuras
El campo de las GNNs sigue avanzando rápidamente, con enfoques emergentes que integran múltiples tipos de datos y redes, desarrollan modelos más interpretables, y manejan datos de redes dinámicas.
