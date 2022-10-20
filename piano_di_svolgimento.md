# Piano di svolgimento

In linea di massima le ore produttive che potremo utilizzare saranno 95 a testa. Tutte queste ore ammoneranno almeno a €12000.

# Obiettivi

- modulare la luminosità a seconda della quantità di persone o tipologia di entità?(Per noi sarebbe un obiettivo interessante ma secondario al modulare l'intensità solamente rilevando la presenza)

- Rilevamento guasti è da gestire solo tramite sensori di luminosità o non ci sono constraint in questo campo?

- Potrebbe aver senso dare la possibilità di impostare delle soglie di luminosità relativamente all'attivazione con presenza di entità?
- L'accensione programmata dell'illuminazione si potrebbe integrare con previsioni di eventi normali(alba e tramonto) ed anomali come eclissi.

- Potrebbe aver senso suddividere gli utenti in "gestore illuminazione pubblica", "installatore/manutentore", "Verificatore d'impianto" , altro
- Potrebbe aver senso creare una pagina disponibile ai "cittadini" dove questi possano (seguendo 2/3 passaggi) caricare una segnalazione di guasto?(obiettivo sencodario). Chiaramento l'inserimento manuale dei guasti da parte del manutentore è obiettivo primario.

- Potrebbe aver senso immaginare integrazioni future con sistemi di alimentazione/UPS vari nella gestione guasti/distribuzione dell'alimentazione?

- Potrebbe aver senso creare una dashboard/(api utilizzabile magari in futuro da pannellistica a led per mostrare ai cittadini i risparmi) che mostri i consumi ed i risparmi?

# Prima stesura architetturale

Visto l'**ambito critico** di operazione del prodotto software per noi i capostipiti nello sviluppo di questo progetto saranno: **alta modularità, alta scalabilità, alta resilienza e facile estensibilità** dello stesso.

L'architettura seguirà quindi i principi base di un sistema a microservizi che tenga conto di tutte queste importanti questioni.

## User stories / casi d'uso

## Utenti

Molteplici saranno gli utenti che utilizzeranno il sistema.

|Utente| utilizzi | Tipo di requisito|
|---|---|---|
|Semplice cittadino|Puà vedere una dashboard relativa all'illuminazione| Aggiuntivo|
|Gestore dell'illuminazione| Può impostare l'illuminazione| Obbligatorio|
|Gestore momentaneo| Può impostare l'illuminazione per un periodo limitato di tempo|Aggiuntivo |
|Installatore/manutentore|Aggiunge nuove sezioni illuminanti, risolve i guasti|Obbligatorio|
|Verificatore di impianto|Gira a controllare periodicamente se ci sono guasti ai corpi illuminanti| Obbligatorio|

## Servizi

|Servizio|Scopo|Tecnologia|
|---|---|---|
|Mqtt|Comunicazione delle componenti IoT |Mosquitto|
|Database|Stoccaggio a lungo termine dei dati per un'analisi futura degli stessi per prevenire guasti o risolvere situazioni ricorrenti| Postgres|
|Coordinatore|Coordinamento e gestione diretta degli apparati illuminanti| Python|
|ApiREST|Api Backend per la webapp e altri utilizzi futuri|Python, Flask|
|WebApp|Consente agli utenti(Definiti più avanti) di interfacciarsi con il sistema|VueJs o React|

