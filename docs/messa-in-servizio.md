# MESSA IN SERVIZIO

# MESSA IN SERVIZIO

## 1 DESCRIZIONE GENERALE

Il D.Lgs. 127/2015 ha sancito l’introduzione della trasmissione telematica dei corrispettivi all’Agenzia delle Entrate.

La trasmissione telematica diventerà obbligatoria secondo le fasce confermate in via definitiva dalla Legge di Bilancio 2019 a partire dal 1° luglio 2019 per gli esercenti con un volume d’affari superiore a 400000 € e dal 1° gennaio 2020 per tutti gli altri esercenti a parte le categorie esentate.

Le fasi necessarie per la messa in servizio di un registratore telematico sono le seguenti:
*   Creazione della chiave privata
*   Censimento
*   Fiscalizzazione
*   Accreditamento portale Fisconline
*   Attivazione
*   Applicazione QR code

Queste fasi devono essere eseguite nell’ordine temporale con cui sono state elencate.

## 2 CREAZIONE DELLA CHIAVE PRIVATA

Il dispositivo necessita di eseguire una procedura di generazione di una chiave privata al fine di poter ottenere e firmare i certificati.

**ATTENZIONE:**
La procedura di generazione della chiave privata è possibile una sola volta.

Procedere come segue:
*   Accendere il dispositivo:
    ```
    [Immagine di un pulsante ON/OFF con "ON" sotto]
    ```
*   Passare all’assetto Programmazione premendo ripetutamente il tasto `CHIAVE` fino a che sul display non compare il messaggio “PROGRAMMAZIONE”:
    ```
    [Immagine di un tasto "Chiave" e un flusso verso "PROGRAMMAZIONE"]
    ```
*   Accedere alla programmazione P699:
    ```
    6   9   9   SubTotale
    ```
*   Selezionare “MENU TECNICO” utilizzando i tasti con le frecce di selezione:
    ```
    [Immagine di frecce di selezione] oppure [Immagine di un tasto "00"]
    ```
*   Sul display viene visualizzato:
    ```
    [MENU TECNICO]
    TIPO MENU
    ```
*   Confermare l’operazione con il tasto:
    ```
    SubTotale
    ```
*   Selezionare “SI” utilizzando i tasti con le frecce di selezione:
    ```
    [Immagine di frecce di selezione] oppure [Immagine di un tasto "00"]
    ```
*   Sul display viene visualizzato:
    ```
    [SI]
    CONFERMI?
    ```
*   Confermare l’operazione con il tasto:
    ```
    SubTotale
    ```
*   Sul display viene visualizzato:
    ```
    GENERAZIONE CHIAVI
    IN CORSO \
    ```
    **NOTA:**
    La procedura di generazione della chiave privata può richiedere diversi minuti (fino a 20). Attendere senza spegnere il dispositivo o senza scollegare l’alimentazione.
*   Durante l’operazione il LED lampeggerà nei colori verde/giallo ad intermittenza.
    ```
    [Immagine di un LED che lampeggia]
    ```
*   Alla fine della procedura, in caso di esito positivo, verrà emesso il seguente scontrino:
    ```
    <Nome Ditta>
    <Indirizzo>
    <Località>
    <Telefono - Fax>
    ------------------------------------
    GENERAZIONE CHIAVE PRIVATA
    ------------------------------------
    <ESITO POSITIVO>

    codice http: <#>
    codice xml: <#>
    risp: <#>
    idoper: <#>
    01/01/24 12:00 <#DOC. GES.>
    NUMERO DI MATRICOLA <matr. fiscale>
    ```

## 3 CENSIMENTO

Per poter funzionare correttamente e trasmettere i dati con l’Agenzia delle Entrate, il dispositivo necessita di essere censito.

La procedura di censimento è possibile anche attraverso l’interfaccia del Web Server (vedere il manuale cod. 0576100M000136).

**ATTENZIONE:**
La seguente procedura di censimento è possibile solamente dopo aver generato la chiave privata (vedere paragrafo 2 di questa sezione).

Procedere come segue:
*   Accendere il dispositivo:
    ```
    [Immagine di un pulsante ON/OFF con "ON" sotto]
    ```
*   Passare all’assetto Programmazione premendo ripetutamente il tasto `CHIAVE` fino a che sul display non compare il messaggio “PROGRAMMAZIONE”:
    ```
    [Immagine di un tasto "Chiave" e un flusso verso "PROGRAMMAZIONE"]
    ```
*   Accedere alla programmazione P699:
    ```
    6   9   9   SubTotale
    ```
