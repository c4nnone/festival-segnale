# Scheda dati — Segnale

## Entità e campi

### Evento

| Campo | Tipo | Esempio |
|---|---|---|
| `id` | numero intero | `1` |
| `titolo` | testo | `"Lettere in movimento"` |
| `data` | data in formato `AAAA-MM-GG` | `"2026-06-12"` |
| `orario` | testo, formato `HH:MM` | `"10:00"` |
| `categoria` | testo | `"Incontro"` |
| `descrizione` | testo | `"Come cambia un messaggio quando cambiano le lettere?"` |
| `immagine` | percorso di un file | `"assets/lettere-in-movimento.svg"` |
| `immagine_alt` | testo alternativo | `"Lettere geometriche disposte su una griglia"` |
| `sede_id` | numero intero | `1` |

### Sede

| Campo | Tipo | Esempio |
|---|---|---|
| `id` | numero intero | `1` |
| `nome` | testo | `"Officina Nord — Sede centrale"` |
| `indirizzo` | testo | `"Corso Duca degli Abruzzi 24, Torino"` |

## Chiavi e relazione

La chiave primaria di ciascuna entità è `id`: è un numero univoco all'interno dell'entità e rimane stabile.

Una sede può ospitare più eventi; ogni evento si svolge in una sede. `Evento.sede_id` fa riferimento a `Sede.id`.

## Quantità e aggiornamento

Il progetto contiene sei eventi e tre sedi. Chi aggiorna il sito modifica i file JSON nella repository e pubblica le modifiche.

## Che cosa mostra la pagina

La pagina Programma legge gli eventi e le sedi dai due file JSON e mostra per ogni evento titolo, data, orario, categoria, descrizione, immagine e nome della sede.

## Schema Evento–Sede

```mermaid
erDiagram
    SEDE ||--o{ EVENTO : ospita
    SEDE {
        int id PK
        string nome
        string indirizzo
    }
    EVENTO {
        int id PK
        string titolo
        date data
        string orario
        string categoria
        string descrizione
        string immagine
        string immagine_alt
        int sede_id FK
    }
    ```