# MyAtticWithIkea

Configuratore 3D per una parete attrezzata IKEA PLATSA in mansarda (nicchia 235 × 246 cm).

Pagina online: **https://fsodano13.github.io/MyAtticWithIkea/**

## Cosa fa

- **Vista 3D interattiva** (three.js) della stanza con falda, travi e soffitto reali rilevati a misura.
- **Anta e contenuto indipendenti**: ogni telaio PLATSA può avere o no l'anta (con il lato
  cerniere), e separatamente si riempie con una pila di cassetti e vani in qualsiasi ordine
  (es. 4 cassetti da 20 più 2 vani da 20). I ripiani nascono dalle divisioni fra i vani, e ogni
  vano si può definire sia per altezza sia scrivendo direttamente la **quota da terra** del suo
  cielo, cioè dove va il ripiano: i vani sopra scorrono di conseguenza.
- **Tre tipi di elemento** nella pila: cassetto, vano a giorno e vano con **bastone appendiabiti**
  (HJÄLPA regolabile 60–100 × 55, l'accessorio PLATSA per i telai da 55). Per il bastone il tool
  calcola l'altezza utile sotto e dice se ci stanno capi lunghi, camicie e giacche, o niente.
- **Controllo collisioni**: ante che sbattono contro falda e travi (con l'angolo massimo di
  apertura), cassetti aperti, altezza totale contro il punto più basso del soffitto.
- **Regola dei telai con anta**: dentro un telaio con anta ci vanno solo vani e bastoni, non
  cassetti. Mettendo l'anta a un telaio che li aveva, i cassetti diventano vani della stessa
  altezza.
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
