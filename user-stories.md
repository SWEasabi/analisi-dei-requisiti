# Descrizione testuale

## Obiettivi obbligatori

- **Rilevamento della presenza di persone** in prossimità della fonte luminosa: attraverso sensori eterogenei (bluetooth, IR, videocamere, ecc.) il sistema rileva la presenza di persone in un’area della città gestita dal sistema e attiva le luci di conseguenza.

- Aumento/riduzione dell’intensità luminosa: il sistema deve essere in grado di comunicare attraverso un protocollo IoT l’aumento o la riduzione dell’intensità luminosa emessa da uno specifico impianto di illuminazione, permettendo una regolazione singola o per l’intera via/piazza (area coperta dal servizio).

- Rilevamento automatico del guasto di un impianto di illuminazione: il sistema deve rilevare ogni eventuale malfunzionamento dell’impianto di illuminazione, notificando il gestore ed aprendo un ticket di assistenza su una piattaforma esterna che permetta di identificare la località del guasto.

- Segnalazione manuale del guasto di un impianto di illuminazione: il sistema deve permettere di inserire manualmente un nuovo guasto ad un impianto di illuminazione.

- Inserimento e gestione di un impianto luminoso: il sistema deve permettere al gestore
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
2. collegamento di un impianto luminoso ai dati derivanti da un sensore (modalità automatica)
4. aumento o riduzione globale dell’intensità luminosa da parte di un operatore o tramite dati di un
sensore
6. Gestione ticketing guasti
---


## Utenti ed attori

- Utente non loggato
- Utente gestore
- Utente Installatore/manutentore
- Lampadina
- Sensore guasti
- Sensore dati
- Sistema ticketing
- Sistema di _DB_

## Storie _utente non registrato_

- utente non loggato può loggarsi

## Storie _utente gestore_

- Utente gestore può regolare l'intensità luminosa di un singolo lampione
- Utente gestore può regolare l'intensità di molteplici lampioni

## Storie _utente installatore/manutentore_

- Utente installatore può creare nuovi account
- Utente installatore può aggiungere al sistema un nuovo lampione
- Utente installatore può aggiungere al sistema un nuovo sensore
- Utente installatore può aggiungere al sistema aree di gestione illuminazione

## Storie _lampadina_

- Lampadina può cambiare la sua luminosità

## Storie _sensore guasti_

## Storie _sensore dati_
- Sensore dati invia al database il valore dell'intensità luminosa
- Sensore dati invia al sistema l'eventuale presenza di entità

## Storie _sistema ticketing_
