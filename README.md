# Ellebi Studio Pilates e Yoga

Questo repository ospita il sito statico di Ellebi Studio Pilates e Yoga. Il layout è stato progettato per mantenere l'esperienza mobile invariata e rendere l'esperienza desktop più dinamica, con un'intestazione fotografica che utilizza "Studio.jpg" come sfondo condiviso tra tutte le pagine principali.

## Struttura del progetto

- `index.html` – Home page con hero introduttiva, riepilogo dei corsi e sezione biografia.
- `corsi.html` – Descrizione dei corsi offerti, organizzati in card responsive.
- `eventi.html` – Spazio per eventi, workshop e comunicazioni speciali.
- `contatti.html` – Informazioni di contatto, orari e form di richiesta.
- `style.css` – Foglio di stile condiviso che definisce tipografia, palette e layout responsive.
- Cartella degli asset – immagini (`*.jpg`, `logo.png`, `instagram.png`, `whatsup.png`) e font personalizzati.

## Intestazione fotografica

Le ultime modifiche rendono coerente l'intestazione del sito con le richieste precedenti:

- Tutte le pagine HTML fanno riferimento a `style.css?v=3` per forzare GitHub Pages a scaricare lo stylesheet aggiornato.
- La regola `.hero-header::before` in `style.css` imposta "Studio.jpg" come immagine di sfondo dell'header.
- Un overlay graduale (`.hero-header::after`) mantiene leggibili logo e navigazione su desktop senza alterare l'esperienza mobile.

Se aprendo `index.html` (o le altre pagine) vedi ancora un'intestazione bianca, verifica che il browser non stia usando una versione cache di `style.css` eseguendo un hard refresh (⌘⇧R su macOS, Ctrl+F5 su Windows) oppure svuotando la cache.

## Aggiornare contenuti e stili

1. Modifica i testi direttamente nei file HTML corrispondenti.
2. Aggiorna colori, spaziature o immagini in `style.css`. I selettori chiave per l'header sono `.hero-header`, `.hero-header::before` e `.topbar`.
3. Per sostituire la foto dell'intestazione, sostituisci il file `Studio.jpg` mantenendo lo stesso nome oppure aggiorna il percorso nello stylesheet.

Dopo ogni modifica, esegui `git status` per controllare i file cambiati e `git diff` per rivedere il contenuto delle modifiche.

## Pubblicazione con GitHub Pages

1. Salva le modifiche con `git commit` e inviale con `git push`.
2. GitHub Pages rigenererà automaticamente il sito online (https://ellebi-pilates.github.io/studio-pilates/).
3. Se non vedi subito l'aggiornamento, aggiungi o incrementa il parametro di versione della risorsa modificata (ad esempio `style.css?v=3`) oppure effettua un hard refresh del browser.

## Supporto

Per ulteriori modifiche strutturali o nuove sezioni, crea un nuovo branch, implementa le modifiche e apri una pull request descrivendo chiaramente gli aggiornamenti.
