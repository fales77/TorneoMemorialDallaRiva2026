# 8° Memorial Matteo Dalla Riva – U12 (2014)

Pagina web ufficiale del torneo, realizzata per **U.S.D. Vanchiglia 1915**.  
Il file `index.html` è autosufficiente: non richiede connessione a internet, server o installazioni. Si apre direttamente con qualsiasi browser (Chrome, Firefox, Edge, Safari).

---

## Come è organizzata la pagina

La pagina rispecchia la struttura del torneo in tre fasi:

1. **Prima Fase** — Gironi A, B e C (4 squadre ciascuno, tutti contro tutti)
2. **Seconda Fase** — Gironi D ed E (le squadre qualificate + invitate)
3. **Fase Finale** — 8 partite di piazzamento dall'1° all'8° posto

---

## Come inserire i risultati

### Prima Fase (Gironi A, B, C)

Apri il file `index.html` con un editor di testo (Blocco Note, TextEdit, VS Code o simili).  
Cerca la tabella del girone che ti interessa, ad esempio il **Girone A**:

```html
<table id="gironeA">
    ...
    <tr><td class="date">16/05</td><td class="time">15:10</td><td class="incontro">Vanchiglia - Sisport</td><td class="result">-</td></tr>
```

Il risultato va inserito al posto del trattino `-` nell'ultima cella `<td class="result">`:

```html
<td class="result">2-1</td>
```

Stessa cosa per tutte le partite dei Gironi B e C.  
**Il formato è sempre: gol squadra di casa trattino gol squadra ospite**, senza spazi (es. `3-0`, `1-1`, `0-2`).

---

## Aggiornamento automatico — come funziona

La pagina contiene uno script che legge i risultati inseriti e aggiorna automaticamente i gironi delle fasi successive. Non devi fare nulla di manuale: basta salvare il file e ricaricare la pagina nel browser.

### Seconda Fase (Gironi D ed E)

I **Gironi D ed E sono sempre visibili** fin dall'inizio, con i segnaposto generici:

- `1° A` → primo classificato del Girone A
- `1° B` → primo classificato del Girone B  
- `1° C` → primo classificato del Girone C
- `Miglior 2°` → migliore secondo classificato tra i tre gironi

Non appena **tutte le 6 partite di un girone sono complete**, il segnaposto viene automaticamente sostituito dal nome reale della squadra qualificata.  
Il **Miglior 2°** viene calcolato solo quando tutti e tre i gironi A, B e C sono completi.

### Fase Finale

Stesso principio: il tabellone della Fase Finale è sempre visibile con i segnaposto `1° D`, `2° D`, `1° E`, `2° E` ecc.  
Quando tutte le 6 partite dei Gironi D ed E avranno un risultato, i nomi reali delle squadre compariranno automaticamente al posto dei segnaposto.

---

## Criteri di classifica

In caso di parità di punti tra due squadre, si applicano nell'ordine:

1. **Scontro diretto** (risultato della partita tra le due squadre a pari punti)
2. **Differenza reti** (gol fatti meno gol subiti)
3. **Gol fatti**

Il **Miglior secondo** tra i gironi A, B e C viene scelto confrontando: punti, poi differenza reti, poi gol fatti.

---

## Consigli pratici

- Inserisci i risultati **subito dopo la fine di ogni partita** per tenere la pagina sempre aggiornata.
- Dopo ogni modifica, **salva il file** e **ricarica la pagina** nel browser (tasto F5 o Cmd+R).
- Se condividi il file via link o su un sito, assicurati di caricare sempre la versione aggiornata.
- Non modificare i nomi delle squadre nelle tabelle dei Gironi A, B e C: lo script li usa per calcolare le classifiche.

---

## Struttura del file

```
index.html      → l'unico file necessario, contiene pagina e script
README.md       → questo documento
```

---

*U.S.D. Vanchiglia 1915 – Via Ernesto Ragazzoni 2, 10153 Torino*  
*Tel. 011 282551 | segreteria@usdvanchiglia.it*
