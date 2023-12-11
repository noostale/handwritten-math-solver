# Riconoscitore e risolutore di espressioni matematiche scritte a mano
Lo scopo del progetto qui descritto è quello di determinare, a partire da un'immagine che contiene un'espressione matematica scritta a mano, l'equivalente espressione scritta in ASCII utilizzando una rete neurale convoluzionale.

# Librerie utilizzate
Per il progetto sono state utilizzate le librerie:

- Numpy
- Pandas
- Matplotlib 
- Sympy
- Cv2
- PIL
- TensorFlow

Il progetto è visionabile sottoforma di 3 Jupiter Notebook. Nei paragrafi successivi si delineano le fondamenta del progetto.

# Funzione di caricamento del dataset
Si definisce una funzione che presa in input una directory che contiene immagini, ne restituisce l'array normalizzato in base alle caratteristiche del modello che si andrà a definire in seguito.

# Caricamento e pre-elaborazione del dataset
Si costruiscono e popolano gli array che contengono il test ed il train set, aggiungendo come ultimo elemento della singola immagine nella matrice la label corrispondente ed estraendolo successivamente.

# Definizione e training del modello
Si definisce un modello sequenziale basato su una rete convoluzionale, che viene successivamente addestrato sul train set. Vengono inoltre date delle informazioni utili alla comprensione della performance del modello tra cui la loss e l'accuracy.

# Riconoscimento e stampa dell'espressione
Si effettua dunque il riconoscimento delle espressioni contenute nella cartella "espressioni", si carica di volta in volta un'espressione, viene effettuata una sua interpretazione per suddividerla negli elementi che la compongono e successivamente viene effettuata una predizione su ogni singolo elemento stampando in output l'espressione completa in formato ASCII.

# Parsing e calcolo del risultato
Se l'espressione è valida si effettua un parsing e si calcola il risultato, altrimenti si stampa un messaggio di errore.