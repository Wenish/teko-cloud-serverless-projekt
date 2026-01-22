# Teko Cloud Serverless Projektarbeit
## Einleitung

### Ausgangslage

Das Spiel Shadow Infection benötigt für den Vertrieb eine Webseite, über die das Spiel verkauft und heruntergeladen werden kann. Das Spiel liegt in drei Artefakten vor: einem Windows Build, einem Linux Build und einem macOS Build. Jedes Build hat eine Grösse von ca. 500 Megabyte.

Aktuell existiert ein Web Client Prototyp, der darstellt, wie der Kunde das Spiel kaufen und anschliessend herunterladen kann. Dieser Prototyp verfügt jedoch noch über keine Backend Logik. Für die Zahlungsabwicklung ist Stripe als Anbieter festgelegt. Das Spiel wird als herunterladbares digitales Produkt vertrieben.

### Problemstellung

Ein Kunde muss ein Benutzerkonto erstellen können. Mit dem Kauf des Spiels erhält der Kunde über sein Benutzerkonto Zugriff auf alle verfügbaren Builds.

Es muss sichergestellt werden, dass Download Links ausschliesslich für angemeldete Benutzerkonten verfügbar sind, die das Spiel erworben haben. Ein Benutzerkonto darf das Spiel beliebig oft herunterladen.

Dem Kunden wird garantiert, dass er mindestens drei Monate im Voraus informiert wird, falls die Downloads künftig nicht mehr zur Verfügung stehen.

Das Spiel selbst soll nach dem Download lokal ohne Benutzerkonto gestartet werden können. Es wird bewusst darauf verzichtet, technische Massnahmen zur Verhinderung von Piraterie umzusetzen.

Zukünftige Updates des Spiels stehen ebenfalls zum Download zur Verfügung.

Dem Benutzer wird stets nur die aktuelle Version zum Download angeboten.


Bedeutung Herunterladbares Spiel:
Videospiele im üblichen Sinne, die elektronisch übertragen werden. Sie werden auf ein Gerät mit dauerhaften gewährten Zufriff heruntergeladen. Ausgenommen hiervon sind Spiele, die als Wetten, Glückspiele, Lotterie usw. gelter. (Quelle Stripe)



### Zielsetzung

## Vorgehen

## Ergebnisse

## Diskussion

## Empfehlung und Ausblick