# Esercitazione: Gestione File e Cartelle in Windows con CMD

**Materia:** Sistemi Operativi / Basi di Informatica  
**Strumenti:** Windows 10/11, Prompt dei comandi (CMD), Esplora File  
**Livello:** Principiante  
**Durata:** 20-30 minuti

---

### 🎯 Obiettivi didattici
Al termine di questa esercitazione saprai:
- Aprire e personalizzare il Prompt dei comandi
- Cambiare aspetto del terminale con `color` e `prompt`
- Creare un file di testo direttamente da CMD con il comando `copy con`
- Visualizzare la directory di lavoro corrente con `cd`
- Verificare i file creati da Esplora File
- Eliminare file con `del`
- Chiudere correttamente la sessione CMD

---

### 📋 Prerequisiti
- PC Windows con account utente standard
- Nessun software aggiuntivo richiesto

---

## Esercizio Guidato Passo-Passo

### a. Apri il Prompt dei comandi (CMD)

1. Premi i tasti `WIN + R` sulla tastiera
2. Digita `cmd` nella finestra "Esegui"
3. Premi `Invio` o clicca su OK
4. Si aprirà una finestra nera con scritta bianca - questo è il Prompt dei comandi

> **Alternativa:** Clicca su Start, scrivi `Prompt dei comandi` o `CMD` nella ricerca e aprilo.
> 
> **Tip:** Clicca con il tasto destro su CMD e seleziona "Esegui come amministratore" se vuoi permessi elevati (per questa esercitazione NON è necessario).

**Risultato atteso:** Vedi una riga simile a `C:\Users\Tuonome>`

---

### b. Personalizza il prompt con `prompt`

Il comando `prompt` ti permette di cambiare il testo che vedi prima di ogni comando.

1. Nel CMD digita esattamente questo comando:

```cmd
prompt INSERISCI COMANDO: 
```

2. Nota lo spazio finale dopo i due punti, è importante per la leggibilità
3. Premi `Invio`

**Risultato atteso:**
Il prompt classico `C:\Users\Tuonome>` scomparirà e vedrai:

```
INSERISCI COMANDO:
```

Da ora in poi, questo sarà il tuo nuovo prompt fino alla chiusura di CMD.

> **Extra per GitHub:** Per ripristinare il prompt predefinito, puoi usare `prompt $P$G` (mostra percorso + >)
> Altri parametri utili:
> - `$T` = ora corrente
> - `$D` = data corrente
> - `$P` = percorso corrente

---

### c. Cambia il colore del terminale: `color E1`

Il comando `color` cambia i colori di sfondo e testo del CMD.

Sintassi: `color SFONDO TESTO` (codici esadecimali da 0 a F)

1. Con il nuovo prompt, digita:

```cmd
color E1
```

2. Premi `Invio`

**Spiegazione:**
- `E` = Giallo chiaro (sfondo)
- `1` = Blu (testo)

**Risultato atteso:** Lo sfondo diventa giallo chiaro e il testo blu.

> **Tabella colori utili:**
> 0=Nero, 1=Blu, 2=Verde, 3=Azzurro, 4=Rosso, 5=Viola, 6=Giallo, 7=Bianco, 8=Grigio, 9=Blu chiaro, A=Verde chiaro, B=Azzurro chiaro, C=Rosso chiaro, D=Viola chiaro, E=Giallo chiaro, F=Bianco brillante
>
> Prova anche `color 0A` (classico hacker verde su nero) o `color F0` per resettare.

---

### d. Crea un file: `copy con materie.txt`

Ora creiamo un file di testo direttamente da CMD senza usare Blocco Note.

1. Digita il comando:

```cmd
copy con materie.txt
```

2. Premi `Invio`
3. Il cursore andrà a capo e lampeggerà senza prompt: sei in modalità scrittura
4. Digita le materie, una per riga. Esempio:

```
Informatica
Sistemi e Reti
Matematica
Italiano
Inglese
```

5. Quando hai finito, premi `CTRL + Z` (tieni premuto Ctrl e premi Z). Vedrai apparire `^Z`
6. Premi `Invio`

**Risultato atteso:**

```
Informatica
Sistemi e Reti
Matematica
Italiano
Inglese
^Z
        1 file copiati.
INSERISCI COMANDO:
```

