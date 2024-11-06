---
description: Mappe di intensità delle precipitazioni
---

# 🛠️ Safer003

La funzione “Safer003” consiste in algoritmi su misura per generare una mappa dell'intensità delle precipitazioni a partire da dati satellitari. L'output di Safer003 viene utilizzato come input per migliorare la mappatura del rischio di alluvione generato dalle alluvioni pluviali.

Il pannello di apertura richiede all'utente di inserire tre parametri di input richiesti dal modulo Safer003:

\- _from date_: data dell'evento di alluvione,

\- _lag (days)_: n° di giorni consecutivi all'evento, in cui il sistema deve verificare la disponibilità dei dati,

\- _step:_ intervallo temporale richiesto.

Il flusso di lavoro per l'ingestione dei dati pluviometrici si basa sull'uso di PERSIANN-PDIR NOW [http://chrsdata.eng.uci.edu/](http://chrsdata.eng.uci.edu/).

<figure><img src="../.gitbook/assets/image (41).png" alt=""><figcaption><p>Mappe di intensità delle precipitazioni</p></figcaption></figure>



