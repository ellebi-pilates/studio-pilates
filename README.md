# Ellebi Studio Pilates e Yoga

Questo repository contiene il sito statico dello studio Ellebi.

## Aggiornare la propria copia locale

Se stai lavorando su un clone locale del repository e su GitHub viene premuto il pulsante **Aggiorna ramo** (che in inglese corrisponde a *Update branch*), GitHub unisce automaticamente le modifiche del ramo principale nel ramo su cui stai lavorando **sul server remoto**. Per avere anche in locale gli stessi file aggiornati ci sono due passaggi:

1. **Scarica le modifiche dal remoto**
   ```bash
   git pull origin <nome-del-tuo-ramo>
   ```
   Questo comando porta nella tua cartella locale gli stessi commit che GitHub ha aggiunto con "Aggiorna ramo".

2. **Verifica gli aggiornamenti**
   Dopo il `git pull` puoi controllare lo stato dei file con:
   ```bash
   git status
   ```
   Se non compaiono modifiche non tracciate, significa che i file locali sono già allineati alla versione aggiornata sul remoto.

> Nota: se hai modifiche locali non ancora salvate, Git potrebbe chiederti di completare un merge o di risolvere conflitti. In questo caso è consigliabile salvare (commit) o accantonare (stash) le modifiche prima di eseguire `git pull`.

### Risolvere eventuali conflitti

Se dopo il `git pull` Git segnala `CONFLICT`, significa che le stesse righe sono state modificate sia in locale sia sul ramo remoto. Per risolvere:

1. **Individua i file in conflitto**: `git status` elenca i file marcati come `both modified`.
2. **Apri i file interessati** e cerca i marcatori `<<<<<<<`, `=======`, `>>>>>>>`. Mantieni solo la versione corretta eliminando i marcatori.
3. **Segna i conflitti come risolti** eseguendo:
   ```bash
   git add <file-risolto>
   ```
4. **Completa il merge** con un nuovo commit:
   ```bash
   git commit
   ```
5. **Aggiorna il remoto** se necessario: `git push origin <nome-del-tuo-ramo>`.

Suggerimento: per annullare l'unione e tornare allo stato precedente puoi usare `git merge --abort` (se il merge è ancora in corso) oppure `git reset --hard HEAD` (attenzione: perde eventuali modifiche locali non salvate).

## Pubblicazione

Il sito può essere pubblicato tramite GitHub Pages. Dopo aver eseguito il commit delle modifiche e averle spinte sul repository remoto, GitHub Pages rigenererà automaticamente la versione online del sito.

