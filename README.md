# Schritt-für-Schritt-Einführung in das Web-Framework [Spring MVC]

**Der Kurs: https://stahe.github.io/de-springmvc-sept-2026/**

Autor des gesamten Codes und des Kurses: **Claude** (KI von Anthropic) im Auftrag von **Serge Tahé** – September 2026.

## Überblick

Dieser Kurs bietet eine Schritt-für-Schritt-Anleitung zur Erstellung von Webanwendungen mit **Spring MVC** (Spring Boot 4), bei denen der Server die HTML-Seiten erzeugt (**Thymeleaf**-Views). Er setzt nur Grundkenntnisse in HTTP, HTML und der Programmiersprache Java voraus.

Er besteht aus zwei Teilen:

- **28 kurze Beispiele**, die sich jeweils auf ein einziges Konzept konzentrieren und in Kapitel gegliedert sind:

| Kapitel | Inhalt | Beispiele |
|---|---|---|
| Controller, Actions, Routing | Vom Browser zur Action: Routen, Antworten, Weiterleitungen, Services und Dependency Injection | 01–06 |
| Das Action-Modell | Request-Parameter: Binding, Konvertierung, Validierung, POST-Requests, eigenes Binding | 07–12 |
| Die View und ihr Modell | Thymeleaf, Templates und Fragmente, Helper, Formulare, Validierung, Post/Redirect/Get | 13–21 |
| Internationalisierung | eine zweisprachige Anwendung (MessageSource, LocaleResolver) | 22 |
| Datenbereiche | Singleton-, Request- und Prototype-Beans; Cookies | 23 |
| Der Lebenszyklus einer Anfrage | Servlet-Filter, Interceptors, `@ControllerAdvice`, Fehlerseite | 24 |
| Authentifizierung und Autorisierung | Spring Security, JWT-Token in einem Cookie, Rollen, CAPTCHA, Rate Limiting | 25–27 |
| Schichtenarchitektur und Datenzugriff | Schichten Web / Geschäftslogik / DAO, Spring Data JPA, Hibernate, MySQL, Transaktionen | 28 |

- **Eine vollständige Fallstudie**: die Anwendung **RdvMedecins** zur Terminplanung in einer Arztpraxis. Sie bietet drei Rollen (Administrator, Ärzte, Patienten), einen Kalender, Funktionen zum Buchen und Stornieren von Terminen, die Verwaltung von Ärzten und Kunden, die Erstellung von Patientenkonten, Schutz vor Bots und eine Oberfläche auf Französisch und Englisch. Jede ihrer Dateien wird im Kurs kommentiert.

## Quellcode

Der Quellcode steht über den Kurs zum Download bereit. Er enthält:

- `exemples/`: die 28 Beispiele, ein Maven-Modul pro Ordner;
- `rdvmedecins2-spring-mvc/`: die Fallstudie.

## Technologien

Java 21 · Spring Boot 4.1 (Spring MVC, Spring Security, Spring Data JPA) · Thymeleaf · Hibernate · MySQL 8 (oder MariaDB) · Maven (Maven Wrapper) · Bootstrap 5.

## Voraussetzungen

- ein JDK 21 (z. B. Eclipse Temurin);
- Visual Studio Code mit den Erweiterungen „Extension Pack for Java“ und „Spring Boot Extension Pack“;
- MySQL 8 (Laragon unter Windows) oder MariaDB, für Beispiel 28 und die Fallstudie;
- curl.

Installationsanleitungen für diese Werkzeuge finden sich in den Anhängen des Kurses.

## Ein Beispiel oder die Fallstudie ausführen

```bash
# ein Beispiel (Port 5000), aus seinem Verzeichnis
cd examples/01-structure
../mvnw spring-boot:run          # Windows: ..\mvnw spring-boot:run

# die Fallstudie (Port 8081), nachdem die Datenbank mit database/dbrdvmedecins2.sql angelegt wurde
cd rdvmedecins2-spring-mvc
./mvnw spring-boot:run           # Windows: mvnw spring-boot:run
```

Beim ersten Start lädt der Maven Wrapper Maven und anschließend die Bibliotheken herunter: Dafür muss eine Internetverbindung bestehen.
