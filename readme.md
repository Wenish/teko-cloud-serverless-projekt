Zielsetzung Präzisieren


# Teko Cloud Serverless Projektarbeit
# Einleitung

## Ausgangslage

Dieses Projekt wird im Fach Cloud and Serverless als Gruppenarbeit (3 Personen) durchgeführt. Es muss eine Cloud Architektur für eine von uns Definierte Problemstellung entworfen werden. Der Fokus liegt nicht auf der Implmentierung der Applikation, sonder auf die Konzeption, Analyse und Begründung der gewählten Cloud Architektur.

Als Anwendungsfall dient das Computerspiel Shadow Infection, ein digital vertriebenes Spiel, das über eine eigene Webseite verkauft und anschliessend heruntergeladen werden soll. Das Spiel liegt in drei separaten Artefakten vor (Windows, Linux und macOS), wobei jedes Build eine Grösse von rund 500 MB aufweist. Der Vertrieb erfolgt ausschliesslich als digitales Produkt.

Für den Kaufprozess existiert bereits ein Web Client Prototyp, der den Ablauf vom Kauf bis zum Download visuell darstellt. Dieser Prototyp enthält jedoch keine Backend Logik. Für die Zahlungsabwicklung ist der externe Zahlungsdienstleister Stripe festgelegt. Dieser Service fällt in die Kategorie "herunterladbares Spiel".

## Problemstellung

Kunden sollen ein Benutzerkonto erstellen können und nach dem Kauf des Spiels dauerhaft Zugriff auf die aktuelle Spielversion erhalten. Die Download Links dürfen ausschliesslich für authentifizierte Benutzerkonten verfügbar sein, die das Spiel erworben haben. Ein Benutzerkonto darf das Spiel beliebig oft herunterladen.

Die Dateien in Form von ZIP sollen möglichst günstig ausgeliefert werden.

Das Spiel selbst soll nach dem Download ohne Online Zwang oder Benutzerkonto lokal gestartet werden können. Auf technische Massnahmen zur Verhinderung von Piraterie wird dort bewusst verzichtet.

Die zentrale Herausforgerung dieser Arbeit besteht darin, eine Cloud Architektur zu definieren, die rein aus PaaS oder SaaS Diensten besteht. Diese Architektur soll, dann noch mit einer IaaS Lösung gegenüber gestellt werden.




## Zielsetzung


### Muss

- Die Anforderungen müssen über Verfügbarkeit und Resilienz analysiert werden.
- Die Anforderungen müssen über Last und Performance analysiert werden.
- Die Anforderungen müssen über Sicherheit und Datenschutz analysiert werden.
- In den Anforderungen muss der Kostenrahmen definiert werden.

- Es muss ein Diagramm der Cloud Architektur erstellt werden.
- Jeder Komponent in der Cloud Architektur muss beschrieben werden, wie es die Anforderungen erfüllt, bzw. Kompromisse eingegangen wurden oder ob es noch offene Fragen gibt.
- Es muss eine Kostenabschätzung der gewählen Cloud Architektur erstellt werden.
- Die Empfohlene Cloud Artchitektur muss Kostenmässig mit einer IaaS Lösung verglichen werden.
- Die Wahl des Cloud Anbieters und der Dienste muss mittels Nutzwertanalyse begründet werden.

### Soll
- Es sollen Dienste mit Ausgabelimit in der Bewertung bevorzugt werden.
- Es sollen Dienste mit Kontrollierbarer Skalierbareit bevorzugt werden.

### Kann

- Das System wird mit OpenTofu als Infrastructure as Code deklariert.
- Definition geeigneter Metriken für das Monitoring, welche die Erfüllung der identifizierten Anforderungen messbar machen.


# Vorgehen
Aus zielen soll die Anforderungen definiert werden. Als Referenz für die Berechnungen der Leistungsparameter nehmen wir downloadzahlen des Spiels: Minecraft.
Statistics

27,728,383 registered users, of which 5,745,560 (20.72%) have bought the game.

In the last 24 hours, 77,468 people registered, and 9,822 people bought the game.




## Re 1.1
Es soll eine Serverless-Architektur entworfen werden, welche eine Verfügbarkeit von mindestens 99.9 % erreicht und Single Points of Failure vermeidet.
## Re 1.2
Die Infrastruktur soll eine Million downloads im Monat ermöglichen. Pro Tag soll eine Peak Leistung von 100'000 Downloads ermöglicht werden.
Der Authentifizierungs Dienst soll 2 Millionen Aktive User speichern 

Vorgehen


# Ergebnisse

# Diskussion

# Empfehlung und Ausblick


# Anhang

## Web Client Prototype

Der Prototype ist auf Github verfügbar im Branch feature/webshop:
https://github.com/VoxelCoreLab/project-alpha-website/tree/feature/webshop


# Glossar


Bedeutung herunterladbares Spiel:

Videospiele im üblichen Sinne, die elektronisch übertragen werden. Sie werden auf ein Gerät mit dauerhaften gewährten Zugriff heruntergeladen. Ausgenommen hiervon sind Spiele, die als Wetten, Glücksspiele, Lotterie usw. gelten. (Quelle Stripe)

# Notizen

## Serverless Datenkbank Services

Firebase Firestore: https://firebase.google.com/docs/firestore/quotas

MongoDB Atlas Flex: https://www.mongodb.com/docs/atlas/billing/atlas-flex-costs/

Neon: https://neon.com/



## Serverless Authentication Services

auth0: https://auth0.com/pricing

firebase auth: https://firebase.google.com/docs/auth/limits, https://cloud.google.com/identity-platform/pricing


## Serverless Storage Services:

AWS S3: https://aws.amazon.com/s3/pricing/?nc=sn&loc=4&refid=6552e9e3-f16d-449d-a95e-e07bdc791281

Firebase Storage: https://firebase.google.com/docs/storage/faqs-storage-changes-announced-sept-2024, https://firebase.google.com/pricing

minio: https://www.min.io/pricing


## Serverless Backend Services:

Railway: https://railway.com/pricing (not serverless its PaaS)

## Serverless Static Site Hosting:

(nicht verwechslen mit App Hosting)

Firebase Hosting: https://firebase.google.com/docs/hosting, https://firebase.google.com/pricing

Azure Static Web Apps: https://azure.microsoft.com/en-us/pricing/details/app-service/static/

Cloudflare Pages: https://pages.cloudflare.com/


Github Pages ist nicht erlaubt für online business / e-commectce / provide SaaS sites: https://docs.github.com/en/pages/getting-started-with-github-pages/github-pages-limits


## Others:

DigitalOcean: https://www.digitalocean.com/

SpacetimeDB: https://spacetimedb.com/pricing

## IaaS Servies:




