 Esercizio: Modellizzare la struttura di una tabella per memorizzare tutti i dati riguardanti delle auto usate messe in vendita da un concessionario

 Steps: 
 -1Dare un nome alla tabella 
 -2Dare un nome alle colonne 
 -3Capire il tipo di dato 
 -4Attributi da assegnare

1- Nome tabella: Cars/ Auto / Macchine (l'entità è la macchina, quindi lo metterei al plurale )

2- Dare un nome alle colonne 
-id 
-targa 
-marca
-modello
-km_percorsi
-numero_telaio
-anno_immatricolazione
-prezzo_vendita

3- Capire il tipo di dato 
-id: INT || BIGINT
-targa: CHAR(7)( perchè è composta da 7 elementi, 4 numeri e 3 lettere, non è una lunghezza variabile)
-marca VARCHAR(20)
-modello VARCHAR(20)
-km_percorsi INT
-numero_telaio CHAR(17) (composto da 17 caratteri alfanumerici)
-anno_immatricolazione YEAR
-prezzo_vendita DECIMAL(10,2) (non uso varchar perchè altrimenti me lo salva in testo e magari potrei voler fare delle operazioni matematiche sul prezzo, tipo sconti, etc..)

4- Attributi da assegnare
-id PK NOTNULL UNIQUE INDEX
-targa NOTNULL UNIQUE INDEX
-marca NULL 
-modello NULL 
-km_percorsi NULL
-numero_telaio NOTNULL UNIQUE INDEX
-anno_immatricolazione NULL 
-prezzo_vendita NULL 


(Penso ad un operaio che deve inserire le informazioni su delle auto che può mettere in vendita, quindi magari inserisce le informazioni principali di tutte e poi in un secondo momento quelle che io ritengo secondarie tipo marca modello e prezzo)