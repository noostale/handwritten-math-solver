# Riconoscitore e risolutore di espressioni matematiche scritte a mano
Lo scopo del progetto è quello di utilizzare modelli di machine learning assieme ad elementi di computer vision per poter determinare, a partire da un'immagine che contiene un'espressione matematica scritta a mano, l'equivalente espressione scritta in ASCII.

# Librerie utilizzate
Per il progetto sono state utilizzate le librerie:

- Numpy
- Pandas
- Matplotlib 
- Sympy
- Cv2
- PIL
- TensorFlow

Il progetto è presentato come un Jupiter Notebook, nelle righe successive andrò a delineare i vari paragrafi in cui esso è suddiviso.

# Definizione della funzione per il caricamento del dataset
Inizialmente nel notebook andiamo a definire una funzione la quale, presa in input una directory che contiene immagini, restituisce una lista di immagini normalizzate in base alle impostazioni del modello che andremo a creare ed allenare.



# Creazione array di training e di test
In questi due paragrafi andiamo a creare gli array che conterrano tutte le immagini con cui vorremo trainare e testare il nostro modello, aggiungendo come ultimo elemento della singola immagine nella matrice la label corrispondente. 



# Creazione set di training e di test
In questi paragrafi prendiamo la nostra matrice di test e traning e ne andiamo a cacciare quelle che sono le label di ogni immagine ed andiamo a categorizzare le label.



# Definizione e training del modello
In questo paragrafo definiamo un modello sequenziale che andremo a trainare utilizzando i dati estratti ed elaborati in precenza.

Terminato il training andiamo a delineare un grafico che ci aiuta a rappresentare la correttezza del nostro modello andiando a valutare in particolare loss, accuracy, val_loss e val_accuracy.



# Riconoscimento
In questo paragrafo andiamo a valutare le prestazioni del nostro modello con delle espressioni scritte a mano prese dalla cartella "espressioni".

Inizialmente carichiamo un'immagine e successivamente andiamo ad effettuare un riconoscimento dei singoli elementi che compongono l'espressione per mezzo di OpenCV.

In seguito effettuiamo delle predizioni sui singoli elementi che OpenCV ha estrapolato dall'imagine di partenza, andando così a creare un'unica espressione finale.


# Parsing e calcolo
Come ultima cosa, se l'espressione è valida ad essa viene effettuato un parsing e viene eguagliata a 0 per essere trasformata in una equazione in cui l'incognita è la variabile y.

# Utilizzo
Per testare il progetto è sufficiente installare le dipendeze, clonare la repository, estrarre il file "dataset.zip" nella cartella contenente il file "Progetto.ipynb" ed avviare il notebook.
