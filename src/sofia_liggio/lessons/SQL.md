<!-- @format -->

# SQL: Structured Query Language

È un linguaggio di programmazione standard utilizzato per gestire e manipolare database relazionali. È stato progettato per eseguire una varietà di operazioni sui dati memorizzati nei database, tra cui:

- **Creare e modificare schemi di database**: Utilizzando comandi come CREATE TABLE, ALTER TABLE, ecc.
- **Inserire, aggiornare e cancellare dati**: Utilizzando comandi come INSERT INTO, UPDATE, DELETE.
- **Recuperare dati**: Utilizzando il comando SELECT per interrogare il database e ottenere i dati necessari.
- **Controllare l'accesso ai dati**: Gestire i permessi e i diritti degli utenti tramite comandi come GRANT e REVOKE.
- **Gestire transazioni**: Assicurare che le operazioni sui dati siano eseguite in modo atomico e consistente utilizzando BEGIN TRANSACTION, COMMIT, e ROLLBACK.

### Tipi di dati

- **Numerici**: INT, FLOAT, DECIMAL
- **Caratteri**: CHAR, VARCHAR
- **Date e Orari**: DATE, TIME, TIMESTAMP
- **Binari**: BLOB
- **Altri**: BOOLEAN, ARRAY

### Creazionee modifica della struttura del database

- `CREATE TABLE`: per creare nuove tabelle.
- `ALTER TABLE`: per modificare tabelle esistenti (ad es. aggiungere, modificare, o eliminare colonne).
- `DROP TABLE`: per eliminare tabelle.

### Manipolazione dei dati

- `INSERT INTO`: per inserire nuovi record in una tabella.
- `UPDATE`: per modificare i record esistenti.
- `DELETE`: per eliminare record.

### Interrogazione dei dati

- `SELECT`: per recuperare i dati. Supporta molte clausole e funzionalità:
- `WHERE`: filtra i risultati in base a condizioni specifiche.
- `JOIN`: combina righe di due o più tabelle.
- `GROUP BY`: raggruppa i risultati in base a una o più colonne.
- `HAVING`: filtra gruppi di risultati.
- `ORDER BY`: ordina i risultati.
- `LIMIT (o FETCH FIRST)`: limita il numero di risultati restituiti.

### Funzioni di aggregazione

- `COUNT`: conta il numero di righe.
- `SUM`: calcola la somma di una colonna numerica.
- `AVG`: calcola la media di una colonna numerica.
- `MIN e MAX`: trovano il valore minimo e massimo di una colonna.

### Gestione delle transazioni

- BEGIN TRANSACTION, COMMIT, ROLLBACK: per controllare transazioni, garantendo che i gruppi di operazioni vengano eseguiti in modo atomico.

### Vincoli di integrità

- `PRIMARY KEY`: identifica in modo univoco ogni record in una tabella.
- `FOREIGN KEY`: mantiene l'integrità referenziale tra tabelle.
- `UNIQUE`: garantisce che tutti i valori in una colonna siano unici.
- `NOT NULL`: impedisce che una colonna accetti valori NULL.
- `CHECK`: garantisce che i valori in una colonna soddisfino una specifica condizione.

### Indicizzazione

- `CREATE INDEX`: crea un indice su una o più colonne per migliorare la velocità delle query.
- `DROP INDEX`: elimina un indice.

### Viste

- `CREATE VIEW`: crea una vista, che è una query salvata.
- `DROP VIEW`: elimina una vista.

### Procedure e funzioni memorizzate

Molti RDBMS supportano le procedure memorizzate (stored procedures) e le funzioni:

- `CREATE PROCEDURE` e `CREATE FUNCTION`: per creare procedure e funzioni memorizzate.
- `EXEC`: per eseguire procedure memorizzate.

### Permessi e Sicurezza

- `GRANT`: assegna permessi a utenti o ruoli.
- `REVOKE`: rimuove permessi da utenti o ruoli.

### Ottimizzazioni delle query

- Uso efficace degli indici.
- Analisi dei piani di esecuzione (`EXPLAIN`).
- Ottimizzazione delle subquery e delle join.

# Postgre SQL

È un sistema di gestione di database relazionali (RDBMS) open-source avanzato che utilizza SQL come linguaggio di query. È noto per la sua robustezza, scalabilità e conformità agli standard SQL.

### Caratteristiche

- **Open Source**: PostgreSQL è gratuito e distribuito sotto la licenza PostgreSQL, che è molto permissiva.
- **Supporto per SQL Standard**: PostgreSQL è altamente conforme agli standard SQL, con molte estensioni.
- **Supporto per Transazioni ACID**: PostgreSQL garantisce le proprietà ACID (Atomicity, Consistency, Isolation, Durability), rendendolo molto affidabile per le applicazioni critiche.
- **Estendibilità**: Consente agli utenti di definire i propri tipi di dati, operatori e funzioni personalizzate.
- **Supporto per le query complesse**: Include supporto per join complessi, subquery, CTE (Common Table Expressions), e molto altro.
- **Supporto per dati geospaziali**: Attraverso l'estensione PostGIS, PostgreSQL può essere utilizzato per applicazioni geospaziali.

### Differenze e relazioni

1. SQL è il linguaggio utilizzato per interagire con i database relazionali, mentre PostgreSQL è uno specifico sistema di gestione di database relazionali che implementa e estende SQL.
2. SQL è standard e può essere utilizzato con vari RDBMS (come MySQL, Oracle, Microsoft SQL Server), mentre PostgreSQL è un'implementazione specifica di un RDBMS.
3. PostgreSQL utilizza SQL come linguaggio principale per le operazioni di database, ma offre anche estensioni e funzionalità specifiche che potrebbero non essere presenti in altri RDBMS.

Per ogni riga, abbiamo una chiave primaria: deve essere **univoca**. Ci permette di selezionare una riga della nostra tabella
Struttura di un database:

- CERCARE POLLING
- CONNESSIONE API E WEBSOCKET: QUEST'ULTIMA RIMANE SEMPRE APERTA, NON C'E' UNA RICHIESTA. I DATI VENGONO SCAMBIATI ATTRAVERSO DEGLI EVENTI CHE SI GENERANO (AD ES: INVIO MESSAGGIO)
- SQL è un linguaggio.
- MySQL implementa il linguaggio SQL e utilizza un sistema per manipolare un database.
- database relazionale: si tratta di tabelle dove puoi relazionare i dati tra loro con le primarykey, mettendo in collegamento le tabelle tra di loro, andando a salvare i dati di riferimento all'interno di una riga mettendo la primarykey di un elemento contenuto in un altra tabella. così sappiamo che tra quei dati c'è una relazione.
