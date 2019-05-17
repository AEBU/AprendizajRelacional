# Aprendizaje Automático Relacional
Se presenta dos enfoques que pueden ayudar a obtener propiedades relacionales de un problema en general.

**1er Enfoque**: Ayudándonos de la teoría de grafos se prevee obtener propiedades relacionales a partir de medidas de centralidad de un grafo(Betweness, Closeness, Degree, PageRank). De tal manera que se pueda entrenar un algoritmo determinado bajo estas propiedades, para una predicción determinada.

**2do Enfoque**: Se utiliza técnicas de DeepLearning como la arquitectura de red neuronal [NegativeSampling], con el objetivo de entrenarla con pares de nodos tanto conectados como no conectados. Para luego obtener los pesos de la capa de incrustación. De tal forma que se obtiene propiedades de relaciones de contexto de cada nodo. Por consiguiente entrenar un modelo de aprendizaje automático para predecir el problema a resolver.


A continuación se presentan dos problemas a resolver en una base de datos de corredores recreativos en el que se trata de predecir el género de un corredor (problema de clasificación) y el tiempo de carrera en una distancia determinada (problema de regresión). Además para el segundo enfoque se cuenta con una base de terroristas, en la cual se predice el tipo de actor (Individual o Grupal) como un problema de clasificación.

Para resolver esta tarea se realiza una transición tomando al problema con Aprendizaje Automático normal, y luego aplicar los dos enfoques antes expuestos.



| Problema  | Descripción  | URL del Código en Colab   |
|:-:|:-:|:-:|
|Aprendizaje Automático Normal | Se predice a través de propiedades inherentes del objeto de estudio, los tiempos de carrear y el género del individuo.  | [CorredoresRecreativos]  |   
|Aprendizaje Automático Relacional **1er Enfoque**  | Se pasa a una base de datos en Neo4j donde se obtiene las métricas de centralidad de cada Corredor  |  [CorredoresRecreativosRelacional] |   
| Aprendizaje Automático Relacional **2do Enfoque**   | De la base de datos pasada a Neo4j se obtiene pares de nodos conectados y pares de nodos desconectados para entrenar la red neuronal con arquitectura NegativeSampling y predecir el género del corredor  | [CorredoresRecreativosRelacional_NegativeSampling]  |   
|Aprendizaje Automático Relacional **2do Enfoque**| Se hace uso de una base de datos de terroristas donde se cuenta con los actores el país al que pertenece y a la organización a la que esta afiliado. Con esto se trata de predecir el tipo de Actor (Individual o Grupal), bajo el segundo enfoque.|  [Actores_NegativeSampling].


[Actores_NegativeSampling]:https://colab.research.google.com/drive/1pchfmvGMclxQ1m-Kg7GovQm46NsM_J-O
[CorredoresRecreativosRelacional_NegativeSampling]:https://colab.research.google.com/drive/16xZo6OYw9G_gktrpMQVpD8EaA5axX7wO
[CorredoresRecreativosRelacional]: https://colab.research.google.com/drive/1oPGXpu7oK2qi2L-gl058STdrWEITVhGI
[CorredoresRecreativos]:https://colab.research.google.com/drive/12UY9IFuROzRnCIxJzkSA9dNATjKYgKbZ
[NegativeSampling]:http://mccormickml.com/2017/01/11/word2vec-tutorial-part-2-negative-sampling/



En los archivos presentados se da un enfoque de resultados. Sin embargo en los próximos días se explicará detalladamente cómo se entrenó y cuales fueron su objetivo.
