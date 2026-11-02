# Schweiz Edition

Eine Karte für [Embedding Drive](https://drive.potentialhedge.com): 100 Schweizer Orte und Dinge, von Zürich und dem Matterhorn bis zu Fondue, Schweizer Taschenmesser und Roger Federer. Jeder Ort ist ein Artikel der deutschsprachigen Wikipedia; das Spiel ordnet sie nach der Bedeutung ihrer Titel an, sodass Verwandtes nur wenige Strassen auseinanderliegt.

Im Spiel unter **World → Community maps** öffnen, oder dort `benedict-armstrong/embedding-drive-schweiz` einfügen. Die englische Ausgabe: [embedding-drive-switzerland](https://github.com/benedict-armstrong/embedding-drive-switzerland).

## Dateien

- `map.json`: Name, Beschreibung, Anzahl Orte und das Embedding-Rezept.
- `titles.txt`: ein Wikipedia-Titel pro Ort, in Reihenfolge.
- `vectors.bin`: ein 768-dimensionales Embedding pro Titel (EmbeddingGemma 300M, q8), als int8-Werte gefolgt von einem float32-Skalenfaktor pro Ort.
- `knn.bin`: die nächsten Nachbarn jedes Orts, vorberechnet.
- `nodes.json`: Beschriftungen und Links zur deutschsprachigen Wikipedia, für die nächste Version des Kartenformats.

Erstellt mit `scripts/embed-vocab.mjs` und `scripts/build-knn.mjs` aus dem Spiel.
