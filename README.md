# exel-course


<pre>
• EXCEL intermedio/avanzato<br>
• Programma: 
• Funzione logiche 
• Funzioni di data
• Gestione dei file e stampe
• Importazione e esportazione di file in/da altri formati
• Le funzioni di testo (stringa.estrai, sinistra, trova, concatena)
• Le funzioni di ricerca
• Ordinamento semplice e personalizzato
• Inserimento di grafici
• Operazioni con i Nomi di Zona
• Progettazione e costruzione di un database in Excel
• Applicazione dei criteri di convalida
• Funzioni avanzate logiche e di database
• Funzioni avanzate di ricerca informazioni
• Ordinamenti semplici e a chiave multipla
• Selezione mediante i filtri (semplici ed avanzati)
• Uso dei Subtotali
• Analisi dati con le Tabelle Pivot
• Grafici di tabelle Pivot
• Power Pivot: analisi di business intelligence
• Importare dati esterni con Power Query
• Funzionalità Scenari per confrontare ed analizzare i dati
• Strumento Risolutore per risolvere problemi complessi
• Consolidamento dei dati (Consolida)
• Proteggere fogli e cartelle 
• Nascondere le formule
• Registrare macro per automatizzare operazioni ripetitive
• Cenni al linguaggio VBA per modificare una macro registrata in precedenza
</pre>


## Funzione logiche 



Excel offre una varietà di funzioni logiche che puoi utilizzare per eseguire operazioni basate su condizioni logiche. Di seguito sono elencate alcune delle funzioni logiche più comuni in Excel:
Puoi combinare queste funzioni e utilizzarle insieme per creare formule complesse basate su condizioni logiche.


### 1. **IF (SE)**
La funzione IF (SE) è una delle funzioni logiche più utilizzate in Excel. Si usa per eseguire un'operazione se una condizione è vera e un'altra operazione se la condizione è falsa.

Esempio:
```excel
=IF(A1>10, "Maggiore di 10", "Minore o uguale a 10")
```

### 2. **AND (E)**
La funzione AND (E) restituisce TRUE se tutte le condizioni specificate sono vere e FALSE se anche una sola condizione è falsa.

Esempio:
```excel
=AND(A1>10, B1<20)
```

### 3. **OR (O)**
La funzione OR (O) restituisce TRUE se almeno una delle condizioni specificate è vera e FALSE se tutte le condizioni sono false.

Esempio:
```excel
=OR(A1>10, B1>10)
```

### 4. **NOT (NON)**
La funzione NOT (NON) restituisce TRUE se la condizione specificata è falsa e FALSE se la condizione è vera.

Esempio:
```excel
=NOT(A1>10)
```

### 5. **IFERROR (SEERRORE)**
La funzione IFERROR (SEERRORE) restituisce un valore specificato se la formula contiene un errore e il risultato della formula se non c'è alcun errore.

Esempio:
```excel
=IFERROR(A1/B1, "Errore: divisione per zero")
```

### 6. **XOR (XOR)**
La funzione XOR (XOR) restituisce TRUE se un numero dispari di condizioni specificate è vera e FALSE se un numero pari di condizioni è vera.

Esempio:
```excel
=XOR(A1>10, B1<20, C1=0)
```
__________________________________________________________


## ESERCIZI CON IF 



### Esercizio 1:
Supponiamo di avere un foglio di calcolo con i voti degli studenti nella colonna A. Se un voto è maggiore o uguale a 60, vuoi assegnare "Pass" nella colonna B, altrimenti "Non passato".

**Formula:**
```excel
=IF(A1>=60, "Pass", "Non passato")
```

### Esercizio 2:
Hai un elenco di temperature nella colonna A. Vuoi classificare le temperature come "Caldo" se sono superiori a 30 gradi Celsius e come "Freddo" altrimenti.

**Formula:**
```excel
=IF(A1>30, "Caldo", "Freddo")
```

