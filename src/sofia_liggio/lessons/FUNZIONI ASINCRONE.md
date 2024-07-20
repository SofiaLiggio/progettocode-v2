<!-- @format -->

# Funzioni Asincrone

Permettono di gestire operazioni che richiedono tempo senza bloccare l'esecuzione del programma.

## Vantaggi e svantaggi della Programmazione Asincrona

### Vantaggi

- **Efficienza**: Le operazioni che richiedono tempo non bloccano l'esecuzione del programma.
- **Responsività** : Applicazioni come le interfacce utente rimangono responsive anche durante operazioni intensive.
- **Parallelismo**: Consente di eseguire più operazioni simultaneamente senza dover utilizzare threading esplicito.

### Svantaggi

- **Complessità**: Può essere più difficile da comprendere e da gestire rispetto alla programmazione sincrona.
- **Debugging**: Il debugging di codice asincrono può essere più complicato.
- **Gestione degli errori**: Gli errori nelle operazioni asincrone possono propagarsi in modi inattesi.

## Cosa è una Promise

È un oggetto in JavaScript e TypeScript che rappresenta il completamento o il fallimento di un'operazione asincrona e il suo valore risultante.
Per creare una Promise, si utilizza il costruttore _Promise_, che prende una funzione con due parametri: _resolve_ e _reject_.
Le Promises permettono di:

- lavorare con operazioni asincrone in modo più semplice e leggibile rispetto ai callback, riducendo il rischio di "callback hell" e migliorando la gestione degli errori.
- concatenare più operazioni asincrone in modo lineare utilizzando then.
- con async/await, il codice asincrono diventa più leggibile e simile al codice sincrono.

### Stati di una Promise

Una Promise può trovarsi in uno dei seguenti stati:

- **Pending**: La Promise è in attesa, cioè non è stata ancora risolta o rifiutata.
- **Fulfilled**: La Promise è stata risolta con successo e ha un valore.
- **Rejected**: La Promise è stata rifiutata e ha un motivo per il fallimento.

### Utilizzo delle Promises

Si usano i metodi _then_ e _catch_:

- **then**: viene chiamato quando la Promise è risolta con successo.
- **catch**: viene chiamato quando la Promise è rifiutata.

### Async/Await

Forniscono una sintassi più semplice e leggibile.

- **async**: rende una funzione asincrona e fa in modo che ritorni una Promise.
- **await**: sospende l'esecuzione della funzione asincrona fino a quando la Promise non è risolta o rifiutata.

## Callback hell

Si verifica quando ci sono più chiamate asincrone annidate una dentro l'altra, rendendo il codice difficile da leggere e mantenere. Questo problema era particolarmente comune in JavaScript prima dell'introduzione delle Promises e delle parole chiave _async/await_, che hanno migliorato di molto la leggibilità.
