# CRM-System Dokumentation

## Übersicht

Dieses CRM-System ist eine umfassende Multi-Mandanten-Lösung für Unternehmen verschiedener Größen. Das System bietet ein differenziertes Rollensystem mit sechs verschiedenen Benutzertypen und unterstützt sowohl mandantenspezifische als auch mandantenübergreifende Verwaltung.

## Rollensystem-Übersicht

Das System verfügt über **6 Hauptrollen** mit unterschiedlichen Berechtigungen:

### 1. Administratoren (2 Typen)
- **Super-Admin**: Mandantenübergreifende Vollzugriffe, Systemverwaltung
- **Mandanten-Admin**: Vollzugriffe nur innerhalb eines spezifischen Mandanten

### 2. C-Level
- Höhere Rechte als Management
- Mandantenübergreifend möglich
- Benutzerverwaltung und strategische Funktionen

### 3. Management
- Führungskräfte und HR-Personal
- Erweiterte Rechte für Personalverwaltung und Berichtswesen

### 4. Operative
- Standard-Mitarbeiter mit Gruppenzuordnung
- Angepasste Menüs basierend auf Gruppenzugehörigkeit

### 5. Kunden
- Zugriff auf das Kundenportal
- Selbstservice-Funktionen und Ticketing

### 6. Lieferanten
- Zugriff auf das Lieferantenportal
- Ausschreibungsmanagement und Angebotserstellung

## Architektur

- **Multi-Mandanten-Architektur**: Vollständige Datentrennung zwischen Mandanten
- **Rollenbasierte Zugriffskontrolle (RBAC)**: Granulare Berechtigungsverwaltung
- **Portal-Integration**: Separate Portale für Kunden und Lieferanten

## Dokumentation

- [Detailliertes Rollensystem](docs/roles.md)
- [Systemarchitektur](docs/architecture.md)
- [Authentifizierung & Demo-Benutzer](docs/authentication.md)

## Erste Schritte

1. Lesen Sie die [Rollensystem-Dokumentation](docs/roles.md) für detaillierte Berechtigungen
2. Verstehen Sie die [Multi-Mandanten-Architektur](docs/architecture.md)
3. Nutzen Sie die [Demo-Benutzer](docs/authentication.md) zum Testen

## Support

Für Fragen zur Dokumentation oder zum System wenden Sie sich an das Entwicklungsteam.