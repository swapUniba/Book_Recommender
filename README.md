# Installazione

Per poter utilizzare il sistema è necessario andare ad installare le seguenti librerie:

- Gensim
- Flask
- SciPy
- Flask
- Numpy


# Contenuto del repository

- Main.py: interfaccia del web service. Gli endpoint definiti sono
    - /SelectModel/id: gli id disponibili sono 1-7 per la selezione dei modelli
    - /getSuggestions: prende in input l'oggetto JSON con i seguenti campi :
    
       ```JSON
        {
            movies
            entities
            movietoIgnore
            negativeEntity
            prefAspects
            negAspects
            recListSize
        }
        ```

- RSCCore.py: contiene le funzioni dei file che accedono alla Knowledge Base ed effettua i calcoli di similarità legati alle proprietà

- Dataset: è presente il file books_info.csv dove sono presenti tutti i libri con annesse caratteristiche (trama, scrittore, subject, genere)

- Model:ogni file identificato da nome_modello.py e seguono la stessa struttura. Inoltre, in ogni cartella devono essere presenti i file dei modelli già addestrati. Qualora non fossero presenti, i modelli saranno riaddestrati alla prima esecuzione del programma oppure sono scaricabili da https://drive.google.com/file/d/1gbbMt6ZeOd8yK5PFrR_9iAtWFfaVzHHS/view?usp=sharing
