# Environnements

[Zurück zur Zusammenfassung](index.md)

Voraussetzungen :
* PHP >= 7.4
* MySQL >= 8.0

Es gibt verschiedene Umgebungen:
* `dev`: Entwicklungsumgebung
* `test`: Testumgebung

Für jede Umgebung muss eine Datei mit den Umgebungsvariablen erstellt werden.

## Entwicklungsumgebung
Beispiel für die Datei `.env.dev.local`.
`` dotenv
Notwendig, wenn Sie Systemtests durchführen möchten

DATABASE_URL=mysql://root:password@127.0.0.1:3306/tiplay_dev
```

## Test Umgebung
Für die einwandfreie Funktion der Tests ist es zwingend erforderlich, die Datei `.env.test.local` zu erstellen, als Grundlage können Sie dieses Beispiel verwenden:
`` dotenv
# Notwendig, wenn Sie Systemtests durchführen möchten

DATABASE_URL=mysql://root:password@127.0.0.1:3306/tiplay_test
```

Vergessen Sie nicht, bei Bedarf andere Umgebungsvariablen wie `MAILER_DSN` zu konfigurieren.

Es ist vorzuziehen, die Umgebungsvariablen in die Konfiguration des virutalhost in der Produktion einzufügen.