*   Selezionare “MENU TECNICO” utilizzando i tasti con le frecce di selezione:
    ```
    [Immagine di frecce di selezione] oppure [Immagine di un tasto "00"]
    ```
*   Sul display viene visualizzato:
    ```
    [MENU TECNICO]
    TIPO MENU
    ```
*   Confermare l’operazione con il tasto:
    ```
    SubTotale
    ```
*   Sul display viene visualizzato:
    ```
    ↑_
    CODICE FISCALE
    ```
*   Digitare il codice fiscale (16 caratteri) del tecnico abilitato che esegue la procedura di censimento utilizzando il tastierino numerico. Ad ogni tasto corrisponde un set di caratteri (vedere legenda sul tasto). Premere ripetutamente un tasto per scorrere il set di caratteri ad esso associato.
    **NOTA:**
    Per cancellare un carattere inserito erroneamente premere il tasto C.
    Per cancellare tutto quanto digitato premere due volte in sequenza il tasto C.
    **NOTA:**
    In tutte le condizioni nelle quali è prevista la digitazione di caratteri, sarà possibile forzare l’immissione dei soli caratteri numerici premendo una volta il tasto:
    ```
    [Immagine di un tasto "Chiave"]
    ```
    Premendo nuovamente il tasto sopra citato, tale modalità verrà disattivata e si tornerà alla modalità di immissione di caratteri alfanumerici. A conferma della modalità in cui ci si trova, a display compariranno le diciture “[NUMERIC]” oppure “[ALPHANUMERIC]”.
*   Confermare con il tasto:
    ```
    SubTotale
    ```
*   Selezionare “CENSIMENTO” utilizzando i tasti con le frecce di selezione:
    ```
    [Immagine di frecce di selezione] oppure [Immagine di un tasto "00"]
    ```
*   Sul display viene visualizzato:
    ```
    [CENSIMENTO]
    SELEZIONA SERVIZIO
    ```
*   Confermare l’operazione con il tasto:
    ```
    SubTotale
    ```
*   Sul display viene visualizzato:
    ```
    ↑_
    CF/P.IVA CENTRO ASS.
    ```
*   Digitare il codice fiscale (16 caratteri) o la partita IVA (11 caratteri) della società a cui il tecnico abilitato che esegue la procedura di censimento risponde utilizzando il tastierino numerico. Ad ogni tasto corrisponde un set di caratteri (vedere legenda sul tasto). Premere ripetutamente un tasto per scorrere il set di caratteri ad esso associato.
    **NOTA:**
    Per cancellare un carattere inserito erroneamente premere il tasto C.
    Per cancellare tutto quanto digitato premere due volte in sequenza il tasto C.
*   Confermare con il tasto:
    ```
    SubTotale
    ```
*   Selezionare “SI” utilizzando i tasti con le frecce di selezione:
    ```
    [Immagine di frecce di selezione] oppure [Immagine di un tasto "00"]
    ```
*   Sul display viene visualizzato:
    ```
    [SI]
    CONFERMI?
    ```
*   Confermare con il tasto:
    ```
    SubTotale
    ```
*   Sul display viene visualizzato:
    ```
    CENSIMENTO
    IN CORSO \
    ```
*   Durante l’operazione il LED lampeggerà nei colori verde/giallo ad intermittenza.
    ```
    [Immagine di un LED che lampeggia]
    ```
*   Alla fine della procedura, in caso di esito positivo, verranno emessi i seguenti scontrini:
    ```
    <Nome Ditta>
    <Indirizzo>
    <Località>
    <Telefono - Fax>
    ------------------------------------
    CENSIMENTO
    ------------------------------------
    <ESITO POSITIVO>

    codice http: <#>
    codice xml: <#>
    risp: certificato ricevuto
    idoper: <#>
    01/01/24 12:00 <#DOC. GES.>
    NUMERO DI MATRICOLA <matr. fiscale>
    ```
    ```
    <Nome Ditta>
    <Indirizzo>
    <Località>
    <Telefono - Fax>
    ------------------------------------
    MIGRA SETDEVICE STATUS
    ------------------------------------
    <ESITO POSITIVO>

    codice http: <#>
    codice xml: <#>
    risp: servizio processato
    01/01/24 12:00 <#DOC. GES.>
    NUMERO DI MATRICOLA <matr. fiscale>
    ```

## 4 FISCALIZZAZIONE