### Esercizio 3:
Hai un elenco di numeri nella colonna A. Vuoi determinare se ciascun numero è positivo, negativo o zero.

**Formula:**
```excel
=IF(A1>0, "Positivo", IF(A1<0, "Negativo", "Zero"))
```

### Esercizio 4:
Supponiamo che tu stia calcolando lo sconto per un elenco di prodotti nella colonna A. Se il prezzo del prodotto è superiore a 100, vuoi applicare uno sconto del 10%, altrimenti uno sconto del 5%.

**Formula:**
```excel
=IF(A1>100, A1*0.9, A1*0.95)
```

### Esercizio 5:
Hai un elenco di età nella colonna A. Vuoi determinare se ciascuna persona è un bambino (età inferiore a 18 anni) o un adulto (età uguale o superiore a 18 anni).

**Formula:**
```excel
=IF(A1<18, "Bambino", "Adulto")
```




### Esercizio 6:
Hai un elenco di punteggi degli studenti nella colonna A. Se il punteggio è maggiore o uguale a 90, assegna "Eccellente", se è tra 70 e 89 assegna "Buono", altrimenti assegna "Da migliorare".

**Formula:**
```excel
=IF(A1>=90, "Eccellente", IF(A1>=70, "Buono", "Da migliorare"))
```

### Esercizio 7:
Hai un elenco di numeri nella colonna A. Se il numero è pari, restituisci "Pari", altrimenti restituisci "Dispari".

**Formula:**
```excel
=IF(MOD(A1,2)=0, "Pari", "Dispari")
```

### Esercizio 8:
Supponiamo che tu abbia un elenco di prodotti nella colonna A e un elenco di quantità nella colonna B. Vuoi calcolare l'importo totale. Se la quantità è superiore a 10, applica uno sconto del 10%, altrimenti non applicare alcuno sconto.

**Formula:**
```excel
=IF(B1>10, A1*B1*0.9, A1*B1)
```

### Esercizio 9:
Hai un elenco di età nella colonna A. Vuoi determinare se ciascuna persona è un bambino (età inferiore a 13 anni), un adolescente (età tra 13 e 19 anni) o un adulto (età uguale o superiore a 20 anni).

**Formula:**
```excel
=IF(A1<13, "Bambino", IF(A1<20, "Adolescente", "Adulto"))
```

### Esercizio 10:
Supponiamo che tu abbia un elenco di voti negli esami di matematica e scienze nella colonna A e B rispettivamente. Vuoi assegnare "Promosso" solo se ha superato entrambi gli esami, altrimenti "Non promosso".

**Formula:**
```excel
=IF(AND(A1>=50, B1>=50), "Promosso", "Non promosso")
```




______________________________________________________________________________________


### esercizi con and


### Esercizio 1:
Hai un elenco di voti degli studenti nella colonna A e i loro punteggi di partecipazione nella colonna B. Vuoi assegnare "Promosso" solo se il voto è maggiore o uguale a 60 e il punteggio di partecipazione è maggiore di 80.

**Formula:**
```excel
=IF(AND(A1>=60, B1>80), "Promosso", "Non promosso")
```

### Esercizio 2:
Hai un elenco di età degli studenti nella colonna A e vuoi determinare se ciascuno di essi è un adolescente (età tra 13 e 19 anni) e se frequenta una scuola media.

**Formula:**
```excel
=IF(AND(A1>=13, A1<=19, B1="Scuola Media"), "Adolescente in Scuola Media", "Altro")
```

### Esercizio 3:
Hai un elenco di temperature nella colonna A e vuoi verificare se ciascuna temperatura è superiore a 0 gradi Celsius e inferiore a 100 gradi Celsius.

**Formula:**
```excel
=IF(AND(A1>0, A1<100), "Valida", "Non valida")
```

### Esercizio 4:
Hai un elenco di orari nella colonna A e vuoi determinare se ciascun orario è tra le 9 del mattino e le 5 del pomeriggio.

