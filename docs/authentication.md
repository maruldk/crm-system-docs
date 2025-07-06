# Authentifizierung und Demo-Benutzer

## Übersicht

Das CRM-System implementiert ein robustes Authentifizierungssystem mit verschiedenen Anmeldemethoden und vorkonfigurierten Demo-Benutzern für jede Rolle. Diese Dokumentation beschreibt die Authentifizierungsmechanismen und stellt die Demo-Benutzer für Testzwecke vor.

## Authentifizierungsmethoden

### Standard-Authentifizierung

#### Benutzername/Passwort
- **Primäre Methode**: E-Mail-Adresse als Benutzername
- **Passwort-Richtlinien**: 
  - Mindestens 8 Zeichen
  - Kombination aus Groß-/Kleinbuchstaben, Zahlen und Sonderzeichen
  - Keine Wiederverwendung der letzten 5 Passwörter
  - Automatische Sperrung nach 5 fehlgeschlagenen Versuchen

#### Multi-Factor Authentication (MFA)
- **TOTP (Time-based One-Time Password)**: Google Authenticator, Authy
- **SMS-Verifizierung**: Backup-Methode für TOTP
- **E-Mail-Verifizierung**: Zusätzliche Sicherheitsebene
- **Hardware-Token**: FIDO2/WebAuthn für höchste Sicherheitsanforderungen

### Enterprise-Integration

#### Single Sign-On (SSO)
- **SAML 2.0**: Integration mit Active Directory, Azure AD
- **OAuth 2.0/OpenID Connect**: Google Workspace, Microsoft 365
- **LDAP**: Anbindung an Unternehmensverzeichnisse
- **Just-in-Time (JIT) Provisioning**: Automatische Benutzererstellung

#### Identity Provider
- **Azure Active Directory**: Microsoft-Umgebungen
- **Google Workspace**: Google-basierte Organisationen
- **Okta**: Spezialisierte Identity-Management-Lösung
- **Auth0**: Flexible Authentifizierungsplattform

## Demo-Benutzer

### Mandant: "Demo Corp"
**Mandanten-ID**: demo-corp-001

### 1. Super-Admin

**Benutzerdaten:**
- **E-Mail**: superadmin@democorp.com
- **Passwort**: SuperAdmin2024!
- **Name**: Max Mustermann
- **Rolle**: Super-Administrator
- **MFA**: Deaktiviert (nur für Demo)

**Zugriffsbereiche:**
- Alle Mandanten
- Systemkonfiguration
- Globale Benutzerverwaltung
- Systemweite Berichte
- Backup/Restore-Funktionen

**Demo-Szenarien:**
- Neuen Mandanten erstellen
- Systemweite Konfiguration ändern
- Mandantenübergreifende Berichte generieren
- Benutzerrollen global verwalten

### 2. Mandanten-Admin

**Benutzerdaten:**
- **E-Mail**: admin@democorp.com
- **Passwort**: TenantAdmin2024!
- **Name**: Anna Administrator
- **Rolle**: Mandanten-Administrator
- **Mandant**: Demo Corp

**Zugriffsbereiche:**
- Vollzugriff auf Demo Corp Mandant
- Benutzerverwaltung innerhalb des Mandanten
- Mandantenspezifische Konfiguration
- Rollenverteilung (außer Super-Admin)

**Demo-Szenarien:**
- Neue Benutzer im Mandanten anlegen
- Rollen zuweisen und verwalten
- Mandantenspezifische Einstellungen konfigurieren
- Berichte für den Mandanten erstellen

### 3. C-Level

**Benutzerdaten:**
- **E-Mail**: ceo@democorp.com
- **Passwort**: CLevel2024!
- **Name**: Dr. Christina Executive
- **Rolle**: C-Level (CEO)
- **Abteilung**: Geschäftsführung

**Zugriffsbereiche:**
- Strategische Dashboards
- Executive Reporting
- Benutzerverwaltung (Management und darunter)
- Budgetplanung und Finanzberichte
- KPI-Übersichten

**Demo-Szenarien:**
- Executive Dashboard einsehen
- Strategische Berichte generieren
- Management-Rollen zuweisen
- Unternehmensweite KPIs analysieren

