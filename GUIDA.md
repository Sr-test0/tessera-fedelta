# SR Art - Tessera Fedeltà: Guida Completa

**App live:** https://tessera-fedelta.vercel.app

---

## ACCESSO RAPIDO

| Chi sei | Cosa fai |
|---|---|
| Cliente | Vai su https://tessera-fedelta.vercel.app → scheda "La mia tessera" → inserisci la tua email |
| Admin | Vai su https://tessera-fedelta.vercel.app → clicca "Pannello Admin" → inserisci la password |

---

## PARTE 1 — ESPERIENZA CLIENTE

### Come accedere alla propria tessera

1. Apri il browser e vai su **https://tessera-fedelta.vercel.app**
2. Sei già nella scheda "La mia tessera" (quella di default)
3. Inserisci la tua **email** nel campo "La tua email..."
4. Clicca il pulsante **Cerca**

### Cosa vedi dopo la ricerca

- **Tessera digitale dorata** con il tuo nome, il codice tessera e i punti attuali
- **10 cerchi colorati** che rappresentano i tuoi punti:
  - Cerchi grigi = punti non ancora raggiunti
    - Cerchi marroni = punti accumulati
      - Cerchio 5 con scritta "tazza" = premio tazza (si illumina in oro quando raggiunto)
        - Cerchio 10 con scritta "set" = premio set 3 pezzi (si illumina in oro quando raggiunto)
        - **Contatore "ancora X per..."** che ti dice quanti punti mancano al prossimo premio
        - **Statistiche**: punti totali guadagnati da sempre + numero premi già ricevuti
        - **Storico movimenti**: lista di tutti gli acquisti con data e punti guadagnati

        ### Regola punti

        - Ogni **10 euro spesi** = **1 punto**
        - A **5 punti** → Premio: **Tazza SR Art**
        - A **10 punti** → Premio: **Set 3 pezzi SR Art**
        - Dopo ogni premio i punti **ripartono da zero**

        ### Esempio pratico (cliente)

        Hai comprato per 45 euro → guadagni 4 punti. Il prossimo acquisto da almeno 10 euro ti darà il 5° punto e sblocchi la tazza!

        ---

        ## PARTE 2 — PANNELLO ADMIN

        ### Come accedere al pannello admin

        1. Vai su **https://tessera-fedelta.vercel.app**
        2. Clicca su **"Pannello Admin"** in alto a destra
        3. Si apre una finestra di accesso → inserisci la password: **srart2024**
        4. Clicca **Entra**

        > La sessione admin rimane attiva finché non chiudi il browser.

        ### Il pannello ha 3 sezioni:

        ---

        ### SEZIONE 1 — "Aggiungi Punti" (uso quotidiano)

        **Usa questa sezione dopo ogni ordine eBay o ogni acquisto manuale.**

        1. Inserisci l'**email del cliente** nel campo "Email cliente..."
        2. Clicca **Cerca**
        3. Appare la tessera mini del cliente con i suoi punti attuali
        4. Inserisci l'**importo dell'ordine in euro** (es: 35.50)
        5. (Opzionale) Inserisci l'**ID ordine** per tracciabilità
        6. (Opzionale) Aggiungi una **nota**
        7. Clicca **"Aggiungi punti"**

        Il sistema calcola automaticamente i punti (1 ogni 10 euro, arrotondato per difetto) e li aggiunge.

        **Se il cliente raggiunge 5 o 10 punti:** appare un popup "PREMIO SBLOCCATO!" — significa che devi spedire/consegnare il premio. I punti si azzerano automaticamente e ripartono.

        **Pulsante "Punti manuali":** ti chiede quanti punti aggiungere a mano (utile per correzioni o regali extra). Ti chiede anche una nota.

        ---

        ### SEZIONE 2 — "Nuovo Cliente" (al primo ordine)

        **Usa questa sezione la prima volta che un cliente ordina.**

        1. Compila **Nome e cognome**
        2. Compila **Email** (deve essere unica — è la chiave di accesso del cliente)
        3. (Opzionale) Telefono e note interne
        4. Clicca **"Crea tessera"**

        Il sistema genera automaticamente un **codice tessera univoco** (es: SR-00042).
        Puoi comunicare questo codice al cliente sulla tessera cartacea che gli spedisci.

        ---

        ### SEZIONE 3 — "Elenco" (panoramica clienti)

        Mostra la lista completa di tutti i clienti registrati con:
        - Nome e codice tessera
        - Email
        - Punti attuali
        - Numero premi già ricevuti
        - Data di registrazione

        **Filtrare:** digita nel campo "Filtra per nome o email..." per trovare un cliente rapidamente.

        **Aggiornare:** clicca il pulsante "Aggiorna" per ricaricare i dati più recenti.

        ---

        ## FLUSSO DI LAVORO SETTIMANALE CONSIGLIATO

        ```
        NUOVO ORDINE RICEVUTO (Shopify o eBay)
          ↓
          Il cliente è già registrato?
            → SÌ: vai su "Aggiungi Punti", cerca per email, inserisci importo
              → NO: prima vai su "Nuovo Cliente" e crea la tessera, poi aggiungi i punti
                ↓
                Premio sbloccato?
                  → SÌ: prepara e spedisci il premio (tazza a 5pt, set a 10pt)
                    → NO: nessuna azione extra
                    ```

                    ---

                    ## CREDENZIALI E RIFERIMENTI TECNICI

                    | Cosa | Valore |
                    |---|---|
                    | URL app cliente | https://tessera-fedelta.vercel.app |
                    | Password admin | [vedi pannello impostazioni] |
                    | Repository GitHub | https://github.com/Sr-test0/tessera-fedelta |
                    | Database (Supabase) | https://lixlgaxkjtjbtudjownk.supabase.co |

                    ---

                    ## DOMANDE FREQUENTI

                    **Il cliente non trova la tessera cercando la sua email?**
                    → Non è ancora registrato. Vai nel pannello admin → "Nuovo Cliente" e creala tu.

                    **Ho inserito l'importo sbagliato. Come correggo?**
                    → Usa "Punti manuali" con un numero negativo (es: -2) per togliere punti, oppure aggiungi 0 punti con una nota esplicativa. In futuro si può aggiungere una funzione di modifica diretta.

                    **Il cliente ha ricevuto il premio ma i punti non si sono azzerati?**
                    → Il sistema azzera automaticamente quando aggiungi punti tramite "Aggiungi punti" e il totale supera 5 o 10. Se hai usato "Punti manuali" devi gestirlo a mano.

                    **Come comunico la tessera al cliente?**
                    → Al primo ordine crei la tessera, poi mandi al cliente l'email con: URL app + suo codice tessera + sua email di accesso. Sulla tessera cartacea puoi stampare solo il codice, il cliente poi accede online con l'email.

                    **Posso collegare Shopify in futuro?**
                    → Sì. Il sistema è già predisposto. Quando attiverai Shopify basterà aggiungere un webhook "order/paid" che chiama la funzione Supabase automaticamente, eliminando il bisogno di aggiungere punti manualmente per gli ordini online.

                    ---

                    *Guida aggiornata al: giugno 2025 — SR Art Tessera Fedeltà v1.0*
