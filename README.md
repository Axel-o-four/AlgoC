# Progetto di Elementi di Ingegneria dei Linguaggi di Programmazione
**Sabato Iaquino (Matricola 0512123029) a.a. 2025/2026**
**Corso di Elementi di Ingegneria dei Linguaggi di Programmazione tenuto dal Professore Gennaro Costagliola**

# AlgoC - Algorythms in C

### Cos'è AlgoC?

**AlgoC** è un **linguaggio di programmazione** per scrivere codice con una **sintassi vicina allo pseudocodice** utilizzato nella specifica degli algoritmi: l'obiettivo è **ridurre la distanza** tra la **rappresentazione teorica** di un algoritmo e la sua **esecuzione pratica**. Un programma in AlgoC può essere tradotto automaticamente in codice C e compilato in un eseguibile.

Il progetto implementa un compilatore completo, formato da:

- **Grammatica Lark** per generare automaticamente il parser, contenuta in grammar.lark.
- **Analisi lessicale e sintattica** tramite lexer e parser Lark, contenuta in ast_generator.py.
- **Costruzione di AST**, contenuta in ast_generator.py, tramite i nodi definiti come classi Python, contenuti in ast_nodes.py.
- **Analisi semantica su AST**, contenuta in code_generator.py, tramite l’uso di symbol table a livello singolo, contenuta in symbol_table.py.
- **Generazione del codice C dall’AST**, contenuta in code_generator.py.
- **Driver generale** del compilatore per compilare codice automaticamente da AlgoC a C ad eseguibile tramite gcc, oppure svolgere la sola compilazione da AlgoC a C.

---

### Caratteristiche principali

- **Compilazione automatica**: dal codice AlgoC si genera codice C ottimizzato e compilabile.
- **Supporto all'uso di array**: sono supportati gli array di `int`, `real`, `char` e `boolean`.
- **Strutture di controllo semplificate**: le strutture di controllo vengono ottimizzate per l'iterazione sugli elementi di una struttura dati.
- **Assegnazione semplificata**: l'assegnazione viene svolta tramite l'operatore `<-`.
- **Operatori semplificati**: viene rimosso il supporto agli operatori bitwise, di poca utilità in questo campo, e viene semplificato l'uso degli operatori, divisi in:
  - **Aritmetici**: `+`,`-`,`*`,`/` e `%`.
  - **Relazionali**: `<`, `>`, `<=`, `>=`, `=` e `<>`.
  - **Logici**: `|`, `&` e `!`.
- **Passaggi commentabili**: è possibile aggiungere commenti in ogni punto del codice racchiudendo il testo tra `%%`.

### Struttura di progetto

AlgoC/\
├ README.md # Questo file\
├ examples/\
| ├ array.algoc # Esempio programma con calcolo e restituzione di un valore\
| ├ calculator.algoc # Esempio di programma con interfaccia a scelta e input e output utente\
| └ whoami.algoc # Esempio di programma con input e output utente\
├ doc/\
| ├ AlgoC - Documentazione tecnica.pdf # Documentazione tecnica di AlgoC in formato PDF\
| └ AlgoC - Documentazione tecnica.pages # Documentazione tecnica di AlgoC in formato Apple Pages\
└ src/\
  ├ algoc.py # Driver generale del compilatore\
  ├ ast_generator.py # Generatore AST con lexer e parser\
  ├ ast_nodes.py # Definizione dei nodi dell'AST\
  ├ code_generator.py # Generazione del codice con analisi semantica\
  ├ grammar.lark # Grammatica in EBNF per Lark\
  └ symbol_table.py # Definizione di simbolo e tabella dei simboli\