**Formula:**
```excel
=IF(AND(A1>=9:00, A1<=17:00), "Orario lavorativo", "Fuori orario")
```

### Esercizio 5:
Hai un elenco di numeri nella colonna A, B e C. Vuoi assegnare "Tutti positivi" solo se tutti e tre i numeri sono positivi.

**Formula:**
```excel
=IF(AND(A1>0, B1>0, C1>0), "Tutti positivi", "Non tutti positivi")
```

### Esercizio 6:
Hai un elenco di valori nella colonna A. Vuoi verificare se ciascun valore è una stringa di testo e contiene la parola "Excel".

**Formula:**
```excel
=IF(AND(ISTEXT(A1), FIND("Excel", A1) > 0), "Contiene Excel", "Non contiene Excel")
```

### Esercizio 7:
Hai un elenco di dati nella colonna A e vuoi verificare se ciascun dato è un numero intero positivo.

**Formula:**
```excel
=IF(AND(ISNUMBER(A1), A1=INT(A1), A1>0), "Numero intero positivo", "Non è un numero intero positivo")
```

### Esercizio 8:
Hai un elenco di orari nella colonna A. Vuoi verificare se ciascun orario è uguale o successivo a un'ora specifica, ad esempio le 14:30.

**Formula:**
```excel
=IF(AND(A1>=14:30), "Uguale o successivo a 14:30", "Antecedente a 14:30")
```

### Esercizio 9:
Hai un elenco di temperature nella colonna A e vuoi verificare se ciascuna temperatura è superiore a una soglia specifica, ad esempio 25 gradi Celsius.

**Formula:**
```excel
=IF(AND(A1>25), "Superiore a 25 gradi", "Non superiore a 25 gradi")
```

### Esercizio 10:
Hai un elenco di numeri nella colonna A, B e C. Vuoi assegnare "Tutti pari" solo se tutti e tre i numeri sono pari.

**Formula:**
```excel
=IF(AND(MOD(A1,2)=0, MOD(B1,2)=0, MOD(C1,2)=0), "Tutti pari", "Non tutti pari")
```

Puoi utilizzare queste formule nelle tue celle Excel per eseguire le verifiche logiche descritte negli esercizi. Assicurati di adattare le formule in base alla disposizione specifica dei dati nel tuo foglio di calcolo.


_____________________________________________________________________



## Esercizi con OR EXEL 


### Esercizio 1:
Hai un elenco di voti nella colonna A. Vuoi assegnare "Approvato" se il voto è maggiore o uguale a 50 o se il punteggio di partecipazione nella colonna B è maggiore di 80.

**Formula:**
```excel
=IF(OR(A1>=50, B1>80), "Approvato", "Non approvato")
```

### Esercizio 2:
Hai un elenco di numeri nella colonna A. Vuoi determinare se ciascun numero è multiplo di 3 o di 5.

**Formula:**
```excel
=IF(OR(MOD(A1,3)=0, MOD(A1,5)=0), "Multiplo di 3 o 5", "Non multiplo di 3 o 5")
```

### Esercizio 3:
Hai un elenco di nomi nella colonna A. Vuoi verificare se ciascun nome è "Alice" o "Bob".

**Formula:**
```excel
=IF(OR(A1="Alice", A1="Bob"), "Nome valido", "Nome non valido")
```

### Esercizio 4:
Hai un elenco di età nella colonna A. Vuoi determinare se ciascuna persona è un bambino (età inferiore a 13 anni) o un anziano (età uguale o superiore a 65 anni).

**Formula:**
```excel
=IF(OR(A1<13, A1>=65), "Bambino o Anziano", "Non Bambino o Anziano")
```

### Esercizio 5:
Hai un elenco di colori nella colonna A. Vuoi verificare se ciascun colore è rosso, verde o blu.

**Formula:**
```excel
=IF(OR(A1="Rosso", A1="Verde", A1="Blu"), "Colore valido", "Colore non valido")
```

