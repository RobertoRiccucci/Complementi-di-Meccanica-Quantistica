# Complementi di Meccanica Quantistica

Appunti in LaTeX pensati come **complemento** al testo di L. E. Ballentine, *Quantum Mechanics: A Modern Development* (World Scientific, 1998), e non come una trattazione autonoma della meccanica quantistica.

**PDF compilato:** [`build/Complementi_MQ.pdf`](build/Complementi_MQ.pdf)

## Il progetto

Il Ballentine è il riferimento seguito per l'impostazione generale della teoria. Su diversi argomenti, però, il libro tace oppure procede per una strada diversa da quella vista a lezione:

- a volte manca la **motivazione fisica** da cui si parte in aula;
- a volte il risultato c'è, ma è ottenuto con un **metodo differente**;
- a volte l'argomento **non compare affatto**.

Queste note raccolgono esattamente questo scarto.

Il materiale proviene dai corsi di Meccanica Quantistica tenuti dal prof. **Ettore Vicari** (Università di Pisa) e dal prof. **Vittorio Giovannetti** (Scuola Normale Superiore).

### Convenzione di lettura

> Di ogni argomento si dà per acquisito quanto il Ballentine espone fino a quel punto.

Definizioni, notazioni e dimostrazioni già presenti nel testo non vengono ripetute: quando servono, si rimanda al libro. Questi appunti quindi **non si leggono da soli, ma accanto al Ballentine**.

## Contenuti

| Capitolo | Argomento |
|---|---|
| Prefazione | Scopo e convenzioni degli appunti |
| 1 | Introduzione agli assiomi — esperimento di Stern-Gerlach e interpretazione dei risultati |
| 2 | Sistemi composti - Prodotto tensore - Matrice densità di un sistema composto|
| 3 | Descrizione quantistica dello stern-gerlach - Spazio $\mathcal{H}_{\text{int}}$ - Ricollimazione del fascio|
| 4 | Oscillatore armonico: soluzione analitica — base degli impulsi |

Il lavoro è in corso (versione attuale: **v0.1**); altri capitoli verranno aggiunti man mano.

## Struttura della repository

```
Complementi_MQ/
├── Complementi_MQ.tex      # File principale: frontespizio e inclusione dei capitoli
├── chapters/
│   ├── template.tex        # Preambolo: classe scrbook, pacchetti, macro e stile
│   ├── preface.tex         # Prefazione
│   ├── capitolo_1.tex      # Cap. 1 – Introduzione agli assiomi
│   ├── capitolo_2.tex      # Cap. 2 – Oscillatore armonico
│   └── bibliografia.bib    # Bibliografia (biblatex/biber)
├── foto/                   # Immagini (frontespizio e figure)
└── build/                  # Output di compilazione (viene versionato solo il PDF)
```

## Compilazione

Serve una distribuzione TeX recente (TeX Live o MacTeX) con `latexmk` e `biber`. Dalla radice della repository:

```bash
latexmk -pdf -outdir=build Complementi_MQ.tex
```

Il PDF viene generato in `build/`. I file ausiliari sono esclusi dal versionamento tramite `.gitignore`.

In alternativa si può usare l'estensione **LaTeX Workshop** di VS Code, impostando `build` come cartella di output.


