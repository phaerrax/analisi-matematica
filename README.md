# Analisi Matematica

Questo volume consiste principalmente nella trascrizione degli appunti dei tre corsi di Analisi Matematica del corso di laurea in Fisica all'Università degli Studi di Milano, rispettivamente
* Analisi Matematica 1, A.A. 2013-2014, tenuto dalla prof.ssa Maura Salvatori;
* Analisi Matematica 2, A.A. 2013-2014, tenuto dal prof. Marco Vignati;
* Analisi Matematica 3, A.A. 2014-2015, tenuto dal prof. Bernhard Ruf.

È arricchito da alcuni approfondimenti personali, spesso di carattere discorsivo e non troppo rigorosi.
Il lavoro è sotto una continua opera di perfezionamento, quindi correzioni e consigli sono sempre i benvenuti.

Buona lettura!

### Informazioni tecniche
##### Struttura dei file
I file `.tex` dei capitoli si trovano, suddivisi per corso, nelle tre cartelle numerate; sono inclusi nel file principale tramite il comando `\include`.
Il codice di ogni grafico è tenuto separato dal corpo principale, e si può trovare nella cartella `grafici`.
Il file `.bib` contiene le informazioni necessarie per la bibliografia.

##### Come compilare
Se volete compilare i file di LaTeX sul vostro computer, ecco i passi da seguire (per una distribuzione Linux con le applicazioni necessarie installate).
I file dei singoli capitoli non possono essere compilati separatamente.
Si consiglia l'uso di `latexmk` per automatizzare i processi di compilazione.

Alla prima compilazione, bisogna generare i file della bibliografia di `biblatex`, perciò serve compilare più volte.
È necessario anche creare una sottocartella chiamata `tex` nella cartella principale: `pgfplots`, con l'opzione `externalize` impostata nel preambolo del file principale, compila i grafici solo alla prima occasione, e li salva in formato PDF in `tex`, per riutilizzarli le volte successive (salvo modifiche al loro codice).
Una compilazione senza aver creato la cartella `tex` dovrebbe arrestarsi in breve tempo con qualche errore.
Trovandosi nella cartella principale, eseguire

```bash
mkdir -p tex
pdflatex -shell-escape analisi-matematica
biber analisi-matematica
pdflatex -shell-escape analisi-matematica
pdflatex -shell-escape analisi-matematica
```

Le volte successive, se il file `analisi-matematica.bib` non è stato modificato e non sono state aggiunte citazioni (in tal caso, ripetere i passaggi precedenti), è sufficiente un unico passaggio:

```bash
pdflatex -shell-escape analisi-matematica
```

ripetuto eventualmente una seconda volta per sistemare riferimenti interni.
