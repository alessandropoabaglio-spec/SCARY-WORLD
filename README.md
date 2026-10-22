# SCARY WORLD

**GPS Horror Experience** — prototipo web mobile-first per un gioco horror cooperativo basato sulla posizione.

## Prototipo 0.1

- Creazione locale di una partita con codice a 6 caratteri.
- Registrazione locale delle squadre e scelta del simbolo horror.
- Mappa interattiva Leaflet con OpenStreetMap.
- Posizione GPS del dispositivo (richiede HTTPS e autorizzazione).
- Inserimento manuale di tappe sulla mappa: presenza inquietante, enigma, luogo maledetto e audio misterioso.
- Salvataggio dei dati nel browser, più esportazione/importazione JSON.

## Limiti attuali

Questa è una **demo locale**: partita, squadre e tappe vengono salvate nel browser del dispositivo. Il codice della partita non connette ancora telefoni diversi e le posizioni delle squadre non sono condivise online. Non è ancora disponibile una vera modalità offline: la cartografia richiede una connessione internet.

## Avvio

Apri `index.html` tramite GitHub Pages o un server HTTPS. Consenti la geolocalizzazione quando il browser la richiede.

## Pubblicazione con GitHub Pages

Nel repository, apri **Settings → Pages** e scegli **Deploy from a branch**, branch `main`, cartella `/ (root)`, quindi salva. Dopo la pubblicazione l'indirizzo sarà:

https://alessandropoabaglio-spec.github.io/SCARY-WORLD/

## Prossime tappe

1. Rifinire l'interfaccia e verificare il prototipo su smartphone.
2. Configurare un backend gratuito per codice partita, squadre e posizioni in tempo reale.
3. Aggiungere area di gioco (raggio o perimetro) e strumenti per l'organizzatore.
4. Preparare la web app installabile e valutare una soluzione cartografica offline con licenza/servizio adeguato.

## Dati cartografici

La mappa usa Leaflet e il servizio standard di tile di OpenStreetMap con attribuzione visibile. Le tile pubbliche standard non devono essere scaricate in massa per l'uso offline; per mappe offline servirà una fonte che lo consenta.

