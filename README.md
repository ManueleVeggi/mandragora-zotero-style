# Stile Zotero – Norme redazionali Mandragora

## Installazione

1. Scarica il file `mandragora-norme-redazionali.csl`.
2. Carica il file all'interno della piattaforma Zotero ([tutorial](https://www.zotero.org/support/preferences/cite)).
3. Lo stile comparirà nell'elenco come *Mandragora – Norme redazionali (stile a note)*.
4. Selezionalo e usa il plugin Zotero nel tuo elaboratore di testi (Word, LibreOffice, Google Docs) per inserire le citazioni nel documento.

---

## Cosa fa lo stile

Lo stile è concepito per la citazione a **note a piè di pagina** (o note di chiusura), secondo le norme redazionali Mandragora. In sintesi:

- nomi degli autori e curatori per esteso, nell'ordine Nome Cognome;
- «et al.» dal quarto autore/curatore in poi;
- tutti i titoli in corsivo;
- nomi di riviste fra virgolette basse « »;
- numeri di pagina sempre per esteso (es. pp. 250-253, non pp. 250-3);
- numeri di volume in numeri romani;
- "a cura di" prima dei curatori, sia nelle note sia in bibliografia;
- nella **bibliografia finale** (se richiesta), se lo stesso autore compare consecutivamente, il nome viene sostituito con *Id.*

---

## Limiti tecnici noti

### Ibid. / Ivi / Id. nelle note

Lo stile **non produce automaticamente** «Id.» nelle note a piè di pagina. Questo è un [limite strutturale](https://forums.zotero.org/discussion/85637/csl-style-subsequent-author-substitute) del linguaggio CSL (il formato usato da Zotero per tutti i suoi stili).

*Id.* funziona invece correttamente nella **bibliografia finale**, dove Zotero lo inserisce in automatico quando lo stesso autore compare in voci consecutive.

## Tipi di voce e campi da compilare

**NB** Il carattere "-" indica il valore specifico della fonte citata. Vengono qui specificati solo i casi di possibile ambiguità

### Monografia

Tipo voce: **Libro**

| Campo | Note |
|---|---|
| Autore | — |
| Titolo | — |
| Luogo | città di stampa |
| Editore | — |
| Data | anno |

> Erwin Panofsky, *Meaning in the Visual Arts*, New York, Anchor Books, 1955.

---

### Articolo in rivista

Tipo voce: **Articolo di rivista**

| Campo | Note |
|---|---|
| Autore | — |
| Titolo | — |
| Pubblicazione | nome della rivista |
| Volume | numero: lo stile lo converte in romano automaticamente |
| Fascicolo | numero progressivo (campo «n.») |
| Data | anno |
| Pagine | estensione completa dell'articolo |

> Mario Rossi, *Titolo dell'articolo*, «Rivista», n. 3, X, 2020, pp. 45-60: 52.

---

### Contributo in volume miscellaneo

Tipo voce: **Sezione di libro**

| Campo | Note |
|---|---|
| Autore | autore del contributo |
| Titolo | titolo del contributo |
| Titolo libro | titolo del volume |
| Curatori | — |
| Luogo | città di stampa |
| Editore | — |
| Data | anno |
| Pagine | estensione del contributo |

> Mario Rossi, *Titolo del contributo*, in *Titolo del volume*, a cura di Paola Bianchi, Firenze, Olschki, 2023, pp. 100-120: 105.

---

### Catalogo di mostra o volume di atti citato come opera intera

Tipo voce: **Libro** (senza autore, solo curatori)

Stessa compilazione di una monografia, con l'aggiunta obbligatoria in **Extra**:

```
Genre: catalogo della mostra
```
oppure
```
Genre: atti del convegno
```

Se il luogo dell'evento coincide con quello di stampa, basta il campo **Luogo** normale.

Se invece i due luoghi sono **diversi**, lascia vuoto il campo Luogo e aggiungi in Extra:

```
Archive Place: Empoli, Museo della Collegiata
Publisher Place: Firenze
```

E opzionalmente, se l'anno dell'evento differisce da quello di stampa:

```
Event Date: 2025
```

> *Empoli 1424. Masolino e gli albori del Rinascimento*, catalogo della mostra (Firenze, 2025), a cura di Andrea De Marchi, Firenze, Mandragora, 2025.

> *Empoli 1424. Masolino e gli albori del Rinascimento*, catalogo della mostra (Empoli, Museo della Collegiata, 2025), a cura di Andrea De Marchi, Firenze, Mandragora, 2025.

---

### Contributo in catalogo di mostra o in atti di convegno

Tipo voce: **Sezione di libro**

Stessa compilazione del contributo in volume miscellaneo, con l'aggiunta obbligatoria in **Extra** del campo Genre (e, se necessario, Archive Place / Event Date come sopra):

```
Genre: catalogo della mostra
```
oppure
```
Genre: atti del convegno
```

| Campo | Note |
|---|---|
| Autore | autore della scheda o del saggio |
| Titolo | titolo della scheda o del saggio |
| Titolo libro | titolo del catalogo o del volume degli atti |
| Curatori | curatori del volume (se presenti) |
| Luogo | città di stampa (o vuoto se diverso da luogo dell'evento) |
| Editore | — |
| Data | anno |
| Pagine | estensione del contributo |
| **Extra** | `Genre: catalogo della mostra` oppure `Genre: atti del convegno` + eventuali Archive Place, Publisher Place, Event Date |

> Andrea De Marchi, *Pacio Vesmias*, in  Empoli 1424. Masolino e gli albori del Rinascimento, catalogo della mostra (Empoli, Museo della Collegiata, 2025), a cura di Andrea De Marchi, Firenze, Mandragora, 2025, pp. 120-128: 124.

> Giovanni Leucci et al., *Non-destructive diagnosis at the Brancacci Chapel*, in Proceedings of the International Conference on Metrology for Archaeology and Cultural Heritage (IMEKO TC4), atti del convegno (Cosenza, 2022), IMEKO, 2022, pp. 521-525: 522.

---
