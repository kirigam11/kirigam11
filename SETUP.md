# Setup — README profilo Cyberpunk 2077

## Cosa c'è già dentro (dati reali, non placeholder)

| Campo | Valore |
|---|---|
| Handle | `kirigam11` |
| Alias fCC | `kirigamii` |
| Email | `kirigamii@proton.me` |
| Base | Italy |
| Età | 17 |
| Stack | Python · C · JavaScript · React · Node.js |
| Progetto in evidenza | `vxwm-systray-patch` (dwm/X11, C) |
| Social | email, freeCodeCamp, GitHub |

**Non ho messo** quello che non mi hai dato: sito web (in costruzione), LinkedIn, X, Docker, Figma, Tailwind/Next/Express/Prisma, SQL.

Tutte le immagini sono state testate: **40/40 rispondono 200** (l'unica 404 è lo snake, normale finché non gira l'Action). `github-readme-stats`, l'activity graph e i trophy oggi sono **offline** (503/402), quindi ho usato `github-profile-summary-cards` col tema **`2077`** (giallo `#FCEE0C`, ciano `#03D8F3`, rosso `#FF0055`).

---

## 1. Crea il repository

1. https://github.com/new
2. Nome: **`kirigam11`** (identico allo username), visibilità **Public**
3. Spunta *Add a README file* → Create
4. Se compare *"You found a secret!"*, è tutto giusto.

## 2. Carica i file

Nel repo → `Add file` → `Upload files` → trascina:

```
README.md
certifications/README.md
.github/workflows/snake.yml
```

Cancella il README generato da GitHub (o sovrascrivilo con il nostro, va bene lo stesso).

## 3. Attiva il serpente

1. **Settings → Actions → General → Workflow permissions** → *Read and write permissions* → Save
2. **Actions → Generate Snake → Run workflow**
3. Crea il branch `output` con gli SVG gialli. Finché non gira, nel README vedrai un'immagine rotta: è normale.

## 4. Le certificazioni freeCodeCamp

Il tuo profilo `freecodecamp.org/kirigamii` esiste ed è collegato a GitHub, ma **l'API pubblica di freeCodeCamp non espone le certificazioni** (restituisce `false` anche per account che ne hanno: l'ho verificato, quindi non è un problema tuo). Non ho potuto ricavarle in automatico.

Quando ne ottieni una, in 30 secondi:

1. Apri `https://www.freecodecamp.org/certification/kirigamii/<slug>` (gli slug sono in `certifications/README.md`)
2. Nel `README.md`, sezione `[ 04 ] CERTIFICATIONS`:
   - cancella il badge `STATUS-IN_PROGRESS`
   - duplica il blocco `TEMPLATE` che trovi nel commento, cambiando nome e link
3. (opzionale) scarica il PDF e mettilo in `certifications/`, poi aggiungi la riga nella tabella lì.

**Mandami i nomi/slug delle certificazioni e le aggiungo io.**

## 5. Il font: perché il nome è un'immagine

GitHub **cancella** `<style>`, gli attributi `style="..."` e i font esterni: **non si può applicare un font al testo normale di un README**. L'unico modo è dentro un'immagine SVG, e `readme-typing-svg` incorpora il font in base64 nell'SVG — ecco perché il tuo nome è Rajdhani vera e non un fallback.

Il font originale di Cyberpunk 2077 è proprietario (CD Projekt, non distribuibile). **Rajdhani** è il sostituto gratuito più vicino: condensato, geometrico, spigoloso.

Cambiare font = cambiare `font=` nel link:

| Font | Vibe | Valore |
|---|---|---|
| **Rajdhani** | UI di CP2077 (default) | `font=Rajdhani` |
| Orbitron | display futuristico | `font=Orbitron` |
| Chakra Petch | HUD militare | `font=Chakra+Petch` |
| Share Tech Mono | terminale | `font=Share+Tech+Mono` |
| Oxanium | angolare sci-fi | `font=Oxanium` |

Spazi nel nome → `+`. Altri parametri utili: `weight=700`, `size=76`, `color=FCEE0A`, `pause=` (ms tra le righe).

## 6. Palette e cambio accento

| Hex | Ruolo | Dove |
|---|---|---|
| `#FCEE0A` | giallo CP2077 | nome, badge, barre, snake |
| `#03D8F3` | ciano | frontend, sottotitolo, divider |
| `#FF0055` | rosso | backend, divider, certificazioni |
| `#0A0A0A` | nero | sfondo card streak |

**Cambio accento globale**: find & replace `FCEE0A` → il colore che vuoi. Cambia in un colpo nome, badge, barre e streak. Poi fai lo stesso in `.github/workflows/snake.yml`.

## 7. Aggiungere tech o repo

Tech (copia una riga, cambia testo/colore/logo — logo da https://simpleicons.org):

```html
<img src="https://img.shields.io/badge/NOME-FCEE0A?style=flat-square&logo=nomedellogo&logoColor=000000" alt="NOME" />
```

Repo: nella tabella `[ 03 ] CONTRACTS` duplica il primo `<td>` e cambia link, descrizione e badge. Quando aggiungi un secondo progetto serio, togli la cella "SEE ALL CONTRACTS" e mettici il repo vero.

## 8. Limiti da sapere

- **Niente CSS = niente glitch/scanline/ombre.** L'effetto "glitch" lo fanno il cursore lampeggiante del typing SVG, le barre gradiente e il tracking largo dei titoli.
- **Le card al 48%** su mobile diventano strette: se dà fastidio, metti `width="100%"` e una per riga.
- **Servizi gratuiti a volte cadono**: se una card sparisce, ricarica. Non è il tuo README.
- **Cache GitHub**: dopo un aggiornamento fai `Ctrl+F5` o aggiungi `&v=2` all'URL dell'immagine.
- **Le stats sono quasi vuote** perché hai 1 repo pubblico: è normale, si riempiono da sole.

## 9. `preview.html`

Anteprima locale del risultato reale. Aprila nel browser per vedere il design prima di pubblicare. **Non caricarla** nel repo (serve solo a te).
