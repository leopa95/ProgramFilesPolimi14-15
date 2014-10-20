    def latomattonelle(b,h,i):
        if b==h:
            return b,i+1
        if b>h:
            return latomattonelle(b-h,h,i+1)
        else:
            return latomattonelle(b,h-b,i+1)
    def piastrellamento(b,h):
        return latomattonelle(b,h,0)
    
    
Il piastrellamento può essere fatto solo con piastrelle quadrate e ho notato che sottraendo il numero che era minore (ricorsivamente) all'altro maggiore alla fine veniva il massimo comun divisore e l'ho implementato in queste righe di codice. 

Cercherò quindi di piastrellarlo con piastrelle più grandi possibili (ovviamente quadrate).

La funzione latomattonelle(..) serve appunto per prendere l'altezza e la base e fare le piastrelle il più grande possibile.

Es: se hai un pavimento (muro) di h=8 e b=5 latomattonelle(b,h,0) (lo zero é un contatore che si va sommando ad 1 (numero passaggi) quindi devono iniziare da 0) creerà arriverà alla soluzione che il massimo comun divisore tra 8 e 5 è 1 e ci dirà inoltre quante volte è passato dentro la funzione latomattonelle(che appunto ci indica la grandezza delle mattonelle).

La funzione piastrequadrate inoltre ha un contatore "i" che conta le volte che il programma richiama latomattonelle(..).

L'output del programma indicherà ( massimo comun divisore/ lato delle mattonelle ,numero di passi fatti ricorsivamente nella funzione) la virgola sul return della terza riga tra "b" e "i+1" serve per fare stampare i due valori nello stesso return.

Spero di esservi stato utile!
