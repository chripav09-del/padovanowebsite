# Christian Padovano — Sito Portfolio

Sito web personale per attività di web design freelance.

---

## Come configurare il form contatti (EmailJS)

Il form di contatto usa **EmailJS**, un servizio gratuito che ti permette di ricevere i messaggi via email senza bisogno di un server.

### Passaggi:

1. Vai su [emailjs.com](https://www.emailjs.com/) e crea un account gratuito
2. Nella dashboard, clicca **"Add New Service"** e collega la tua email (es. Gmail)
3. Copia il **Service ID** (lo trovi nella pagina del servizio appena creato)
4. Vai su **"Email Templates"** e crea un nuovo template. Nel corpo del template usa queste variabili:
   - `{{nome}}` — nome del cliente
   - `{{attivita}}` — nome dell'attività
   - `{{contatto}}` — telefono o email del cliente
   - `{{messaggio}}` — il messaggio
5. Copia il **Template ID** dalla pagina del template
6. Vai su **Account > API Keys** e copia la **Public Key**
7. Apri il file `script.js` e sostituisci:
   - `YOUR_PUBLIC_KEY` con la tua Public Key
   - `YOUR_SERVICE_ID` con il tuo Service ID
   - `YOUR_TEMPLATE_ID` con il tuo Template ID

---

## Come pubblicare su Netlify (gratis)

1. Vai su [netlify.com](https://www.netlify.com/) e crea un account gratuito
2. Nella dashboard, clicca **"Add new site" > "Deploy manually"**
3. Trascina la cartella `christian-padovano-site` (quella con index.html dentro) nell'area indicata
4. Aspetta qualche secondo — il sito sarà online!
5. Netlify ti assegnerà un indirizzo tipo `nome-casuale.netlify.app`
6. Per cambiarlo vai su **Site settings > Domain management > Change site name** e scrivi ad esempio `christianpadovano`

Il tuo sito sarà raggiungibile su `christianpadovano.netlify.app`.

Alternative se quel nome fosse già preso:
- `christianpadovano-webdesign.netlify.app`
- `cpwebdesign-salerno.netlify.app`

---

## Come aggiornare il portfolio con progetti reali

Quando avrai dei progetti veri da mostrare:

1. Apri `index.html`
2. Cerca il commento `<!-- SOSTITUIRE con screenshot/link reali quando disponibili -->`
3. Per ogni card del portfolio, puoi:
   - Sostituire il mockup CSS con un'immagine vera: cambia il `<div class="portfolio__mockup ...">` con un `<img src="screenshot.jpg" alt="..." loading="lazy">`
   - Aggiornare titolo e descrizione nel `<div class="portfolio__info">`
   - Rimuovere la scritta "Progetto dimostrativo" dal `<span class="portfolio__badge">`
   - Aggiungere un link al sito pubblicato

---

## Struttura dei file

```
christian-padovano-site/
├── index.html      ← pagina principale
├── style.css       ← stili
├── script.js       ← animazioni, Three.js, form EmailJS
├── favicon.svg     ← icona del sito
└── README.md       ← questo file
```