### Esercizio 6:
Hai un elenco di temperature nella colonna A. Vuoi determinare se ciascuna temperatura è inferiore a 0 gradi Celsius o superiore a 30 gradi Celsius.

**Formula:**
```excel
=IF(OR(A1<0, A1>30), "Estremo", "Nella norma")
```

### Esercizio 7:
Hai un elenco di numeri nella colonna A. Vuoi verificare se ciascun numero è negativo o superiore a 100.

**Formula:**
```excel
=IF(OR(A1<0, A1>100), "Negativo o Maggiore di 100", "Positivo e Minore o Uguale a 100")
```

### Esercizio 8:
Hai un elenco di date nella colonna A. Vuoi determinare se ciascuna data è di un giorno festivo (ad esempio, Natale o Capodanno).

**Formula:**
```excel
=IF(OR(MONTH(A1)=12, DAY(A1)=1, MONTH(A1)=1, DAY(A1)=1), "Giorno festivo", "Non giorno festivo")
```

### Esercizio 9:
Hai un elenco di numeri nella colonna A. Vuoi verificare se ciascun numero è un quadrato perfetto o un cubo perfetto.

**Formula:**
```excel
=IF(OR(SQRT(A1)=INT(SQRT(A1)), A1^(1/3)=INT(A1^(1/3))), "Quadrato o Cubo perfetto", "Non Quadrato o Cubo perfetto")
```

### Esercizio 10:
Hai un elenco di temperature nella colonna A. Vuoi determinare se ciascuna temperatura è inferiore a 0 gradi Celsius o superiore a 25 gradi Celsius.

**Formula:**
```excel
=IF(OR(A1<0, A1>25), "Estremo", "Nella norma")
```

Questi esercizi ti permetteranno di praticare l'utilizzo della funzione OR in diverse situazioni. Puoi adattare le formule in base alle tue esigenze specifiche e sperimentare con altre condizioni logiche per ampliare le tue competenze in Excel.

_____________________________________________________________


## FUNZIONE NOT IN EXEL  ESERCITAZIONE 


### Esercizio 1:
Hai un elenco di voti nella colonna A. Vuoi assegnare "Promosso" se il voto è superiore a 50, altrimenti "Non promosso".

**Formula:**
```excel
=IF(NOT(A1>50), "Non promosso", "Promosso")
```

### Esercizio 2:
Hai un elenco di età nella colonna A. Vuoi determinare se ciascuna persona non è un bambino (età maggiore o uguale a 13 anni).

**Formula:**
```excel
=IF(NOT(A1<13), "Non bambino", "Bambino")
```

### Esercizio 3:
Hai un elenco di valori nella colonna A. Vuoi verificare se ciascun valore è diverso da zero.

**Formula:**
```excel
=IF(NOT(A1=0), "Diverso da zero", "Zero")
```

### Esercizio 4:
Hai un elenco di stringhe di testo nella colonna A. Vuoi verificare se ciascuna stringa non è vuota.

**Formula:**
```excel
=IF(NOT(A1=""), "Non vuota", "Vuota")
```

### Esercizio 5:
Hai un elenco di numeri nella colonna A. Vuoi verificare se ciascun numero è negativo.

**Formula:**
```excel
=IF(NOT(A1<0), "Non negativo", "Negativo")
```

### Esercizio 6:
Hai un elenco di booleani (VERO o FALSO) nella colonna A. Vuoi ottenere il valore opposto (es. da VERO a FALSO e viceversa).

**Formula:**
```excel
=NOT(A1)
```

### Esercizio 7:
Hai un elenco di valori nella colonna A. Vuoi verificare se ciascun valore è un numero intero.

**Formula:**
```excel
=IF(NOT(ISNUMBER(A1)), "Non è un numero", "È un numero")
```

