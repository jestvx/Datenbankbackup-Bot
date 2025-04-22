# 🗄️ MySQL/MariaDB Backup Bot – Installationsanleitung

Ein automatisierter Discord-Bot, der regelmäßig Datenbank-Backups von MySQL oder MariaDB erstellt und direkt in einen Discord-Channel hochlädt.

---

## 📦 Voraussetzungen

- Node.js (empfohlen: v18 oder höher)
- Zugriff auf eine MySQL- oder MariaDB-Datenbank
- Discord-Bot mit Token & korrekten Rechten
- Ein Discord-Channel zum Hochladen der Backups

---

## 🔧 Installation

### 1. Projektdateien bereitstellen

Stelle sicher, dass du alle Dateien des Projekts vom Entwickler oder GitHub erhalten hast.

### 2. Abhängigkeiten installieren

Navigiere in das Projektverzeichnis und installiere alle nötigen Module:

```bash
npm install
```

---

## ⚙️ Konfiguration

Öffne die Datei `config.json` und passe folgende Werte an:

```json
{
  "token": "DEIN_DISCORD_BOT_TOKEN",
  "licensekey": "RECON-XXXXX",
  "backupMode": "interval", 
  "intervalMinutes": 60,  // Zeitintervall für automatische Backups

  "uploadChannelId": "DISCORD_CHANNEL_ID_FÜR_UPLOADS",
  "allowedRoleId": "ROLE_ID_MIT_BACKUP_BERECHTIGUNG",

  "databases": [
    {
      "name": "datenbankname",
      "user": "nutzername",
      "password": "passwort",
      "host": "localhost"
    }
  ]
}
```

> 📌 Hinweis: Du kannst mehrere Datenbanken in der Liste eintragen, wenn gewünscht.

---

## 🚀 Bot starten

```bash
node index.js
```

Wenn alles korrekt eingerichtet ist, wird der Bot automatisch gemäß `intervalMinutes` ein Backup erstellen und es im angegebenen Discord-Channel posten.

---

## 🛠 Manuelle Nutzung (optional)

Falls vorgesehen, kann der Bot auch per Befehl manuell ein Backup auslösen (sofern `allowedRoleId` vergeben ist).

---

## 📂 Backup-Aufbau

Die gesendeten Backups enthalten:

- Name der Datenbank
- Zeitstempel
- `.sql` Datei als Anhang
- Embed-Nachricht mit Details

---

## ❗ Lizenz

Dieser Bot erfordert einen gültigen Lizenzschlüssel. Ohne diesen funktioniert der Bot nicht.

---

## 📬 Support

Fragen, Hilfe oder Lizenzanfragen?  
➡️ Erstelle ein Ticket auf unserem [Support-Discord](https://discord.gg/DEININVITE)

---
