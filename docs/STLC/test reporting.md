### from pathlib import Path

# Inhalt der Markdown-Datei
content = """# Homework – Testplanung:
User Registration & Shop Functions

## 1. Ziel

Ziel dieser Testplanung ist die Überprüfung der grundlegenden 
Benutzer- und Shop-Funktionen eines Websystems.  
Es soll sichergestellt werden, dass Registrierung, Anmeldung,
Navigation, Social-Media-Login und Produktfunktionen erwartungsgemäß 
funktionieren.

---

## 2. Testumgebung

| Komponente | Beschreibung |
|-------------|--------------|
| System | Webapplikation (Frontend + Backend) |
| Browser | Chrome, Firefox, Safari |
| Testdaten | Standardnutzer mit Altersangabe |
| Zahlungsart | Kreditkarte (Testmodus) |

---

## 3. Testobjekte

- Benutzerregistrierung und Authentifizierung  
- Hauptnavigation (Home, Shop, Favoriten)  
- Social-Media-Kontakte  
- Produktanzeige und Kaufprozess  
- Favoriten- und Warenkorbfunktion

---

## 4. Testfälle

### 4.1 Benutzeraktionen

| Nr. | Testfallbeschreibung | Erwartetes Ergebnis | Status |
|-----|----------------------|----------------------|---------|
| TC01 | User registriert sich mit gültigen Daten | Registrierung <br/><br/>erfolgreich | ✅ Erfolg |
| TC02 | User meldet sich mit gültigen Daten an | Anmeldung erfolgreich | ✅ Erfolg |
| TC03 | User meldet sich ab | Abmeldung erfolgreich | ✅ Erfolg |
| TC04 | User registriert sich mit Altersangabe „18 Jahre“ oder älter | Registrierung erlaubt | ✅ Erfolg |
| TC05 | Navigation: Home-Button | Startseite wird geladen | ✅ Erfolg |
| TC06 | Navigation: Shop-Button | Shop-Seite öffnet sich korrekt | ✅ Erfolg |
| TC07 | Navigation: Favoriten-Button | Favoritenseite öffnet sich nicht / Fehlfunktion | ❌ Kein Erfolg |

---

### 4.2 Social-Media & Kontakte

| Nr. | Testfallbeschreibung | Erwartetes Ergebnis | Status |
|-----|----------------------|----------------------|---------|
| TC08 | Login via Facebook (an/abmelden) | Erfolgreiche Anmeldung & Abmeldung | ✅ Erfolg |
| TC09 | Login via Instagram (an/abmelden) | Erfolgreiche Anmeldung & Abmeldung | ✅ Erfolg |
| TC10 | Login via Twitter (an/abmelden) | Erfolgreiche Anmeldung & Abmeldung | ✅ Erfolg |
| TC11 | Login via TikTok (an/abmelden) | Erfolgreiche Anmeldung & Abmeldung | ✅ Erfolg |
| TC12 | Kontaktaufnahme via Telefon | Verbindung hergestellt | ✅ Erfolg |

---

### 4.3 Produkte & Kaufprozess

| Nr. | Testfallbeschreibung | Erwartetes Ergebnis | Status |
|-----|----------------------|----------------------|---------|
| TC13 | Produkte auf Seiten 1–24 werden geladen | Alle Produktseiten werden korrekt angezeigt | ✅ Erfolg |
| TC14 | User wählt Menge ≥ 1 bis max. Lagerbestand | Auswahl möglich und validiert | ✅ Erfolg |
| TC15 | Bezahlung per Karte | Zahlung schlägt fehl | ❌ Kein Erfolg |
| TC16 | Produkt zu Favoriten hinzufügen | Funktion nicht verfügbar / fehlgeschlagen | ❌ Kein Erfolg |

---

## 5. Beobachtungen

- Favoritenfunktion und Kartenzahlung funktionieren **nicht** korrekt.  
- Alle anderen Kernfunktionen (Navigation, Login, Registrierung, Social-Media, Produktanzeige) funktionieren wie erwartet.

---

## 6. Empfehlungen

- Fehleranalyse und Bugfixing für Favoriten-Button und Kreditkartenzahlung durchführen.  
- Nach Fix erneut **Regressionstest** starten.  
- Logging aktivieren, um Fehlerquellen im Backend nachzuvollziehen.  
- Optional: Automatisierte Tests für Login- und Shop-Seiten erstellen.

---

## 7. Fazit

Die Anwendung funktioniert in ihren Kernbereichen stabil.  
Es bestehen **zwei kritische Defekte**:
1. Favoritenfunktion (nicht verfügbar)  
2. Kreditkartenzahlung (nicht funktionsfähig)  

Alle übrigen Funktionen sind erfolgreich getestet worden.
"""

# Datei speichern
file_path = Path("/mnt/data/Homework_Testplan_User_Registration_and_Shop.md")
file_path.write_text(content, encoding="utf-8")

file_path
