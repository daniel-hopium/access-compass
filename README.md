# Rechte-Kompass – Login und Rechte zum Anfassen

53 Lektionen zu Authentifizierung und Autorisierung: Sessions, JWT, OAuth 2.0, OpenID
Connect, PKCE, BFF, SSO, MFA und Keycloak, dazu die Zugriffsmodelle RBAC, ABAC, PBAC und
ReBAC – und wie man alles in **Angular 22** und **Spring Boot 4 / Spring Security 7**
umsetzt. Auf Deutsch und Englisch.

Online: https://daniel-hopium.github.io/access-compass/

## Starten

`index.html` im Browser öffnen, per Doppelklick. Kein Build, keine Abhängigkeiten. Internet
braucht es nur für die Google-Schriften. Die Token-Beispiele signieren mit `crypto.subtle`;
das geht nur in einem sicheren Kontext, also über `https://` oder `http://localhost`
(z. B. `python -m http.server`).

## Das Beispiel: Nordwind GmbH

Alle Lektionen spielen in derselben kleinen Rechnungs-App. Oben im Kopf wechselst du unter
„Angemeldet als“ die Person – und jedes Live-Beispiel reagiert sofort:

| Person | Rolle | Darf |
|---|---|---|
| Gast | – | nichts, wird zum Login geschickt |
| Vera | `VIEWER` | Rechnungen lesen |
| Tom | `TEAM_LEAD` | eigene Rechnungen freigeben, bis 5 000 € |
| Bea | `ACCOUNTANT` | anlegen, bearbeiten, buchen |
| Ada | `ADMIN` | alles, inklusive Benutzerverwaltung |

## Inhalt

| Kapitel | Lektionen |
|---|---|
| Grundlagen (8) | AuthN vs. AuthZ, Passwörter, Session oder Token, Token-Speicherort, JWT von innen und richtig prüfen, Access/Refresh Token, MFA und Passkeys |
| OAuth 2.0 & OpenID Connect (7) | Rollen in OAuth, Code Flow mit PKCE, OIDC, Scopes vs. Rollen, BFF, SSO und Logout, Keycloak |
| Autorisierung denken (4) | Least Privilege, PEP/PDP/PIP/PAP, Permissions entwerfen, Funktion/Objekt/Feld |
| Zugriffsmodelle (10) | Überblick, RBAC, Hierarchie, Funktionstrennung, Rollen-Explosion, Mandanten, ABAC, PBAC, ReBAC, Modellwahl |
| Angular 22 (11) | angular-auth-oidc-client, AuthStore mit Signals, Interceptor, Guards, `*appCan`, Ausblenden vs. Deaktivieren, Navigation aus Rechten, CASL, Signal Forms, 401/403, Tests |
| Spring Boot & Spring Security (9) | Resource Server, `JwtAuthenticationConverter`, `authorizeHttpRequests`, `@PreAuthorize`, Policy-Bean, `/api/me`, OPA/Cedar/OpenFGA, Client Credentials, Tests |
| Ende zu Ende & Angriffe (4) | Der ganze Weg vom Login bis zum 403, IDOR/BOLA, Manipulation im Frontend, Audit-Log |

Jede Lektion ist gleich aufgebaut: die Regel, „Auf einen Blick“ als Tabelle, ein
Live-Beispiel oder Diagramm, „So nicht – so“ als Code, weiterer Code mit Erklärung,
Richtig/Falsch, „Warum?“ und Links zur Quelle. Dazu ein Glossar unter `#glossar`.

## Bedienung

- **Sprache:** „English“ / „Deutsch“ oben rechts; steht als `?lang=en` in der Adresse.
- Jede Lektion hat eine eigene Adresse (`#jwt`), der Zurück-Button funktioniert.
- Lektionen lassen sich als gelernt markieren; der Stand bleibt im Browser.
- Hell/dunkel folgt dem System, der Knopf mit Sonne/Mond legt es fest.
- Der Breite-Knopf daneben lässt die Lektion die ganze Spalte füllen; am Griff rechts lässt
  sich jede Breite dazwischen ziehen.

## Aufbau

Alles steckt in einer Datei:

- **Domäne:** `PERMS`, `ROLES`, `PERSONAS`, `INVOICES` und `can()` – die Rechte-Logik, die
  alle Beispiele teilen.
- **`CHAPTERS`** und **`LESSONS`**: ein Objekt pro Lektion mit Regel, Tabelle, Demo samt
  `init()`, Code-Paaren (`bad`/`good`) und eigenem CSS.
- **Bausteine:** `table()`, `chain()`, `seq()` (Sequenzdiagramm), `stepperHTML()`,
  `verdict()`, `quizHTML()` und `miniHTML()` (die Mini-Rechnungs-App).
- **Icons:** `tools/make_icons.py` erzeugt Favicon und Apple-Touch-Icon.

Teil einer Reihe mit [Angular-Patterns](https://daniel-hopium.github.io/angular-patterns/),
dem [ARIA-Kompass](https://daniel-hopium.github.io/aria-compass/), dem
[HTML-Atlas](https://daniel-hopium.github.io/html-atlas/), dem
[CSS-Atlas](https://daniel-hopium.github.io/css-atlas/) und dem
[UI-Atlas](https://daniel-hopium.github.io/ui-atlas/). Die App-Hülle stammt aus dem UI-Atlas.
