# Analisi Matematica

Questo volume nasce come la trascrizione degli appunti dei tre corsi di **Analisi Matematica**, rispettivamente
* Analisi Matematica 1, A.A. 2013-2014, tenuto dalla prof.ssa Maura Salvatori;
* Analisi Matematica 2, A.A. 2013-2014, tenuto dal prof. Marco Vignati;
* Analisi Matematica 3, A.A. 2014-2015, tenuto dal prof. Bernhard Ruf.

Il tutto è arricchito da approfondimenti personali, spesso di carattere discorsivo e non troppo rigorosi.
Il lavoro è sotto una continua opera di perfezionamento, quindi correzioni e consigli sono sempre i benvenuti.

Buona lettura!

### Informazioni tecniche
##### Struttura dei file
I file `.tex` dei capitoli si trovano, suddivisi per corso, nelle tre cartelle numerate; sono inclusi nel file principale tramite il comando `\include`.
Il codice di ogni grafico è tenuto separato dal corpo principale, e si può trovare nella cartella `grafici`.
##### Come compilare
Se volete provare a compilare i file di LaTeX sul vostro computer, è sufficiente il comando, trovandosi nella cartella principale,

    pdflatex -shell-escape analisi-matematica.tex

I file dei singoli capitoli non possono essere compilati separatamente.

Prima di compilare per la prima volta, è necessario creare una cartella chiamata `tex`, sempre nella cartella principale: `pgfplots`, con l'opzione `externalize` impostata nel preambolo del file principale, compila i grafici solo la prima volta e li salva in formato PDF in tale cartella, per riutilizzarli le volte successive (salvo modifiche al loro codice).
Una compilazione senza aver creato la cartella `tex` dovrebbe arrestarsi in breve tempo con qualche errore.
