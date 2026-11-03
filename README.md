# 🎓 SVILUPPO DI UN'APPLICAZIONE BASATA SUL PARADIGMA MAAS CON APPLICAZIONE ALLA CITTA DI SCICLI 

> **Progettazione e implementazione di una piattaforma Mobility as a Service per l'ottimizzazione dei trasporti urbani, turistici e dei pagamenti digitali.**

## 📌 Panoramica del Progetto

Questo progetto rappresenta il lavoro sviluppo condotto per la mia **Tesi di Laurea Triennale in Informatica** presso l'**Università degli Studi di Roma Tor Vergata**, discussa nell'Anno Accademico 2025/2026.

L'obiettivo principale del progetto è stato affrontare la frammentazione geografica e la forte stagionalità turistica del comune di Scicli. La soluzione proposta è una piattaforma centralizzata in grado di digitalizzare l'offerta di mobilità, integrando il trasporto pubblico ordinario, i servizi su richiesta (DRT - Demand Responsive Transport), la gestione dei parcheggi tariffati e il monitoraggio in tempo reale della viabilità.

## 💡 L'Idea e la Metodologia

Il sistema è stato progettato seguendo rigorosamente i principi dell'ingegneria del software (modellazione UML: Use Case, Sequence Diagram, Activity Diagram, Class Diagram) per definire le interazioni di ben 6 attori di sistema (Utente Registrato, Utente Non Registrato, Turista, Admin Ente, Operatore, Funzionario Comunale).

## 🛠 Stack Tecnologico

Il prototipo è stato sviluppato adottando un approccio **Backend-as-a-Service (BaaS)** e un'architettura ibrida per garantire portabilità, scalabilità e reattività:

* **Frontend (PWA):** React Native, distribuito come Progressive Web App (PWA) per offrire un'esperienza multipiattaforma fluida e interfacce differenziate per ruolo (Cittadino, Turista, Admin, Operatore, Funzionario).
* **Backend Applicativo:** Java e Spring Boot per l'esposizione delle API REST, l'orchestrazione delle transazioni finanziarie e le logiche di validazione.
* **Infrastruttura Dati:** Il sistema sfrutta il paradigma più adatto in base alla tipologia di dato:
    * **Cloud Firestore (NoSQL) & Firebase Authentication:** Utilizzati per l'autenticazione, la gestione in tempo reale dei profili, le transazioni e la consultazione rapida in lettura dei dati di base del trasporto.
    * **H2 in memoria (SQL):** Database relazionale integrato in un modulo specifico per l'elaborazione complessa del formato GTFS (General Transit Feed Specification), superando i limiti del NoSQL nell'incrocio e calcolo relazionale dei percorsi.

## 📊 Funzionalità e Risultati dell'Esperimento

Il sistema sviluppato e testato con successo implementa:
* **Integrazione DRT:** Prenotazione di corse "a chiamata" per collegare le frazioni periferiche (es. Donnalucata, Sampieri) al centro, riducendo l'impatto ambientale nei periodi di bassa stagione.
* **Wallet e Pagamenti Digitali:** Un sistema client-server sicuro per l'acquisto di titoli di viaggio e il pagamento delle soste (strisce blu), gestito tramite chiavi di idempotenza per prevenire transazioni duplicate.
* **Viabilità Real-Time:** Pannello dedicato ai funzionari comunali per l'inserimento di ordinanze e il calcolo di percorsi alternativi in caso di eventi o chiusure stradali.
* **Gestione Flotta e Staff:** Dashboard per l'amministrazione dell'ente e per gli operatori a bordo (validazione biglietti tramite QR Code e aggiornamento stato corsa).

## 📂 Documentazione e Materiale

Tutta la documentazione ufficiale prodotta per la tesi è disponibile pubblicamente in questa repository. 

* 📄 [**Leggi l'Elaborato Completo (Tesi.pdf)**](docs/Tesi.pdf)
* 📊 [**Guarda le Slide della Discussione (PDF)**](presentation/Presentazione20minuti.html)

## 🔒 Nota sul Codice Sorgente

> **Il codice sorgente sviluppato per questa tesi sperimentale è attualmente mantenuto in una repository privata.**
> Questo approccio è stato scelto per tutelare i futuri sviluppi della piattaforma e la sicurezza delle logiche di integrazione dei pagamenti e dei dati territoriali. 
> Questa repository funge da vetrina pubblica per illustrare l'architettura, la metodologia ingegneristica seguita e i risultati finali del progetto.

