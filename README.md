# Spécialisations — MSc AI for Business

Petite interface web qui lit **en direct** un Google Sheet (rempli via un Google Form)
et permet de voir, dans les deux sens :

- **par spécialisation** → qui la suit,
- **par personne** → quelle spécialisation elle a choisie.

Recherche par nom, compteurs par spécialisation, et **actualisation automatique toutes les 45 s**
au fur et à mesure des réponses.

## Comment ça marche

La page est 100 % statique (un seul fichier `index.html`, aucune dépendance).
Elle récupère les données côté navigateur via l'endpoint public `gviz` de Google Sheets —
aucune donnée n'est stockée dans ce dépôt, seulement le code.

> Le Google Sheet doit être partagé en **« Tous les utilisateurs disposant du lien — Lecteur »**
> pour que la page puisse le lire.

## Déploiement (GitHub Pages)

1. Pousser ce dossier sur un dépôt GitHub.
2. **Settings → Pages → Build and deployment → Source : Deploy from a branch**,
   branche `main`, dossier `/ (root)`, puis **Save**.
3. Le site est publié sous `https://<utilisateur>.github.io/<dépôt>/` (~1 min).

## Lancer en local

```bash
node server.js        # puis ouvrir http://localhost:8813
```
