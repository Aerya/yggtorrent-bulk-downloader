# 📥 YggTorrent Bulk Downloader

Un userscript pour [Violentmonkey](https://violentmonkey.github.io/) (ou Tampermonkey) qui permet de **télécharger en masse tous les fichiers `.torrent`** présents sur une page YggTorrent.  

Il repère les liens du type https://www.yggtorrent.top/engine/download_torrent?id=xxxx et propose une interface flottante pour les récupérer d’un coup, avec délai configurable, retries, et fallback en ouverture d’onglets si besoin.

---

## 🚀 Installation

1. Installer une extension userscript (ex. [Violentmonkey](https://violentmonkey.github.io/get-it/)).  
2. Ajouter un nouveau script et coller le contenu de [`ygg-bulk.user.js`](./ygg-bulk.user.js).  
3. Sauvegarder.  

Le script sera actif automatiquement sur les pages YggTorrent, indépendamment de leur extension.  

---

## 🛠️ Fonctionnalités

- ✅ Détection automatique des liens `engine/download_torrent?id=xxxx` sur la page  
- ✅ Téléchargement **massif** avec `GM_download` (cookies/session conservés)  
- ✅ Délai configurable entre chaque requête (évite l’anti-bot)  
- ✅ Retries automatiques si une requête échoue  
- ✅ Nom de fichier récupéré depuis `Content-Disposition` (si dispo)  
- ✅ Fallback : ouverture des liens en onglets (si le site bloque les requêtes directes)  
- ✅ Panneau flottant discret et réutilisable  

---

## ⚙️ Options

Le panneau flottant (en bas à droite) permet de configurer :  
- **Délai (ms)** : temps d’attente entre deux téléchargements (par défaut `1200`)  
- **Retries** : nombre de tentatives en cas d’échec (par défaut `2`)  
- **Fallback** : ouvre les liens en onglets plutôt que de les télécharger directement  

Toutes les options sont sauvegardées localement.

---

## 🖼️ Aperçu



---

## 📌 Remarques

- Vous devez être **connecté à YggTorrent** pour que les téléchargements fonctionnent.  
- YggTorrent peut mettre en place des protections anti-bot (Cloudflare). Si c’est le cas, activez le **mode fallback** (ouverture d’onglets).  
- Compatible avec :  
  - Firefox + Violentmonkey  
  - Chrome/Chromium + Violentmonkey ou Tampermonkey  

---

## 📄 Licence

MIT – faites-en ce que vous voulez ✨  

---



