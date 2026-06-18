# Actividad 04 — Clustering comparativo: Iris, Moons y Circles

Comparacion de tres algoritmos de clustering no supervisado (K-means, DBSCAN, SpectralClustering) sobre tres datasets con geometrias distintas.

## Datasets utilizados
-	Iris: 150 muestras reales, 4 features, 3 clases (setosa, versicolor, virginica).
-	Moons: 2000 muestras sinteticas, forma de media luna, 2 clases.
-	Circles: 2000 muestras sinteticas, circulos concentricos, 2 clases.

## Algoritmos y configuracion
-	K-means: k=3 (Iris), k=2 (Moons/Circles). Metodo del Codo para seleccion de k.
-	DBSCAN: eps=0.5, min_samples=5 (Iris) / eps=0.15, min_samples=15 (Moons) / eps=0.15, min_samples=5 (Circles).
-	SpectralClustering: affinity='rbf' (Iris/Moons) / affinity='nearest_neighbors' (Circles).

## Metricas utilizadas
-	Externas: Adjusted Rand Index (ARI), V-measure.
-	Internas: Silhouette Score, Davies-Bouldin Index, Inercia (Elbow Method).

## Resultado principal
SpectralClustering es el algoritmo mas robusto: obtiene el mejor ARI en los tres datasets (0.645 / 0.937 / 1.000). K-means falla en datos con geometria no convexa. DBSCAN detecta ruido automaticamente pero es sensible a sus hiperparametros.

## Como ejecutar
pip install numpy matplotlib scikit-learn
Abrir cada notebook en Jupyter y ejecutar todas las celdas 