La fiscalizzazione deve essere eseguita dal tecnico di assistenza solo al momento della definitiva messa in funzione del dispositivo. Dopo aver eseguito tale operazione è consentito l’uso fiscale dell’apparecchio.

**ATTENZIONE:**
L’operazione di fiscalizzazione è irreversibile, per cui una volta effettuata non sarà possibile ritornare nello stato non fiscale.

Prima della fiscalizzazione accertarsi che la data impostata sia corretta, poiché a fiscalizzazione avvenuta non sarà più possibile introdurre una data precedente a quella di fiscalizzazione.

Al momento della fiscalizzazione tutti i dati eventualmente contenuti nei totalizzatori del dispositivo vengono azzerati.

Prima di eseguire la fiscalizzazione del dispositivo, è necessario effettuare l’attivazione mediante la procedura descritta al paragrafo 6 di questa sezione.

Procedere come segue:
*   Passare all’assetto Programmazione premendo ripetutamente il tasto `CHIAVE` fino a che sul display non compare il messaggio “PROGRAMMAZIONE”:
    ```
    [Immagine di un tasto "Chiave" e un flusso verso "PROGRAMMAZIONE"]
    ```
*   Accedere alla programmazione P690:
    ```
    6   9   0   SubTotale
    ```
*   Inserire la password di protezione:
    ```
    1   4   7   8   9   6   SubTotale
    ```
*   Il dispositivo emette il seguente scontrino di conferma dell’avvenuta fiscalizzazione:
    ```
    ------------------------------------
    P(690) FISCALIZZAZIONE
    ------------------------------------
    *** FISCALIZZATO ***

    01/01/24 12:00 <#SNF #ST>
    NUMERO DI MATRICOLA: <matr. fiscale>
    ```
*   Inizializzare la memoria permanente di dettaglio (vedere paragrafo 4 di questa sezione).

## 5 ACCREDITAMENTO AL PORTALE FISCONLINE

