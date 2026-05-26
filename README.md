# Porta di ingresso al Calendario Protezione Civile

Questo file serve come **link stabile** al calendario della Protezione Civile
Occhiobello e Stienta.

Quando qualcuno apre questo link, viene reindirizzato automaticamente al
calendario vero, che si trova su Google.

---

## Perché esiste questa pagina?

Chrome (il browser di Google) — quando hai più account Google aperti —
a volte riscrive certi indirizzi e li rompe. Un indirizzo su GitHub
non viene toccato da Chrome, quindi il reindirizzamento funziona sempre.

**L'indirizzo da condividere su Telegram è quello GitHub Pages
(es. `https://nome-organizzazione.github.io/calendario/`)
NON il link diretto di Google.**

---

## L'unica cosa che potresti dover cambiare

Se il calendario viene spostato o re-deployato su Google, il suo indirizzo
cambia. In quel caso devi aggiornare **una sola riga** in questo file
(`github-pages/index.html`).

La riga da cercare è questa (circa alla riga 5):

```
content="0; url=https://script.google.com/macros/s/AKfy.../exec?view=public"
```

E qualche riga sotto, nel testo del link di riserva:

```
<a href="https://script.google.com/macros/s/AKfy.../exec?view=public">
```

Sostituisci la parte `https://script.google.com/...` con il nuovo indirizzo.

---

## Come aggiornare l'indirizzo — passo passo (senza usare il terminale)

### Di cosa hai bisogno
- Un account GitHub con accesso a questo progetto

### Passi

**1.** Apri la pagina del progetto su GitHub.

**2.** Naviga nella cartella `github-pages` e clicca sul file `index.html`.

**3.** Clicca sull'icona della matita ✏️ in alto a destra per modificare il file.

**4.** Trova le due righe con l'indirizzo `https://script.google.com/...`
   e sostituisci solo quella parte con il nuovo indirizzo.
   (Lascia tutto il resto esattamente com'è.)

**5.** Scorri in fondo alla pagina e clicca **"Commit changes"**.

**6.** Scrivi una breve descrizione (es. "Aggiornato link calendario") e clicca
   di nuovo **"Commit changes"**.

**7.** Aspetta 1–2 minuti, poi prova ad aprire il link GitHub Pages
   per verificare che il reindirizzamento funzioni.

---

## Come trovare il nuovo indirizzo del calendario

Se il calendario è stato re-deployato, il nuovo indirizzo si trova così:

1. Apri [script.google.com](https://script.google.com) con l'account
   `protcivocchiobello@gmail.com`

2. Apri il progetto **"Calendar Protezione Civile"**

3. Clicca su **"Distribuisci"** → **"Gestisci distribuzioni"**

4. Accanto al deploy attivo, clicca sull'icona 🔗 o copia l'**URL di distribuzione**

5. L'URL che trovi finisce con `/exec` — aggiungi `?view=public` alla fine:
   ```
   https://script.google.com/macros/s/XXXXX.../exec?view=public
   ```

6. Questo è il nuovo indirizzo da incollare in `index.html`

---

## Come attivare GitHub Pages (solo la prima volta)

*(Queste istruzioni servono solo per la configurazione iniziale del progetto.)*

1. Vai nelle **Impostazioni** (Settings) del repository GitHub
2. Nel menu a sinistra, clicca su **"Pages"**
3. In "Source" seleziona il ramo `main` e la cartella `/github-pages`
4. Clicca **"Save"**
5. Dopo qualche minuto apparirà l'URL pubblico (es. `https://nome.github.io/calendario/`)

---

*In caso di problemi, contatta il responsabile tecnico del progetto.*
