# Angebot·AI — Deployment Guide

## Was du hast
- `index.html` — Die komplette Web-App (single file, kein Build nötig)
- `manifest.json` — PWA-Manifest (App installierbar auf iOS/Android)
- `sw.js` — Service Worker (Offline-Unterstützung)

## In 5 Minuten live auf Vercel

1. **Erstelle ein GitHub-Repo** und lade diese 3 Dateien hoch
2. **Gehe zu vercel.com** → "Add New Project" → Repo auswählen
3. Framework: **Other** (kein Build-Step nötig)
4. Deploy klicken → fertig ✓

Deine App ist live unter `https://dein-name.vercel.app`

## Domain verbinden
- Kaufe `angebotai.at` oder `angebot.ai` bei Porkbun/Namecheap (~€15/Jahr)
- In Vercel: Settings → Domains → Custom Domain hinzufügen
- DNS-Eintrag setzen wie von Vercel angegeben

## PWA (App installierbar machen)
Die App ist bereits PWA-fähig. User können sie über den Browser installieren:
- **iPhone/iPad**: Safari → Teilen → "Zum Home-Bildschirm"
- **Android**: Chrome → Menü → "App installieren"
- **Desktop (Chrome/Edge)**: Adressleiste → App-Symbol

Für echte App-Icons brauchst du noch:
- `icon-192.png` (192×192px, dein Logo)
- `icon-512.png` (512×512px, dein Logo)

## Stripe Integration (Zahlungen)
Ersetze die Paywall-Buttons mit Stripe Checkout Links:

```javascript
// In den plan-card onclick-Handlers:
window.location.href = 'https://buy.stripe.com/dein-link-hier';
```

Stripe-Links erstellst du in deinem Stripe Dashboard unter "Payment Links".

## Nächste Schritte
1. Icons erstellen (Canva reicht)
2. Vercel deployen
3. Domain verbinden  
4. Stripe-Links einbauen
5. Erste 10 User gewinnen (LinkedIn, Slack, Reddit)

---
Powered by Claude Sonnet · Built with Angebot·AI
