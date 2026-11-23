# Resoconto dell’uso dell’AI

## Sessione 1

- Ho chiesto all’AI di aiutarmi a rendere dinamica la pagina Programma con i file `eventi.json` e `sedi.json` e di aggiungere il meteo di Torino tramite l’API Open-Meteo.
- Con il supporto dell’AI ho completato i dati delle tre sedi e dei sei eventi, documentato le entità Evento e Sede in `dati/SCHEMA.md` e modificato `programma.html` per generare le schede con `fetch`.
- Ho verificato i casi principali: lista di eventi vuota, `sede_id` non valido e file JSON non disponibile. Nei casi previsti compaiono i messaggi corretti, compreso «Sede da definire».
- Ho iniziato ad aggiungere la sezione meteo in `info.html`. Durante il controllo ho notato che andava spostata all’interno di `<main>` e che mancava ancora il codice per leggere i dati dell’API.

## Sessione 2

- Ho chiesto all’AI di aiutarmi a completare e verificare la sezione meteo e i collegamenti tra eventi e sedi.
- Ho spostato la sezione «Meteo a Torino adesso» dentro `<main>` in `info.html` e completato la richiesta all’API Open-Meteo. La sezione mostra temperatura, velocità del vento e ora del dato, cita la fonte e chiarisce che si tratta del meteo attuale, non di una previsione per le date del festival.
- Ho verificato che, se la richiesta del meteo fallisce, appare un messaggio d’errore senza bloccare il resto della pagina.
- Ho controllato il caricamento degli eventi, il messaggio per la lista vuota, l’errore quando un file non è disponibile e il testo «Sede da definire» per un `sede_id` non valido. Ho anche verificato che cambiando il nome di una sede in `sedi.json` si aggiornino le schede dei relativi eventi.
- Ho completato e controllato `dati/SCHEMA.md`, con i campi e le chiavi delle entità, la relazione uno-a-molti, le quantità dei dati, le modalità di aggiornamento e il diagramma Mermaid.
- Ho verificato il sito con Live Preview: i file JSON vengono caricati tramite un server locale; la mappa può avere problemi in quell’ambiente, come indicato dal docente. Galleria e resto del sito funzionano.