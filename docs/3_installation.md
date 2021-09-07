# Installation

[Zurück zur Zusammenfassung](index.md)


## Voraussetzungen
* PHP >= 8.0
* Extensions PHP :
    * ctype
    * iconv
    * json
    * xml
    * intl
    * mbstring
* composer
* MySQL/MariaDB
* NodeJS >= 14.4
* npm >= 6.14

## Abhängigkeiten installieren
Gehen Sie zunächst in den Projektordner:
```
cd <repo-name>
```

Führen Sie den folgenden Befehl aus
```
make install
```

## Environnements
Damit das Projekt auf Ihrem Computer funktioniert, denken Sie daran, die verschiedenen Umgebungen zu konfigurieren. Eine Dokumentation zu diesem Thema gibt es [hier] (4_umgebung.md).

## Datenbanken initialisieren
Angefangen bei der Umwelt `test`
```
make database-test
```

Dann die Umwelt `dev`:
```
make database-dev
```

Wenn Sie möchten, können Sie zusätzlich zum Einrichten der Datenbank auch Fixtures injizieren:

Für die Umwelt `test`
```
make fixtures-test
```

Dann die Umwelt `dev`:
```
make fixtures-dev
```

## Lancer le serveur en local
Es ist notwendig, die installiert zu haben [binaire de symfony](https://symfony.com/download).
```
symfony serve
```

## Verwaltung externer Ressourcen (css, js)
Kompilieren Sie die Dateien einmal in der Entwicklungsumgebung:
```
npm run dev
```

Automatisches Kompilieren aktivieren:
```
npm run watch
```

Kompilieren Sie die Dateien für die Produktion:
```
npm run build
```
