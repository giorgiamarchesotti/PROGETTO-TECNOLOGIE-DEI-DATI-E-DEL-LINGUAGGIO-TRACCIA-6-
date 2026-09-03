# “Il gran rifiuto”: Analisi dei Filtri di Sicurezza e della Comprensione Semantica nei LLM

Progetto sviluppato per l’esame di **Tecnologie dei Dati e del Linguaggio** (Traccia 6: *”Il gran rifiuto”*). L’indagine analizza il confine tra la moderazione dei contenuti e la censura preventiva nei Large Language Models, confrontando il comportamento dei sistemi commerciali con i modelli open-source.

---

## Panoramica e Obiettivo
L’obiettivo principale del progetto è testare se i modelli open-source privi di filtri commerciali riescano a superare la censura preventiva riscontrata su ChatGPT (durante l’analisi di trascrizioni sensibili tratte dal podcast d’inchiesta *Veleno* di Pablo Trincia e Alessia Rafanelli) e valutarne l’effettiva affidabilità semantica e i limiti interpretativi.

---

## Metodologia e Corpus
* **Il Corpus:** Basato sulle trascrizioni personali dei passaggi chiave del podcast *Veleno* (2017/2018), focalizzandosi esclusivamente sui frammenti (relativi ad audizioni protette, testimonianze e contesti investigativi) che in precedenza erano stati bloccati da ChatGPT per violazione delle direttive di sicurezza (*safety guidelines*).
* **Griglia a Doppia Intenzione:** Ogni frammento è stato testato interrogando il modello open-source con una duplice formulazione:
  1. *Prompt Crudo / Operativo* (estrazione fattuale diretta).
  2. *Prompt Accademico / Teoretico* (contestualizzato all’interno di una ricerca universitaria).

---

## Stack Tecnologico
* **Linguaggio:** Python
* **Ambiente di esecuzione:** Google Colab (validato anche da dispositivo mobile / iPad)
* **Librerie:** Pandas (strutturazione dati), Matplotlib (generazione del grafico statistico)
* **Supporto allo sviluppo:** Progettato e implementato con il supporto di **Gemini Plus** come co-pilota concettuale e assistente di *pair programming*.

---

## Risultati Principali
* **0% di Rifiuti Espliciti (*Hard Refusal*):** Il modello open-source ha completato tutte le esecuzioni, superando la barriera della censura commerciale.
* **Criticità Semantiche:** L’analisi qualitativa ha evidenziato limiti strutturali rilevanti, tra cui il **fraintendimento dei ruoli narrativi** e l’**edulcorazione** dei passaggi emotivamente e tematicamente più forti.

---

## Struttura del Repository
* `notebook_progetto.ipynb`: Taccuino con l’intero codice eseguibile.
* `risultati_test_rifiuti_ampliato.json`: Dataset strutturato con gli output dei test.
* `grafico_test.png`: Grafico a barre descrittivo generato con Matplotlib.
* `report.html`: Artifact finale che raccoglie in modo pulito e autonomo l’intero esperimento.
* `presentazione_progetto.pptx` (file delle slide): Presentazione strutturata in 10 slide per la discussione orale dell’esame.
