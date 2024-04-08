# Übungsaufgabe: Rückgängig machen eines Commits mit git reset (soft, mixed und hard)

Durch diese Übung kannst du den Unterschied zwischen den verschiedenen Reset-Modi
(`soft`, `mixed` und `hard`) kennenlernen und verstehen, wie sie sich auf
die Commit-Historie, den Staging-Bereich und das Arbeitsverzeichnis auswirken.

## Schritt 1
Initialisiere ein neues Git-Repository in einem leeren Verzeichnis.
Verwende dazu den Befehl:

```
git init
```

## Schritt 2
Erstelle eine neue Textdatei mit einem Texteditor oder der Befehlszeile.
Nenne die Datei `example.txt` und füge einen beliebigen Textinhalt hinzu.

## Schritt 3
Füge die neue Textdatei dem Staging-Bereich hinzu und mache einen Commit.
Verwende dazu die folgenden Befehle:

```
git add example.txt
git commit -m "example.txt hinzugefügt"
```

## Schritt 4
Lösche die Datei example.txt, füge die Änderung zur Stage hinzu und erstelle 
einen neuen Commit mit der Nachricht "example.txt gelöscht".
Prüfe mit `git status` das der Arbeitsbereich sauber ist.

## Schritt 5
Führe den Befehl `git log` aus, um die Commit-Historie anzuzeigen und
den SHA-1-Hash des ersten Commits zu kopieren.

## Schritt 6
Probiere nun nacheinander `git reset --soft`, `git reset --mixed`
aus, um den Unterschied zu sehen:

```
git reset --soft <Commit-Hash>
```
```
git reset --mixed <Commit-Hash>
```

Überprüfe den Status deines Git-Repositories nach jedem Reset-Befehl und
führe erneut Befehle zum stagen und commiten aus, damit wieder 2 Commits in der Historie sind.

## Schritt 7
Benutze nun `git reset --hard` um das Löschen der Datei ganz rückgängig zu machen.
```
git reset --hard <Commit-Hash>
```
