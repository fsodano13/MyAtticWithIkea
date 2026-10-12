# MyAtticWithIkea

Configuratore 3D per una parete attrezzata IKEA PLATSA in mansarda (nicchia 235 × 246 cm).

Pagina online: **https://fsodano13.github.io/MyAtticWithIkea/**

## Cosa fa

- **Vista 3D interattiva** (three.js) della stanza con falda, travi e soffitto reali rilevati a misura.
- **Anta e contenuto indipendenti**: ogni telaio PLATSA può avere o no l'anta (con il lato
  cerniere), e separatamente si riempie con una pila di cassetti e vani in qualsiasi ordine
  (es. 4 cassetti da 20 più 2 vani da 20). I ripiani nascono dalle divisioni fra i vani, anche
  dietro un'anta, e la quota di ognuno viene calcolata e riportata nei disegni.
- **Controllo collisioni**: ante che sbattono contro falda e travi (con l'angolo massimo di
  apertura), cassetti aperti, altezza totale contro il punto più basso del soffitto.
- **Visibilità selettiva** di soffitto, parete di fondo e parete destra, per guardare dentro la nicchia.
- **Viste 2D e PDF**: il tasto *Salva PDF* produce un A4 orizzontale di quattro tavole — viste 3D
  con il riepilogo dei quattro vani, prospetto e pianta in 1:20, una sezione per vano in 1:30,
  lista componenti e composizione quota per quota. Il tasto *Viste 2D* mostra le stesse tavole a
  schermo e permette di stamparle. Disegni vettoriali, immagini 3D catturate dalla scena.
- La configurazione resta salvata nel browser (localStorage); le vecchie configurazioni vengono
  migrate automaticamente al nuovo formato.

## Geometria rilevata

| | |
|---|---|
| Nicchia | 235 (parete finestra → parete destra) × 246 (lato aperto → fondo) |
| Travi | larghe 13,5 cm, a 73,5 e 184 cm dal lato aperto |
| Intradosso travi | 80 cm a sinistra, 154,5 cm a destra |
| Soffitto tra le travi | 108,5 cm a sinistra, 183 cm a destra |
| Falda davanti | 263 cm al muro finestra, 239 cm alla prima trave |
| Mobili | fronte a 180 cm dalla parete finestra, profondità 55, a terra senza piedini |

## Come si apre

Online al link qui sopra, oppure aprendo `index.html` in un browser: è un unico file statico,
senza build. Servono soltanto due CDN (three.js, e jsPDF solo quando si salva il PDF).
