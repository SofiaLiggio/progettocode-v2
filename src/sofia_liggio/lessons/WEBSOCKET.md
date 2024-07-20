<!-- @format -->

# WebSocket: cosa è e come funziona

È una tecnologia che fornisce un canale di comunicazione simultanea su una singola connessione TCP. È progettata per essere implementata nei browser web e nei server web, ma può essere utilizzata anche da qualsiasi applicazione client/server.

I dati vengono scambiati simultaneamente in entrambe le direzioni e vengono visualizzati rapidamente.
Per richiamare un sito web, il client deve prima inviare una richiesta al server tramite HTTP. Solo allora il server può fornire le risposte e i contenuti desiderati. Si tratta di un semplice modello di richiesta e risposta, che spesso implica un notevole ritardo tra una e l’altra.

### A cosa serve

WebSocket è particolarmente utile in scenari dove è necessaria una comunicazione bidirezionale in tempo reale. Alcuni esempi di applicazioni includono:

- **Applicazioni di chat**: permette di inviare e ricevere messaggi istantaneamente tra utenti.

- **Notifiche in tempo reale**: per inviare notifiche push ai client in tempo reale senza dover fare polling (= verificare la presenza di nuovi dati o eventi) continuo sul server.

- **Giochi online**: dove è fondamentale la comunicazione in tempo reale tra il server e i vari client.

- **Aggiornamenti di dati in tempo reale**: qualsiasi scenario dove i dati devono essere aggiornati in tempo reale.

- **Collaborazione in tempo reale**: strumenti di collaborazione dove più utenti possono vedere e modificare un documento simultaneamente per sincronizzare i cambiamenti in tempo reale.

### Come funziona

È sufficiente che il client apra la connessione a un server web. La connessione tra client e server viene stabilita con un _handshake_ HTTP, dove un client invia una richiesta al server per aggiornare la connessione a WebSocket. Se il server accetta, la connessione viene stabilita.

Dopo l’handshake, il canale di _comunicazione_ rimane praticamente aperto. Il server può diventare attivo da solo e fornire al client tutte le informazioni senza attendere le richieste. Se ci sono nuove informazioni lato server, il server le comunica al client senza che venga emessa una richiesta extra lato client. La comunicazione continua finché la connessione non viene chiusa da una delle parti.
I dati sono trasmessi in forma di _frame_ (testo o dati binari).

### Vantaggi

Viene utilizzato ogni volta che è necessaria una connessione rapida, come in una live chat di assistenza, news ticker, ticker di borsa, messenger e giochi in tempo reale.
Anche i social media possono trarne vantaggio consentendo collegamenti in diretta con altre persone e l’invio e la ricezione di messaggi immediati.
I tempi di caricamento sono quindi più veloci e non bisogna sempre attendere l'intero caricamento di una pagina HTML completa.

# Socket.IO

È una libreria che permette la comunicazione in tempo reale tra i browser web e i server. Utilizza il protocollo WebSocket quando possibile, ma ha la capacità di ricorrere ad altri metodi di trasporto se WebSocket non è supportato dal client o dal server.

Socket.IO è composta da due parti:

- **Client-side library**: che gira nel browser.
- **Server-side library**: che gira su Node.js.

### A cosa serve

È utilizzato per costruire applicazioni che richiedono comunicazione bidirezionale in tempo reale, come:

- chat in tempo reale
- notifiche in tempo reale
- giochi online
- collaborazione in tempo reale
- monitoraggio in tempo reale
- stream di dati

### Funzionalità

- **Eventi**: emette e ascolta eventi sia sul lato client che server, facilitando la comunicazione e la gestione dello stato applicativo.

- **Rooms and namespaces**: crea "stanze" (rooms) e "spazi di nomi" (namespaces) per organizzare e suddividere la comunicazione in diverse parti logiche.

- **Scalabilità**: supporta la scalabilità su più server tramite adattatori che permettono di sincronizzare i messaggi tra diversi processi o server.

- **Fallbacks automatici**: gestisce automaticamente il fallback se WebSocket non è disponibile, garantendo che la connessione rimanga aperta e attiva.

### Vantaggi

- **Affidabilità**: grazie ai fallback automatici, la connessione è sempre mantenuta attiva.
- **Facilità d'uso**: fornisce un'API semplice e intuitiva per lavorare con la comunicazione in tempo reale.
- **Compatibilità**: funziona su tutti i principali browser e può essere utilizzato in vari ambienti server.
- **Scalabilità**: supporta la scalabilità su più server tramite adattatori, rendendolo adatto per applicazioni di grandi dimensioni.
