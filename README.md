# Ellebi Studio Pilates e Yoga

Questo repository ospita il sito statico di Ellebi Studio Pilates e Yoga. Il layout è stato progettato per mantenere l'esperienza mobile invariata e rendere l'esperienza desktop più dinamica, con un'intestazione fotografica che impiega "Lalla in posa.jpg" come base e immagini dedicate per le diverse pagine desktop.

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
- La regola `.hero-header::before` in `style.css` applica "Lalla in posa.jpg" allo sfondo della home su desktop, mantenendo una resa neutra su smartphone.
- Le classi `.hero-corsi`, `.hero-eventi` e `.hero-contatti` impostano rispettivamente "Lallaposa3.jpg", "Lallaposa2.jpg" e "lallaposa4.jpg". Ognuna include un fallback automatico a "Lalla in posa.jpg" nel caso in cui l'immagine specifica non sia presente nel repository.
- Un overlay graduale (`.hero-header::after`) mantiene leggibili logo e navigazione su desktop senza alterare l'esperienza mobile.

### Come verificare rapidamente che lo sfondo sia attivo

1. Apri uno qualunque dei file HTML e verifica che il tag `<link rel="stylesheet" href="style.css?v=3">` sia presente nell'`<head>`.
2. Apri `style.css` e controlla che all'interno della regola `.hero-header::before` la dichiarazione `background: url('Lalla in posa.jpg') center/cover no-repeat;` sia valorizzata e che le varianti `.hero-corsi`, `.hero-eventi` e `.hero-contatti` elenchino prima l'immagine dedicata e poi il fallback.
3. Se stai navigando il sito pubblicato e non vedi l'immagine, effettua un hard refresh (⌘⇧R su macOS o Ctrl+F5 su Windows) per costringere il browser a scaricare l'ultima versione dello stylesheet.

Se aprendo `index.html` (o le altre pagine) vedi ancora un'intestazione bianca, verifica che il browser non stia usando una versione cache di `style.css` eseguendo un hard refresh (⌘⇧R su macOS, Ctrl+F5 su Windows) oppure svuotando la cache.

## Aggiornare contenuti e stili

1. Modifica i testi direttamente nei file HTML corrispondenti.
2. Aggiorna colori, spaziature o immagini in `style.css`. I selettori chiave per l'header sono `.hero-header`, `.hero-header::before` e `.topbar`.
3. Per sostituire la foto dell'intestazione, sostituisci i file JPEG corrispondenti mantenendo lo stesso nome oppure aggiorna i percorsi nello stylesheet.

Dopo ogni modifica, esegui `git status` per controllare i file cambiati e `git diff` per rivedere il contenuto delle modifiche.

## Pubblicazione con GitHub Pages

1. Salva le modifiche con `git commit` e inviale con `git push`.
2. GitHub Pages rigenererà automaticamente il sito online (https://ellebi-pilates.github.io/studio-pilates/).
3. Se non vedi subito l'aggiornamento, aggiungi o incrementa il parametro di versione della risorsa modificata (ad esempio `style.css?v=3`) oppure effettua un hard refresh del browser.

## Supporto

Per ulteriori modifiche strutturali o nuove sezioni, crea un nuovo branch, implementa le modifiche e apri una pull request descrivendo chiaramente gli aggiornamenti.
