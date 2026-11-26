# URL Convert

Boîte à outils URL hébergée sur Cloudflare Workers (assets statiques) :

- **Encoder / Décoder** (encodeURIComponent / encodeURI, option espaces en `+`)
- **Analyser** une URL : composants + édition des paramètres de requête
- **Nettoyer** : retire les paramètres de suivi (utm_*, fbclid, gclid…)
- **Slug** à partir d'un titre
- **Base64URL** encodage / décodage (UTF-8)

Tout tourne côté navigateur, aucune donnée n'est envoyée.

## Développement

```bash
npm install
npm run dev
```

## Déploiement sur Cloudflare

**Option A, depuis le dashboard (recommandé)** : Cloudflare → Workers & Pages → Create → Import a repository → choisir ce dépôt. Commande de déploiement : `npx wrangler deploy`. Chaque push redéploie automatiquement.

**Option B, en ligne de commande** :

```bash
npx wrangler login
npm run deploy
```

Le site sera disponible sur `https://url-convert.<votre-sous-domaine>.workers.dev`.
