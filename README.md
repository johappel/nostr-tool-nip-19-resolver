# NIP-19 naddr Resolver

Einfache statische Seite zum Dekodieren von Nostr `naddr`-Zeichenketten gemäß [NIP-19](https://github.com/nostr-protocol/nostr/blob/master/nips/19.md).

## Features

- Zerlegt eine `naddr` in ihre TLV-Bestandteile:
  - `identifier` – der `d`-Tag des adressierbaren Events
  - `pubkey` – öffentlicher Schlüssel des Autors (Hex)
  - `kind` – Event-Typ (Zahl)
  - `relays` – optionale Relay-URLs
- Vollständig clientseitig – **keine externen Abhängigkeiten**
- Syntax-hervorgehobene JSON-Ausgabe
- Live-Dekodierung während der Eingabe

## Lokale Vorschau

Einfach `index.html` im Browser öffnen – kein Build-Schritt nötig.

## Deployment (GitHub Pages)

1. Repo auf GitHub pushen
2. **Settings → Pages → Source: GitHub Actions** wählen
3. Der Workflow `.github/workflows/pages.yml` deployt bei jedem Push auf `main` automatisch

## Technisches

Der bech32-Decoder und der TLV-Parser sind vollständig in Vanilla-JavaScript implementiert (keine npm-Pakete).  
Unterstützt werden ausschließlich `naddr`-Zeichenketten; andere NIP-19-Typen werden abgewiesen.

## Lizenz

MIT
