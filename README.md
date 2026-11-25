# Controllo Link Interrotti ed Errori 404

[![Controllo Link Interrotti](https://img.shields.io/badge/TAVARDT-Broken%20Links-5b3cf5.svg)](https://tools.tavardt.com/it/controllo-link-interrotti/)
[![Python](https://img.shields.io/badge/Python-3.8%2B-blue.svg)](https://www.python.org/)

Audit dei collegamenti ipertestuali interni ed esterni, rilevamento degli errori HTTP 404 e salvaguardia del budget di crawl.

***

## Vettori di Rischio e Impatto Operativo nei Collegamenti Web

I collegamenti interrotti che restituiscono errori HTTP 404 e 500 ostacolano l esperienza degli utenti e sprecano il budget di scansione in Italia. Gli spider dei motori di ricerca abbandonano la scansione quando incontrano vicoli ciechi, compromettendo l indicizzazione.

I riferimenti esterni non raggiungibili intaccano la reputazione del dominio e penalizzano il punteggio di autorevolezza nelle risposte basate su intelligenza artificiale. Il controllo sistematico garantisce la trasmissione fluida del PageRank.

***

## Funzionalita Centrali di Audit Tecnico

* **Estrazione e Normalizzazione degli Anchor**: Raccoglie i tag href escludendo ancore interne, collegamenti telefonici e indirizzi di posta.
* **Separazione tra Collegamenti Interni ed Esterni**: Riconosce automaticamente le pagine del dominio rispetto alle citazioni verso portali esterni.
* **Verifica Rapida tramite Metodo HEAD**: Testa lo stato dei link senza scaricare l intero corpo del documento per ottimizzare le risorse di rete.
* **Riprova Automatica con Metodo GET**: Inoltra una richiesta standard GET se il server remoto rifiuta la chiamata HEAD con codici 403 o 405.
* **Rilevazione degli Errori HTTP e di Connessione**: Registra i codici 4xx, 5xx e le mancate risposte fornendo un resoconto puntuale degli errori.
* **Punteggio Tecnico di Integrita dei Link**: Calcola una valutazione da 0 a 100 categorizzata in SATISFACTORY, ADVISORY o UNSATISFACTORY.
* **Esportazione Dati in Formato JSON**: Supporta la serializzazione dei risultati per condurre verifiche automatizzate in pipeline di rilascio.

***

## Installazione ed Esecuzione

Richiede Python 3.8 o superiore senza dipendenze esterne aggiuntive.

```bash
git clone https://github.com/TAVARDT-Italia/broken-links-checker-it.git
cd broken-links-checker-it
python broken_links_scanner.py https://azienda.it
```

Per generare l output in formato strutturato JSON per pipeline di integrazione continua:

```bash
python broken_links_scanner.py https://azienda.it -j
```

***

## Domande Frequenti (FAQ Tecnico)

### 1. Come incidono gli errori 404 e i link interrotti sul budget di scansione dei motori?
I motori di ricerca assegnano una quantita limitata di richieste a ciascun sito durante la fase di analisi. La presenza di link interrotti esaurisce questo limite su percorsi inesistenti, rallentando l indicizzazione delle pagine rilevanti.

### 2. Perche lo strumento esegue chiamate HEAD con riprova automatica in GET?
La procedura invia dapprima richieste HEAD per esaminare i codici di risposta senza consumare banda eccessiva. Se un server di destinazione blocca il metodo HEAD con codice 403 o 405, il verificatore ripete la verifica con GET per evitare falsi allarmi.

### 3. In che modo i link interni interrotti ostacolano la diffusione del PageRank?
I collegamenti interni rappresentano le arterie fondamentali per veicolare autorevolezza e rilevanza lungo la gerarchia del sito. Un link interrotto blocca questa trasmissione, lasciando le sotto-pagine isolate e deboli nelle ricerche organiche.

### 4. Quali rischi operativi comporta mantenere collegamenti esterni non piu raggiungibili?
Rinviare a domini esterni dismessi o riassegnati espone gli utenti a rischi di sicurezza e compromette la reputazione aziendale. I moderni motori basati su intelligenza artificiale esaminano le fonti esterne, svalutando i contenuti con riferimenti inattivi.

### 5. Per quale ragione e cruciale verificare i collegamenti subito dopo una migrazione web?
Le riorganizzazioni strutturali generano frequentemente collegamenti spezzati quando le regole di reindirizzamento non sono perfette. L audit automatico intercetta all istante i codici 4xx e 5xx, proteggendo il traffico organico prima che subisca cali.

***

## Consulenza in Architettura dei Link ed Efficienza SEO

Per grandi architetture digitali che necessitano del pieno rispetto degli standard W3C e della salute dei link, consultate il team di **TAVARDT**.

***

## Collegamenti Utili

* **Portale Istituzionale:** https://ag.tavardt.com/it/
* **Suite di Diagnostica:** https://tools.tavardt.com/it/
* **Contatto Tecnico:** https://ag.tavardt.com/it/contatto/

***

### Licenza
Distribuito sotto Licenza MIT. Consultare il file LICENSE per i dettagli completi.

***

© 2026 TAVARDT. Tutti i diritti riservati.