### Esercizio 8:
Hai un elenco di date nella colonna A. Vuoi verificare se ciascuna data è superiore alla data odierna.

**Formula:**
```excel
=IF(NOT(A1>TODAY()), "Data passata", "Data futura o odierna")
```

### Esercizio 9:
Hai un elenco di valori nella colonna A. Vuoi verificare se ciascun valore è un numero intero positivo.

**Formula:**
```excel
=IF(NOT(INT(A1)=A1, A1>0), "Non è un numero intero positivo", "È un numero intero positivo")
```

### Esercizio 10:
Hai un elenco di stringhe di testo nella colonna A. Vuoi verificare se ciascuna stringa contiene la parola "Excel".

**Formula:**
```excel
=IF(NOT(ISNUMBER(FIND("Excel", A1))), "Non contiene Excel", "Contiene Excel")
```


________________________________________________________________________________

## Esercizi funzione IFERROR (SE.ERRORE) in Excel:

### Esercizio 1:
Hai un elenco di calcoli nella colonna A. Vuoi visualizzare "Errore di calcolo" se c'è un errore, altrimenti il risultato del calcolo.

**Formula:**
```excel
=IFERROR(A1, "Errore di calcolo")
```

### Esercizio 2:
Hai un elenco di numeri nella colonna A. Vuoi calcolare il reciproco di ciascun numero e visualizzare "Errore" se il numero è zero.

**Formula:**
```excel
=IFERROR(1/A1, "Errore")
```

### Esercizio 3:
Hai un elenco di valori nella colonna A. Vuoi visualizzare "Maggiore di 10" se il valore è maggiore di 10, altrimenti "Minore o uguale a 10".

**Formula:**
```excel
=IFERROR(IF(A1>10, "Maggiore di 10", "Minore o uguale a 10"), "Errore")
```

### Esercizio 4:
Hai un elenco di prezzi nella colonna A e un elenco di quantità nella colonna B. Vuoi calcolare l'importo totale e visualizzare "Errore" se uno dei valori è errato.

**Formula:**
```excel
=IFERROR(A1*B1, "Errore")
```

### Esercizio 5:
Hai un elenco di date nella colonna A. Vuoi visualizzare "Data valida" se la data è valida, altrimenti "Data non valida".

**Formula:**
```excel
=IFERROR(IF(DATE(YEAR(A1), MONTH(A1), DAY(A1))=A1, "Data valida", "Data non valida"), "Errore")
```

### Esercizio 6:
Hai un elenco di stringhe di testo nella colonna A. Vuoi visualizzare "Lunghezza valida" se la lunghezza della stringa è inferiore a 10 caratteri, altrimenti "Lunghezza non valida".

**Formula:**
```excel
=IFERROR(IF(LEN(A1)<10, "Lunghezza valida", "Lunghezza non valida"), "Errore")
```

### Esercizio 7:
Hai un elenco di numeri nella colonna A. Vuoi visualizzare "Numero positivo" se il numero è positivo, altrimenti "Numero non positivo".

**Formula:**
```excel
=IFERROR(IF(A1>0, "Numero positivo", "Numero non positivo"), "Errore")
```

### Esercizio 8:
Hai un elenco di valori nella colonna A. Vuoi visualizzare "Pari" se il valore è pari, altrimenti "Dispari".

**Formula:**
```excel
=IFERROR(IF(MOD(A1,2)=0, "Pari", "Dispari"), "Errore")
```

### Esercizio 9:
Hai un elenco di percentuali nella colonna A. Vuoi visualizzare "Valido" se la percentuale è compresa tra 0 e 100, altrimenti "Non valido".

**Formula:**
```excel
=IFERROR(IF(AND(A1>=0, A1<=100), "Valido", "Non valido"), "Errore")
```

### Esercizio 10:
Hai un elenco di codici nella colonna A. Vuoi visualizzare "Formato valido" se il codice segue un formato specifico, altrimenti "Formato non valido".

