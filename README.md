# 📱 Wellbeing Tracker - Native Android App

## ✅ Was du jetzt hast:

Eine **komplett saubere** Wellbeing Tracker App ohne Testdaten, bereit für die Umwandlung in eine native Android App!

---

## 🚀 Installation als Android App

### **Schritt 1: Dateien auf GitHub Pages hochladen**

Du hast bereits einen GitHub Account und ein Repository erstellt. Jetzt musst du diese Dateien hochladen:

1. Gehe zu deinem Repository auf GitHub
2. Klicke **"Add file"** → **"Upload files"**
3. Lade **alle** diese Dateien hoch:
   - `index.html`
   - `manifest.json`
   - `sw.js`
   - `icon-192.png`
   - `icon-512.png`

4. Klicke **"Commit changes"**
5. **Warte 1-2 Minuten** (GitHub Pages braucht etwas Zeit)
6. Teste deine URL: `https://DEIN-USERNAME.github.io/wellbeing-tracker/`

---

### **Schritt 2: APK mit PWABuilder generieren**

1. Gehe zu **https://www.pwabuilder.com/**
2. Füge deine GitHub Pages URL ein:
   ```
   https://DEIN-USERNAME.github.io/wellbeing-tracker/
   ```
3. Klicke **"Start"**
4. PWABuilder analysiert deine App
5. Klicke auf **"Android"** → **"Generate Package"**
6. Lade die **APK-Datei** herunter

---

### **Schritt 3: APK auf Android installieren**

#### **Option A: Direkt auf dem Handy**
1. Lade die APK auf dein Handy (z.B. per E-Mail oder USB)
2. Öffne die APK-Datei
3. Bestätige **"Aus unbekannten Quellen installieren"**
4. Installiere die App

#### **Option B: Via ADB (für Entwickler)**
```bash
adb install wellbeing-tracker.apk
```

---

## 🔔 Benachrichtigungen aktivieren

Nach der Installation:

1. Öffne die App
2. Gehe zu **"Verwalten"** (⚙️ Tab)
3. Klicke **"Benachrichtigungen aktivieren 🔔"**
4. Erlaube Benachrichtigungen in den Einstellungen

Die App sendet dir dann:
- **Tägliche Stimmungsabfrage** (Standard: 21:00 Uhr)
- **Wöchentlicher Check-in** (Standard: Montag 09:00 Uhr)
- **Wöchentlicher Checkout** (Standard: Sonntag 18:00 Uhr)

Du kannst alle Zeiten in den Einstellungen anpassen!

---

## 🎯 Features

### **Tägliches Tracking**
- ✅ Stimmung erfassen (5 Stufen)
- ✅ Notizen zum Tag
- ✅ Routinen abhaken (nach Kategorie)

### **Intelligente Wochenreflexion**
- 🌟 **Check-in (Montag)**: Zusammenfassung letzte Woche + personalisierte Empfehlungen
- 📊 **Checkout (Sonntag)**: Wochenrückblick + Lebensrad-Update

### **Algorithmen**
- 📈 Stimmungsanalyse (7-Tage-Durchschnitt)
- 🎯 Lebensrad-Gap-Analyse
- 💪 Routinen-Performance-Tracking
- 🔥 Trend-Erkennung

### **Kategorien**
- 🏃 Körperlich
- 🧠 Geistig
- ❤️ Sozial
- 🌿 Spirituell
- 📋 Alltägliches

### **Lebensbereiche**
- 💪 Gesundheit
- ❤️ Liebe
- 👥 Soziales
- 💼 Karriere
- 🌱 Persönliche Entwicklung
- 🎉 Spaß & Freizeit
- 💰 Finanzen

---

## 📊 Datenstruktur

Alle Daten werden **lokal** im Browser/App gespeichert:

```javascript
{
  routines: [],           // Deine Routinen
  moods: [],             // Stimmungsverlauf
  completions: {},       // Abgehakte Routinen pro Tag
  lifeWheel: {},         // Lebensrad-Werte + Historie
  weeklyChecks: {},      // Check-ins/Checkouts pro Woche
  settings: {}           // Erinnerungszeiten
}
```

**Wichtig:** 
- Daten sind **nicht geräteübergreifend** synchronisiert
- Bei App-Deinstallation gehen Daten verloren
- Backup-Funktion kommt in zukünftiger Version

---

## 🛠️ Problemlösung

### **PWABuilder meldet "Keine PWA erkannt"**
Das ist normal beim ersten Mal. Lösungen:

1. **Cache leeren:** Öffne die URL im Inkognito-Modus
2. **Warten:** GitHub Pages braucht manchmal 5-10 Minuten
3. **Prüfen:** Sind alle 5 Dateien hochgeladen?

### **Benachrichtigungen funktionieren nicht**
- ✅ Hast du die Berechtigung erteilt?
- ✅ Ist die App im Vordergrund?
- ✅ Android: Batterie-Optimierung deaktiviert?

### **App lädt nicht**
- Prüfe deine GitHub Pages URL
- Schau in die Browser-Konsole (F12)
- Stelle sicher, dass alle Dateien korrekt hochgeladen wurden

---

## 🎨 Anpassungen

Du kannst die App einfach anpassen:

### **Farben ändern (in index.html)**
```css
:root {
  --bg: #faf8f5;           /* Hintergrund */
  --primary: #f4a261;      /* Primärfarbe */
  --success: #06d6a0;      /* Erfolg */
  --warning: #fcbf49;      /* Warnung */
  --danger: #e63946;       /* Gefahr */
}
```

### **Standard-Erinnerungszeiten (in index.html)**
```javascript
settings: {
  moodReminder: "21:00",     // Stimmungsabfrage
  checkinDay: 1,             // 1 = Montag
  checkinTime: "09:00",
  checkoutDay: 0,            // 0 = Sonntag
  checkoutTime: "18:00"
}
```

---

## 📝 Changelog

### **Version 1.0** (Februar 2026)
- ✅ Sauberer Start ohne Testdaten
- ✅ PWA-ready mit manifest.json + Service Worker
- ✅ Browser-Benachrichtigungen (Android)
- ✅ Wöchentliche Check-ins mit Algorithmus
- ✅ Wöchentliche Checkouts mit Lebensrad
- ✅ Responsive Design (Smartphone-optimiert)
- ✅ 5 Routinen-Kategorien
- ✅ 7 Lebensbereiche
- ✅ Kalender-Ansicht
- ✅ Fortschritts-Tracking
- ✅ Stimmungs-Charts

---

## 💡 Tipps

1. **Erste Schritte:**
   - Erstelle 3-5 Routinen in verschiedenen Kategorien
   - Setze realistische Ziele im Lebensrad
   - Tracke täglich deine Stimmung

2. **Wöchentliche Reflexion:**
   - Nimm dir Montags 5 Minuten für den Check-in
   - Nutze die Empfehlungen zur Fokussierung
   - Update dein Lebensrad Sonntags ehrlich

3. **Motivation:**
   - Feiere kleine Erfolge (Streaks!)
   - Passe Routinen an, wenn nötig
   - Sei nicht zu streng mit dir selbst

---

## 🚀 Nächste Schritte

1. Lade alle Dateien auf GitHub Pages hoch
2. Teste die App im Browser
3. Generiere die APK mit PWABuilder
4. Installiere auf deinem Android-Handy
5. Aktiviere Benachrichtigungen
6. Beginne mit dem Tracking!

---

**Viel Erfolg auf deinem Wellbeing-Journey! 🌟**
