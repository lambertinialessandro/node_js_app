
# 🛠️ Istruzioni di Avvio del Servizio API

1. **Clonazione**: Clona il repository condiviso contenente l'API Node.js.

1. **Avvio**: Avvia il servizio API all'interno dell'ambiente di sviluppo (es. Codespace).

1. **Pubblicazione**: Rendi pubblico il link/URL generato da Codespace per l'accesso esterno all'API.

1. **Documentazione**: Analizza la documentazione esistente dell'API (End-point, corpi delle richieste, ecc.).


# 💻 Compiti della Single Page Application (SPA)
L'applicazione front-end deve essere sviluppata per consumare l'API e permettere le seguenti operazioni CRUD (Create, Read, Update).

1. **Lettura (Read)**
    **Visualizzazione Lista**: Visualizza tutti gli elementi restituiti dalla richiesta GET /users.

    **Dettaglio Utente**: Aggiungi un pulsante per ogni utente che permetta di accedere alle informazioni complete consumando l'API sulla rotta GET /users/{id}.

2. **Aggiornamento (Update)**
    **Modifica**: Aggiungi un pulsante "Modifica" a ogni utente.

    **Conferma**: I campi dell'utente devono diventare modificabili. La conferma della modifica deve contattare la rotta PUT /users/{id}.

    **Aggiornamento Vista**: Dopo la modifica, aggiorna l'elenco degli utenti.

3. **Creazione (Create)**
    **Form**: Aggiungi una form per permettere l'aggiunta di un nuovo utente.

    **Invio Dati**: Contatta la rotta POST /users per caricare l'utente.

    **Aggiornamento Lista**: Dopo la creazione, leggi la rotta della nuova risorsa creata (dall'header della risposta POST) e, consumando una richiesta GET su quella rotta, aggiorna la lista degli utenti.

4. **Aggiornamento Automatico della Vista**
    **Polling**: Mantieni aggiornata la vista degli utenti ogni 2 secondi.

    **Ottimizzazione**: Aggiorna la vista solamente per gli elementi che sono stati effettivamente modificati, creati o eliminati.

5. **Delete di uno user**


# 📄 **Tabella Informazioni API**

| Endpoint | Metodo | Descrizione             | Body Esempio                                     | Risposta Esempio               |
| -------- | ------ | ----------------------- | ------------------------------------------------ | ------------------------------ |
| `/users` | GET    | Ritorna la lista utenti | *N/A*                                            | `{ "users": [...] }`           |
| `/users` | POST   | Crea un nuovo utente    | `{ "name": "Mario", "email": "mario@test.com" }` | `{ "id": 1, "name": "Mario" }` |
|          |        |                         |                                                  |                                |
