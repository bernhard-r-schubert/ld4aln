Anleitung schamlos gestohlen von Wolfram Seidler aus [https://wiki.univie.ac.at/x/IxPHB](https://wiki.univie.ac.at/x/IxPHB)

# Linked Data aus ALMA

Alma ermöglicht auch den Zugriff auf bzw. den Export von bibliografischen Daten als Linked Data.

Die entsprechende Dokumentation für Alma ist im Developers Network zu finden: [https://developers.exlibrisgroup.com/alma/integrations/linked_data/](https://developers.exlibrisgroup.com/alma/integrations/linked_data/)

## Zugriff auf die Daten

via HTTP-Request
Folgende 3 Formate sind (derzeit?) möglich:

- BIBFRAME
- JSONLD
- RDA/RDF

Der Aufruf erfolgt unter der folgenden URL: [https://open-eu.hosted.exlibrisgroup.com/alma/43ACC_UBW/](https://open-eu.hosted.exlibrisgroup.com/alma/43ACC_UBW/)

An diese URL angehängt wird:

- BIBFRAME	`bf/entity/instance/<MMSID>`
- JSONLD	`bibs/<MMSID>`
- RDA/RDF	`rda/entity/manifestation/<MMSID>`

## Beispiele

- BIBFRAME: [https://open-eu.hosted.exlibrisgroup.com/alma/43ACC_UBW/bf/entity/instance/9980752866303332](https://open-eu.hosted.exlibrisgroup.com/alma/43ACC_UBW/bf/entity/instance/9980752866303332)
- JSONLD: [https://open-eu.hosted.exlibrisgroup.com/alma/43ACC_UBW/bibs/9980752866303332](https://open-eu.hosted.exlibrisgroup.com/alma/43ACC_UBW/bibs/9980752866303332)
- RDA/RDF: [https://open-eu.hosted.exlibrisgroup.com/alma/43ACC_UBW/rda/entity/manifestation/9980752866303332](https://open-eu.hosted.exlibrisgroup.com/alma/43ACC_UBW/rda/entity/manifestation/9980752866303332)
