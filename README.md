# 🎥 Visio-diagnostic-simple

Outil de diagnostic WebRTC pour tester la connectivité vers [visio.numerique.gouv.fr](https://visio.numerique.gouv.fr).

Version autonome — **un seul fichier HTML, aucune dépendance, aucune installation**.

[![License: MIT](https://img.shields.io/badge/License-MIT-green.svg)](LICENSE)
[![GitHub Pages](https://img.shields.io/badge/GitHub%20Pages-ready-blue)](https://pages.github.com)

---

## Démonstration

👉 **[Accéder à l'outil en ligne](https://joelcha.github.io/visio-diagnostic-simple)**

---

## Ce que ça teste

| Test | Description |
|---|---|
| Connectivité HTTPS | Serveur applicatif, signaling LiveKit, CoTurn |
| Capacités WebRTC | RTCPeerConnection, getUserMedia, getDisplayMedia, WebSocket, AudioContext |
| Candidats ICE | STUN public (srflx), TURN relay, local (host) |
| Export journal | Téléchargement du rapport en `.txt` |

> Les tests TCP/UDP sur les ports exacts (7881, 50000–60000…) nécessitent la [version complète avec backend Node.js](https://github.com/joelcha/visio-diagnostic).

---

## Utilisation

### En ligne

Ouvrez directement l'outil : **[joelcha.github.io/visio-diagnostic-simple](https://joelcha.github.io/visio-diagnostic-simple)**

Aucune installation requise.

### En local

> ⚠️ Ne pas ouvrir `index.html` en double-cliquant dessus — les tests seront bloqués par le navigateur en protocole `file://`. Il faut le servir via un serveur HTTP local :

```bash
# Python (disponible par défaut sur Linux/macOS)
python3 -m http.server 8080
# puis ouvrir http://localhost:8080

# Node.js
npx serve .
```

### Sur votre propre serveur ou GitHub Pages

Copiez simplement `index.html` à la racine de votre hébergement ou de votre dépôt GitHub Pages.

Pour GitHub Pages : Settings → Pages → Source : branch `main` → Save.

---

## Débogage WebRTC

Si les tests ICE échouent, consultez les logs WebRTC de votre navigateur :

- **Chrome** : `chrome://webrtc-internals/`
- **Firefox** : `about:webrtc`

---

## Contribuer

Les contributions sont les bienvenues — issues, pull requests, suggestions.

---

## Contact

📧 [joel@jchastagnier.fr](mailto:joel@jchastagnier.fr)

---

## Licence

[MIT](LICENSE) — libre d'utilisation, modification et redistribution, y compris à des fins commerciales.