> **Cosa succede:** `copy con` significa "copia dalla console (tastiera) al file materie.txt". `CTRL+Z` è il carattere di fine file (EOF) in Windows.

**Verifica rapida:** Puoi controllare che il file esista con:

```cmd
dir materie.txt
```

---

### e. Mostra la cartella corrente: `cd`

Il comando `cd` (Change Directory) senza parametri mostra la directory in cui ti trovi.

1. Digita:

```cmd
cd
```

2. Premi `Invio`

**Risultato atteso:** Vedrai il percorso completo, es:

```
INSERISCI COMANDO: cd
C:\Users\Tuonome
```

Questo è importante perché `materie.txt` è stato creato proprio qui.

> **Approfondimento:**
> - `cd` senza parametri = mostra cartella corrente
> - `cd ..` = torna indietro di una cartella
> - `cd Documenti` = entra nella cartella Documenti
> - `cd /d D:\` = cambia unità disco

Puoi anche vedere il contenuto dettagliato con:

```cmd
dir
```

Cercherai `materie.txt` nell'elenco.

---

### f. Da Esplora File visualizza la cartella creata

Verifichiamo con interfaccia grafica ciò che abbiamo fatto da riga di comando.

1. Premi `WIN + E` per aprire Esplora File
2. Nella barra degli indirizzi, incolla il percorso che hai visto al punto e. (es. `C:\Users\Tuonome`) e premi Invio
3. Cerca il file `materie.txt` tra i file
4. Fai doppio clic per aprirlo con Blocco Note e verifica che il contenuto sia quello inserito
5. Chiudi Blocco Note

> **Obiettivo didattico:** Capire che CMD ed Esplora File lavorano sugli stessi file reali. La riga di comando non è un mondo separato.

**Screenshot per GitHub (da aggiungere):**
```
[Inserire qui screenshot di Esplora File che mostra materie.txt]
```

---

### g. Elimina il file: `del materie.txt`

Torniamo al CMD (che hai lasciato aperto) per pulire.

1. Assicurati di essere nella cartella corretta (verifica con `cd`)
2. Digita:

```cmd
del materie.txt
```

3. Premi `Invio`

Se il comando va a buon fine, non vedrai alcun messaggio (in CMD, nessun messaggio = successo).

**Verifica eliminazione:**

```cmd
dir materie.txt
```

**Risultato atteso:**

```
Impossibile trovare il file C:\Users\Tuonome\materie.txt
```

Oppure:

```cmd
del materie.txt /p
```
Con `/p` ti chiederà conferma prima di eliminare: utile per evitare errori.

> **Attenzione:** `del` elimina definitivamente senza cestino. In Windows non esiste undo.

---

### h. Chiudi la sessione: `exit`

Hai completato l'esercitazione.

1. Digita:

```cmd
exit
```

2. Premi `Invio`

La finestra CMD si chiuderà automaticamente.

> **Comandi equivalenti:** Puoi anche chiudere cliccando sulla X in alto a destra, ma `exit` è la chiusura pulita e professionale.

---

## ✅ Checklist finale di verifica

- [ ] CMD aperto correttamente
- [ ] Prompt personalizzato in `INSERISCI COMANDO:`
- [ ] Colori cambiati con `color E1`
- [ ] File `materie.txt` creato con `copy con`
- [ ] Percorso verificato con `cd`
- [ ] File visualizzato in Esplora File
- [ ] File eliminato con `del`
- [ ] Sessione chiusa con `exit`

## 🧠 Domande di autovalutazione

1. Cosa succede se digiti `copy con` senza nome file?
2. Perché dopo `color E1` lo sfondo è giallo e non blu?
3. Qual è la differenza tra `del` e cancellare da Esplora File?
4. Come ripristineresti il prompt originale?

## 📦 Consegna su GitHub

Carica questo file `.md` nella repo con il file creato durante l'esercitazione (se richiesto dal docente, crea prima una copia di backup).

Comandi Git rapidi:

```bash
git add Gestione_file_e_cartelle_in_Windows.md
git commit -m "Aggiunta esercitazione CMD - Gestione file e cartelle"
git push origin main
```

---

**Autore:** Academy - Modulo Basi di Sistemi Operativi  
**Licenza:** CC BY-SA 4.0 - Uso didattico libero
