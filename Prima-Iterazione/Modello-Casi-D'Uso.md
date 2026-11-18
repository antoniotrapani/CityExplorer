# Modello dei casi d'uso – City Explorer

## 1. Requisiti

City Explorer è un sistema software per la pianificazione degli spostamenti in città mediante trasporto pubblico. Il sistema deve calcolare, dati due punti qualsiasi della mappa della città e un orario, l'itinerario migliore che li collega, combinando corse dei mezzi pubblici (bus, tram, treno, metropolitana) e tratti percorribili a piedi.

Per la prima iterazione il sistema deve occuparsi dei seguenti aspetti:

- Registrazione di un nuovo utente e autenticazione di utenti registrati e amministratori.
- Pianificazione di un itinerario tra due punti qualsiasi della città, indicati come coordinate, fermata o luogo noto, a partire da un orario di partenza. Il sistema individua le fermate raggiungibili a piedi dalla partenza e dall'arrivo, stima i tratti a piedi in linea d'aria e restituisce l'itinerario migliore secondo il criterio scelto dall'utente (tempo totale minimo, numero minimo di cambi, minor distanza a piedi). La pianificazione è disponibile sia agli utenti registrati sia a quelli non registrati.
- Visualizzazione dell'itinerario calcolato come sequenza di tratte (mezzo, linea, fermate di salita e discesa, orari, durata; per i tratti a piedi distanza e durata).
- Gestione della rete di trasporto da parte dell'amministratore: inserimento, modifica ed eliminazione di fermate, linee, corse e relativi orari, con validazione dei dati inseriti.
- Gestione da parte dell'amministratore dell'elenco dei luoghi noti (nome e coordinate) utilizzabili come partenza o arrivo.
- Visualizzazione da parte dell'amministratore della rete di trasporto presente nel sistema.

---

## 2. Obiettivi e casi d'uso

Sono stati individuati gli attori principali a cui è destinato il sistema e gli obiettivi che intendono portare a termine; da queste informazioni sono stati ricavati i casi d'uso della prima iterazione.

Gli attori individuati sono:

- **Utente non registrato**: chiunque utilizzi l'applicazione senza essersi autenticato.
- **Utente registrato**: cittadino in possesso di un account. Può svolgere tutte le attività dell'utente non registrato.
- **Amministratore**: gestore della rete di trasporto e del sistema.

| Attore | Obiettivo | Caso d'uso |
|---|---|---|
| Utente non registrato | Creare un account per accedere alle funzionalità riservate agli utenti registrati | UC1: Registrazione |
| Utente registrato, Amministratore | Accedere al sistema con le proprie credenziali | UC2: Autenticazione |
| Utente non registrato, Utente registrato | Calcolare l'itinerario migliore per spostarsi tra due punti della città a partire da un certo orario, secondo un criterio scelto | UC3: Pianificazione itinerario |
| Amministratore | Inserire una nuova fermata alla rete | UC4: Inserimento fermate |
| Amministratore | Eliminare una fermata alla rete | UC5: Eliminazione fermate |
| Amministratore | Inserire una linea, con il tipo di mezzo e la sequenza ordinata di fermate per ciascuna direzione | UC5: Inserimento linea |
| Amministratore | Eliminare una linea, dato il nome | UC6: Eliminazione linea |
| Amministratore | Inserire le corse di una linea | UC7: Inserimento corse |
| Amministratore | Eliminare le corse di una linea | UC8: Eliminazione corse |
| Amministratore | Inserire luoghi noti utilizzabili nella ricerca | UC9: Inserimento luoghi noti |
| Amministratore | Eliminare luoghi noti utilizzabili nella ricerca | UC10: Eliminazione luoghi noti |
| Amministratore, Utente Registrato, Utente non registrato | Visualizzare le informazioni complessive della rete: visualizza l'intera mappa con  fermate, linee e corse presenti nel sistema | UC11: Visualizzazione rete di trasporto |
