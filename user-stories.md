# Descrizione testuale

## Obiettivi obbligatori

1. **Rilevamento della presenza di persone** in prossimità della fonte luminosa: attraverso sensori eterogenei (bluetooth, IR, videocamere, ecc.) il sistema rileva la presenza di persone in un’area della città gestita dal sistema e attiva le luci di conseguenza.

2. Aumento/riduzione dell’intensità luminosa: il sistema deve essere in grado di comunicare attraverso un protocollo IoT l’aumento o la riduzione dell’intensità luminosa emessa da uno specifico impianto di illuminazione, permettendo una regolazione singola o per l’intera via/piazza (area coperta dal servizio).

3. Rilevamento automatico del guasto di un impianto di illuminazione: il sistema deve rilevare ogni eventuale malfunzionamento dell’impianto di illuminazione, notificando il gestore ed aprendo un ticket di assistenza su una piattaforma esterna che permetta di identificare la località del guasto.

4. Segnalazione manuale del guasto di un impianto di illuminazione: il sistema deve permettere di inserire manualmente un nuovo guasto ad un impianto di illuminazione.

5. Inserimento e gestione di un impianto luminoso: il sistema deve permettere al gestore
l’inserimento di nuovi impianti luminosi e il loro inserimento o rimozione all’interno di un’area coperta dal servizio.

## Obiettivi secondari

- modulare la luminosità a seconda della quantità di persone o tipologia di entità;

- Rilevamento tipologia guasti (Guasti locali o distribuiti, guasti a sistemi di alimentazione);

- Preset di illuminazione per le varie situazioni

- integrazione con previsioni di eventi normali(alba e tramonto) ed anomali come eclissi;

- Gestione multi utente ("gestore illuminazione pubblica", "installatore/manutentore", "Verificatore d'impianto" , altro)

- Pagina disponibile ai "cittadini" dove questi possano (seguendo 2/3 passaggi, ad esempio caricando un'immagine del guasto) caricare una segnalazione di guasto.

## Ottica di espansione futura
- Integrazioni future con sistemi di alimentazione/UPS vari nella gestione guasti/distribuzione dell'alimentazione;

- Api pubblica regolamentata utilizzabile in futuro da pannellistica a led per mostrare ai cittadini i risparmi o altro.



# Analisi

----
7. inserimento e gestione di un impianto luminoso
8. creazione, modifica e rimozione di nuove aree illuminate
9. tracciamento delle intensità luminose di ogni impianto.
10. Rilevamento della presenza in un’area illuminata e aumento automatico dell’intensità
luminosa
---


## Utenti ed attori

- Utente non loggato
- Utente gestore
- Utente Installatore/manutentore
- Lampadina
- Sensore guasti
- Sistema ticketing
- Sistema di _DB_

## Storie _utente non loggato

- utente non loggato può loggarsi

## Storie _utente gestore_

- Utente gestore può regolare l'intensità luminosa di un singolo lampione

- Utente gestore può regolare l'intensità di molteplici lampioni

- Utente gestore può emettere un ticket di guasto su un impianto

- Utente gestore può emettere un ticket di guasto su un lampione

## Storie _utente installatore/manutentore_

- Utente installatore può creare nuovi account

- Utente installatore può aggiungere un nuovo sensore al sistema

- Utente installatore può aggiungere un nuovo lampione al sistema

## Storie _lampadina_

- Lampadina può cambiare la sua luminosità

## Storie _sensore guasti_

## Storie _sistema ticketing_

- Sistema di ticketing riceve un ticket
