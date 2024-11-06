# STEP 1  DTM - Raster GeoTiff

L'utente definisce l'area di studio inserendo la località di interesse nella apposita finestra di ricerca "area".\
Dopo avere selezionato la località o città, la mappa visualizza l'area e propone un rettangolo in blue come area di attivazione.

Agendo con il mouse con il tasto destro è possibile ridimensionare o allargare l'area di attivazione.

Una volta definita l'area l'utente deve selezionare il DTM che intende utilizzare per attivare la Digital Twin ed il progetto di Saferplaces.

Nel menu a tendina DATASET può selezionare il DTM tra i layer disponibili ordinati in senso decrescente in relazione alla loro risoluzione spaziale (dalla alta risoluzione LIDAR alla bassa risolizione).

Infine occorre definire il sistema di proiezione EPSG che si intende utilizzare nella creazione del progetto.

{% hint style="danger" %}
La piattaforma Saferplaces in funzione della risoluzione spaziale del DTM selezionato e dell'estensione dell'are da attivare ha un limite in termini di numero di pixel che non può essere superato.

Nel caso esso venga superato appare un messaggio di errore specifico.
{% endhint %}



{% embed url="https://drive.google.com/open?id=1Dnu0KEDRb_yGvBRcywYGD9BP8Wgn3RIr&usp=drive_fs" %}

Nel caso in cui l'utente voglia caricare un layer DTM propietario può farlo mediante la funzione UPLOAD e caricare un file raster in formato GeoTIFF.
