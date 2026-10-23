# SCARY WORLD

**GPS Horror Experience** — prototipo web mobile-first per un gioco horror cooperativo basato sulla posizione.

## Versioni di prova

- **Administrator:** https://alessandropoabaglio-spec.github.io/SCARY-WORLD/administrator/
- **Player:** https://alessandropoabaglio-spec.github.io/SCARY-WORLD/player/
- **Prototipo originale:** https://alessandropoabaglio-spec.github.io/SCARY-WORLD/

Le nuove pagine sono una prima bozza per provare il flusso amministratore/giocatore. Nell'Administrator, per la demo, usa utente `mastro` e password `notte-demo`. **Non sono credenziali sicure**: il sito è pubblico e l'accesso è verificato nel browser. Prima di usare il pannello in una partita reale bisogna implementare autenticazione lato server.

## Administrator — bozza

- Nome partita, durata, numero squadre e raggio di attivazione configurabili.
- Creazione di tappe e scelta del tipo di enigma: codice a rotelle, ingranaggi, rebus o quiz.
- Campo per testo dell'enigma e soluzione attesa.
- Coordinate GPS per ogni tappa: si possono inserire manualmente o acquisire dalla posizione attuale dello smartphone.
- Generazione di codice dimostrativo e import/export JSON per trasferire la configurazione.

## Player — bozza

- Nome squadra e codice partita.
- Importazione del JSON preparato dall'Administrator.
- Prova degli enigmi animati: rotelle numeriche, ingranaggi, rebus visivo e quiz a scelta multipla.
- Attivazione GPS delle tappe con coordinate: la pagina mostra la distanza e sblocca l'enigma entro il raggio impostato.
- Avanzamento salvato localmente nel browser.

## Limiti attuali

Questa è una **demo locale**, non ancora un multiplayer completo. Il codice partita non sincronizza telefoni diversi. L'attivazione GPS funziona nel browser con HTTPS e permesso di geolocalizzazione, ma dipende dalla precisione del dispositivo e non sostituisce un sistema anti-manomissione. Il puzzle degli ingranaggi resta un minigioco dimostrativo. Per giocare sui diversi telefoni occorre implementare un backend in tempo reale. Per sicurezza, non usare ancora la password dimostrativa per proteggere dati reali.

Non è disponibile una vera modalità offline: la mappa del prototipo originale richiede internet. Per le mappe offline servirà una fonte che ne autorizzi il download e l'utilizzo.

## Pubblicazione con GitHub Pages

Repository: https://github.com/alessandropoabaglio-spec/SCARY-WORLD

In GitHub, apri **Settings → Pages** e scegli **Deploy from a branch**, branch `main`, cartella `/ (root)`. Le nuove pagine sono sottocartelle dello stesso progetto e usano gli indirizzi sopra indicati.

## Dati cartografici

La mappa del prototipo originale usa Leaflet e il servizio standard di tile di OpenStreetMap con attribuzione visibile. Le tile pubbliche standard non devono essere scaricate in massa per l'uso offline.


## Minigiochi animati (prima versione)

La pagina Player ora include:
- **Rotelle del codice** con feedback animato quando il codice è errato o corretto.
- **Ingranaggi** da selezionare e collocare nelle sedi; la sequenza corretta fa girare il meccanismo.
- **Rebus visivo** con simboli animati e campo per inserire la soluzione.
- **Quiz a scelta multipla** con pulsanti, feedback e barra temporale visuale.
- **Enigma testuale** con verifica della risposta.

Nell'Administrator si possono definire fino a quattro opzioni per i quiz, separate da punto e virgola, e indicare la soluzione corretta. Questi minigiochi sono una prima demo: non sono ancora puzzle grafici avanzati con editor visuale, e il timer del quiz è al momento un effetto visivo.

## Prossimi passi

1. Provare Administrator e Player su smartphone.
2. Migliorare gli ingranaggi con trascinamento e rotazione fisica più credibile.
3. Implementare autenticazione reale per l'Administrator.
4. Aggiungere backend per sincronizzare partita, squadre, posizioni e scoperte in tempo reale.
5. Verificare installabilità PWA, prestazioni e opzioni offline gratuite.
