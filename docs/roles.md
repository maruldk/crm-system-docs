# Rollensystem - Detaillierte Dokumentation

## Übersicht

Das CRM-System implementiert ein sechsstufiges Rollensystem mit differenzierten Berechtigungen. Jede Rolle hat spezifische Zugriffs- und Funktionsrechte, die auf die jeweiligen Geschäftsanforderungen zugeschnitten sind.

## 1. Administratoren

### Super-Admin
- **Berechtigungen**: Vollzugriff auf alle Mandanten und Systemfunktionen
- **Zuständigkeiten**:
  - Systemkonfiguration und -wartung
  - Mandantenverwaltung (Erstellen, Bearbeiten, Löschen)
  - Globale Benutzerverwaltung
  - Systemweite Berichte und Analytics
  - Backup- und Wiederherstellungsoperationen
- **Einschränkungen**: Keine
- **Mandantenzugriff**: Alle Mandanten

### Mandanten-Admin
- **Berechtigungen**: Vollzugriff nur innerhalb eines spezifischen Mandanten
- **Zuständigkeiten**:
  - Mandantenspezifische Konfiguration
  - Benutzerverwaltung innerhalb des Mandanten
  - Rollenverteilung (außer Super-Admin)
  - Mandantenspezifische Berichte
  - Datenimport/-export für den Mandanten
- **Einschränkungen**: Kein Zugriff auf andere Mandanten oder Systemfunktionen
- **Mandantenzugriff**: Ein spezifischer Mandant

## 2. C-Level

- **Berechtigungen**: Höhere Rechte als Management, mandantenübergreifend möglich
- **Zuständigkeiten**:
  - Strategische Entscheidungen und Planung
  - Benutzerverwaltung (außer Admin-Rollen)
  - Zugriff auf alle Geschäftsbereiche
  - Executive Dashboards und KPI-Übersichten
  - Budgetplanung und Finanzberichte
  - Mandantenübergreifende Analysen (falls berechtigt)
- **Einschränkungen**: Keine Systemadministration
- **Mandantenzugriff**: Ein oder mehrere Mandanten (konfigurierbar)

## 3. Management

- **Berechtigungen**: Erweiterte Rechte für Führungskräfte und HR-Personal
- **Zuständigkeiten**:
  - Personalverwaltung und HR-Funktionen
  - Teamleitung und Mitarbeiterbetreuung
  - Berichtswesen für den Verantwortungsbereich
  - Genehmigungsprozesse
  - Projektmanagement
  - Leistungsbeurteilungen
- **Einschränkungen**: Keine Benutzerverwaltung, begrenzte Systemkonfiguration
- **Mandantenzugriff**: Ein Mandant

## 4. Operative

- **Berechtigungen**: Standard-Mitarbeiterrechte mit Gruppenzuordnung
- **Zuständigkeiten**:
  - Tägliche operative Aufgaben
  - Kundenkontakt und -betreuung
  - Dateneingabe und -pflege
  - Bearbeitung von Tickets und Anfragen
  - Nutzung von Standardberichten
- **Gruppenzuordnung**: 
  - Vertrieb: CRM-Funktionen, Lead-Management
  - Support: Ticketing, Kundensupport
  - Marketing: Kampagnenmanagement, Analytics
  - Buchhaltung: Rechnungswesen, Zahlungsabwicklung
- **Einschränkungen**: Keine Administrationsrechte, gruppenspezifische Menüs
- **Mandantenzugriff**: Ein Mandant

## 5. Kunden

- **Berechtigungen**: Zugriff auf das Kundenportal
- **Zuständigkeiten**:
  - Selbstservice-Funktionen
  - Ticket-Erstellung und -Verfolgung
  - Bestellhistorie und Rechnungen einsehen
  - Kontaktdaten aktualisieren
  - Wissensdatenbank nutzen
  - Support-Chat und Kommunikation
- **Portal-Funktionen**:
  - Dashboard mit Kontoübersicht
  - Dokumenten-Download
  - Terminbuchung
  - Feedback und Bewertungen
- **Einschränkungen**: Nur eigene Daten einsehbar, keine internen Systemfunktionen
- **Mandantenzugriff**: Zugeordneter Mandant

## 6. Lieferanten

- **Berechtigungen**: Zugriff auf das Lieferantenportal
- **Zuständigkeiten**:
  - Ausschreibungsmanagement
  - Angebotserstellung und -abgabe
  - Auftragsverfolgung
  - Rechnungsstellung
  - Produktkatalog-Pflege
  - Kommunikation mit Einkauf
- **Portal-Funktionen**:
  - Ausschreibungsübersicht
  - Angebotsvorlagen
  - Dokumentenmanagement
  - Qualitätszertifikate hochladen
  - Liefertermin-Tracking
- **Einschränkungen**: Nur ausschreibungsbezogene Daten, keine internen Unternehmensdaten
- **Mandantenzugriff**: Zugeordneter Mandant

## Rollenübergänge und Vererbung

### Hierarchie
1. Super-Admin (höchste Berechtigung)
2. Mandanten-Admin
3. C-Level
4. Management
5. Operative
6. Kunden/Lieferanten (externe Rollen)

### Berechtigungsvererbung
- Höhere Rollen erben grundsätzlich die Berechtigungen niedrigerer Rollen
- Ausnahme: Externe Rollen (Kunden/Lieferanten) haben separate Berechtigungsstrukturen
- Mandantenbeschränkungen gelten unabhängig von der Rollenhierarchie

## Sicherheitsrichtlinien

### Rollenzuweisung
- Nur Administratoren können Rollen zuweisen
- C-Level kann Management- und Operative-Rollen verwalten
- Mandanten-Admins können nur innerhalb ihres Mandanten Rollen zuweisen

### Audit und Compliance
- Alle Rollenwechsel werden protokolliert
- Regelmäßige Überprüfung der Rollenzuweisungen
- Automatische Deaktivierung bei Inaktivität

### Datenschutz
- Rollenbasierte Datenzugriffskontrolle
- Mandantentrennung auf Datenbankebene
- Verschlüsselung sensibler Daten

## Konfiguration und Anpassung

### Gruppenspezifische Menüs (Operative)
- Konfigurierbare Menüstrukturen pro Gruppe
- Dynamische Rechtevergabe basierend auf Gruppenzugehörigkeit
- Anpassbare Dashboards und Widgets

### Portal-Anpassungen
- Mandantenspezifisches Branding für Kunden-/Lieferantenportale
- Konfigurierbare Funktionen und Workflows
- Integration mit externen Systemen

## Best Practices

1. **Prinzip der minimalen Berechtigung**: Benutzer erhalten nur die notwendigen Rechte
2. **Regelmäßige Überprüfung**: Rollenzuweisungen quartalsweise überprüfen
3. **Dokumentation**: Alle Rollenwechsel dokumentieren
4. **Schulung**: Benutzer über ihre Rollenrechte informieren
5. **Monitoring**: Verdächtige Aktivitäten überwachen