### 4. Management

#### HR-Manager
**Benutzerdaten:**
- **E-Mail**: hr.manager@democorp.com
- **Passwort**: HRManager2024!
- **Name**: Sandra Personalerin
- **Rolle**: Management (HR)
- **Abteilung**: Human Resources

**Zugriffsbereiche:**
- Personalverwaltung
- Mitarbeiterbetreuung
- Leistungsbeurteilungen
- HR-Berichte
- Genehmigungsprozesse

#### Vertriebsleiter
**Benutzerdaten:**
- **E-Mail**: sales.manager@democorp.com
- **Passwort**: SalesManager2024!
- **Name**: Robert Verkäufer
- **Rolle**: Management (Vertrieb)
- **Abteilung**: Sales

**Zugriffsbereiche:**
- Vertriebsteam-Management
- Sales-Pipeline-Übersicht
- Umsatzberichte
- Kundensegmentierung
- Verkaufsziele und Forecasting

**Demo-Szenarien:**
- Team-Performance überwachen
- Mitarbeiterbeurteilungen durchführen
- Abteilungsberichte erstellen
- Genehmigungsprozesse bearbeiten

### 5. Operative Mitarbeiter

#### Vertriebsmitarbeiter
**Benutzerdaten:**
- **E-Mail**: sales.rep@democorp.com
- **Passwort**: SalesRep2024!
- **Name**: Thomas Verkauf
- **Rolle**: Operativ (Vertrieb)
- **Gruppe**: Sales Team

**Zugriffsbereiche:**
- CRM-Funktionen
- Lead-Management
- Kundenkontakte
- Opportunity-Tracking
- Verkaufsberichte

#### Support-Mitarbeiter
**Benutzerdaten:**
- **E-Mail**: support@democorp.com
- **Passwort**: Support2024!
- **Name**: Lisa Hilfe
- **Rolle**: Operativ (Support)
- **Gruppe**: Customer Support

**Zugriffsbereiche:**
- Ticketing-System
- Kundensupport-Tools
- Wissensdatenbank
- Chat-Support
- Support-Berichte

#### Marketing-Mitarbeiter
**Benutzerdaten:**
- **E-Mail**: marketing@democorp.com
- **Passwort**: Marketing2024!
- **Name**: Julia Werbung
- **Rolle**: Operativ (Marketing)
- **Gruppe**: Marketing Team

**Zugriffsbereiche:**
- Kampagnenmanagement
- Lead-Generierung
- Marketing-Analytics
- Content-Management
- Social Media Tools

**Demo-Szenarien:**
- Kundenkontakte bearbeiten
- Tickets erstellen und bearbeiten
- Kampagnen durchführen
- Tägliche operative Aufgaben

### 6. Externe Benutzer

#### Kunde
**Benutzerdaten:**
- **E-Mail**: kunde@beispielfirma.com
- **Passwort**: Customer2024!
- **Name**: Peter Kunde
- **Rolle**: Kunde
- **Unternehmen**: Beispiel GmbH

**Portal-Zugriff:**
- Kundenportal-Dashboard
- Ticket-Erstellung und -Verfolgung
- Bestellhistorie
- Rechnungen und Dokumente
- Kontaktdaten-Verwaltung

#### Lieferant
**Benutzerdaten:**
- **E-Mail**: lieferant@zulieferer.com
- **Passwort**: Supplier2024!
- **Name**: Michael Lieferant
- **Rolle**: Lieferant
- **Unternehmen**: Zulieferer AG

**Portal-Zugriff:**
- Lieferantenportal-Dashboard
- Ausschreibungsübersicht
- Angebotserstellung
- Auftragsverfolgung
- Dokumentenmanagement

**Demo-Szenarien:**
- Kundenportal-Funktionen testen
- Tickets erstellen und verfolgen
- Ausschreibungen einsehen
- Angebote erstellen und abgeben

## Sicherheitsfeatures

### Session-Management

