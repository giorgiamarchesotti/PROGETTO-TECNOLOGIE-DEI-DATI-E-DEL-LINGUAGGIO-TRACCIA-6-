# Analisi della Distorsione Semantica e dell’Edulcorazione nei LLM: Il Caso “Veleno”

Progetto sviluppato per l’esame di **Tecnologie dei Dati e del Linguaggio** (Traccia 6: *"Il gran rifiuto"*), Corso di Laurea in Scienze Umanistiche per la Comunicazione, Università degli Studi di Milano.

---

## 1. Abstract e Obiettivi di Ricerca
Il presente progetto sposta il focus dalla semplice analisi binaria della censura informatica a un’indagine rigorosa di **linguistica computazionale e analisi del discorso**. L’obiettivo primario è verificare in che modo i Large Language Models (LLM) open-source elaborano, distorcono o edulcorano le trascrizioni orali di cronaca giudiziaria caratterizzate da un’elevata densità emotiva e da una forte asimmetria dei ruoli narrativi. A partire dal corpus del podcast d’inchiesta *Veleno* (2017) di Pablo Trincia e Alessia Rafanelli, la ricerca misura oggettivamente la perdita di fedeltà semantica, il fraintendimento dei ruoli e la tendenza alla censura interna.

---

## 2. Il Corpus e le Dimensioni di Analisi
Il corpus di riferimento è costituito da passaggi chiave estrapolati dalle trascrizioni integrali del podcast, suddivisi in tre nuclei tematici fondamentali:
* **Le audizioni protette dei minori:** Analisi del discorso infantile riportato, dei verbi di percezione e del tasso di ambiguità sintattica.
* **Le testimonianze dei familiari e i contesti rituali:** Esame dei marcatori di soggettività, della densità lessicale e delle narrazioni ad alto impatto traumatico.
* **Le dinamiche investigative e le incongruenze:** Contrasto tra il linguaggio tecnico-giuridico e la drammaticità del parlato.

---

## 3. Metodologia e Griglia Sperimentale a Doppia Intenzione
Per valutare la sensibilità del modello alle variazioni di framing, è stata adottata una griglia sperimentale basata su una duplice modalità di interrogazione:
1. **Prompt Operativo / Fattuale:** Richiesta di estrazione, sintesi e rielaborazione diretta dei fatti narrati nelle trascrizioni.
2. **Prompt Accademico / Teoretico:** Richiesta di analisi stilistica e pragmatica contestualizzata all’interno di una ricerca di ambito umanistico.

---

## 4. Pipeline Tecnica e Stack Computazionale
L’esperimento è stato condotto in ambiente **Google Colab** attraverso una pipeline automatizzata in **Python**:
* **Inferenza e Gestione Dati:** Elaborazione dei frammenti e persistenza dei risultati in formato strutturato (`risultati_test_rifiuti_ampliato.json`).
* **Analisi Quantitativa (Pandas):** Misurazione algoritmica della variazione della lunghezza dei testi e calcolo della **percentuale di conservazione del lessico critico** (parole chiave emotive e giudiziarie originali presenti nell’output del modello).
* **Visualizzazione dei Dati (Matplotlib):** Generazione del grafico statistico (`grafico_test.png`) per la rappresentazione visiva dello scostamento semantico.
* **Reporting:** Produzione di un artifact statico interattivo (`report.html`) per la consultazione autonoma dei risultati.

*Nota di trasparenza metodologica:* Lo sviluppo del codice e la strutturazione logica dell’analisi sono stati condotti con il supporto di Gemini Plus in qualità di assistente di pair programming, sotto costante supervisione e validazione umana.

---

## 5. Risultati e Discussione Critica
* **Assenza di Hard Refusal (0%):** I modelli open-source analizzati non attivano blocchi formali o preventivi, portando sempre a termine l’esecuzione dell'output.
* **Censura Semantica Interna e Edulcorazione:** L’analisi quantitativa e qualitativa rivela una drastica riduzione della conservazione lessicale (spesso compresa tra lo 0% e il 16.7%). Questo evidenzia un fenomeno di edulcorazione: il modello, pur non rifiutando il testo, attenua sistematicamente i termini più forti, fraintende i ruoli narrativi e neutralizza la complessità del discorso orale.

---

## 6. Struttura del Repository
* `notebook_progetto.ipynb`: Taccuino Python contenente il codice sorgente, la pipeline di calcolo e l’esecuzione dei test.
* `risultati_test_rifiuti_ampliato.json`: Dataset strutturato in formato JSON contenente i metadati e gli output dell’esperimento (in allegato anche il dataset del progetto precedente).
* `grafico_test.png`: Grafico statistico generato tramite Matplotlib sulla conservazione lessicale (in allegato anche il grafico del progetto precedente).
* `report.html`: Artifact HTML autonomo riassuntivo dell’esperimento (in allegato anche l’Artifact HTML del progetto precedente).
* `presentazione_progetto.pptx`: Presentazione in 10 slide strutturata per la discussione orale dell’esame.
