# Esercizio guidato — Gestione di file e cartelle in Ubuntu

## Obiettivo

Eseguire una sequenza di operazioni di base sulla struttura delle cartelle utilizzando il gestore dei file di Ubuntu.

L'attività verifica la capacità di:

- creare cartelle;
- creare sottocartelle;
- rinominare elementi;
- spostare una cartella all'interno di un'altra;
- creare un file;
- controllare la struttura finale.

## Passaggio 1 — Creare Esercizi

Apri la cartella **Documenti** e crea la sottocartella:

```text
Esercizi
```

Struttura:

```text
Documenti
└── Esercizi
```

## Passaggio 2 — Creare Alfa e Beta

Apri `Esercizi` e crea:

```text
Alfa
Beta
```

Struttura:

```text
Documenti
└── Esercizi
    ├── Alfa
    └── Beta
```

## Passaggio 3 — Rinominare le cartelle

Rinomina:

```text
Alfa → Nazioni
Beta → Capitali
```

Struttura:

```text
Documenti
└── Esercizi
    ├── Nazioni
    └── Capitali
```

## Passaggio 4 — Spostare Capitali

Sposta la cartella `Capitali` dentro `Nazioni`.

Risultato:

```text
Documenti
└── Esercizi
    └── Nazioni
        └── Capitali
```

## Passaggio 5 — Creare test.txt

Apri:

```text
Documenti/Esercizi/Nazioni/Capitali
```

e crea il file:

```text
test.txt
```

Non è necessario inserire testo nel file.

## Verifica finale

La struttura completa deve essere:

```text
Documenti
└── Esercizi
    └── Nazioni
        └── Capitali
            └── test.txt
```

### Checklist

- [ ] `Esercizi` è dentro `Documenti`.
- [ ] Sono state create `Alfa` e `Beta`.
- [ ] `Alfa` è stata rinominata `Nazioni`.
- [ ] `Beta` è stata rinominata `Capitali`.
- [ ] `Capitali` è dentro `Nazioni`.
- [ ] `test.txt` è dentro `Capitali`.
- [ ] La struttura finale è corretta.

## Estensione facoltativa

Ripeti l'esercizio utilizzando il **Terminale** di Ubuntu invece del gestore grafico dei file.

Individua quali comandi useresti per:

```text
creare una directory
rinominare una directory
spostare una directory
creare un file vuoto
```

L'obiettivo è comprendere che interfaccia grafica e terminale sono due strumenti diversi per lavorare sulla stessa struttura del file system.
