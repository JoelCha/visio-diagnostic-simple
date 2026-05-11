# 🎥 Visio-diagnostic-simple

Outil de diagnostic WebRTC pour [visio.numerique.gouv.fr](https://visio.numerique.gouv.fr) — version autonome, sans backend, un seul fichier HTML.

[![License: MIT](https://img.shields.io/badge/License-MIT-green.svg)](LICENSE)
[![GitHub Pages](https://img.shields.io/badge/GitHub%20Pages-ready-blue)](https://pages.github.com)

---

## Ce que ça teste

| Test | Description |
|---|---|
| Connectivité HTTPS | Serveur applicatif, signaling LiveKit, CoTurn |
| Capacités WebRTC | RTCPeerConnection, getUserMedia, getDisplayMedia, WebSocket, AudioContext |
| Candidats ICE | STUN public (srflx), TURN relay, local (host) |
| Export journal | Téléchargement du rapport en `.txt` |

> Les tests TCP/UDP sur les ports exacts (7881, 50000–60000…) nécessitent la [version complète avec backend Node.js](https://github.com/<votre-user>/visio-diagnostic).

---

## Utilisation

### Option 1 — GitHub Pages (recommandé)

Accessible directement sur `https://<user>.github.io/visio-diagnostic-simple` — aucune installation.

### Option 2 — En local via un serveur HTTP

> ⚠️ Ne pas ouvrir `index.html` en double-clic (`file://`) — les tests HTTPS vers des domaines externes seront bloqués par le navigateur.

```bash
# Python
python3 -m http.server 8080
# puis ouvrir http://localhost:8080

# Node.js
npx serve .
```

---

## Déploiement sur GitHub Pages

1. Forkez ou clonez ce repo
2. Settings → Pages → Source : **Deploy from branch `main`**
3. C'est en ligne en 2 minutes

---

## Structure

```
visio-diagnostic-simple/
├── index.html   ← tout-en-un, aucune dépendance
├── LICENSE
└── README.md
```

---

## Débogage WebRTC

- **Chrome** : `chrome://webrtc-internals/`
- **Firefox** : `about:webrtc`

---

## Contact

📧 [reseau-visio@numerique.gouv.fr](mailto:reseau-visio@numerique.gouv.fr)

---

## Licence

[MIT](LICENSE)
