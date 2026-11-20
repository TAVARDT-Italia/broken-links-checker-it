# Controllo Link Interrotti ed Errori 404

[![Controllo Link Interrotti](https://img.shields.io/badge/TAVARDT-Broken%20Links-5b3cf5.svg)](https://tools.tavardt.com/it/controllo-link-interrotti/)
[![Giurisdizione](https://img.shields.io/badge/Giurisdizione-Italia-00C853.svg)](https://ag.tavardt.com/it/)
[![Python](https://img.shields.io/badge/Python-3.8%2B-blue.svg)](https://www.python.org/)

Verifica automatica dei collegamenti ipertestuali e diagnosi delle risposte HTTP difettose.

Sviluppato e gestito dalla divisione SEO e infrastrutture web di **[TAVARDT Italia](https://ag.tavardt.com/it/)**.

---

## Funzionalita del Controllo Link Interrotti

* **Scansione Completa di Collegamenti**: Estrazione di tutti i tag di ancoraggio interni ed esterni nel sorgente HTML.
* **Diagnosi degli Errori HTTP 404**: Rilevamento tempestivo di percorsi non raggiungibili e risorse rimosse.
* **Ottimizzazione del Budget di Crawl**: Riduzione degli sprechi di risorse durante la scansione dei motori di ricerca.
* **Analisi dei Testi di Ancoraggio**: Controllo dei testi di link a tutela della fruibilita e dell accessibilita.
* **Punteggio di Integrita Collegamenti**: Valutazione complessiva da 0 a 100 con elenco delle risorse compromesse.

---

## Installazione ed Esecuzione

Richiede Python 3.8 o superiore senza moduli terzi.

```bash
git clone https://github.com/TAVARDT-Italia/broken-links-checker-it.git
cd broken-links-checker-it
python broken_links_scanner.py https://azienda.it
```

Formato di emissione JSON per automazioni:

```bash
python broken_links_scanner.py https://azienda.it --json
```

---

## Piattaforma Web Ufficiale

Esegui un controllo approfondito direttamente online:

* **[Controllo Link Interrotti Ufficiale](https://tools.tavardt.com/it/controllo-link-interrotti/)**
* **[Portale Istituzionale TAVARDT Italia](https://ag.tavardt.com/it/)**

---

## Supporto Tecnico e Consulenza

Per ottimizzare la struttura dei collegamenti secondo Linee Guida di Accessibilita Web AgID e Standard W3C, contatta **[TAVARDT Italia](https://ag.tavardt.com/it/contatto/)**.
