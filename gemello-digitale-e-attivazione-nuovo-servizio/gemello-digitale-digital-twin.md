---
cover: ../.gitbook/assets/Asset 10.jpg
coverY: 0
layout:
  cover:
    visible: true
    size: hero
  title:
    visible: true
  description:
    visible: true
  tableOfContents:
    visible: true
  outline:
    visible: true
  pagination:
    visible: true
---

# 📔 Gemello Digitale - Digital Twin

L'attivazione di un nuovo progetto o servizio sulla piattaforma Saferplaces, consiste nella generazione della  Digital Twin dell'area di interesse.&#x20;

{% content-ref url="creazione-digital-twin-e-attivazione-del-servizio-nellarea-di-interesse/" %}
[creazione-digital-twin-e-attivazione-del-servizio-nellarea-di-interesse](creazione-digital-twin-e-attivazione-del-servizio-nellarea-di-interesse/)
{% endcontent-ref %}

La Digital Twin è costituita dai seguenti dati geospaziali:

<details>

<summary>Modello digitale del Terreno (DTM) - LIDAR</summary>

La piattaforma SaferPlaces consente all'utente di scegliere tra diversi layer di DTM disponibili con diversa risoluzione spaziale.&#x20;

Nella fase di attivazione i layer DTM vengono ordinati in funzione della risoluzione proponendo secondo un ordine a risoluzione decrescente.

L'utente può scegliere i DTM disponibili a partire da quelli a più alta risoluzione spaziale (LIDAR) fino ai prodotti regionali o nazionali con risoluzione più bassa.

Alternativamente, se l'utente dispone di dati DTM proprietari  può caricarle direttamente sulla piattaforma mediante l'opzione UPLOAD ed utilizzare il datate nella creazione della Digital Twin.\
\
Per sfruttare al meglio i DEM ad alta risoluzione, la piattaforma è stata ottimizzata per lavorare con i dati LIDAR.&#x20;

I DTM pre-caricati e disponibili a livello nazionale sono:

* LIDAR Ministero dell'Ambiente - [Piano Nazionale di Telerilevament](https://sim.mase.gov.it/portalediaccesso/mappe/#/viewer/new)o
* DTM [TINITALY](https://tinitaly.pi.ingv.it/Download\_Area1\_1.html)
* LIDAR Regione Emilia Romagna
* LIDAR Regione Veneto
* DTM Regionionali

\


</details>

<details>

<summary>Footprint Edifici - Shapefile Vettoriale</summary>

La sagoma (footprint) degli edifici costituisce un dato di input per il calcolo del Danno Economico associato agli eventi di allagamento e calcolati mediante[modello-di-danno-economico-safer\_damage.md](../simulazioni-allagamento-pericolo-e-danno/modello-di-danno-economico-safer\_damage.md "mention")

Si tratta di un layer geospazile di ti vettoriale shapefile che viene automaticamente acquisito dal data set di [Open Street Map](https://osmbuildings.org/?lat=43.94654\&lon=12.63075\&zoom=16.0\&tilt=30).\
Alternativamente, se l'utente ha delle informazioni specifiche può caricarle direttamente sulla piattaforma attraverso l'opzione UPLOAD.

</details>

<details>

<summary>Tasso di infiltrazione</summary>

Questo layer esprime la capacità di infiltrazione nel suolo che è associata alla classe di uso del suolo. In dettaglio un uso del suolo di tipo urbanizzato o industriale avrà un tasso di infiltrazione pari o vicino allo zero mentre un suolo agricolo o ad aree verdi avrà un tasso di inflitrazione pari o vicino ad 1.

Nella fase di generazione della Digital Twin, Saferplaces utilizza come classificazione di uso del suolo il layer a 10 m fornito da ESA ([The European Space Agency (ESA) WorldCover 10 m 2021](https://esa-worldcover.org/)) .

Per l'area della Regione Emilia Romagna si utilizza il mosaico dell'uso del suolo da CORINE LAND COVER.

Anche per questo layer, nel caso in cui l'utente avesse a disposizione informazioni di maggiore dettaglio, è possibile mediante la funzione UPLOAD caricare lo shapefile vettoriale con le classi di uso del suolo.

\


</details>

<details>

<summary>Litologia</summary>

La  litologia del suolo in termini di composizione di classi tessiturali (Sand, Clay e Silt) influenza la capacità e velocità di infiltrazione dell'acqua sottraendone al run-off superficiale e quindi alla quota parte che contribuisce all'allagamento.

Questa informazione è un dato di input al modello di infiltrazione di Green-Ampt implementato nei [modelli-di-allagamento-hazard-saferplaces](../simulazioni-allagamento-pericolo-e-danno/modelli-di-allagamento-hazard-saferplaces/ "mention").

Il dato tessiturale integrato nella piattaforma Saferplaces, è un dato con copertura globale e risoluzione spaziale a 100 m prodotto da [OpenLandMap](https://opengeohub.org/about-openlandmap/)

Per l'area della Regione Emilia Romagna sono disponibili le classi tessiturali fornite dal [Servizio Geologico](https://mappegis.regione.emilia-romagna.it/gstatico/documenti/dati\_pedol/tessitura\_pianura.pdf) \
Anche per questo layer, nel caso in cui l'utente avesse a disposizione informazioni di maggiore dettaglio, è possibile mediante la funzione UPLOAD caricare lo shapefile vettoriale con le classi di uso del suolo.

</details>

<details>

<summary>Dati Climatici</summary>

Nella fase di attivazione del servizio è possibile acquisire automaticamente i dati climatici dei dataset presenti in [Copernicus CDS.](https://cds.climate.copernicus.eu)

</details>

<details>

<summary>Immagini Satellitari</summary>

Le funzioni si processamento dei dati satellitari consentono di estrarre automaticamente le aree allagate analizzando le immagini [Copernicus Sentinel](https://dataspace.copernicus.eu/explore-data/data-collections) sia ottiche che SAR.

</details>

{% hint style="danger" %}
Ai fini della creazione del nuovo progetto e della Digital Twin, sono necessari come dati di input obbligatori il DTM e il "Footprint" degli Edifici.

Il  DTM è l'input principale e cruciale richiesto dai modelli di pericolosità da alluvione SaferPlaces.

Il Wizard di attivazione chiede all'utente di selezionare tra i dati disponibili o di caricare mediante upload i dati a disposizione dell'utente per :

* DTM
* EDIFICI
* INFILTRAZIONE
* LITOLOGIA

I dati Climatici e le Immagini Satellitari vengono caricati in background nella attivazione del progetto.


{% endhint %}

