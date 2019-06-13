## Versionierung
- BS: Anscheinend wird beim Export immer die neueste Version der LoC verwendet (was naheliegend wäre, da auf GitHub das [XSL](https://github.com/lcnetdev/marc2bibframe2/blob/master/xsl/marc2bibframe2.xsl) frei zugänglich ist)
## Modellierung
- SS: `<bf:Source>` enthält den SW-Vergebenden bei DDC statt der Quelle der Klassifikation
- BS: Expressionen-Elemente finden sich beim Werk - wie funktioniert die FRBRisierung hier?
- BS: CV-Werte kommen aus dem LoC-Vokabular, z.B. `<bf:GenreForm rdf:about="http://id.loc.gov/vocabulary/marcgt/cpb">conference publication`. Wie können wir hier Einfluss nehmen? Vermutlich müsste das XSL für den D-A-CH-Raum angepasst werden.
- BS: Identifier verweisen auf VIAF und nicht auf GND (`<rdf:value rdf:resource="http://viaf.org/viaf/sourceID/DNB|107077085X"/>`), gibt allerdings einen fragmentierten Verweis mittels ISIL.
- BS: Problem in `<bf:Title>`: Keine Trennung zwischen Haupt- und Untertitel in `<rdfs:label>` und `<bflc:titleSortKey>`, da wir die Interpunktion weglassen.
- BS: `gnd-content`-Modellierung aus `655` funktioniert gut.
- BS: `<bf:hasInstance>` nimmt die eigentlich im MARC-DS beschriebene Instance, aber auch z.B. `776`. Die Beziehungsfelder werden nur richtig ausgewertet, wenn sie auch MARC-konform befüllt werden!
- BS: `856` erzeugt `<bf:hasItem>`, auch wenn der Link nicht zur Ressource führt (noch zu verifizieren!). `856` mit richtigen Indikatoren erzeugt offenbar `<bf:supplementaryContent>`.
- BS: `<bf:place>` verwendet die MARC-Ländercodes, ISO kommt aber auch vor.
- BS: Stichwörter in `246` kommen als Titelportion an.
- BS: Illustationsangabe auf Instance-Ebene, als `<bf:note>`.
- BS: TATs machen Probleme: Sortierung von `$$n` und `$$p` kommt nicht an, bevorzugter Titel des Werks wird aus der `245` genommen, was bei Formaltiteln und Übersetzungen nicht stimmt - aber es gibt eine `partOf`-Beziehung zum übergeordneten Datensatz. Werkclustering in diesem Fall immer falsch!
- BS: Nichtsortierzeichen werden nicht erkannt
## Fehlende Informationen
## Sonstiges