**Formula:**
```excel
=IFERROR(IF(REGEXMATCH(A1, "^[A-Z]{3}-\d{3}$"), "Formato valido", "Formato non valido"), "Errore")
```

Questi esercizi ti consentiranno di praticare l'utilizzo della funzione IFERROR in diverse situazioni. Puoi adattare le formule in base alle tue esigenze specifiche e sperimentare con altre condizioni per ampliare le tue competenze in Excel.


___________________________________________


## Esercizi Misti Exel :



### Esercizio 1:
Hai un elenco di età nella colonna A e un elenco di punteggi nella colonna B. Vuoi assegnare "Ammesso" solo se l'età è maggiore o uguale a 18 e il punteggio è maggiore di 70.

**Formula:**
```excel
=IF(AND(A1>=18, B1>70), "Ammesso", "Non Ammesso")
```

### Esercizio 2:
Hai un elenco di voti nella colonna A. Vuoi calcolare la media dei voti solo se tutti i voti sono superiori a 50.

**Formula:**
```excel
=IF(AND(A1>50, B1>50, C1>50, D1>50, E1>50), (A1+B1+C1+D1+E1)/5, "Almeno un voto inferiore a 50")
```

### Esercizio 3:
Hai un elenco di numeri nella colonna A. Vuoi assegnare "Numero positivo" se il numero è positivo, "Zero" se il numero è zero, e "Numero negativo" se il numero è negativo.

**Formula:**
```excel
=IF(A1>0, "Numero positivo", IF(A1=0, "Zero", "Numero negativo"))
```

### Esercizio 4:
Hai un elenco di temperature nella colonna A. Vuoi assegnare "Caldo" se la temperatura è superiore a 30 gradi Celsius o "Freddo" se è inferiore a 10 gradi Celsius.

**Formula:**
```excel
=IF(OR(A1>30, A1<10), IF(A1>30, "Caldo", "Freddo"), "Temperatura moderata")
```

### Esercizio 5:
Hai un elenco di valori numerici nella colonna A. Vuoi assegnare "Pari" se il numero è pari e "Dispari" se è dispari. Se il valore non è un numero, visualizza "Non è un numero".

**Formula:**
```excel
=IF(ISNUMBER(A1), IF(MOD(A1,2)=0, "Pari", "Dispari"), "Non è un numero")
```

_________________


TIPS :


Per verificare se tutti i dati in una colonna sono pari in Excel, puoi utilizzare la funzione `MOD` insieme alla funzione `SUMPRODUCT`. Ecco come farlo:

Supponiamo che i dati che desideri verificare siano nella colonna A da A1 ad A1000. La formula per verificare se tutti i dati nella colonna A sono pari sarebbe la seguente:

```excel
=IF(SUMPRODUCT(MOD(A1:A1000, 2))=0, "Tutti pari", "Non tutti pari")
```

Questa formula utilizza `MOD(A1:A1000, 2)` per ottenere il resto della divisione di ogni numero nella colonna A per 2. Se tutti i numeri sono pari, la somma di questi resti sarà 0. La funzione `SUMPRODUCT` somma questi resti, e se il risultato è 0, la formula restituirà "Tutti pari", altrimenti "Non tutti pari". Puoi adattare l'intervallo `A1:A1000` nella formula in base alla tua esigenza specifica.


_______________________

 ## RANGE IN EXEL 


In Excel, puoi specificare un intervallo (range) utilizzando la notazione A1:B10, dove A1 rappresenta la cella in alto a sinistra del tuo intervallo e B10 rappresenta la cella in basso a destra. Questo intervallo include tutte le celle dalla A1 alla B10.

Ecco alcuni modi comuni per specificare un intervallo in Excel:

### Intervallo singolo:
- **A1**: Rappresenta una singola cella nella colonna A e nella riga 1.
- **A1:B10**: Rappresenta tutte le celle nel rettangolo dalla A1 alla B10.
- **C**: Rappresenta l'intera colonna C.
- **2**: Rappresenta l'intera riga 2.

