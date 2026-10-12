# MyAtticWithIkea

Configuratore 3D per una parete attrezzata IKEA PLATSA in mansarda (nicchia 235 × 246 cm).

Pagina online: **https://fsodano13.github.io/MyAtticWithIkea/**

## Cosa fa

- **Vista 3D interattiva** (three.js) della stanza con falda, travi e soffitto reali rilevati a misura.
- **Anta e contenuto indipendenti**: ogni telaio PLATSA può avere o no l'anta (con il lato
  cerniere), e separatamente si riempie di pezzi.
- **I pezzi si mettono a quota, non si impilano**: un ripiano è una mensola a una quota da terra,
  un bastone è un tondino a una quota, un cassetto è una base più l'altezza del frontale. Si
  scrive la quota e il pezzo va lì; i vani liberi sono quello che resta in mezzo e vengono
  calcolati e quotati da soli. Sovrapposizioni e pezzi fuori dal telaio vengono segnalati.
- **Bastone appendiabiti** (HJÄLPA regolabile 60–100 × 55, l'accessorio PLATSA per i telai da 55):
  il tool misura l'altezza utile sotto, cioè fino al primo pezzo che trova, e dice se ci stanno
  capi lunghi, camicie e giacche, o niente. Controlla anche la luce **sopra** il tubo: se non ci
  sono 4 cm il gancio della gruccia non passa, e il tool dice di quanto abbassarlo.
- **Controllo collisioni**: ante che sbattono contro falda e travi (con l'angolo massimo di
  apertura), cassetti aperti, altezza totale contro il punto più basso del soffitto.
- **Regola dei telai con anta**: dentro un telaio con anta ci vanno solo ripiani e bastoni, non
  cassetti.
- **Visibilità selettiva** di soffitto, parete di fondo e parete destra, per guardare dentro la nicchia.
- **Apertura per singolo pezzo**: il cursore 0–90° sta sulla riga dell'anta, il tasto *Sfila* sulla
  riga di ogni cassetto, e nel 3D si tocca direttamente l'anta o il singolo cassetto. L'apertura è
  stato di vista, non viene salvata con la configurazione.
- **Viste 2D e PDF**: il tasto *Salva PDF* produce un A4 orizzontale di quattro tavole — viste 3D
  con il riepilogo dei quattro blocchi, prospetto e pianta in 1:20, una sezione per blocco in 1:30,
  lista componenti e composizione quota per quota. Il tasto *Viste 2D* mostra le stesse tavole a
  schermo e permette di stamparle. Disegni vettoriali, immagini 3D catturate dalla scena.
- La configurazione resta salvata nel browser (localStorage); le vecchie configurazioni vengono
  migrate automaticamente al nuovo formato.

## Il progetto

La pagina si apre sulla configurazione decisa:

| | contenuto |
|---|---|
| Blocco 1 (fondo) | anta cerniera a sinistra, bastone appendiabiti a 113 · 111,8 cm utili |
| Blocco 2 (centro) | anta cerniera a destra, bastone a 113 · 111,8 cm utili |
| Blocco 3 | a vista: cassetti 40 + 20 + 20, ripiano a 80, vano aperto sopra |
| Blocco 4 (colonna) | telaio 180 con anta: ripiani a 30 e 60, bastone a 173 · 110 cm utili · sopra telaio 40 con anta |

Mobili appoggiati a terra **senza piedini**: ogni centimetro di zoccolo toglie un centimetro al
margine dell'anta del Blocco 1, che è di 5,9 cm e sparisce a 6. Il tasto *Riparti dal progetto*
rimette questa configurazione se nel frattempo è stata modificata nel browser.

## I quattro blocchi

Numerati dal fondo verso il lato aperto, nello stesso ordine in cui si leggono da sinistra nel
prospetto e nella pianta.

| | | |
|---|---|---|
| Blocco 1 | fondo | da 186 a 246 cm dal lato aperto |
| Blocco 2 | centro | da 126 a 186 |
| Blocco 3 | vicino alla colonna | da 66 a 126 |
| Blocco 4 | colonna, zona alta | da 6 a 66, moduli impilabili 40/60/120/180 |

## Geometria rilevata

| | |
|---|---|
| Nicchia | 235 (parete finestra → parete destra) × 246 (lato aperto → fondo) |
| Travi | larghe 13,5 cm, a 73,5 e 184 cm dal lato aperto |
| Intradosso travi | 80 cm a sinistra, 154,5 cm a destra |
| Soffitto tra le travi | 108,5 cm a sinistra, 183 cm a destra |
| Falda davanti | 263 cm al muro finestra, 239 cm alla prima trave |
| Mobili | fronte a 180 cm dalla parete finestra, profondità 55, a terra senza piedini |
| Piano sopra i bassi | elemento top SMÅSTAD 60 × 55 × 2, uno per blocco (alternativa: SPILDRA 60 × 56,8 × 3) |

## Come si apre

Online al link qui sopra, oppure aprendo `index.html` in un browser: è un unico file statico,
senza build. Servono soltanto due CDN (three.js, e jsPDF solo quando si salva il PDF).