Prima di iniziare la fase di attivazione, l’esercente deve accreditarsi al portale Fisconline dell’Agenzia delle Entrate (https://telematici.agenziaentrate.gov.it) dedicato ai servizi telematici per ricevere l’autorizzazione all’attivazione.

```
[Diagramma che mostra:
- "Esercente" che effettua "accreditamento al portale (anche tramite il commercialista)" verso "Fisconline".
- "Fisconline" che invia "autorizzazione all'attivazione" verso "Esercente accreditato".
]
```

## 6 ATTIVAZIONE

Per poter funzionare come registratore telematico (RT) operante sul campo secondo quanto previsto dal D.Lgs. 127/2015, il dispositivo necessita di essere attivato.

La procedura di attivazione è possibile anche attraverso l’interfaccia del Web Server (vedere il manuale cod. 0576100M000136).

**ATTENZIONE:**
La seguente procedura di attivazione è possibile solamente su dispositivo fiscalizzato, dopo aver generato la chiave privata e dopo avere effettuato il censimento (vedere rispettivamente paragrafo 2 e paragrafo 3 di questa sezione).

Procedere come segue:
*   Accendere il dispositivo:
    ```
    [Immagine di un pulsante ON/OFF con "ON" sotto]
    ```
*   Passare all’assetto Programmazione premendo ripetutamente il tasto `CHIAVE` fino a che sul display non compare il messaggio “PROGRAMMAZIONE”:
    ```
    [Immagine di un tasto "Chiave" e un flusso verso "PROGRAMMAZIONE"]
    ```
*   Accedere alla programmazione P699:
    ```
    6   9   9   SubTotale
    ```
*   Selezionare “MENU TECNICO” utilizzando i tasti con le frecce di selezione:
    ```
    [Immagine di frecce di selezione] oppure [Immagine di un tasto "00"]
    ```
*   Sul display viene visualizzato:
    ```
    [MENU TECNICO]
    TIPO MENU
    ```
*   Confermare l’operazione con il tasto:
    ```
    SubTotale
    ```
*   Sul display viene visualizzato:
    ```
    ↑_
    CODICE FISCALE
    ```
*   Digitare il codice fiscale (16 caratteri) del tecnico abilitato che esegue la procedura di attivazione utilizzando il tastierino numerico. Ad ogni tasto corrisponde un set di caratteri (vedere legenda sul tasto). Premere ripetutamente un tasto per scorrere il set di caratteri ad esso associato.
    **NOTA:**
    Per cancellare un carattere inserito erroneamente premere il tasto C.
    Per cancellare tutto quanto digitato premere due volte in sequenza il tasto C.
*   Confermare con il tasto:
    ```
    SubTotale
    ```
*   Sul display viene visualizzato:
    ```
    ↑_
    CF/P.IVA CENTRO ASS.
    ```
*   Digitare il codice fiscale (16 caratteri) o la partita IVA (11 caratteri) della società a cui il tecnico abilitato che esegue la procedura di attivazione risponde utilizzando il tastierino numerico. Ad ogni tasto corrisponde un set di caratteri (vedere legenda sul tasto). Premere ripetutamente un tasto per scorrere il set di caratteri ad esso associato.
    **NOTA:**
    Per cancellare un carattere inserito erroneamente premere il tasto C.
    Per cancellare tutto quanto digitato premere due volte in sequenza il tasto C.
    **NOTA:**
    In tutte le condizioni nelle quali è prevista la digitazione di caratteri, sarà possibile forzare l’immissione dei soli caratteri numerici premendo una volta il tasto:
    ```
    [Immagine di un tasto "Chiave"]
    ```
    Premendo nuovamente il tasto sopra citato, tale modalità verrà disattivata e si tornerà alla modalità di immissione di caratteri alfanumerici. A conferma della modalità in cui ci si trova, a display compariranno le diciture “[NUMERIC]” oppure “[ALPHANUMERIC]”.
*   Confermare con il tasto:
    ```
    SubTotale
    ```
*   Selezionare “ATTIVAZIONE” utilizzando i tasti con le frecce di selezione:
    ```
    [Immagine di frecce di selezione] oppure [Immagine di un tasto "00"]
    ```
*   Sul display viene visualizzato:
    ```
    [ATTIVAZIONE]
    SELEZIONA SERVIZIO
    ```
*   Confermare l’operazione con il tasto:
    ```
    SubTotale
    ```
*   Sul display viene visualizzato:
    ```
    ↑_
    CF/P.IVA GESTORE
    ```
*   Digitare il codice fiscale (16 caratteri) o la partita IVA (11 caratteri) del gestore dell’esercizio commerciale utilizzando il tastierino numerico. Ad ogni tasto corrisponde un set di caratteri (vedere legenda sul tasto). Premere ripetutamente un tasto per scorrere il set di caratteri ad esso associato.
    **NOTA:**
    Per cancellare un carattere inserito erroneamente premere il tasto C.
    Per cancellare tutto quanto digitato premere due volte in sequenza il tasto C.
*   Confermare con il tasto:
    ```
    SubTotale
    ```
*   Sul display viene visualizzato:
    ```
    ATTIVAZIONE
    IN CORSO \
    ```
*   Durante l’operazione il LED lampeggerà nei colori verde/giallo ad intermittenza.
    ```
    [Immagine di un LED che lampeggia]
    ```
*   Alla fine della procedura, in caso di esito positivo, verrà emesso il seguente scontrino:
    ```
    <Nome Ditta>
    <Indirizzo>
    <Località>
    <Telefono - Fax>
    ------------------------------------
    ATTIVAZIONE
    ------------------------------------
    <ESITO POSITIVO>

    codice http: <#>
    codice xml: <#>
    risp: attivazione ricevuta
    idoper: <#>
    01/01/24 12:00 <#DOC. GES.>
    NUMERO DI MATRICOLA <matr. fiscale>
    ```
*   In occasione della prima operazione che si eseguirà con dispositivo attivato, verrà emesso il seguente scontrino:
    ```
    GESTIONE LOTTERIA
    ATTIVATA!

    01/01/24 12:00 <#DOC. GES.>
    NUMERO DI MATRICOLA <matr. fiscale>
    ```
    ```
    DOCUMENTO GESTIONALE

    <Nome Ditta>
    <Indirizzo>
    <Località>
    <Telefono - Fax>
    MESSA IN SERVIZIO
    COMPLETATA
    01/01/24 12:00 <#DOC. GES.>
    NUMERO DI MATRICOLA <matr. fiscale>
    ```

## 7 APPLICAZIONE QR CODE

Completata la fase di attivazione, l’esercente dovrà scaricare dal sito https://telematici.agenziaentrate.gov.it (portale Fisconline) il QR code identificativo della macchina che deve essere stampato e applicato sul dispositivo D.Lgs 175/2015.

```
[Diagramma che mostra:
- "Fisconline" che genera un "QR code identificativo".
- "Esercente accreditato" che riceve il "QR code identificativo".
- Il "Registratore telematico RT (stato RT ATTIVATO)" che riceve un "QR code identificativo" (presumibilmente stampato e applicato).
]
```
