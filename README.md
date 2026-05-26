# Porte di ingresso al Calendario Protezione Civile

Questo progetto contiene due "link stabili" al calendario della Protezione
Civile Occhiobello e Stienta. Quando qualcuno apre uno di questi link, viene
reindirizzato automaticamente al calendario vero, che si trova su Google.

| Chi lo usa | Link da salvare/condividere | File che gestisce il redirect |
|---|---|---|
| **Volontari** (sola lettura) | `https://protezione-civile-occhiobello-stienta.github.io/calendario/` | `index.html` |
| **Amministratore** (gestione eventi) | `https://protezione-civile-occhiobello-stienta.github.io/calendario/admin/` | `admin/index.html` |

Il link admin apre una schermata che chiede la **password**: l'indirizzo NON
contiene nessuna password, quindi è sicuro salvarlo nei preferiti o condividerlo
con chi deve gestire il calendario.

---

## Perché esistono queste pagine?

Chrome (il browser di Google) — quando hai più account Google aperti —
a volte riscrive certi indirizzi e li rompe. Un indirizzo su GitHub
non viene toccato da Chrome, quindi il reindirizzamento funziona sempre.

**I link da condividere sono quelli `github.io` qui sopra, NON i link diretti
di Google.**

---

## L'unica cosa che potresti dover cambiare

Se il calendario viene spostato o re-deployato su Google, il suo indirizzo
cambia. In quel caso devi aggiornare l'indirizzo in **DUE file**:

- `index.html` → contiene il link che finisce con `?view=public`
- `admin/index.html` → contiene il link che finisce con `?view=admin`

In ciascun file l'indirizzo compare **due volte** (una nella riga `content=...`
e una nel link di riserva poco sotto). Vanno aggiornate entrambe.

---

## Come aggiornare gli indirizzi — passo passo (senza usare il terminale)

### Di cosa hai bisogno
- Un account GitHub con accesso a questo progetto

### Passi (ripetere per ENTRAMBI i file)

**1.** Apri la pagina del progetto su GitHub.

**2.** Clicca sul file da modificare:
   - `index.html` (è nella pagina principale del progetto), oppure
   - la cartella `admin` e poi il suo `index.html`

**3.** Clicca sull'icona della matita ✏️ in alto a destra per modificare il file.

**4.** Trova le due righe con l'indirizzo `https://script.google.com/...`
   e sostituisci solo quella parte con il nuovo indirizzo.
   (Lascia tutto il resto esattamente com'è — compreso `?view=public`
   o `?view=admin` alla fine.)

**5.** Scorri in fondo alla pagina e clicca **"Commit changes"**.

**6.** Scrivi una breve descrizione (es. "Aggiornato link calendario") e clicca
   di nuovo **"Commit changes"**.

**7.** Ripeti dal punto 2 per l'altro file.

**8.** Aspetta 1–2 minuti, poi prova ad aprire i due link GitHub Pages
   per verificare che i reindirizzamenti funzionino.

---

## Come trovare il nuovo indirizzo del calendario

Se il calendario è stato re-deployato, il nuovo indirizzo si trova così:

1. Apri [script.google.com](https://script.google.com) con l'account
   `protcivocchiobello@gmail.com`

2. Apri il progetto **"Calendar Protezione Civile"**

3. Clicca su **"Distribuisci"** → **"Gestisci distribuzioni"**

4. Accanto al deploy attivo, copia l'**URL di distribuzione**
   (finisce con `/exec`)

5. Per il file pubblico aggiungi `?view=public` alla fine;
   per il file admin aggiungi `?view=admin`:
   ```
   .../exec?view=public      → va in index.html
   .../exec?view=admin       → va in admin/index.html
   ```

---

## Come cambiare la password dell'amministratore

La password NON è in questi file. Si cambia direttamente su Google Apps Script,
senza re-deploy:

1. Apri [script.google.com](https://script.google.com) con `protcivocchiobello@gmail.com`
2. Apri il progetto → **⚙️ Impostazioni progetto**
3. Sezione **Proprietà script** → modifica (o aggiungi) la proprietà
   chiamata `ADMIN_TOKEN`, mettendo come valore la nuova password
4. Salva — la nuova password è subito attiva

> Usa solo lettere, numeri, trattino `-` e underscore `_` nella password
> (niente spazi o simboli).

---

## Come attivare GitHub Pages (solo la prima volta)

*(Queste istruzioni servono solo per la configurazione iniziale del progetto.)*

1. Vai nelle **Impostazioni** (Settings) del repository GitHub
2. Nel menu a sinistra, clicca su **"Pages"**
3. In "Source" seleziona il ramo `main` e la cartella `/ (root)`
4. Clicca **"Save"**
5. Dopo qualche minuto appariranno gli URL pubblici

---

*In caso di problemi, contatta il responsabile tecnico del progetto.*
