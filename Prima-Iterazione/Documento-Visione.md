# Documento di Visione

## 1. Introduzione
Il seguente elaborato si propone di in implementare un sistema, chiamato **City Explorer**, per la gestione degli spostamenti in città mediante traporto pubblico. L'obiettivo dell'applicazione è di facilitare gli utenti nei tragitti urbani permettendogli di pianificare in anticipo i percorsi migliori, secondo vari criteri, per raggiungere le proprie destinazioni. 
Per fare ciò il sistema gestisce le linee e le corse di diversi mezzi di trasporto pubblico (bus, tram, treno, metropolitana) e la rete stradale percorribile a piedi, così da collegare due punti qualsiasi della città, anche quando non coincidono con una fermata.

## 2. Formulazione del problema
I dati relativi al trasporto in Italia dimostrano che la densità delle auto rispetto al numero di abitanti è la più alta rispetto al resto d'Europa, con **701 auto ogni 1000 abitanti**, ben sopra la media europea di 578 (fonte ISTAT su dati Eurostat). Oltre il 90% dei veicoli sopracitati è legato a motori termici tradizionali.

Nel futuro si assisterà, forzatamente, ad un passaggio al trasporto pubblico, per necessità fisiche, economiche ed ecologiche.
Lo scopo dell'applicazione è **incentivare il cittadino all'utilizzo di mezzi comunitari**; allo stato attuale le informazioni sui trasporti sono sparse fra gestori diversi (bus, metro, treno), ognuno con orari e app propri, inoltre, non è chiaro come combinare più mezzi né quanto camminare fra una fermata e l’altra e soprattutto non si sa se una corsa è in ritardo o soppressa.
Il sistema risponde a quesrte necessità attraverso **un'interfaccia facile da usare, accessibile a tutti e sempre aggiornato, permettendogli di programmare i propri spostamenti velocemente, salvare le tratte usuali e ricevere informazioni su eventuali ritardi o malfunzionamenti dei trasporti in tempo reale ed utile per riprogrammare il proprio itinerario.**

## 3. Descrizione delle parti interessate
### 3.1 Obiettivi a livello utente
Gli utenti necessitano di un sistema che soddisfi i seguenti obiettivi:

- Amministratore del sistema: Gestire fermate, linee, corse e orari; importare la rete da file; gestire la mappa stradale; registrare ritardi e interruzioni del servizio; gestire gli account utente
- Utente non registrato: pianificare un itinerario; consultare linee, fermate e orari;
- Utente registrato: tutto ciò che può fare l'utente non registrato; salvare luoghi e itinerari preferiti; impostare preferenze di ricerca; iscriversi agli aggiornamenti delle linee di interesse.


## 4. Riepilogo delle caratteristiche del sistema
Il sistema dovrà possedere le seguenti caratteristiche:

- Gestione della rete di trasporto: fermate, linee, corse e orari dei diversi mezzi;
- Gestione della rete stradale e dei collegamenti pedonali tra fermate;
- Consultazione delle linee, delle fermate servite e dei prossimi passaggi;
- Pianificazione di un itinerario tra due punti qualsiasi della mappa (coordinate, fermata o luogo noto), secondo diversi criteri: tempo minimo, cambi  minimi, minor distanza a piedi;
- Pianificazione di un itinerario a più tappe, visitate nell'ordine stabilito dall'utente;
- Gestione di ritardi e interruzioni del servizio, di cui il calcolo dell'itinerario tiene conto;
- Gestione del profilo utente, salvataggio di itinerari e luoghi preferiti, iscrizione agli aggiornamenti delle linee di interesse.

## 5. Ambito e Iterazioni
Rispetto alle iterazioni di sviluppo:

- Prima Iterazione: modello della rete; pianificazione tra due punti con tratti a piedi stimati in linea d'aria; registrazione e autenticazione; gestione della rete da parte dell'amministratore; esportazione dell'itinerario in un formato visualizzabile su mappa.
- Successive Iterazioni: itinerari a più tappe; ritardi e interruzioni con ricalcolo dell'itinerario; iscrizione agli aggiornamenti e notifiche;Implementazione di un'interfaccia grafica

## 6. Vincoli
- Il sistema gestisce solo una città alla volta;
- Vengono gestiti dati reali per le mappe in un formato aperto;
- Per il testing vengono simulati i flussi di traffico, i malfunzionamenti e i ritardi.

## 7. Ulteriori requisiti
- Il calcolo di un itinerario deve essere svolto velocemente per permettere interattività;
- La rete dei mezzi, gli utenti e i loro dati sono salvati su file e ricaricati all'avvio del sistema;
- Imput non validi e file corrotti vengono gestiti senza interrompere il programma.
