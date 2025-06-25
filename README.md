# 🎬 Sistema di prenotazione posti per sala cinematografica

## 📌 Introduzione

Questo progetto rappresenta un sistema di prenotazione posti per una sala cinematografica.

Un processo su una macchina **server** gestisce una mappa di posti per una sala. Ciascun posto è caratterizzato da:

- Un numero di **fila**
- Un numero di **poltrona**
- Un **flag** indicante se il posto è già stato prenotato o meno

Il server accetta e processa richieste di prenotazione da uno o più **client** (anche su macchine diverse).

Il client offre all'utente le seguenti funzionalità:

1. 🔍 **Visualizzare la mappa** dei posti per individuare quelli disponibili.
2. 📨 **Inviare al server** l’elenco dei posti da prenotare (identificati tramite `numero di fila` e `numero di poltrona`).
3. ✅ **Ricevere conferma** dal server con l’avvenuta prenotazione e un `codice di prenotazione`.
4. ❌ **Disdire una prenotazione** esistente fornendo il relativo codice.

🧵 Il server gestisce le richieste dei client in modo **concorrente**, assegnando un **thread dedicato** a ogni client al momento della connessione.
