# Hinweis zum Anwendungsbereich

[Zurück zur Zusammenfassung](index.md)

## Erste Bedürftigkeitsäußerung

```text
Voraussetzungen:
- Verwaltung und Anzeige eines Batch-Shops
    - Effiziente und reaktionsschnelle UX
    - Filter und mehrere Suchkriterien
- Rollen- und Zugriffsrechte: Admin LADR, Admin Group, Unabhängiger Admin, Adherent Sales Representative, Garagiste-Aufbaubauer, Adherent Collaborator
- Backoffice-Zugang für die CRUD-Verwaltung der Begünstigten; für den Zugriff: Admin LADR, Admin Groupement, Unabhängiger Admin
- Backoffice-Zugang zur Konfiguration der Anzeige von Shops nach Art der Mitglieder; nur für LADR Admin-Zugriff
- Verwaltung von Schlüsselkäufen und Abrechnungsverfolgung
- Verwaltung der wichtigsten Bewegungen: Gutschrift, Lastschrift, Abhebung
- Logistikverfolgung von Chargenaufträgen
- Fügen Sie für jeden Begünstigten einer Charge die Möglichkeit hinzu, eine Kundendienstanfrage auszulösen
- Bis heute wurden einige der oben genannten Funktionalitäten entwickelt, sind jedoch nicht einfach zu verwalten und zu konsultieren. Es bereitet zum Beispiel Kopfschmerzen, ein Mitglied hinzuzufügen. Es ist auch unmöglich, Schlüsselbewegungen für einen Administrator einfach zu verfolgen.
```
## Q/R

```text
Viele Geschäfte:
    - Bedeutet dies für die Verwaltung der Filialen nach Mitglied, dass wir die angezeigten Lose nach Mitglied filtern können? => Ja. Derzeit tun wir dies, indem wir an einer Bedingung von Gui herumbasteln, damit die Kunden, die vom Ouest Injection-Mitglied profitieren, die Geschenkgutscheine im Geschäft nur sehen. Ich weiß nicht, ob es auf der Backoffice-Seite von LADR (Speculoos) erforderlich sein wird, es konfigurieren zu können, oder auf der Backoffice-Seite des KP-Projekts auf den Zugriff des Projektteams, aber aus Erfahrung Ich weiß, dass es notwendig ist zu wissen, wie man verschiedene Shops gemäß den Erwartungen jedes Mitglieds verwaltet / ablehnt.
    - Und hat der nach Mitglied gefilterte Batch-Shop Auswirkungen auf den Kunden des Mitglieds? => Ich glaube, Sie haben die Antwort in dem, was ich zuvor geantwortet habe.
    - Beispiel für den ultimativen Store (UX / UI) => Wartest du dort, bis Tim das gewünschte Modell für dich vorbereitet?

Unternehmenstyp:
    - Gruppierung> Mitglied / Unabhängig> Kunde (Werkstattmechaniker / Aufbauhersteller)

Ich glaube nicht, dass wir das richtige gemeinsame Vokabular haben können, um uns zu verstehen, aber wir werden es tun. Hier ist ein neuer Versuch, die Art der Unternehmen aufzulisten:
    - Multi-Warehouse-Mitglied. Aktuelles Beispiel: Aurélie Jeannette, die die Firmennamen über verschiedene Zugänge verwalten muss: IDLP, NED, Choisy Auto Parts. Letztendlich sollte sie nur einen Zugang haben können.
    - Einzellagermitglied. Aktuelles Beispiel: Ouest Injection
    - Kunde (Mechaniker / Aufbauhersteller): Dies sind die Begünstigten des Programms, die von den 2 Arten von vorgelisteten Mitgliedern registriert sind
Benutzerregeln:
    - LADR-Administrator
    - Multi-Warehouse-Mitglieder-Administrator
    - Single-Warehouse-Mitgliedsadministrator
    - Kommerziell: Derzeit besteht seine Rolle nur in der Überwachung, keine Maßnahmen. Ziehen wir in Erwägung, seine Rolle auszuweiten? => Ja, wir müssen ihm 2 Optionen ermöglichen: einen Kunden registrieren (standardmäßig kann er nicht, es ist für den Administrator reserviert) + von einem persönlichen Schlüsselkonto profitieren (standardmäßig gibt es kein nicht, es gehört ihm Administrator, der sich entscheiden könnte, den KP-Store zu nutzen, um seine Verkäufer auch mit Schlüsseln zu belohnen)
    - Mitarbeiter: Was bedeutet Mitarbeiter? Rolle des Visus? => Nein, keine visuelle Rolle. Für mich ist es eher ein „Joker“-Status, den wir bei vielen Projekten vermissen, wenn uns unsere Kunden sagen: Wir möchten Jeannine de la compta den Zugang freigeben und ihr 100 Schlüssel gutschreiben, damit sie im Laden bestellen kann gut gearbeitet. Aber Jeannine ist weder Kunde (Mechanikerin / Bodybuilderin) noch Verkäuferin (kaufmännische Funktion). Plötzlich basteln wir an einem Patch. Die Rolle des Mitbearbeiters würde diese fehlende Rolle spielen, um es den Begünstigten zu ermöglichen, ohne besondere Verbindungslogik (ein Kunde zu einem Verkäufer) Zugriff zu gewähren.

Kein Mitgliedsadministrator? => Zu Ihrem Eintrag oben hinzugefügt.

Was ist am Ende der wirkliche Unterschied zwischen Mitglied und unabhängig, wenn nicht in seiner Typologie? => Meine bisherigen Antworten sollten diese Frage beantwortet haben, was nicht wirklich sinnvoll ist, wenn wir nun ein Mitglied nach seiner Art des Multi- oder Single-Lagers mit den gleichen Begriffen bezeichnen.

Sollen wir den Kauf mit Kreditkarte planen? Wenn ja, Streifen? Zitrone? Paypal? Oder die Bank? ...Oder bleiben wir bei der Paarüberweisung/Überprüfung und daher etwas manuell? => Im Moment bleiben wir beim aktuellen Betrieb.

Falls manuell, im Backoffice für die Abrechnungsverwaltung mit Schlüsselguthaben versehen? => Ja, so bleiben wir.

Wie funktioniert der After-Sales-Service? Senden Sie eine E-Mail oder eine Bedienungsanleitung auf der Website? => Wir bleiben auf Kundenseite bei etwas "Einfachem", indem wir eine E-Mail an uns senden. Andererseits ist die Idee von Hand, in unserem Backoffice Zugriff auf die eingegangenen Anfragen (Anfrage in Bearbeitung, Anfrage geschlossen, auf Antwort wartend, nicht vom Kundendienst unterstützt usw.) und dass der Benutzer über seinen Zugang eine „Nachverfolgung von Kundendienstanfragen“ genauso einsehen kann wie eine „Nachverfolgung von Sammelbestellungen“.
```