#### Session-Konfiguration
- **Session-Timeout**: 8 Stunden Inaktivität
- **Concurrent Sessions**: Maximal 3 gleichzeitige Sitzungen
- **Session-Invalidierung**: Bei Passwort-Änderung
- **Secure Cookies**: HTTPOnly und Secure Flags

#### Token-Management
- **JWT-Token**: 1 Stunde Gültigkeit
- **Refresh-Token**: 30 Tage Gültigkeit
- **Token-Rotation**: Automatische Erneuerung
- **Token-Revocation**: Sofortige Ungültigkeitserklärung

### Audit und Compliance

#### Login-Protokollierung
- **Erfolgreiche Anmeldungen**: Zeitstempel, IP-Adresse, User-Agent
- **Fehlgeschlagene Versuche**: Brute-Force-Erkennung
- **Anomalie-Erkennung**: Ungewöhnliche Anmeldemuster
- **Compliance-Berichte**: DSGVO-konforme Protokollierung

#### Passwort-Sicherheit
- **Passwort-Hashing**: bcrypt mit Salt
- **Passwort-Historie**: Verhindert Wiederverwendung
- **Passwort-Stärke-Meter**: Echtzeit-Bewertung
- **Kompromittierte Passwörter**: Abgleich mit bekannten Breaches

## Entwicklung und Testing

### Test-Umgebungen

#### Staging-Umgebung
- **URL**: https://staging-crm.democorp.com
- **Datenbank**: Separate Staging-Datenbank
- **Features**: Alle Produktionsfeatures aktiviert
- **Reset**: Täglicher Reset der Demo-Daten

#### Development-Umgebung
- **URL**: https://dev-crm.democorp.com
- **Datenbank**: Entwicklungs-Datenbank
- **Features**: Experimentelle Features verfügbar
- **Reset**: Wöchentlicher Reset

### API-Testing

#### Authentication Endpoints
```
POST /api/auth/login
POST /api/auth/logout
POST /api/auth/refresh
POST /api/auth/forgot-password
POST /api/auth/reset-password
GET  /api/auth/profile
```

#### Demo-API-Keys
- **Development**: `dev_key_12345abcdef`
- **Staging**: `staging_key_67890ghijkl`
- **Rate Limit**: 1000 Requests/Stunde

## Troubleshooting

### Häufige Probleme

#### Anmeldung fehlgeschlagen
1. **Passwort vergessen**: Reset-Link über "Passwort vergessen"
2. **Account gesperrt**: Kontakt zum Administrator
3. **MFA-Probleme**: Backup-Codes verwenden
4. **Browser-Cache**: Cache leeren und erneut versuchen

#### Session-Probleme
1. **Session abgelaufen**: Erneute Anmeldung erforderlich
2. **Concurrent Session Limit**: Andere Sitzungen beenden
3. **Cross-Origin Issues**: CORS-Konfiguration prüfen

### Support-Kontakte

#### Technischer Support
- **E-Mail**: support@democorp.com
- **Telefon**: +49 (0) 123 456-789
- **Chat**: Verfügbar Mo-Fr 9:00-17:00

#### Notfall-Kontakt
- **24/7 Hotline**: +49 (0) 123 456-999
- **Kritische Systeme**: Sofortige Eskalation
- **Security Incidents**: security@democorp.com

## Best Practices

### Für Administratoren
1. **Regelmäßige Passwort-Updates**: Alle 90 Tage
2. **MFA aktivieren**: Für alle privilegierten Accounts
3. **Session-Monitoring**: Verdächtige Aktivitäten überwachen
4. **Backup-Accounts**: Notfall-Zugriff sicherstellen

### Für Endbenutzer
1. **Starke Passwörter**: Passwort-Manager verwenden
2. **Sichere Verbindungen**: Nur HTTPS verwenden
3. **Logout**: Sitzung nach Nutzung beenden
4. **Verdächtige Aktivitäten**: Sofort melden

### Für Entwickler
1. **API-Keys sicher**: Niemals in Code committen
2. **Test-Daten**: Keine Produktionsdaten verwenden
3. **Logging**: Sensible Daten nicht protokollieren
4. **Updates**: Regelmäßige Sicherheitsupdates