### Intervallo combinato:
- **A1, B3, C5**: Rappresenta tre celle separate: A1, B3 e C5.
- **A1:B2, C3:D4**: Rappresenta due intervalli distinti: A1:B2 e C3:D4.

### Intervallo dinamico:
- **A1:A**: Rappresenta l'intera colonna A a partire dalla cella A1.
- **1:1**: Rappresenta l'intera riga 1 a partire dalla colonna A.

### Utilizzo di nomi:
Puoi assegnare un nome a un intervallo per riferirti più facilmente ad esso. Ad esempio, assegnando il nome "MioIntervallo" all'intervallo A1:B10, puoi fare riferimento a questo intervallo utilizzando il nome "MioIntervallo" nelle formule anziché l'indirizzo delle celle.

### Utilizzo di formule e funzioni:
Gli intervalli possono essere specificati anche all'interno di formule e funzioni. Ad esempio, puoi sommare tutti i valori in un intervallo utilizzando la formula `=SUM(A1:B10)`.

Puoi inserire un intervallo direttamente nelle caselle di input delle formule o nelle finestre di dialogo delle formule di Excel. 




__________________


## Funzioni di data :


In Excel, ci sono diverse funzioni di data che puoi utilizzare per eseguire operazioni su dati di data e ora. 

il formato e la lingua del tuo Excel possono influenzare la rappresentazione delle date e le funzioni disponibili. Puoi consultare la documentazione di Excel o il menu di aiuto di Excel per ulteriori dettagli e opzioni specifiche relative alle funzioni di data nel tuo ambiente Excel specifico.


Ecco un elenco delle principali funzioni di data in Excel:

### Funzioni di Data di Base:
1. **TODAY()**: Restituisce la data odierna.
2. **NOW()**: Restituisce la data e l'orario correnti.
3. **DATE(anno, mese, giorno)**: Restituisce una data in base agli argomenti specificati.
4. **TIME(ora, minuto, secondo)**: Restituisce un orario in base agli argomenti specificati.

### Estrazione di Componenti dalla Data:
5. **YEAR(data)**: Restituisce l'anno dalla data specificata.
6. **MONTH(data)**: Restituisce il mese dalla data specificata (da 1 a 12).
7. **DAY(data)**: Restituisce il giorno del mese dalla data specificata.
8. **HOUR(ora)**: Restituisce l'ora dalla data o dall'orario specificato.
9. **MINUTE(ora)**: Restituisce i minuti dalla data o dall'orario specificato.
10. **SECOND(ora)**: Restituisce i secondi dalla data o dall'orario specificato.

### Operazioni su Date:
11. **DATEVALUE(testo)**: Converte una data in formato testo in un valore numerico della data.
12. **TIMEVALUE(testo)**: Converte un orario in formato testo in un valore numerico dell'orario.
13. **DATEDIF(data_iniziale, data_finale, "unità")**: Calcola la differenza tra due date in base all'unità specificata ("y" per anni, "m" per mesi, "d" per giorni, ecc.).

### Formattazione di Date e Orari:
14. **TEXT(data, "formato")**: Converte una data o un orario in formato testo utilizzando il formato specificato.
15. **DAYNAME(data)**: Restituisce il nome del giorno dalla data specificata.
16. **MONTHNAME(data)**: Restituisce il nome del mese dalla data specificata.

### Manipolazione Avanzata:
17. **EDATE(data, numero_mesi)**: Restituisce la data che si trova a un certo numero di mesi prima o dopo la data specificata.
18. **EOMONTH(data, numero_mesi)**: Restituisce l'ultimo giorno del mese, un numero specificato di mesi prima o dopo la data specificata.
19. **NETWORKDAYS(data_iniziale, data_finale, [festivi])**: Restituisce il numero di giorni lavorativi tra due date, escludendo i giorni festivi specificati.



























































